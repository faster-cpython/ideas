# StackRef Semantics

Author: Ken Jin

## Prelude and Rationale
Due to PEP 703 (Making the Global Interpreter Lock Optional in CPython),
tagged pointers will be introduced to CPython. Tagged pointers have in past attempts,
been very hard to debug. From the author's own experience, there are the following
sources of bugs:

1. Casting to-and-from a tagged pointer directly.
2. Untagging a tagged pointer, then operating on it directly.
3. Forgetting to convert deferred references to new references when required,
   this leads to hard-to-track segfaults.
4. Using the wrong conversion function to convert a tagged pointer
   to a `PyObject *`.

We can solve 1. using the C compiler by making tagged pointers a struct, called
`_PyStackRef`. 2. is quite easily detectable because it immediately leads to
crashes during GC. However, 3. and 4. lead to hard-to-track reference leaks
in the CPython interpreter.

Mark Shannon suggested since we are revamping the entire interpreter loop,
we might as well make sure we do it right and in a principled way.
Taking inspiration from HPy and Mark, I introduce `_PyStackRef`, basically
a watered-down HPy for CPython that solves problems 3. and 4. automatically.

## Definition in Words

(Copied from `pycore_stackrefs.h`)

This file introduces a new API for handling references on the stack, called
`_PyStackRef`. This API is inspired by HPy.
There are 3 main operations, that convert `_PyStackRef` to `PyObject*` and
vice versa:

1. Borrow (discouraged)
2. Steal
3. New

Borrow means that the reference is converted without any change in ownership.
This is discouraged because it makes verification much harder. It also makes
unboxed integers harder in the future.

Steal means that ownership is transferred to something else. The total
number of references to the object stays the same.

New creates a new reference from the old reference. The old reference
is still valid.

With these 3 API, a strict stack discipline must be maintained. All
_PyStackRef must be operated on by the new reference operations:

1. DUP
2. CLOSE

DUP is roughly equivalent to `Py_NewRef`. It creates a new reference from an old
reference. The old reference remains unchanged

CLOSE is roughly equivalent to `Py_DECREF`. It destroys a reference.

## Definition in Operational Semantics
We define two initial mappings:

$$
\begin{align}
    & \color{blue} live_{\text{PyStackRef}} \color{black}
    & = \\{l \longmapsto \\{0, 1\\} \mid  type(l) = \text{PyStackRef} \\}
    \\
    & \color{red} dead_{\text{PyObject}} \color{black}
    & = \\{l \longmapsto \mathbb{Z}^{0+} \mid  type(l) = \text{PyObject *} \\}
\end{align}
$$

The program state is defined as the two-tuple:

$$
(\color{blue} live_{\text{PyStackRef}} \color{black},
 \color{red} dead_{\text{PyObject}} \color{black} )
$$

All operations are defined as operations on this two-tuple.
These are the operational semantics:

$$
\begin{align}
& borrow(Ref)[\text{PyStackRef} \hookrightarrow \text{PyObject}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black},
    \color{red} dead_{\text{PyObject}} \color{black} )
\\
& steal(Ref)[\text{PyStackRef} \hookrightarrow \text{PyObject}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black} - Ref,
    \color{red} dead_{\text{PyObject}} \color{black} - Ref_O)
\\
& steal(O)[\text{PyObject} \hookrightarrow \text{PyStackRef}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black} + O_{Ref},
    \color{red} dead_{\text{PyObject}} \color{black} + O)
\\
& new(Ref)[\text{PyStackRef} \hookrightarrow \text{PyObject}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black},
    \color{red} dead_{\text{PyObject}} \color{black} - Ref_O)
\\
& new(O)[\text{PyObject} \hookrightarrow \text{PyStackRef}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black} + O_{Ref},
    \color{red} dead_{\text{PyObject}} \color{black})
\\
\end{align}
$$

$$
% Note: defined in a separate block because the first expression is too big for GH.
\begin{align}
& dup(Ref):
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black} + Ref_{Ref},
    \color{red} dead_{\text{PyObject}} \color{black})
\\
& close(Ref):
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black} - Ref,
    \color{red} dead_{\text{PyObject}} \color{black})
\\
\end{align}
\\
$$

1. $Ref_O$ reads as "the object from reference Ref".
2. $O_{Ref}$ reads as "the reference of the object O".
3. The $set - A$ operation must deduct $1$ from the corresponding
   $A$ in $set$.
4. The $set + A$ operation should add $1$ to the corresponding $A$
   in $set$.

## Invariants (Detecting Unsoundness)

1. $\text{PyStackRef}$ s are unique.
2. $\text{PyObject}$ s are not necessarily unique
   (this is for compatibility with CPython).
3. At normal function call frame exit, the program state should be
   $len(\text{live}) == 1$.
4. $steal(Ref)[\text{PyStackRef} \hookrightarrow \text{PyObject}]$ should
   at the point of stealing, have exactly one stack ref available to steal.
5. $steal(Ref)[\text{PyObject} \hookrightarrow \text{PyStackRef}]$ does
   not need to have exactly one `PyObject *` in the mapping, because of 2.
6. The mapping for $\text{PyStackRef}$ can only map to 0 or 1.
7. The mapping for $dead_{\text{PyObject}}$ can never map to a negative number.
   

## Implementation

We will only enforce invariants in debug builds. There will be no
performance loss in release builds.

1. On each frame push, we create 2 hashmaps to represent the mappings,
   and an empty array to contain the mappings of handles to actual
   $\text{PyObject}$.
2. These data structures will be tied to frame state.
3. Each $\text{Steal(Ref)}$ and
   $\text{New(Ref)}$ will create a new handle.
4. Each handle is just the index into the handle array.
