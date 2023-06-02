# Our plan for Python 3.13

Author: Mark Shannon, Michael Droettboom

### Overview

The plan for 3.13 is similar to [early plans for 3.12](../3.12/README.md).

The big difference is that we have now finished the foundational work that we need:

* [Low impact monitoring (PEP 669)](https://peps.python.org/pep-0669/) is implemented.
* The bytecode compiler is a much better state.
* The interpreter generator is working.
* Experiments on the register machine are complete.
* We have a viable approach to create a low-overhead maintainable machine code generator, based on [copy-and-patch](https://fredrikbk.com/publications/copy-and-patch.pdf).

We plan three parallelizable pieces of work for 3.13:

* The tier 2 optimizer
* Enabling subinterpreters from Python code ([PEP 554](https://peps.python.org/pep-0554/)).
* Memory management

### The tier 2 optimizer

See [Tier 2 optimizer](https://github.com/faster-cpython/ideas/issues/557) for an explanation of what the tier2 optimizer is.

The workplan is roughly as follows:
* Get the tier 2 interpreter working
* Generate (poor quality) superblocks
* Implement basic superblock management
* In parallel:
  * Add support for deoptimization to superblocks
  * Enhance the superblock creation code
  * Implement the specializer
  * Implement the partial evaluator
  * Implement the copy-and-patch machine code generator
    * Build-time integration
    * Generation of tier 2 code

Our goal for 3.13 is to reduce the time spent in the interpreter by at least 50%.

[Detailed plan](https://github.com/faster-cpython/ideas/issues/587).
[Detailed plan for copy-and-patch](https://github.com/faster-cpython/ideas/issues/588).

### Enabling subinterpreters from Python

Unlike the other tasks, which are mainly focused on single-threaded performance, this work builds on the per-interpreter GIL work that shipped in Python 3.12 to allow Python programmers to take advantage of better parallelism in subinterpreters from Python code (without the need to write a C extension).

A draft [PEP 554](https://peps.python.org/pep-0554/) already exists for this work.  The first step will be to get it updated and push for an early approval, so we can change course if necessary.

[Detailed plan](https://github.com/faster-cpython/ideas/issues/589).

### Better memory management

The [profiling data](https://github.com/faster-cpython/benchmarking/blob/main/profiling/profiling.png) shows that quite a large amount of time spent is spent in memory management and cycle GC. That fraction will only get larger as we speed up the rest of the VM.

Unlike the tasks above, we are less certain about the appropriate solutions, so some more research and experimentation is required first.
We plan to do this as a side project based on what we learn from the Tier 2 work above.

We want to:
* Do fewer allocations by improving data structures<sup>*</sup>
* Spend less time doing cycle GCs. This could be as simple as doing fewer collections, or as complex as implementing a new, incremental cycle finder.

**TODO:** Create issues for investigation

List our detailed strategy and workplan for improving allocation/deallocation speed and reducing cycle GC overhead.

---------------------------

__*__ We also hope that partial evaluation will reduce the number of temporary objects, but that is in the scope of the tier 2 optimizer, not memory management.
