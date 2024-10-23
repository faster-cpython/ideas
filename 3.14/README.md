# Plan for 3.14

## Performance

### The Just-In-Time (JIT) compiler

> NOTE: We now use the term "The JIT" to refer to both the (a) Tier 2 micro-opcodes and optimizer and (b) machine code generator.
  In the past, we referred to these as (a) Tier 2 and (b) the JIT.
  This naming is more consistent with other runtimes.

* Improved handling of generated machine code, both lifetime and organization
* Improved quality of the final generated code
* Improved optimization before final generation of code:
  * Enhanced type-based redundancy elimination
  * Partial-evaluation
* Increase the percentage of bytecodes that are executed in the JIT

### More efficient reference counting

For many references, we know that there is another reference that will outlive that reference.
For these references we can either:

* Omit the reference count altogether. This might only happen in the JIT.
* Replace expensive memory operations with cheap ALU operations, by storing the count for the reference in the reference and not the object.

### Better cycle collector (experiment)

With improved reference counting, there are a number of reference count operations that don't change the counter.
We can take advantage of that to move a bit of work into decrementing reference counts to mark possible roots of cycles.
When doing cycle GC, we only need to look at these objects, not all objects, when searching for a cycle.

### Moving some code from C to Python

There are a number of small built-in functions, such as `any`, `all`, and `enumerate`, that are implemented in C.
These functions are an obstacle to optimization as execution flows from Python to C and then back to Python.
By rewriting these functions in Python, the optimizer can see across the function call boundary, so they can be better optimized.

### Extensible optimizations for arithmetic operations and subscripting

Specializations are currently written by hand for specific built-in types that we know will have the most impact.
However, some important libraries, e.g., Numpy, could benefit from participating in the specialization system by being able to cache redundant work at specific call sites.

> Berlakovich, Felix, and Stefan Brunthaler. 2024. “Cross Module Quickening - The Curious Case of C Extensions.” Schloss Dagstuhl – Leibniz-Zentrum für Informatik. https://doi.org/10.4230/LIPICS.ECOOP.2024.6.

## Subinterpreters

* Implement an interpreter pool executor, analogous to the existing thread pool and process pool executors, to allow the use of subinterpreters with a familiar paradigm.
* Get PEP734 accepted for 3.14, so the [Python API for subinterpreters](https://pypi.org/project/interpreters-pep-734/) will ship in the standard library.
* Performance improvements for subinterpreters.
* HOWTO document for concurrency, including subinterpreters.

## Developer documentation

Producing developer documentation on CPython implementation, including the changes in recent years by this team.

## Possible future work for 3.15

#### Tagged integer references

Integers are ubiquitous in software. Python's arbitrary precision integers are slow and memory-hungry compared with integers in C or Java.
Tagged integer references give us all the memory efficiency and much of the performance of C integers.
There is a sizeable cost in new APIs and code changes, though.

#### HPy-like C API

Tagged integers will require new internal APIs to pass opaque references, so we might as well add a new, consistent API modeled on [HPy](https://hpyproject.org/).
We will use this internally to start with, but we expect tools like [Cython](https://cython.org/) and [Pybind11](https://github.com/pybind/pybind11) will want to use it to avoid the overhead of going through the `PyObject *` based API.