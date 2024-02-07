# pystats documentation

This describes the meaning of the various sections and fields in the pystats output.

## Execution counts

This is the count of how many times each Tier 1 instruction is executed.

The "miss ratio" column shows the percentage of times the instruction executed that it deoptimized.

## Pair counts

Shows the Top 100 most frequently occurring pairs of instructions as executed.

## Predecessor / Successor pairs

Shows the top 5 instructions that are executed before and after each instruction.

## Specialization stats

TBD

## Specialization effectiveness

TBD

## Call stats

TBD

## Object stats

TBD

## GC stats

TBD

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

- set_class : Setting an object's class, `obj.__class__ = ...`
- set_bases: Setting the bases of a class, `cls.__bases__ = ...`
- set_eval_frame_func: Setting the PEP 523 frame eval function,
  `_PyInterpreterState_SetFrameEvalFunc()`
- builtin_dict: Modifying the builtins, `__builtins__.__dict__[var] = ...`
- func_modification: Modifying a function, e.g. `func.__defaults__ = ...`, etc.