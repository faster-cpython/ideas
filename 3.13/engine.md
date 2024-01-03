# Tier 2 execution engine

Author: Mark Shannon

The [plan for 3.13](./README.md) describes the main components that we will produce for 3.13. This document explains how the bits fit together at runtime.

## Overview

The design of the tier 2 optimizer is based around "superblock"s.
These superblocks are a specification of execution,
rather than something that is executed.

We expect to have two different execution engines for superblocks:
* The tier 2 interpreter
* The copy-and-patch compiler

We need to manage entry to and exits from superblocks, so that
as programs execute, a graph of superblocks will be built up.

While it is critical for performance that execution within
a superblock is fast, the performance of jumping from one
superblock to another is also important.

Memory consumption is also important.

### Either interpreter or compiler. Not both.

We assume that there will only be one execution engine.
If we have a JIT, we will use it to execute *all* superblocks.
This simplifies things as we do not need to concern ourself with
transfers from the tier-2-interpreter to JIT-compiled code, or vice versa.

### Superblocks and executors

A superblock is a sequence of micro-ops with minimal control flow.
It is the input and output of tier 2 optimization phases.
An executor is the runtime object that is the executable
representation of a superblock. 

#### Creating executors

Creating executors from superblocks is the first job of the execution engine.
This transformation is currently trivial for the tier 2 interpreter as we
use the same format for optimization and execution. This is inefficient, so
we will probably change the executable format.
For the JIT, we will use copy-and-patch to convert the micro-ops to machine code.

### Exits from executors

On creation of an executor, there will be a number of potential exits
from that executor. For each entry to an executor, exactly one exit
will occur. This means that a few of the exits will be hot, but most will be cold.

We want hot exits to be implemented such that transfer to the next executor is fast.
However, we want cold exits to consume as little memory as possible.
Unfortunately we cannot know in advance which are which, although there are
some exits we expect to be very rare. We can handle these very rare exits
differently, to save space.

### Linking executors

When an exit from an executor gets hot we need to create a new executor
to attach to that exit. Once we have done that we need to link the exit to 
the new executor in a way that allows fast transfer of execution.

### Making progress

If an executor exits before it does any work *and* it exits to another
executor that can also exit before it does any work, or it exits to itself,
we can find ourselves in an infinite loop.

There are two possible approaches to avoiding this:
1. We track which executors might not make
progress and are careful about which executors are linked together, or
2. We require all executors to make progress.

1 has many edge cases which makes it hard to reason about and get correct.

2 is simpler, but may be a bit slower as we may need to [pessimize the first instruction](#guaranteeing-progress-within-an-executor).

We will use approach 2. It is much easier to reason about and should be almost as fast.

If all executors are guaranteed to make progress, then transfers from one executor 
to another can be implemented by a single jump/tail-call.

### Inter-superblock optimization

Some superblocks can be quite short, but form a larger region of hot code, that 
we want to optimize. In order to do that we want to propagate type information
and representation changes across edges, which means storing that information
on exits when they are cold. Since most exits will remain cold, we need to 
store this information in a compact form.

### Making "hot" exits fast and "cold" exits small

In order to make hot exits fast, we need them to be as simple as possible,
passing as little information as possible.

We also want to make cold exits as small as possible, but cold exits
may become hot exits, so we need them both to use the same interface.

## The implementation

This section describes one possible implementation. The initial implementation
will not support inter-superblock optimization, but we should plan to support it
in the future.

### Making "hot" exits fast

In order to make hot exits fast, we want to implement them as a single, unconditional jump.
In the tier 2 interpreter, that will be implemented by setting the IP to the first
instruction of the target executor.
In the JIT, it will be implemented as a tail call to the function pointer of the target executor.

### Making "cold" exits small

All side exits from an executor will start cold, and most of them will remain cold.

We need to track various pieces of information for cold exits, none of which will be
required once the exit becomes hot, so we want to store that information in a way
that minimizes the cost to hot exits and minimizes the memory used for cold exits.
That information is:
* The offset/location of the pointer to the exit in the executor, so it can be updated.
* The target (offset into the code object of the tier 1 instruction)
* Any relevant known type information (this is optional but will improve optimization)
* Any representation changes that have been made.
* The "hotness" counter

### Minimizing memory use

There are number of ways we can reduce memory use, for example:
* Putting things in (ideally const) arrays, so we can refer to them by a one or two byte index,
  instead of an eight byte pointers.
* For complex data like type information and representation changes, use trees or deltas,
  so that the information like `(A, B, C)` can be stored as `(A, B) <- C` allowing `(A, B)` to
  be shared.

### Each executor gets a table of exit data

Each executor will get a table of exit data. We can compute the size of this
when creating the executor. The entries in this table are described below.

### Fixed number of exit objects

Since the vast majority of exits will not need patching, we do not want to pass the offset,
so we need to store the offset in the executor.

Since there is a fixed number of micro-ops allowed in a superblock (currently 512), we have an upper
bound on the offset. We will preallocate one exit object per possible offset.

### Exit data

* The offset/location of the pointer: Implicit if we embed the exit pointer in the exit data
* The target: Has a maximum value of about 10**9, so store as a `uint32_t`
* Any relevant known type information: Format TBD.
  We don't need to decide on the format of this data for now.
* Any representation changes that have been made: Likewise, format TDB.
* The "hotness" counter. See below.

#### Representation changes

Representation changes are things like storing the top value(s) of the stack in registers, or performing scalar replacement on objects or frames.
In order to drop back to tier1, we need to be able to undo those changes, so we need to record them.

#### Hotness counters

We need to track how hot an exit is. Ideally we want to be able to distinguish
between an exit that is hot, and one that is cold but has exited a large number of
times over prolonged execution.

There are three ways we can store counters:
1. Store a counter for each exit in the superblock.
2. Have one exit per counter, and change the exit object to change the counter.
3. Store the counters in a global (per-interpreter) table.
<!-- Prevent 1 below being numbered as 4 -->
1. is simple and deterministic.
2. either prevents mapping the exits to offsets, or will require many thousands
   of exit objects (number_of_offsets * max_counter_value)
3. will require hashing the executor and offset, and thus be non-determinstic due to collisions.
   Allows us to decay the counter to distinguish between hot counters and long-lived "cool" counters.
   LuaJIT does something like this (but with a very small table).

We should probably start with option 1, with the intention of 
implementing option 3 later.

### `EXIT_IF` and `UNLIKELY_EXIT_IF`

We will replace the misnamed `DEOPT_IF` (it doesn't de-optimize, it exits)
with `EXIT_IF` and `UNLIKELY_EXIT_IF`.
`EXIT_IF` will be used for most exits.
`UNLIKELY_EXIT_IF` will be used for unlikely exits, like eval breaker checks or stack overflow.

`EXIT_IF` will exit through the pointer, as described above.
`UNLIKELY_EXIT_IF` will exit to tier 1.

For efficiency reasons, all exits in the same micro op will use the same exit object and data.
For simplicity, we will also require that no micro op contains both
an `EXIT_IF` and an `UNLIKELY_EXIT_IF`.

We also need to make sure that tier1 never enters an invalid executor, but 
we should be doing that anyway.

Since `UNLIKELY_EXIT_IF` has no attached exit/executor it is compact;
it only needs two bytes to store the target.

### Guaranteeing progress

We need to guarantee progress within an executor and when exiting executors.

#### Guaranteeing progress within an executor

In order to guarantee progress, the superblock cannot `EXIT_IF` without having made progress,
but it can do an `UNLIKELY_EXIT_IF` since `UNLIKELY_EXIT_IF` always drops to tier 1.

This means that the micro ops for the first tier 1 instruction in an executor
cannot contain an `EXIT_IF`. In practice this means that before translating
to micro-ops, the first instruction must be converted to its unspecialized form.

### Exiting to invalid executors

We want `EXIT_IF` to be efficient, so it needs to enter the next executor unconditionally.
This means that when we invalidate an executor, we need to modify that executor so that
it immediately drops into tier 1 upon being executed. Since tier 1 will never enter an invalid
executor, we are thus guaranteed not to execute an invalid executor.
In the tier 2 interpreter, we change the first instruction to `EXIT_TRACE`.
In the JIT, we will need to change the function pointer to point to a function that returns to tier 1.

### The mechanics of transferring execution between executors

When transfering control we need to:
1. Incref the new executor
2. Set `current_executor` to the new executor 
3. Decref the old executor.

In the future, when we have deferred references, we can make the current executor a deferred reference
and skip the incref/decref.

#### JIT compiler

To transfer control between executors, we make a jump, implemented as an indirect
 tail-call in the
generated stencil.

The generated code must decref the old executor, as we cannot decref the old executor when still executing it, meaning we must pass the old executor as an argument in the tail call.


#### Interpreter 

We can do the three steps (incref, update current executor, decref) before entering the new executor, since then we don't need to worry about freeing code that we are running.
Entering the new executor is simple: set the 
instruction pointer to the first instruction of the new executor.

## Future optimizations

We plan to leave inter-executor optimizations for the future, in order to get a working
implementation with JIT compiler ready in good time for 3.13.

### Specialization across executors

For this we will need to record known type information at exits, to avoid redundant checks,
and to allow us to create multiple specialized executors for the same tier 1 instructions.

### Representation changes across executors

By tracking representation changes across executors, we can avoid the overhead of restoring
the canonical representation on exits.
For example, if a value is represented by an unboxed float, it is expensive to box, then unbox it
across an exit.
This optimization has the potential to be a significant performance win
*and* to consume a lot of memory, so we need to design our data structures carefully.