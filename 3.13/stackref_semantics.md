# StackRef Semantics

This is the formal definition for stack references
(expressed in operational semantics).

It takes inspiration from HPy.

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

1. $\text{PyStackRef}$s are unique.
2. $\text{PyObject}$s are not necessarily unique
   (this is for compatibility with CPython).
3. At normal function call frame exit, the program state should be
   $len(\text{live}) == 1$.
4. $steal(Ref)[\text{PyStackRef} \hookrightarrow \text{PyObject}]$ should
   at the point of stealing, have exactly one stack ref available to steal.
5. $steal(Ref)[\text{PyObject} \hookrightarrow \text{PyStackRef}]$ does
   not need to have exactly one `PyObject *` in the mapping, because of 2.
6. There can never be a negative count for $\text{PyStackRef}$.
   

## Implementation

We will only enforce invariants in debug builds.

1. On each frame push, we create 2 hashmaps to represent the mappings,
   and an empty array to contain the mappings of handles to actual
   $\text{PyObject}$.
2. These data structures will be tied to frame state.
3. Each $\text{Steal(Ref)}$ and
   $\text{New(Ref)}$ will create a new handle.
4. Each handle is just the index into the handle array.