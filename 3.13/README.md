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

We plan four parallelizable pieces of work for 3.13:

* The tier 2 optimizer
* Copy-and-patch machine code generator
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

Our goal for 3.13 is to reduce the time spent in the interpreter by at least 50%.

[Detailed plan](https://github.com/faster-cpython/ideas/issues/587).

### Copy-and-patch machine code generator

This work is expected to reduce the interpretive overhead of the tier 2
interpreter above, but much of it can proceed in parallel with that work.

Unlike other JITs, copy-and-patch combines a fairly complex build-time system to
create templates, with a very simple run-time component to build machine code
from those templates. We have already developed a working prototype for
CPython's existing Tier 1 interpreter, and the next step is to get it
production-ready for use with the Tier 2 interpreter described above.

The main chunks of remaining work are:
* Improve the build-time component to lower its maintenance cost.
  * This includes, for example, reusing existing components for parsing object files, rather than writing our own.
* Improve the integration of copy-and-patch into CPython's build system.
* Improve the quality of the generated code.
  * There are many unimplemented ideas from the paper here, including pinning locals or stack items in registers across calls, "burning in" constants, and more.
* (When components are ready above)
  * Use the superblocks created by the new optimizer/executor API
  * Port to use the Tier 2 interpreter

[Detailed plan](https://github.com/faster-cpython/ideas/issues/588).

### Enabling subinterpreters from Python

Unlike the other tasks, which are mainly focused on single-threaded performance, this work builds on the per-interpreter GIL work that shipped in Python 3.12 to allow Python programmers to take advantage of better parallelism in subinterpreters from Python code (without the need to write a C extension).

A draft [PEP 554](https://peps.python.org/pep-0554/) already exists for this work.  The first step will be to get it updated and push for an early approval, so we can change course if necessary.

[Detailed plan](https://github.com/faster-cpython/ideas/issues/589).

### Better memory management

The [profiling data](https://github.com/faster-cpython/benchmarking/blob/main/profiling/profiling.png) shows that quite a large amount of time spent is spent in memory management and cycle GC. That fraction will only get larger as we speed up the rest of the VM.

Unlike the tasks above, we are less certain about the appropriate solutions, so some more research and experimentation is required first.

We want to:
* Do fewer allocations by improving data structures<sup>*</sup>
* Spend less time doing cycle GCs. This could be as simple as doing fewer collections, or as complex as implementing a new, incremental cycle finder.

**TODO:** Create issues for investigation

List our detailed strategy and workplan for improving allocation/deallocation speed and reducing cycle GC overhead.

---------------------------

__*__ We also hope that partial evaluation will reduce the number of temporary objects, but that is in the scope of the tier 2 optimizer, not memory management.
