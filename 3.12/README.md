# What will 3.12 look like?

## Fundamentals

* We can't speedup opaque blobs of C code.
    * And we don't want use some elaborate mechanism like PyPy or GraalPython to understand the C code.
* We can speedup code that runs in the interpreter
* We can reduce the overhead of memory management, by doing less of it, and by doing it more efficiently.
* Not doing something at all is always preferable to doing it faster.

### This means that we want:

* C code to consist of builtin functions that are well typed and don't call back in Python (much).
* Everything else in bytecode (99.9% Python, but we might need a few key trampolines in hand written bytecode).
* To able to execute Python code faster.
* To remove incidental overhead due to poor memory layout, reference counting and cycle GC.

## Executing Python faster

This is the most important part of a fast VM, and the most complex (unless we want a fully concurrent, parallel cycle GC).
Ultimately we will need a JIT compiler, but it is clear from the relatively poor performance of Jython and IronPython that simply compiling to machine code is not magic pixie dust.
Remembering that not doing something at all is always preferable to doing it faster, we want to optimize by removing overheads, including type-checks, boxing and unboxing, reference counting operations, object allocation.

### Region selection

The simplest region to optimize is a linear trace; all instructions dominate the latter ones, and there are no merge points.
Traces can be stitched together to form larger regions, or even recompiled as a larger region (see HHVM).

Pyston and Cinder choose single Python functions as their base region of optimization. Even with inlining, this is quite limiting.

My PhD thesis compares a tracing interpreter (HotPy) with a method-at-a-time JIT compiler that did little or no specialization (Unladen Swallow); the interpreter wins easily.

#### Trace selection

There are two main approaches to tracing in the literature and in industry.
* Long traces: Traces cover a whole loop, or large number of instructions, as used in PyPy, luajit and tracemonkey.
* Short traces: Tracelets, or single BB traces, as used in HHVM or YJIT.

Long traces have the advantage that larger regions enable better optimization, and may include a loop which allows loop optimizations.
Short traces fail to complete much less often, an do not need a custom tracing interpreter.

We are greedy and want the advantages of both!
We will use the mechanisms for creating short traces, but the type information gathered by the adaptive interpreter will allow us
to lengthen the traces, without losing the advantages of short traces.

#### Trace generation and optimization

There are three key optimization phases needed to execute traces as fast as possible:
* Specialization
* Redundancy elimination
* Compilation to machine code

The best data we have for the relative and combined effectiveness of these approaches is from my PhD thesis.

The VM used (HotPy) was quite different from CPython, and there were no optimization other than trace-based ones, so the numbers should not be considered to be indicative of speedups we might achieve.
However, they do show how the optimizations interact.

Each number shows the relative speedup from adding one or more phases, relative to the base interpreter.

<sp> | T | TS | TD | TSD | TC | TSC | TDC | TSDC
---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:
Short Benchmarks | 1.10 | 1.91| 0.96 | 2.11 | 0.76 | 1.46 | 0.75 | 1.83
Medium Benchmarks | 1.09 | 1.96 | 0.95 | 2.19 | 1.05 | 2.51 | 1.04 | 3.78
Long Benchmarks | 1.16 | 2.14 | 1.01 | 2.41 | 1.24 | 3.42 | 1.25 | 5.83

Key:
* **T** Tracing
* **S** Specialization (including redundant type-check elimination)
* **R** Object elimination and other redundancy elimination
* **C** Compilation to machine code

A few things to note:
* Without specialization, the other phases have little value. 
* For short running benchmarks the compiler can slow things down a bit.
* Combined, all four optimization resulted in a large speedup.


## Better calling convention(s)

Cffi and argument clinic take a typed description of the arguments to a function and a low-level implementation that does no dispatch, typechecking or unboxing.
Ultimately we want to be able to call directly into these functions from JIT compiled code.
With that ultimate goal in mind, we also want an intermediate calling convention suitable for calling from a specializing interpreter.
Nicknamed "hasty call" as nod to "fast call", this calling convention would leave parsing and re-ordering the arguments to the caller,
but handle unboxing and type-checking in the caller.

For example, consider a function wih the signature `foo(a:int, b:int, *, c:Any=None)->None`
with the underlying C implementation signature `void foo_impl(Py_ssize_t a, Py_ssize_t b, PyObject *c)`
The "hasty call" signature would be `PyObject *foo_hasty(PyObject args[3])`

It will be up to the caller to reorder arguments and fill in defaults, so that if we call `foo(b=1, a=0)`
the VM would swap `a` and `b` and push `None`, before calling the C function `foo_hasty`.

It will be up to the tooling, whether cffi, argument clinic or something else, to create `foo_hasty`, which in this case would look something like:
```C
PyObject *foo_hasty(PyObject args[3]) {
    PyObject *a_obj = args[0];
    PyObject *b_obj = args[1];
    PyObject *c = args[2];
    if (!PyLong_Check(a_obj)) {
        goto error; 
    }
    if (!PyLong_Check(b_obj)) {
        goto error; 
    }
    Py_ssize_t a, b;
    if (PyLong_ToSsize_t(a_obj, &a)) {
        goto error;
    }
    if (PyLong_ToSsize_t(b_obj, &b)) {
        goto error;
    }
    foo_impl(a, b);
    Py_RETURN_NONE;
  error:
    /* Handle error */
}
```

The tooling will also need to create the `vectorcall` form to handle argument parsing when called from
unspecialized code or from other C extensions.

## Other parts

* Better GC:
  * Fewer collections (this shouldn't be too hard to achieve)
  * More effective collections (this is harder)
* Compact object headers
* Better frame layout for faster (Python-to-Python) calls.

### Better GC

We currently perform cycle collection too often, and not very effectively.
We should be able to fix this be using better triggers.

We could also reduce the overhead of tracing during GC with a more declarative model, or some parallelism and pre-fetching. This is likely to both harder and less profitable than just doing fewer collections.

### Compact object headers

See https://github.com/faster-cpython/ideas/discussions/125
With saturating reference counts, and a more compact GC header, we can halve the memory consumption of a Python object (not including its values or dict).

### Better layout for frames

By inserting (another) NULL before the callable during the calling sequence, and omitting the globals and builtins from the frame (fetching them from the function when needed) we can avoid moving or copying arguments for Python-to-Python calls.