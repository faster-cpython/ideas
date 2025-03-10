# Plan for 3.14

## Performance

### Top-of-stack caching

Store the top-of-stack in a local variable to avoid unnecessary indirect reads and writes to the stack.

### The Just-In-Time (JIT) compiler

> NOTE: We now use the term "The JIT" to refer to both the (a) Tier 2 micro-opcodes and optimizer and (b) machine code generator.
  In the past, we referred to these as (a) Tier 2 and (b) the JIT.
  This naming is more consistent with other runtimes.

* Improved handling of generated machine code, both lifetime and organization
* Improved quality of the final generated code
* Improved optimization before final generation of code:
  * Enhanced type-based redundancy elimination
  * Top-of-stack caching
  * Partial-evaluation
* Increase the percentage of bytecodes that are executed in the JIT

### More efficient reference counting

For many references, we know that there is another reference that will outlive that reference.
For these references we can either:

* Omit the reference count altogether. This might only happen in the JIT.
* Replace expensive memory operations with cheap ALU operations, by storing the count for the reference in the reference and not the object.

### Tail-calling interpreter

Rather than using a classic switch statement or computed gotos for the main interpreter loop, tail call between functions implementing each bytecode.  This shows a speedup of 1-5% geometric mean on various platforms.

This approach currently only works with Clang 19.  We hope to find a way to make this work in more places through some combination of improving other compilers, compiling only parts of CPython with Clang 19, and/or moving platforms to use Clang 19 by default.  This is mainly ecosystem / community work.

### Extensible optimizations for arithmetic operations and subscripting

Specializations are currently written by hand for specific built-in types that we know will have the most impact.
However, some important libraries, e.g., Numpy, could benefit from participating in the specialization system by being able to cache redundant work at specific call sites.

> Berlakovich, Felix, and Stefan Brunthaler. 2024. “Cross Module Quickening - The Curious Case of C Extensions.” Schloss Dagstuhl – Leibniz-Zentrum für Informatik. https://doi.org/10.4230/LIPICS.ECOOP.2024.6.

## Subinterpreters

* [ ] Get PEP734 accepted for 3.14, so the [Python API for subinterpreters](https://pypi.org/project/interpreters-pep-734/) will ship in the standard library.  (**This is mostly just waiting on steering council.**)
* [X] Implement an interpreter pool executor, analogous to the existing thread pool and process pool executors, to allow the use of subinterpreters with a familiar paradigm.
* [ ] HOWTO document for concurrency, including subinterpreters.  (Ideally, I'll hand most of the work off to other people.)
* [ ] HOWTO document for subinterpreters specifically.
* [ ] Write a new PEP about "sharing" protocol (i.e. `tp_xid`).

I'd also like to see performance improvements for subinterpreters (e.g. startup speed, memory usage), but there might not be enough time for anything meaningful in 3.14.

## Other Runtime Improvements

* [ ] Split up PyThreadState.
* [ ] Introduce runtime lifecycle phases.
* [ ] Freeze/restore runtime init memory, for faster startup.
* [ ] Support fast finalization by skipping all cleanup except resouce-based finalizers.  (First, analyze and decide if worth it.)

Realistically, it would be hard to fit much of that work into the 3.14 timeframe, but we'll do as much as we can and roll the rest into 3.15 plans.

## Developer documentation

Produce developer documentation on CPython implementation, including the changes in recent years by this team.

## Possible future work for 3.15

#### Tagged integer references

Integers are ubiquitous in software. Python's arbitrary precision integers are slow and memory-hungry compared with integers in C or Java.
Tagged integer references give us all the memory efficiency and much of the performance of C integers.
There is a sizeable cost in new APIs and code changes, though.

#### HPy-like C API

Tagged integers will require new internal APIs to pass opaque references, so we might as well add a new, consistent API modeled on [HPy](https://hpyproject.org/).
We will use this internally to start with, but we expect tools like [Cython](https://cython.org/) and [Pybind11](https://github.com/pybind/pybind11) will want to use it to avoid the overhead of going through the `PyObject *` based API.

### Moving some code from C to Python

There are a number of small built-in functions, such as `any`, `all`, and `enumerate`, that are implemented in C.
These functions are an obstacle to optimization as execution flows from Python to C and then back to Python.
By rewriting these functions in Python, the optimizer can see across the function call boundary, so they can be better optimized.

(Deferred to 3.15 because it will have more impact when more optimizations are implemented)

### Better cycle collector (experiment)

With improved reference counting, there are a number of reference count operations that don't change the counter.
We can take advantage of that to move a bit of work into decrementing reference counts to mark possible roots of cycles.
When doing cycle GC, we only need to look at these objects, not all objects, when searching for a cycle.
