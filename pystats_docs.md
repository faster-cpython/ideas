# pystats documentation

This describes the meaning of the various sections and fields in the pystats output.

## Execution counts

This is the count of how many times each Tier 1 instruction is executed.

The "miss ratio" column shows the percentage of times when instruction executed that it deoptimized. In this case the base unspecialized instruction is not counted.

## Pair counts

Shows the Top 100 most frequently occurring pairs of instructions as executed.

Pairs of specialized operations that deoptimize and are then followed by the corresponding unspecialized instruction are not counted as pairs.

## Predecessor / Successor pairs

Shows the top 5 instructions that are executed before and after each instruction.

This does not include the unspecialized instructions that occur after a specialized instruction deoptimizes.

## Specialization stats

For each bytecode, the following tables are present:

### Kind

- deferred: Lists the number of "deferred" (i.e. not specialized) instructions
  executed
- hit: specialized instructions that complete
- misses: specialized instructions that deopt

### Unnamed

- Success: Number of specialization attempts that were successful
- Failure: Number of specialization attempts that failed for some reason

### Failure kind

Numbers for the various kinds of specialization failures.
The total should add up to the "Failure" entry in the above table.

## Specialization effectiveness

### Specialization effectiveness

All entries are execution counts. Should add up to the total number of Tier 1
instructions executed.

- Basic: Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
- Not specialized: Instructions could be specialized but aren't, e.g.
  `LOAD_ATTR`, `BINARY_SLICE`.
- Specialized hits: Specialized instructions, e.g. `LOAD_ATTR_MODULE` that
  complete
- Specialized misses: Specialized instructions, e.g. `LOAD_ATTR_MODULE` that
  deopt

### Deferred by instruction

Breakdown of deferred (not specialized) instruction counts by family.

### Misses by instruction

Breakdown of misses (specialized deopts) instruction counts by family.

## Call stats

This is shows what fraction of calls to Python functions are inlined (i.e. not
having a call at the C level) and for those that are not, where the call comes
from. The various categories overlap.

Also includes count of frame objects created.

## Object stats

Grab bag of stats about objects:

"Allocations" means "allocations that are not from a freelist". Total
allocations = "Allocations from freelist" + "Allocations"

"New values" is the number of values array created for objects with managed
dicts.

The cache hit/miss numbers are for the MRO cache, split into dunder and other
names.

## GC stats

Garbage collection stats by generation.

Collected/visits gives some measure of efficiency.

## Optimization (Tier 2) stats

- Optimization attempts: The number of times a potential trace is identified.
  Specifically, occurs in the JUMP_BACKWARD instruction when the counter reaches
  `optimizer_backedge_threshold`.
- Traces created: The number of traces that were successfully created.
- Trace stack overflow: A potential trace is truncated because it would require
  more than 5 stack frames.
- Trace stack underflow: A potential trace is abandoned because it pops more
  frames than it pushes.
- Trace too long: A potential trace is truncated because it is longer than the buffer.
- Trace too short: A potential trace is abandoned because it is too short.
- Inner loop found: A potential trace is truncated because it has an inner loop.
- Recursive call: A potential trace is truncated because is has a recursive
  call.
- Low confidence: A potential trace is abandoned because the likelihood of the
  jump to top being taken is too low.
- Traces executed: The number of trace executions that occurred.

### Trace histograms

There are histograms for:

- The length of traces before optimization
- The length of traces after optimization
- The number of instructions executed per trace

### Uop execution stats

The number of times each uop was executed.

### Unsupported opcodes

The number of times an unsupported opcode caused a potential trace to be truncated.

## Rare events

- set class: Setting an object's class, `obj.__class__ = ...`
- set bases: Setting the bases of a class, `cls.__bases__ = ...`
- set eval frame func: Setting the PEP 523 frame eval function,
  `_PyInterpreterState_SetFrameEvalFunc()`
- builtin dict: Modifying the builtins, `__builtins__.__dict__[var] = ...`
- func modification: Modifying a function, e.g. `func.__defaults__ = ...`, etc.