# The Tier 2 Redundancy Eliminator

Author: Ken Jin, Mark Shannon

Tier 2 traces require optimization. At minimum, redundant operations
should be removed. This is where the name "Redundancy Eliminator" is
derived from. This forms part of the larger effort towards
the tier 2 optimizer.

## Abstract Interpretation of Uops

To analyze the uops, we use
[abstract interpretation](https://en.wikipedia.org/wiki/Abstract_interpretation).

Just like the CPython interpreter is an interpretation over
Python program state, represented by `PyObject *`, the abstract interpreter
shall be an interpretation over Python symbolic information state,
represented by `_Py_UOpsSymType *`.

The abstract interpreter has the equivalent constructs of the
CPython interpreter to represent state. It has symbolic
local and symbolic frames. This allows it to emulate CPython
runtime state accurately.

Executing "steps" in the abstract interpreter is thus similar to
doing the same in CPython -- by interpreting bytecode instructions.
The abstract interpreter thus "executes" a bytecode, update its
symbolic state, and repeats until it reaches a terminator (the end
of the trace).

### Lattice

**Note: if you are uninterested in the theory behind data-flow analysis,\
please skip this section.**

The states of information in such an abstract interpretation can be
represented by a [lattice](https://en.wikipedia.org/wiki/Lattice_(order))
of values. The lattice itself is an ordered powerset
of all variables and their associated information.

For example, here is a trivial lattice for the statement 
```python
x = 1
y = 2.0
```
:

```mermaid
flowchart BT
    A("`Bottom, ie. x: *?*, y: *?*`") --> B("`x: *int*, y: *?*`")
    A --> C("`x: *?*, y: *float*`")
    B --> D("`Top, x: *int*, y: *float*`")
    C --> D
  
```

Real Python runtime information
may contain more complex types, constants, and unions of types.

Each `_Py_UOpsSymType` captures all the information associated
with a variable at any point in the lattice. For example, it contains
type information stored as `PyTypeObject *`, and constant values.

For more information regarding lattices in compiler theory,
Page 27 onwards of this presentation provides a gentle introduction
https://ilyasergey.net/CS4212/_static/lectures/PLDI-Week-12-dataflow.pdf
Credits to the courses UPenn Compilers (CIS 341) and NUS Compiler
Design (CS4212).

The hiearchy of types in the type system can also be represented
by a lattice. Roughly, it looks like this:

```mermaid
graph BT;
    t("True");
    f("False");
    bl("bool");
    nnull(not NULL);
    nnone(not None);
    ot(other types);
    oc(other constants);
    b("bottom(unknown)");
    b-->NULL;
    b-->nnull;
    nnull-->nnone;
    nnull-->None;
    nnone-->ot;
    nnone-->bl;
    ot-->oc;
    oc-->top;
    None-->top;
    NULL-->top;
    bl-->t;
    bl-->f;
    t-->top;
    f-->top;
```

Note: there should be edges going from each type to `top`, but
for brevity and clarity we have omitted them.

Edges in the lattice represent a
[partial order relation](https://en.wikipedia.org/wiki/Partially_ordered_set).
For example, `bool <: True`, where `<:` is the supertype relation,
because `bool` is the supertype of `True`. The supertype relation is
reflexive, antisymmetric, and transitive, and is thus a partial
order relation.

The [least upper bound](https://www.infinitelymore.xyz/p/lattices)
of any pair `{a, b}` in the lattice, ie the *join* of `{a, b}`, represents
the the lowest common subtype of both `a` and `b`. In this case,
the lowest common subtype of any two types,
assuming `a != b`, is `top`. This means we can never reach
`top`, as that is a contradiction -- there is no type
in CPython that represents the subtype of all types. (Think:
how can something be a subtype of `int`, `float`, `str`, `bool`, etc.
all at the same time!)

The greatest lower bound of any pair `{a, b}` in the lattice, ie the
*meet* of `{a, b}`, represents the lowest common supertype of `{a, b}`,
where `a != b`.
For example, the lowest common supertype of `True` and `False` is
`bool`. The lowest common supertype of `bool` and `other types` is
`not None`, and so on. The *meet* represents a loss of specificity.


### Abstract DSL

A extra specification that overrides the original cases in
`Python/bytecodes.c` is used.
This generates an abstract interpreter that operates on these symbolic values.
Where there is no overridden case, the generator falls back to a generic
version where all output stack values are unknown symbolic values.

```
// Python/bytecodes.c
op(OP, (arg1 -- out)) {
    eggs();
}
```
```
// Python/tier2_redundancy_eliminator_bytecodes.c
// Nothing to see here :).
```
```
// Python/abstract_interp_cases.c.h
case OP: {
    _Py_UOpsSymType *out;
    out = sym_init_unknown(ctx);
    if (out == NULL) goto error;
    stack_pointer[-1] = out;
    break;
}
```

Where this is an overridden case, all information from the overridder
takes precedence. For example:

```
// Python/bytecodes.c
op(OP, (arg1 -- out)) {
    out = eggs(arg1);
}
```
```
// Python/tier2_redundancy_eliminator_bytecodes.c
op(OP, (arg1 -- out)) {
    out = spam(arg1);
}
```
```
// Python/abstract_interp_cases.c.h
case OP: {
    _Py_UOpsSymType *arg1;
    _Py_UOpsSymType *out;
    arg1 = stack_pointer[-1];
    out = spam(arg1);
    stack_pointer[-1] = out;
    break;
}
```


