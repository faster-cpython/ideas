# Our plan for 3.13

Author: Mark Shannon

### Overview 

The plan for 3.13 is similar to early plans for 3.12.
[3.12 plan](../3.12/README.md)

The big difference is that we now done the various pieces of foundational work that needed to be done:
* PEP 669 is implemented.
* The bytecode compiler is a much better state.
* The interpreter generator is working
* Experiments on the register machine are complete
* We have a viable apporach to create a low-overhead maintainable machine code generator

We can now work on the tier 2 optimizer chain unimpeded.

We plan two main pieces of work for 3.13:
* The tier 2 optimizer
* Faster memory allocation and deallocation, and reduced cycle GC ovehead 

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

Our goal for 3.13 is to reduce the time spent in the interpreter by at least 50%.

### Better memory management

The [profiling data](https://github.com/faster-cpython/benchmarking/blob/main/profiling/profiling.png) shows that quite a large amount of time spent is spent in memory management and cycle GC. That fraction will only get larger as we speed up the rest of the VM.

We want to:
* Do fewer allocations by improving data structures<sup>*</sup>
* Spend less time doing cycle GCs. This could be as simple as doing fewer collections, or as complex as implementing a new, incremental cycle finder.

#### TO DO

List our detailed strategy and workplan for improving allocation/deallocation speed and reducing cycle GC overhead.



---------------------------

__*__ We also hope that partial evaluation will reduce the number of temporary objects, but that is in the scope of the tier 2 optimizer, not memory management.
