# This file is for reserving opcodes to avoid needless conflicts.

Before starting any work on adding new bytecodes, whether manually or automatically, please reserve the opcode(s) here.


## Guido

* INT_ADD 166
* RETURN_NONE 88
* RETURN_CONST 99
* POP_JUMP_IF_NONE 127
* POP_JUMP_IF_NOT_NONE 128

Super-instructions, e.g.
* LOAD_FAST_LOAD_FAST 167
* STORE_FAST_LOAD_FAST 168
* LOAD_FAST_LOAD_ATTR 169
* LOAD_FAST_LOAD_CONST 170
* LOAD_GLOBAL_LOAD_FAST 171
* LOAD_FAST_STORE_ATTR 172
* LOAD_GLOBAL_CALL_FUNCTION 173

## Mark

* GEN_START 129 (was 99, which is why I've made this file :)

## Eric
