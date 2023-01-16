# VM definition

## Abstract

The core of the VM consists of a bytecode array, a stack, an array of locals, an array of names, an array of constants, and several special registers.
In addition, there's infrastructure to handle call/return, yield/resume/throw, and await.
This description is geared towards the 3.12 interpreter (whose design is very much in flux).

## Data

Note that some of these are raw arrays, whereas others are Python objects (typically tuples).

- Bytecode: an array of ``_Py_CODEUNIT`` (16-bit) words containing instructions and inline caches. Accessed via ``next_instr``.
- Stack: an array of ``PyObject`` pointers used as temporary values.
  The stack grows up. The top is ``stack_pointer``.
- "Fast" locals (``frame->f_localsplus``): an array of ``PyObject`` pointers used to hold arguments, local variables, and "cells" used for nonlocal variables.
  Not to be confused with ``LOCALS()`` described below; these "fast" locals are used in regular functions.
- Names (``names``, caching ``frame->f_code->co_names``): a tuple of string objects used for accessing globals and attributes.
- Constants (``consts``, caching ``frame->f_code->co_consts``): a tuple of ``PyObject`` pointers holding constants referenced by the ``LOAD_CONST`` instruction.

## Special registers

- Frame pointer (``frame``, type ``_PyInterpreterFrame *``):
  The current stack frame.
  Other values can be found through this, though some are cached in other special registers.
  The previous frame (where ``return`` or ``yield`` should go) is ``frame->previous``.
- Instruction pointer (``next_instr``, type ``_Py_CODEUNIT *``):
  Address of the next instruction (or sometimes the current one or its inline cache).
  This points somewhere into the bytecode array.
- Stack pointer (``stack_pointer``, type ``PyObject **``):
  Address of the next free stack entry.
  A push operation is ``*stack_pointer++ = x``; a pop operation is ``x = *--stack_pointer``.
  The top value on the stack is ``stack_pointer[-1]``.
- Eval breaker (``eval_breaker``, type ``_Py_atomic_int *``):
  Pointer to a flag set by other threads and signal handlers to make the interpreter check for interrupts.
  This is accessed via macros like ``CHECK_EVAL_BREAKER()``.
  There is supposed to be an upper bound on the delay between eval breaker checks,
  which is enforced by checking it on all backwards jumps and calls.

## Other values used by the VM

- Globals (``GLOBALS()``, ``frame->f_globals``): A mapping (usually a dictionary) holding the current function's global variables.
- Builtins (``BUILTINS()``, ``frame->f_builtins``): A mapping (dictionary) holding the current function's builtins.
  This caches the ``__builtins__`` value in the globals.
- Locals (``LOCALS()``, ``frame->f_locals``): An optional mapping (dict) holding the locals in a class or module.

## Instruction dispatch

The instruction decoding logic is supposed to be equivalent to the following.
Note the special case for the ``EXTENDED_ARG`` opcode --
this is used (rarely) when the ``oparg`` value (e.g. a jump offset) doesn't fit in 8 bits.

```cc
_Py_CODEUNIT next_instr = ...;
PyObject **stack_pointer = ...;

for (;;) {
    _Py_CODEUNIT word = *next_instr++;
    uint8_t opcode = word.first_byte;
    uint32 oparg = word.second_byte;  // Second byte

    while (opcode == EXTENDED_ARG) {
        word = *next_instr++;
        oparg = word.first_byte;
        oparg = (oparg << 8) | word.second_byte;
    }

    switch (opcode) {

        case NOP:
            break;

        case OP:
            ... // Code for OP
            break;

        ... // Etc.

        default:
            Py_FatalError("...");  // Does not return

    }
}
```

## Branches

A jump or branch simply adjusts ``next_instr``:

```cc
        case JUMP_BACKWARD:
            next_instr -= oparg;
            CHECK_EVAL_BREAKER();
            break;

        case JUMP_FORWARD:
            next_instr += oparg;
            break;

        case POP_JUMP_IF_TRUE:
            PyObject *cond = POP();
            jump = Py_IsTrue(cond);
            Py_DECREF(cond);
            if (jump) {
                next_instr += oparg;
            }
            break;

        // Etc.
```

There is no absolute jump instruction (the compiler uses a relative forward or backward jump).

The actual code uses a macro ``JUMPBY(n)`` defined as ``next_instr += (n)``.

## Inline caches

When an instruction has inline cache data, the following idiom is used (obscured by macros):

```cc
        case OP:
            struct CacheForOp *cache = (struct CacheForOp *)next_instr;
            ... // Code using cache
            next_instr += sizeof(struct CacheForOp) / sizeof(_Py_CODEUNIT);
            break;
```

# Proposal: variable length instructions

Register instructions may require more than one argument.
For example, a register-based ``UNARY_NEGATIVE`` instruction has one input register and one output register.
A register-based ``BINARY_OP`` has three register arguments (two input, one output) and a fourth argument indicating the operation (``+``, ``*``, etc.).

An earlier design upgraded *all* instructions (but not ``_Py_CODEUNIT`` or cache entries) to be four bytes, but this is wasteful for simple instructions -- even a ``NOP`` would become four bytes.
(TODO: Investigate how many instructions would need at most one argument in a pure register world -- it's possible that the "wasteful" argument isn't that strong.)

Instead I propose a new format where instructions can be any number of ``_Py_CODEUNIT`` words in length.
Note that if we take the inline cache into account, this is already the case.

The dispatch code would look like this:

```cc
for (;;) {
    _Py_CODEUNIT word = *next_instr++;
    uint8_t opcode = word.first_byte;
    uint32 oparg1 = word.second_byte;
    uint32 oparg2;
    uint32 oparg3;
    uint32 oparg4;
    uint32 oparg5;

    switch (opcode) {

        case NOP:
            break;

        case OP_1_ARG:
            ... // Code using oparg1
            break;

        case OP_2_ARGS:
            word = *next_instr++;
            oparg2 = word.first_byte;
            ... // Code using oparg1 and oparg2
            break;

        case OP_3_ARGS:
            word = *next_instr++;
            oparg2 = word.first_byte;
            oparg3 = word.second_byte;
            ... // Code using oparg1, oparg2 and oparg3
            break;

        ...  // Etc.

    }
}
```

A design detail is what to do if ``oparg2`` or ``oparg3`` needs to be extended.
Because not all instructions use ``oparg2`` etc., we can't simply extend the
``EXTENDED_ARG`` scheme of the basic interpreter.

One possibility would be to have an instructions ``EXTENDED_ARG_3``, itself having three arguments.
It would do the same thing as ``EXTENDED_ARG``, first decoding its own three arguments,
then decode the following instruction (which is also assumed to have three arguments), and then...
It *switches* on that opcode and jumps into the implementation of that instruction *past* the argument decoding step.

```cc
for (;;) {
    _Py_CODEUNIT word = *next_instr++;
    uint8_t opcode = word.first_byte;
    uint32 oparg1 = word.second_byte;
    uint32 oparg2;
    uint32 oparg3;
    uint32 oparg4;
    uint32 oparg5;

    switch (oparg) {

        case OP_3_ARGS:
            word = *next_instr++;
            oparg2 = word.first_byte;
            oparg3 = word.second_byte;
        into_op_3_args:
            ... // Code using oparg1, oparg2 and oparg3
            break;

        case EXTENDED_ARG_3:
            // Decode second word of EXTENDED_ARG_3
            word = *next_instr++;
            oparg2 = word.first_byte;
            oparg3 = word.second_byte;
        into_extended_arg_3:
            // Decode following 3-arg instruction
            // First word
            word = *next_instr++;
            opcode = word.first_byte;
            oparg1 = (oparg1 << 8) | word.second_byte;
            // Second word
            word = *next_instr++;
            oparg2 = (oparg2 << 8) | word.first_byte;
            oparg3 = (oparg3 << 8) | word.second_byte;
            // Jump *into* the desired instruction,
            // after the instruction decoding part
            switch (oparg) {
                case OP_3_args:
                    goto into_op_3_args;
                // A case for every 3-arg opcode
                case EXTENDED_ARG_3:
                    goto into_extended_arg_3;
                default:
                    Py_FatalError("...");
            }

    }
}
```

The inner switch only contains cases for 2-arg and 3-arg opcodes.
There should be a similar opcode ``EXTENDED_ARG_5`` which handles 4-arg and 5-arg opcodes.
(For 2-arg and 4-arg opcodes, we waste some time setting ``oparg3`` or ``oparg5``,
but this should not be a big deal as long as extended arguments are rare.)
The original ``EXTENDED_ARG`` should still be retained for 1-arg opcodes.
The code generator can conveniently generate the necessary labels and the switch.

### Example

Suppose we wanted to emit a ``BINARY_OP`` instruction with opargs ``1, 2, 1000, 4``.
We'd emit this sequence:

```
EXTENDED_ARG_3  0, 0, 3
BINARY_OP       1, 2, 232, 4
```

And for ``BINARY_OP 100000, 2, 1000, 4`` we'd do:

```
EXTENDED_ARG_3  1, 0, 0
EXTENDED_ARG_3  134, 0, 3
BINARY_OP       160, 2, 232, 4
```

Note that in this case, because ``BINARY_OP`` has _four_ arguments, we need to jump into the ``BINARY_OP`` implementation after the decoding of the second word but before the decoding of the third and final word of the instruction.
This means that the generated code for ``BINARY_OP`` would look like this:

```cc
        case BINARY_OP:
            word = *next_instr++;
            oparg2 = word.first_byte;
            oparg3 = word.second_byte;
        into_binary_op_3:  // Label for EXTENDED_ARG_3
            word = *next_instr++;
            oparg4 = word.first_byte;
        into_binary_op_5:  // Label for EXTENDED_ARG_5
            ... // Implementation of BINARY_OP
            break;
```
