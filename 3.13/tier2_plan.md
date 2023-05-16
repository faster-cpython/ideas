## Plan for building the tier 2 optimizer.

### Components

* VM hooks and callbacks -- Enable VM to tell optimizer about hotspots and to warn it of changes.
* The superblock generator
* Specializer
* Partial evaluator
* Interpreter
* Compiler (Copy & patch)

### Design artifacts

* Optimizer API
* Optimizer instruction format
* Tier 2 interpreter instruction format (if different from the optimizer instruction format)
* Executable object layout

### Dependencies

#### TO DO -- Make a nice diagram

```
Optimizer API -> Superblock generator
Optimizer instruction format -> Superblock generator
Superblock generator -> Specializer
Superblock generator -> Partial evaluator
Superblock generator -> Compiler
Optimizer instruction format -> Interpreter instruction format
Interpreter instruction format -> Interpreter
Executable object layout -> Interpreter
Executable object layout -> Compiler
```

In theory the specializer, partial evaluator, interpreter, and compiler can all be developed in parallel.
But we need to able to test things.
In effect that means that we need to add the following arrows:

```
Interpreter -> Specializer
Interpreter -> Partial evaluator
Interpreter -> Compiler
```
