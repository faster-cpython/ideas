# Tier 2 Optimizer for CPython -- Early design


## Abstract

We need a second tier of optimization to improve performance
beyond that of CPython 3.11.

The tier 2 optimizer for CPython will build on PEP 659, 
the tier 1 optimizer.

The tier 2 optimizer will optimize larger regions of code than
the tier 1 optimizer, optimizing tens of instructions at a time,
rather than a single instruction. This means that optimization
will be slower, with the expectation that performance will be
better.

The tier 2 optimizer will optimize short traces of bytgecode,
transforming them into instructions for a custom interpreter
that operates on lower level, more specialized instructions
than the normal interpreter.

Like tier 1 execution, tier 2 will be an interpreter, 
retaining full portability and ease of debugging.

Unlike the PEP 659 interpreter, it will execute on a purely in-memory
code representation, with no on-disk representation.

As the tier 2 optimizer will be slower than tier 1, the threshold for
optimization will be higher than PEP 659.
Initial counter settings will probably be in the low hundreds.

## Motivation

PEP 659 gives us a worhtwhile speed up over 3.10, but performance is
still poor compared to node.js and well-engineered JIT compilers.

We can raise performance from 3.11 levels by choosing larger regions
of code to optimize, allowing redundant computations to be dropped,
and moving some repeated checks out of the optimized code and adding
mechanisms to de-optimize these regions when changes occur elsewhere.

The performance gains will still not match those of well engineered
JIT compilers, but will provide a strong base for a JIT to be built on.


## Specification

Entries to functions, the `RESUME` instruction, and backward jumps, 
the `JUMP_BACKWARD` instruction, will gain counters. When these counters
reach a threshold, the instruction will be replaced with an `ENTER_TRACE`
instruction which will execute the optimized trace.

Traces will be projected from the current point of execution, using the
type information gathered by the PEP 659 interpreter to estimate when to
end the trace.

Once a trace has been formed, it will be optimized. Then it will be
executed next time the `ENTER_TRACE` instruction is reached.

To encourage experimentation and porting of PEP 523 JIT compilers,
an optimizer server API will be added.

## Optimizer Server API



```C
  type struct {
      OBJECT_HEADER;
      _PyInterpreterFrame *(*execute)(PyExecutorObject *self, _PyInterpreterFrame *frame, PyObject **stack_pointer);
      /* Data needed by the executor goes here, but is opaque to the VM */
  } PyExecutorObject;

  typedef enum {
      function_entry = 1,
      back_edges = 2,
      anywhere = 4,
      /* thread-safety? */
  } PyOptimizerCapabilities;

  type struct {
      OBJECT_HEADER;
      PyExecutorObject *(*compile)(PyOptimizerObject* self, PyCodeObject *code, int offset);
      PyOptimizerCapabilities capabilities;
      float optimization_cost;
      float run_cost;
      /* Data needed by the compiler goes here, but is opaque to the VM */
  } PyOptimizerObject;

  void _Py_Executor_Replace(PyCodeObject *code, int offset, PyExecutorObject *executor);

  int _Py_Optimizer_Register(PyOptimizerObject* optimizer);
```

## Projecting traces

Unlike the long traces gathered by tracing in tracing optimizer like PyPy,
we do not record traces, merely estimate forward execution to form a trace.
Unlike the very short traces in HHVM or YJIT, we can use the type information
gathered by the specializing interpreter to project longer traces with a higher
confidence in our estimates of how likely code is to stay on trace.


Consider this code::

   def f(y):
       return y*2

   def sumf(x):
       t = 0
       for y in x:
           t += f(y)

The functions compile to this bytecode (once specialized):

```
  f:
    RESUME                   0
    
    LOAD_FAST__LOAD_CONST    0 (y)
    LOAD_CONST               1 (2)
    BINARY_OP_MULTIPLY_INT   5 (*)
    RETURN_VALUE

  sumf:
    RESUME_QUICK             0
    
    LOAD_CONST               1 (0)
    STORE_FAST__LOAD_FAST     1 (t)
    
    LOAD_FAST                0 (x)
    GET_ITER
  loop:
    FOR_ITER_RANGE          18 (to 50)
    STORE_FAST__LOAD_FAST     2 (y)
    
    LOAD_FAST                1 (t)
    LOAD_GLOBAL_MODULE       1 (NULL + f)
    LOAD_FAST                2 (y)
    CALL_PY_EXACT_ARGS       1
    BINARY_OP_ADD_INT       13 (+=)
    STORE_FAST               1 (t)
    JUMP_BACKWARD_QUICK     loop
    
    LOAD_CONST               0 (None)
    RETURN_VALUE
```

Assuming that the counter triggers at `JUMP_BACKWARD_QUICK`
then the trace starts at `FOR_ITER_RANGE`,
we can then project the trace to `CALL_PY_EXACT_ARGS`
as there are no branches, and the specialized instructions
have good hit rates (100% in this case).
We can even project the trace into `f` as `CALL_PY_EXACT_ARGS`
has 100% hit rates. Resulting in the following trace:

```
  start:
    SAVE_LASTI
    FOR_ITER_RANGE           exit_trace
    SAVE_LASTI
    STORE_FAST               2 (y)
    SAVE_LASTI
    LOAD_FAST                1 (t)
    SAVE_LASTI
    LOAD_GLOBAL_MODULE       1 (NULL + f)
    SAVE_LASTI
    LOAD_FAST                2 (y)
    SAVE_LASTI
    CALL_PY_EXACT_ARGS       1
    SAVE_LASTI
    LOAD_FAST                0 (y)
    SAVE_LASTI
    LOAD_CONST               1 (2)
    SAVE_LASTI
    BINARY_OP_MULTIPLY_INT   5 (*)
    SAVE_LASTI
    RETURN_VALUE
    SAVE_LASTI
    BINARY_OP_ADD_INT       13 (+=)
    SAVE_LASTI
    STORE_FAST               1 (t)
    SAVE_LASTI
    JUMP_BACKWARD_QUICK      start
  exit_trace:
    EXIT_TO_INTERPRETER
```

Note the addition of `SAVE_LASTI` in between each instruction.
This is so that when an instruction deopts, it will return to the correct location in the original bytecode.

## Optimizing traces

Optimizing traces is a well research area. Rather than regurgitate that
research we run through how the above trace would be optimized,
as an example.

First of all we lower the specialized instructions into their
two parts; guard then action:

```
  start:
    SAVE_LASTI
    CHECK_IS_RANGE           deopt1
    FOR_ITER_RANGE_UNCHECKED exit_trace
    SAVE_LASTI
    STORE_FAST               2 (y)
    SAVE_LASTI
    LOAD_FAST                1 (t)
    SAVE_LASTI
    CHECK_GLOBAL_KEYS_VERSION deopt2
    LOAD_GLOBAL_MODULE_UNCHECKED 1 (NULL + f)
    SAVE_LASTI
    LOAD_FAST                2 (y)
    SAVE_LASTI
    CHECK_PY_EXACT_ARGS      1 (f)
    ENTER_PY_FUNCTION        1 (f)
    SAVE_LASTI
    LOAD_FAST                0 (y)
    SAVE_LASTI
    LOAD_CONST               1 (2)
    SAVE_LASTI
    CHECK_INTS_2             deopt3
    BINARY_OP_MULTIPLY_INT_UNCHECKED (*)
    SAVE_LASTI
    RETURN_VALUE
    SAVE_LASTI
    CHECK_INTS_2             deopt4
    BINARY_OP_ADD_INT_UNCHECKED (+=)
    SAVE_LASTI
    STORE_FAST               1 (t)
    SAVE_LASTI
    JUMP_BACKWARD_QUICK      start
  exit_trace:
    EXIT_TO_INTERPRETER
  deopt1:
    EXIT_TO_INTERPRETER
  deopt2:
    EXIT_TO_INTERPRETER
  deopt3:
    EXIT_TO_INTERPRETER
  deopt4:
    EXIT_TO_INTERPRETER
```

Then we move the `SAVE_LASTI`s to the exits:
```
  start:
    CHECK_IS_RANGE           deopt1
    FOR_ITER_RANGE_UNCHECKED exit_trace
    STORE_FAST               2 (y)
    LOAD_FAST                1 (t)
    CHECK_GLOBAL_KEYS_VERSION deopt2
    LOAD_GLOBAL_MODULE_UNCHECKED 1 (NULL + f)
    LOAD_FAST                2 (y)
    CHECK_PY_EXACT_ARGS      1 (f)
    ENTER_PY_FUNCTION        1 (f)
    LOAD_FAST                0 (y)
    LOAD_CONST               1 (2)
    CHECK_INTS_2             deopt3
    BINARY_OP_MULTIPLY_INT_UNCHECKED (*)
    RETURN_VALUE
    CHECK_INTS_2             deopt4
    BINARY_OP_ADD_INT_UNCHECKED (+=)
    STORE_FAST               1 (t)
    JUMP_BACKWARD_QUICK      start
  exit_trace:
    EXIT_TO_INTERPRETER
  deopt1:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt2:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt3:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt4:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
```

Then we add additional checks before the loop:
```
    CHECK_IS_RANGE           deopt1
    LOAD_FAST                1 (t)
    CHECK_INT                deopt5
    POP_TOP
  start:
    CHECK_IS_RANGE           deopt1
    FOR_ITER_RANGE_UNCHECKED exit_trace
    STORE_FAST               2 (y)
    LOAD_FAST                1 (t)
    CHECK_GLOBAL_KEYS_VERSION deopt2
    LOAD_GLOBAL_MODULE_UNCHECKED 1 (NULL + f)
    LOAD_FAST                2 (y)
    CHECK_PY_EXACT_ARGS      1 (f)
    ENTER_PY_FUNCTION        1 (f)
    LOAD_FAST                0 (y)
    LOAD_CONST               1 (2)
    CHECK_INTS_2             deopt3
    BINARY_OP_MULTIPLY_INT_UNCHECKED (*)
    RETURN_VALUE
    CHECK_INTS_2             deopt4
    BINARY_OP_ADD_INT_UNCHECKED (+=)
    STORE_FAST               1 (t)
    JUMP_BACKWARD_QUICK      start
  exit_trace:
    EXIT_TO_INTERPRETER
  deopt1:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt2:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt3:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt4:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt5:
    POP_TOP
    SAVE_LASTI
    EXIT_TO_INTERPRETER
```

Then we add watchers for the global `f` and for the function version,
so that the whole trace is deoptimized if they change:

```
  [ Whole trace is invalidated if f is redefined or modified ]
    CHECK_IS_RANGE           deopt1
    LOAD_FAST                1 (t)
    CHECK_INT                deopt5
    POP_TOP
  start:
    FOR_ITER_RANGE_UNCHECKED exit_trace
    STORE_FAST               2 (y)
    LOAD_FAST                1 (t)
    PUSH_NULL
    LOAD_CONSTANT            (f)
    LOAD_FAST                2 (y)
    CHECK_PY_EXACT_ARGS      1 (f)
    ENTER_PY_FUNCTION        1 (f)
    LOAD_FAST                0 (y)
    LOAD_CONST               1 (2)
    CHECK_INTS_2             deopt3
    BINARY_OP_MULTIPLY_INT_UNCHECKED (*)
    RETURN_VALUE
    CHECK_INTS_2             deopt4
    BINARY_OP_ADD_INT_UNCHECKED (+=)
    STORE_FAST               1 (t)
    JUMP_BACKWARD_QUICK      start
  exit_trace:
    EXIT_TO_INTERPRETER
  deopt1:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt2:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt3:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt4:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt5:
    POP_TOP
    SAVE_LASTI
    EXIT_TO_INTERPRETER
```

Then we perform type inference:

```
    CHECK_IS_RANGE           deopt1
    LOAD_FAST                1 (t)
    CHECK_INT                deopt5
    POP_TOP
  start:
    FOR_ITER_RANGE_UNCHECKED exit_trace
    STORE_FAST               2 (y)
    LOAD_FAST                1 (t)
    PUSH_NULL
    LOAD_CONSTANT            (f)
    LOAD_FAST                2 (y)
    # Removed as know f
    ENTER_PY_FUNCTION        1 (f)
    LOAD_FAST                0 (y)
    LOAD_CONST               1 (2) 
    # Removed as we know both are ints
    BINARY_OP_MULTIPLY_INT_UNCHECKED (*)
    RETURN_VALUE
    # Removed as we know both are ints
    BINARY_OP_ADD_INT_UNCHECKED (+=)
    STORE_FAST               1 (t)
    JUMP_BACKWARD_QUICK      start
  exit_trace:
    EXIT_TO_INTERPRETER
  deopt1:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt5:
    POP_TOP
    SAVE_LASTI
    EXIT_TO_INTERPRETER
```

Then we remove the temporary frame:
```
    CHECK_IS_RANGE           deopt1
    LOAD_FAST                1 (t)
    CHECK_INT                deopt5
    POP_TOP
  start:
    FOR_ITER_RANGE_UNCHECKED exit_trace
    STORE_FAST               2 (y)
    LOAD_FAST                1 (t)
    LOAD_FAST                2 (y)
    LOAD_CONST               1 (2) 
    BINARY_OP_FMA_UNCHECKED (*)
    BINARY_OP_ADD_INT_UNCHECKED (+=)
    STORE_FAST               1 (t)
    JUMP_BACKWARD_QUICK      start
  exit_trace:
    EXIT_TO_INTERPRETER
  deopt1:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt5:
    POP_TOP
    SAVE_LASTI
    EXIT_TO_INTERPRETER
```

Finally, we insert superinstructions:
```
    CHECK_IS_RANGE           deopt1
    LOAD_FAST                1 (t)
    CHECK_INT                deopt5
    SWAP                     2
  start:
    FOR_ITER_RANGE_UNCHECKED exit_trace
    STORE_FAST__LOAD_FAST    (y, t)
    LOAD_FAST__LOAD_CONST    (y, 2)
    BINARY_OP_MULTIPLY_INT_UNCHECKED (*)
    BINARY_OP_ADD_INT_UNCHECKED (+=)
    STORE_FAST               1 (t)
    JUMP_BACKWARD_QUICK      start
  exit_trace:
    STORE_FAST               1 (t)
    EXIT_TO_INTERPRETER
  deopt1:
    SAVE_LASTI
    EXIT_TO_INTERPRETER
  deopt5:
    POP_TOP
    SAVE_LASTI
    EXIT_TO_INTERPRETER
```

Unboxing integers is also a possibility.

