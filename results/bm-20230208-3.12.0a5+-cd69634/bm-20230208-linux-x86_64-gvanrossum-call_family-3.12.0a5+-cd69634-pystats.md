
# Pystats results

- fork: gvanrossum
- ref: call-family
- commit hash: cd69634
- commit date: 2023-02-08T07:19:49-08:00

## Execution counts

<details>
<summary> execution counts for all instructions </summary>

|Name | Count | Self | Cumulative | Miss ratio | 
|---|---:|---:|---:|---:|
| LOAD_FAST | 17,035,315,667 | 15.1% | 15.1% |  |
| LOAD_FAST__LOAD_FAST | 5,747,506,592 | 5.1% | 20.3% |  |
| RESUME | 4,826,105,991 | 4.3% | 24.5% |  |
| STORE_FAST__LOAD_FAST | 4,341,602,396 | 3.9% | 28.4% |  |
| POP_JUMP_IF_FALSE | 4,141,851,344 | 3.7% | 32.1% |  |
| LOAD_GLOBAL_BUILTIN | 4,039,073,404 | 3.6% | 35.7% | 0.0% |
| LOAD_CONST | 3,983,427,470 | 3.5% | 39.2% |  |
| LOAD_ATTR_INSTANCE_VALUE | 3,526,219,573 | 3.1% | 42.4% | 5.2% |
| RETURN_VALUE | 2,796,020,337 | 2.5% | 44.8% |  |
| LOAD_GLOBAL_MODULE | 2,551,854,501 | 2.3% | 47.1% | 0.0% |
| CALL_PY_EXACT_ARGS | 2,482,271,828 | 2.2% | 49.3% | 3.8% |
| JUMP_BACKWARD | 2,357,996,886 | 2.1% | 51.4% |  |
| POP_TOP | 2,220,442,438 | 2.0% | 53.4% |  |
| LOAD_FAST__LOAD_CONST | 2,047,850,790 | 1.8% | 55.2% |  |
| STORE_FAST__STORE_FAST | 2,009,493,456 | 1.8% | 57.0% |  |
| STORE_FAST | 2,009,311,023 | 1.8% | 58.8% |  |
| LOAD_ATTR_METHOD_WITH_VALUES | 1,716,315,581 | 1.5% | 60.3% | 8.4% |
| INTERPRETER_EXIT | 1,639,977,920 | 1.5% | 61.8% |  |
| LOAD_ATTR_SLOT | 1,408,842,329 | 1.3% | 63.0% | 6.2% |
| LOAD_ATTR_METHOD_NO_DICT | 1,343,893,099 | 1.2% | 64.2% | 3.9% |
| LOAD_ATTR | 1,339,922,689 | 1.2% | 65.4% |  |
| RETURN_CONST | 1,337,761,631 | 1.2% | 66.6% |  |
| COMPARE_AND_BRANCH_INT | 1,319,943,776 | 1.2% | 67.8% | 0.1% |
| FOR_ITER_LIST | 1,248,287,291 | 1.1% | 68.9% | 5.3% |
| BINARY_OP_ADD_INT | 1,213,400,138 | 1.1% | 70.0% | 0.0% |
| POP_JUMP_IF_TRUE | 1,173,959,474 | 1.0% | 71.0% |  |
| BINARY_SUBSCR | 1,117,016,271 | 1.0% | 72.0% |  |
| STORE_ATTR_SLOT | 1,050,600,013 | 0.9% | 72.9% | 10.8% |
| LOAD_CONST__LOAD_FAST | 989,991,420 | 0.9% | 73.8% |  |
| CALL_NO_KW_BUILTIN_FAST | 982,731,212 | 0.9% | 74.7% | 0.0% |
| CALL | 959,248,494 | 0.9% | 75.5% |  |
| LOAD_DEREF | 914,173,214 | 0.8% | 76.3% |  |
| BINARY_SUBSCR_LIST_INT | 903,339,185 | 0.8% | 77.1% | 0.4% |
| PUSH_NULL | 882,291,686 | 0.8% | 77.9% |  |
| BINARY_OP | 858,939,640 | 0.8% | 78.7% |  |
| CALL_NO_KW_BUILTIN_O | 852,494,625 | 0.8% | 79.5% | 0.3% |
| SWAP | 840,124,248 | 0.7% | 80.2% |  |
| BINARY_OP_MULTIPLY_FLOAT | 827,610,461 | 0.7% | 80.9% | 0.8% |
| STORE_ATTR_INSTANCE_VALUE | 811,841,142 | 0.7% | 81.7% | 7.8% |
| COPY | 811,665,002 | 0.7% | 82.4% |  |
| CONTAINS_OP | 740,041,783 | 0.7% | 83.0% |  |
| CALL_NO_KW_ISINSTANCE | 710,568,347 | 0.6% | 83.7% |  |
| YIELD_VALUE | 686,035,619 | 0.6% | 84.3% |  |
| IS_OP | 664,533,097 | 0.6% | 84.9% |  |
| UNPACK_SEQUENCE_TWO_TUPLE | 616,685,151 | 0.5% | 85.4% |  |
| BUILD_TUPLE | 599,332,761 | 0.5% | 86.0% |  |
| GET_ITER | 548,499,145 | 0.5% | 86.4% |  |
| NOP | 505,483,854 | 0.4% | 86.9% |  |
| POP_JUMP_IF_NOT_NONE | 468,536,707 | 0.4% | 87.3% |  |
| BINARY_OP_SUBTRACT_INT | 466,165,544 | 0.4% | 87.7% | 0.1% |
| FOR_ITER_RANGE | 464,135,705 | 0.4% | 88.1% | 0.0% |
| JUMP_FORWARD | 446,699,418 | 0.4% | 88.5% |  |
| EXTENDED_ARG | 429,299,555 | 0.4% | 88.9% |  |
| UNPACK_SEQUENCE_TUPLE | 427,162,490 | 0.4% | 89.3% | 0.3% |
| CALL_NO_KW_METHOD_DESCRIPTOR_FAST | 407,536,326 | 0.4% | 89.7% | 8.1% |
| CALL_NO_KW_TYPE_1 | 393,391,002 | 0.3% | 90.0% |  |
| BINARY_OP_ADD_FLOAT | 390,022,266 | 0.3% | 90.3% | 1.6% |
| BINARY_SUBSCR_DICT | 381,156,484 | 0.3% | 90.7% | 0.0% |
| FOR_ITER | 378,970,834 | 0.3% | 91.0% |  |
| LOAD_ATTR_MODULE | 361,737,918 | 0.3% | 91.3% | 0.0% |
| POP_JUMP_IF_NONE | 344,928,920 | 0.3% | 91.7% |  |
| STORE_SUBSCR | 332,547,148 | 0.3% | 91.9% |  |
| LOAD_ATTR_WITH_HINT | 325,056,270 | 0.3% | 92.2% | 2.4% |
| SEND | 319,385,810 | 0.3% | 92.5% |  |
| CALL_NO_KW_LEN | 318,894,856 | 0.3% | 92.8% |  |
| STORE_SUBSCR_LIST_INT | 317,831,648 | 0.3% | 93.1% | 0.0% |
| BUILD_LIST | 306,199,892 | 0.3% | 93.4% |  |
| FOR_ITER_TUPLE | 297,364,006 | 0.3% | 93.6% | 22.3% |
| COPY_FREE_VARS | 271,725,997 | 0.2% | 93.9% |  |
| BINARY_OP_SUBTRACT_FLOAT | 269,783,531 | 0.2% | 94.1% | 5.6% |
| BINARY_OP_MULTIPLY_INT | 267,696,403 | 0.2% | 94.3% | 3.2% |
| CALL_NO_KW_LIST_APPEND | 256,206,751 | 0.2% | 94.6% | 0.0% |
| CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS | 238,552,376 | 0.2% | 94.8% | 8.7% |
| BINARY_SUBSCR_TUPLE_INT | 232,083,144 | 0.2% | 95.0% | 0.0% |
| CALL_BOUND_METHOD_EXACT_ARGS | 230,614,142 | 0.2% | 95.2% | 12.7% |
| COMPARE_OP | 224,516,260 | 0.2% | 95.4% |  |
| RETURN_GENERATOR | 221,025,288 | 0.2% | 95.6% |  |
| CALL_BUILTIN_CLASS | 219,431,914 | 0.2% | 95.8% | 0.0% |
| CALL_NO_KW_METHOD_DESCRIPTOR_O | 216,957,940 | 0.2% | 96.0% | 0.2% |
| KW_NAMES | 188,627,905 | 0.2% | 96.1% |  |
| STORE_SUBSCR_DICT | 186,473,842 | 0.2% | 96.3% |  |
| BINARY_SLICE | 163,370,570 | 0.1% | 96.5% |  |
| BUILD_SLICE | 158,520,478 | 0.1% | 96.6% |  |
| CALL_PY_WITH_DEFAULTS | 153,376,444 | 0.1% | 96.7% | 3.4% |
| BINARY_SUBSCR_GETITEM | 148,412,522 | 0.1% | 96.9% | 0.6% |
| JUMP_IF_FALSE_OR_POP | 147,838,893 | 0.1% | 97.0% |  |
| LOAD_ATTR_METHOD_LAZY_DICT | 144,462,043 | 0.1% | 97.1% | 0.0% |
| CALL_INTRINSIC_1 | 142,912,985 | 0.1% | 97.3% |  |
| COMPARE_AND_BRANCH | 142,674,800 | 0.1% | 97.4% |  |
| UNPACK_SEQUENCE_LIST | 140,459,316 | 0.1% | 97.5% | 0.9% |
| DELETE_SUBSCR | 131,997,659 | 0.1% | 97.6% |  |
| FOR_ITER_GEN | 128,325,040 | 0.1% | 97.7% | 0.1% |
| JUMP_BACKWARD_NO_INTERRUPT | 125,849,532 | 0.1% | 97.8% |  |
| MAKE_FUNCTION | 122,940,736 | 0.1% | 98.0% |  |
| UNARY_NEGATIVE | 121,639,475 | 0.1% | 98.1% |  |
| MAKE_CELL | 121,012,009 | 0.1% | 98.2% |  |
| LIST_APPEND | 117,942,577 | 0.1% | 98.3% |  |
| STORE_SLICE | 117,635,220 | 0.1% | 98.4% |  |
| LOAD_ATTR_CLASS | 113,610,378 | 0.1% | 98.5% | 1.2% |
| FORMAT_VALUE | 111,055,620 | 0.1% | 98.6% |  |
| GET_ANEXT | 100,136,760 | 0.1% | 98.7% |  |
| CALL_FUNCTION_EX | 96,387,671 | 0.1% | 98.8% |  |
| LOAD_CLOSURE | 94,726,575 | 0.1% | 98.8% |  |
| COMPARE_AND_BRANCH_STR | 90,162,937 | 0.1% | 98.9% | 0.5% |
| CALL_BUILTIN_FAST_WITH_KEYWORDS | 86,537,579 | 0.1% | 99.0% | 0.0% |
| GET_AWAITABLE | 83,837,114 | 0.1% | 99.1% |  |
| BUILD_MAP | 82,021,758 | 0.1% | 99.1% |  |
| STORE_DEREF | 66,506,211 | 0.1% | 99.2% |  |
| LOAD_ATTR_PROPERTY | 65,650,884 | 0.1% | 99.3% | 13.3% |
| BINARY_OP_ADD_UNICODE | 62,695,000 | 0.1% | 99.3% |  |
| COMPARE_AND_BRANCH_FLOAT | 62,016,795 | 0.1% | 99.4% | 0.0% |
| STORE_ATTR | 57,324,596 | 0.1% | 99.4% |  |
| BUILD_STRING | 56,411,220 | 0.1% | 99.5% |  |
| CALL_NO_KW_STR_1 | 55,976,263 | 0.0% | 99.5% |  |
| JUMP_IF_TRUE_OR_POP | 54,856,611 | 0.0% | 99.6% |  |
| STORE_ATTR_WITH_HINT | 50,302,458 | 0.0% | 99.6% | 2.0% |
| LIST_EXTEND | 49,458,469 | 0.0% | 99.7% |  |
| UNARY_NOT | 46,520,224 | 0.0% | 99.7% |  |
| END_FOR | 38,659,026 | 0.0% | 99.7% |  |
| MAP_ADD | 37,774,888 | 0.0% | 99.8% |  |
| DICT_MERGE | 31,382,862 | 0.0% | 99.8% |  |
| CALL_NO_KW_TUPLE_1 | 26,012,216 | 0.0% | 99.8% |  |
| CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS | 24,271,185 | 0.0% | 99.8% | 7.2% |
| PUSH_EXC_INFO | 17,759,861 | 0.0% | 99.9% |  |
| POP_EXCEPT | 17,759,861 | 0.0% | 99.9% |  |
| CHECK_EXC_MATCH | 17,359,204 | 0.0% | 99.9% |  |
| LOAD_GLOBAL | 14,618,697 | 0.0% | 99.9% |  |
| UNARY_INVERT | 11,928,511 | 0.0% | 99.9% |  |
| GET_YIELD_FROM_ITER | 9,562,404 | 0.0% | 99.9% |  |
| IMPORT_FROM | 9,556,734 | 0.0% | 99.9% |  |
| LOAD_NAME | 9,003,000 | 0.0% | 99.9% |  |
| DELETE_ATTR | 8,615,157 | 0.0% | 99.9% |  |
| IMPORT_NAME | 8,341,242 | 0.0% | 100.0% |  |
| BUILD_CONST_KEY_MAP | 7,373,717 | 0.0% | 100.0% |  |
| STORE_GLOBAL | 6,152,400 | 0.0% | 100.0% |  |
| GET_AITER | 6,000,000 | 0.0% | 100.0% |  |
| END_ASYNC_FOR | 6,000,000 | 0.0% | 100.0% |  |
| LOAD_FAST_CHECK | 5,610,627 | 0.0% | 100.0% |  |
| BEFORE_WITH | 4,074,277 | 0.0% | 100.0% |  |
| SET_ADD | 3,114,300 | 0.0% | 100.0% |  |
| BINARY_OP_INPLACE_ADD_UNICODE | 2,871,580 | 0.0% | 100.0% |  |
| RERAISE | 2,589,480 | 0.0% | 100.0% |  |
| RAISE_VARARGS | 2,253,368 | 0.0% | 100.0% |  |
| BUILD_SET | 1,520,188 | 0.0% | 100.0% |  |
| DELETE_FAST | 1,347,480 | 0.0% | 100.0% |  |
| UNPACK_SEQUENCE | 401,905 | 0.0% | 100.0% |  |
| UNPACK_EX | 220,200 | 0.0% | 100.0% |  |
| WITH_EXCEPT_START | 36,000 | 0.0% | 100.0% |  |
| SET_UPDATE | 16,680 | 0.0% | 100.0% |  |
| DICT_UPDATE | 13,140 | 0.0% | 100.0% |  |
| STORE_NAME | 5,220 | 0.0% | 100.0% |  |
| LOAD_CLASSDEREF | 2,580 | 0.0% | 100.0% |  |
| LOAD_BUILD_CLASS | 1,320 | 0.0% | 100.0% |  |
| DELETE_DEREF | 1,200 | 0.0% | 100.0% |  |
| CLEANUP_THROW | 240 | 0.0% | 100.0% |  |
| BEFORE_ASYNC_WITH | 60 | 0.0% | 100.0% |  |


</details>

## Pair counts

<details>
<summary> Pair counts for top 100 pairs </summary>

|Pair | Count | Self | Cumulative | 
|---|---:|---:|---:|
| LOAD_FAST LOAD_ATTR_INSTANCE_VALUE | 2,804,694,687 | 2.5% | 2.5% |
| LOAD_GLOBAL_BUILTIN LOAD_FAST | 2,320,786,496 | 2.1% | 4.6% |
| CALL_PY_EXACT_ARGS RESUME | 2,232,932,662 | 2.0% | 6.5% |
| RESUME LOAD_FAST | 1,926,195,654 | 1.7% | 8.3% |
| POP_JUMP_IF_FALSE LOAD_FAST | 1,813,356,165 | 1.6% | 9.9% |
| LOAD_FAST LOAD_ATTR_SLOT | 1,113,177,368 | 1.0% | 10.9% |
| LOAD_FAST LOAD_ATTR_METHOD_WITH_VALUES | 1,099,575,026 | 1.0% | 11.8% |
| LOAD_ATTR_INSTANCE_VALUE LOAD_FAST | 1,020,380,722 | 0.9% | 12.7% |
| LOAD_FAST LOAD_GLOBAL_BUILTIN | 977,050,361 | 0.9% | 13.6% |
| JUMP_BACKWARD FOR_ITER_LIST | 914,687,578 | 0.8% | 14.4% |
| POP_JUMP_IF_FALSE LOAD_GLOBAL_BUILTIN | 889,952,943 | 0.8% | 15.2% |
| RESUME LOAD_GLOBAL_BUILTIN | 884,055,277 | 0.8% | 16.0% |
| STORE_FAST__STORE_FAST STORE_FAST__STORE_FAST | 822,937,356 | 0.7% | 16.7% |
| STORE_FAST__LOAD_FAST LOAD_FAST | 770,073,597 | 0.7% | 17.4% |
| LOAD_FAST CALL_PY_EXACT_ARGS | 761,004,042 | 0.7% | 18.1% |
| POP_TOP JUMP_BACKWARD | 731,897,375 | 0.7% | 18.7% |
| LOAD_FAST__LOAD_FAST CALL_PY_EXACT_ARGS | 663,819,636 | 0.6% | 19.3% |
| CONTAINS_OP POP_JUMP_IF_FALSE | 656,984,897 | 0.6% | 19.9% |
| LOAD_FAST__LOAD_FAST LOAD_FAST__LOAD_FAST | 643,351,741 | 0.6% | 20.5% |
| LOAD_FAST RETURN_VALUE | 641,512,872 | 0.6% | 21.1% |
| POP_TOP LOAD_FAST | 621,714,371 | 0.6% | 21.6% |
| LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST__LOAD_FAST | 612,112,823 | 0.5% | 22.2% |
| LOAD_ATTR_METHOD_NO_DICT LOAD_FAST | 611,370,772 | 0.5% | 22.7% |
| YIELD_VALUE INTERPRETER_EXIT | 596,523,325 | 0.5% | 23.2% |
| UNPACK_SEQUENCE_TWO_TUPLE STORE_FAST__STORE_FAST | 586,600,607 | 0.5% | 23.8% |
| LOAD_FAST LOAD_GLOBAL_MODULE | 571,294,439 | 0.5% | 24.3% |
| IS_OP POP_JUMP_IF_FALSE | 559,188,426 | 0.5% | 24.8% |
| CALL_NO_KW_ISINSTANCE POP_JUMP_IF_FALSE | 554,306,333 | 0.5% | 25.3% |
| RESUME POP_TOP | 552,814,168 | 0.5% | 25.7% |
| COMPARE_AND_BRANCH_INT LOAD_FAST | 552,004,674 | 0.5% | 26.2% |
| RETURN_CONST POP_TOP | 547,740,410 | 0.5% | 26.7% |
| LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST | 546,627,286 | 0.5% | 27.2% |
| LOAD_FAST POP_JUMP_IF_TRUE | 540,513,998 | 0.5% | 27.7% |
| LOAD_ATTR_INSTANCE_VALUE POP_JUMP_IF_FALSE | 539,789,560 | 0.5% | 28.2% |
| STORE_FAST LOAD_GLOBAL_BUILTIN | 525,411,696 | 0.5% | 28.6% |
| RETURN_CONST INTERPRETER_EXIT | 525,400,243 | 0.5% | 29.1% |
| RETURN_VALUE INTERPRETER_EXIT | 503,693,372 | 0.4% | 29.5% |
| LOAD_FAST LOAD_ATTR_METHOD_NO_DICT | 503,234,646 | 0.4% | 30.0% |
| LOAD_FAST__LOAD_FAST STORE_ATTR_SLOT | 502,486,513 | 0.4% | 30.4% |
| LOAD_FAST LOAD_ATTR | 486,147,313 | 0.4% | 30.9% |
| FOR_ITER_LIST STORE_FAST__LOAD_FAST | 484,768,633 | 0.4% | 31.3% |
| POP_JUMP_IF_TRUE LOAD_FAST | 482,910,872 | 0.4% | 31.7% |
| PUSH_NULL LOAD_FAST__LOAD_FAST | 480,220,756 | 0.4% | 32.2% |
| LOAD_DEREF LOAD_FAST | 472,217,074 | 0.4% | 32.6% |
| LOAD_CONST LOAD_CONST | 458,914,413 | 0.4% | 33.0% |
| STORE_FAST__LOAD_FAST LOAD_CONST | 455,583,786 | 0.4% | 33.4% |
| STORE_FAST__STORE_FAST LOAD_FAST | 445,230,311 | 0.4% | 33.8% |
| RETURN_VALUE RETURN_VALUE | 439,035,905 | 0.4% | 34.2% |
| LOAD_GLOBAL_BUILTIN CALL_NO_KW_BUILTIN_FAST | 435,765,640 | 0.4% | 34.6% |
| JUMP_BACKWARD FOR_ITER_RANGE | 428,472,955 | 0.4% | 34.9% |
| LOAD_CONST BINARY_OP_ADD_INT | 426,341,962 | 0.4% | 35.3% |
| LOAD_FAST BINARY_SUBSCR | 420,561,189 | 0.4% | 35.7% |
| BINARY_SUBSCR LOAD_FAST | 413,519,637 | 0.4% | 36.1% |
| LOAD_ATTR_METHOD_WITH_VALUES CALL_PY_EXACT_ARGS | 402,379,719 | 0.4% | 36.4% |
| CALL_NO_KW_BUILTIN_FAST POP_JUMP_IF_FALSE | 400,893,172 | 0.4% | 36.8% |
| UNPACK_SEQUENCE_TUPLE STORE_FAST__STORE_FAST | 391,868,812 | 0.3% | 37.1% |
| LOAD_FAST CALL_NO_KW_TYPE_1 | 389,714,234 | 0.3% | 37.5% |
| STORE_FAST__LOAD_FAST LOAD_ATTR_METHOD_WITH_VALUES | 389,372,143 | 0.3% | 37.8% |
| LOAD_FAST CALL_NO_KW_BUILTIN_O | 388,769,611 | 0.3% | 38.2% |
| CALL_NO_KW_BUILTIN_O POP_TOP | 386,831,386 | 0.3% | 38.5% |
| LOAD_FAST__LOAD_FAST LOAD_CONST | 381,508,162 | 0.3% | 38.9% |
| LOAD_GLOBAL_MODULE CALL_NO_KW_ISINSTANCE | 367,534,201 | 0.3% | 39.2% |
| STORE_FAST__LOAD_FAST POP_JUMP_IF_FALSE | 366,870,075 | 0.3% | 39.5% |
| LOAD_FAST__LOAD_FAST LOAD_FAST | 364,617,525 | 0.3% | 39.8% |
| LOAD_FAST BINARY_OP_MULTIPLY_FLOAT | 363,615,000 | 0.3% | 40.2% |
| LOAD_FAST__LOAD_CONST BINARY_OP_ADD_INT | 360,353,640 | 0.3% | 40.5% |
| LOAD_CONST COMPARE_AND_BRANCH_INT | 341,737,364 | 0.3% | 40.8% |
| POP_JUMP_IF_TRUE JUMP_BACKWARD | 341,166,235 | 0.3% | 41.1% |
| POP_JUMP_IF_FALSE LOAD_FAST__LOAD_FAST | 340,550,175 | 0.3% | 41.4% |
| STORE_FAST__LOAD_FAST LOAD_GLOBAL_MODULE | 340,415,290 | 0.3% | 41.7% |
| BUILD_TUPLE RETURN_VALUE | 337,650,089 | 0.3% | 42.0% |
| LOAD_GLOBAL_MODULE LOAD_ATTR_MODULE | 336,653,087 | 0.3% | 42.3% |
| LOAD_FAST__LOAD_FAST STORE_ATTR_INSTANCE_VALUE | 321,911,686 | 0.3% | 42.6% |
| LOAD_ATTR_SLOT LOAD_FAST | 320,971,277 | 0.3% | 42.9% |
| FOR_ITER_LIST UNPACK_SEQUENCE_TWO_TUPLE | 319,430,100 | 0.3% | 43.1% |
| RETURN_VALUE STORE_FAST__LOAD_FAST | 314,435,324 | 0.3% | 43.4% |
| LOAD_CONST STORE_FAST | 314,367,119 | 0.3% | 43.7% |
| RESUME LOAD_FAST__LOAD_FAST | 313,140,747 | 0.3% | 44.0% |
| STORE_FAST__LOAD_FAST LOAD_ATTR_METHOD_NO_DICT | 308,892,618 | 0.3% | 44.3% |
| LOAD_FAST POP_JUMP_IF_FALSE | 306,197,110 | 0.3% | 44.5% |
| LOAD_GLOBAL_BUILTIN LOAD_FAST__LOAD_CONST | 304,025,889 | 0.3% | 44.8% |
| LOAD_FAST BINARY_SUBSCR_LIST_INT | 302,830,291 | 0.3% | 45.1% |
| LOAD_FAST__LOAD_CONST LOAD_CONST | 292,554,746 | 0.3% | 45.3% |
| CALL STORE_FAST__LOAD_FAST | 291,906,849 | 0.3% | 45.6% |
| LOAD_CONST CALL_NO_KW_BUILTIN_FAST | 290,712,040 | 0.3% | 45.8% |
| STORE_FAST PUSH_NULL | 287,347,229 | 0.3% | 46.1% |
| CALL_NO_KW_METHOD_DESCRIPTOR_FAST STORE_FAST__LOAD_FAST | 286,231,147 | 0.3% | 46.4% |
| BINARY_OP_MULTIPLY_FLOAT BINARY_OP_ADD_FLOAT | 284,043,300 | 0.3% | 46.6% |
| LOAD_ATTR LOAD_FAST | 283,668,865 | 0.3% | 46.9% |
| LOAD_CONST__LOAD_FAST STORE_ATTR_SLOT | 282,953,597 | 0.3% | 47.1% |
| LOAD_FAST BINARY_OP_ADD_INT | 281,326,822 | 0.3% | 47.4% |
| STORE_ATTR_SLOT LOAD_FAST__LOAD_FAST | 281,273,578 | 0.3% | 47.6% |
| RESUME LOAD_GLOBAL_MODULE | 280,831,902 | 0.2% | 47.9% |
| JUMP_BACKWARD FOR_ITER | 270,505,723 | 0.2% | 48.1% |
| COPY COPY | 270,086,400 | 0.2% | 48.3% |
| SWAP SWAP | 270,086,400 | 0.2% | 48.6% |
| LOAD_GLOBAL_MODULE CONTAINS_OP | 266,981,914 | 0.2% | 48.8% |
| LOAD_GLOBAL_MODULE LOAD_FAST | 266,684,712 | 0.2% | 49.1% |
| NOP LOAD_FAST | 266,157,610 | 0.2% | 49.3% |
| STORE_ATTR_INSTANCE_VALUE LOAD_FAST | 265,735,218 | 0.2% | 49.5% |


</details>

## Predecessor/Successor Pairs

<details>
<summary> Top 5 predecessors and successors of each opcode </summary>

### <252>

<details>
<summary> Successors and predecessors for <252> </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|

|Successors | Count | Percentage | 
|---|---:|---:|
| EXTENDED_ARG | 99,358,740 | 69.1% |
| STORE_FAST__LOAD_FAST | 44,469,720 | 30.9% |


</details>

### BEFORE_ASYNC_WITH

<details>
<summary> Successors and predecessors for BEFORE_ASYNC_WITH </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 60 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| GET_AWAITABLE | 60 | 100.0% |


</details>

### BEFORE_WITH

<details>
<summary> Successors and predecessors for BEFORE_WITH </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RETURN_VALUE | 1,998,280 | 49.0% |
| LOAD_ATTR_INSTANCE_VALUE | 1,476,244 | 36.2% |
| CALL | 491,925 | 12.1% |
| LOAD_GLOBAL_MODULE | 70,928 | 1.7% |
| CALL_BUILTIN_FAST_WITH_KEYWORDS | 36,900 | 0.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_TOP | 3,463,132 | 85.0% |
| STORE_FAST__LOAD_FAST | 516,785 | 12.7% |
| STORE_FAST | 92,920 | 2.3% |
| UNPACK_SEQUENCE_TWO_TUPLE | 1,440 | 0.0% |


</details>

### BINARY_OP

<details>
<summary> Successors and predecessors for BINARY_OP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 215,138,482 | 25.0% |
| LOAD_FAST | 111,661,225 | 13.0% |
| LOAD_FAST__LOAD_FAST | 76,129,945 | 8.9% |
| CALL_NO_KW_METHOD_DESCRIPTOR_O | 72,002,140 | 8.4% |
| RETURN_VALUE | 49,381,755 | 5.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 131,600,277 | 15.3% |
| LOAD_FAST | 107,880,076 | 12.6% |
| LOAD_FAST__LOAD_FAST | 106,838,711 | 12.4% |
| RETURN_VALUE | 81,130,645 | 9.4% |
| LOAD_CONST | 66,842,791 | 7.8% |


</details>

### BINARY_OP_ADD_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_FLOAT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_MULTIPLY_FLOAT | 284,043,300 | 72.8% |
| LOAD_FAST | 65,128,643 | 16.7% |
| RETURN_VALUE | 17,287,200 | 4.4% |
| BINARY_OP_MULTIPLY_INT | 8,437,640 | 2.2% |
| BINARY_OP | 6,097,100 | 1.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| SWAP | 116,255,040 | 29.8% |
| STORE_FAST | 90,506,403 | 23.2% |
| LOAD_FAST | 45,573,260 | 11.7% |
| LOAD_FAST__LOAD_FAST | 41,370,060 | 10.6% |
| RETURN_VALUE | 31,350,960 | 8.0% |


</details>

### BINARY_OP_ADD_INT

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_INT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 426,341,962 | 35.1% |
| LOAD_FAST__LOAD_CONST | 360,353,640 | 29.7% |
| LOAD_FAST | 281,326,822 | 23.2% |
| LOAD_FAST__LOAD_FAST | 47,607,610 | 3.9% |
| SEND | 29,134,080 | 2.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 237,571,081 | 19.6% |
| LOAD_CONST | 129,229,054 | 10.7% |
| STORE_SLICE | 103,909,740 | 8.6% |
| BINARY_OP_MULTIPLY_INT | 96,055,140 | 7.9% |
| BINARY_SUBSCR | 88,165,020 | 7.3% |


</details>

### BINARY_OP_ADD_UNICODE

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_UNICODE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 33,779,800 | 53.9% |
| LOAD_CONST | 12,177,380 | 19.4% |
| CALL_NO_KW_STR_1 | 4,820,800 | 7.7% |
| LOAD_ATTR | 2,417,980 | 3.9% |
| BUILD_STRING | 2,011,200 | 3.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 16,301,100 | 26.0% |
| CALL_NO_KW_BUILTIN_O | 15,909,600 | 25.4% |
| LOAD_CONST | 8,836,380 | 14.1% |
| STORE_FAST | 6,334,200 | 10.1% |
| RETURN_VALUE | 3,795,900 | 6.1% |


</details>

### BINARY_OP_INPLACE_ADD_UNICODE

<details>
<summary> Successors and predecessors for BINARY_OP_INPLACE_ADD_UNICODE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 751,440 | 26.2% |
| RETURN_VALUE | 680,220 | 23.7% |
| BINARY_OP_ADD_UNICODE | 411,820 | 14.3% |
| LOAD_ATTR_SLOT | 358,800 | 12.5% |
| LOAD_FAST | 284,640 | 9.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 1,982,580 | 69.0% |
| JUMP_BACKWARD | 545,500 | 19.0% |
| LOAD_FAST__LOAD_CONST | 216,660 | 7.5% |
| LOAD_CONST__LOAD_FAST | 60,360 | 2.1% |
| LOAD_FAST__LOAD_FAST | 52,320 | 1.8% |


</details>

### BINARY_OP_MULTIPLY_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_MULTIPLY_FLOAT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 363,615,000 | 43.9% |
| LOAD_FAST__LOAD_FAST | 234,480,420 | 28.3% |
| LOAD_ATTR_INSTANCE_VALUE | 118,763,280 | 14.4% |
| BINARY_SUBSCR | 67,701,000 | 8.2% |
| CALL_BUILTIN_CLASS | 12,782,880 | 1.5% |

|Successors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_ADD_FLOAT | 284,043,300 | 34.3% |
| YIELD_VALUE | 210,931,680 | 25.5% |
| BINARY_OP_SUBTRACT_FLOAT | 109,285,680 | 13.2% |
| LOAD_FAST__LOAD_FAST | 96,886,480 | 11.7% |
| LOAD_FAST | 50,101,980 | 6.1% |


</details>

### BINARY_OP_MULTIPLY_INT

<details>
<summary> Successors and predecessors for BINARY_OP_MULTIPLY_INT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_ADD_INT | 96,055,140 | 35.9% |
| LOAD_ATTR_INSTANCE_VALUE | 50,990,578 | 19.0% |
| LOAD_FAST__LOAD_FAST | 44,483,020 | 16.6% |
| BINARY_OP | 27,332,780 | 10.2% |
| LOAD_FAST | 23,886,017 | 8.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 83,455,620 | 31.2% |
| LOAD_FAST | 46,484,940 | 17.4% |
| STORE_FAST | 31,324,860 | 11.7% |
| STORE_FAST__LOAD_FAST | 30,966,737 | 11.6% |
| LOAD_FAST__LOAD_FAST | 28,380,780 | 10.6% |


</details>

### BINARY_OP_SUBTRACT_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBTRACT_FLOAT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_MULTIPLY_FLOAT | 109,285,680 | 40.5% |
| LOAD_FAST | 99,736,020 | 37.0% |
| LOAD_ATTR_INSTANCE_VALUE | 28,661,940 | 10.6% |
| BINARY_SUBSCR | 12,729,580 | 4.7% |
| BINARY_OP_SUBTRACT_FLOAT | 10,737,420 | 4.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 96,378,810 | 35.7% |
| LOAD_FAST__LOAD_FAST | 73,322,880 | 27.2% |
| SWAP | 55,701,000 | 20.6% |
| LOAD_FAST | 28,349,160 | 10.5% |
| BINARY_OP_SUBTRACT_FLOAT | 10,737,420 | 4.0% |


</details>

### BINARY_OP_SUBTRACT_INT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBTRACT_INT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 207,805,646 | 44.6% |
| LOAD_FAST__LOAD_CONST | 145,267,567 | 31.2% |
| LOAD_FAST | 73,380,089 | 15.7% |
| LOAD_FAST__LOAD_FAST | 22,610,944 | 4.9% |
| LOAD_ATTR_INSTANCE_VALUE | 10,026,960 | 2.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_PY_EXACT_ARGS | 79,108,360 | 17.0% |
| STORE_FAST__LOAD_FAST | 78,548,209 | 16.8% |
| SWAP | 68,066,916 | 14.6% |
| RETURN_VALUE | 41,308,860 | 8.9% |
| BINARY_OP | 37,397,087 | 8.0% |


</details>

### BINARY_SLICE

<details>
<summary> Successors and predecessors for BINARY_SLICE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 94,986,061 | 58.1% |
| BINARY_OP_ADD_INT | 34,710,660 | 21.2% |
| LOAD_FAST | 24,402,840 | 14.9% |
| LOAD_ATTR_SLOT | 2,747,460 | 1.7% |
| LOAD_ATTR | 2,053,260 | 1.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 33,807,411 | 20.7% |
| CALL_PY_EXACT_ARGS | 24,750,840 | 15.2% |
| CALL_NO_KW_LIST_APPEND | 19,300,980 | 11.8% |
| STORE_FAST | 18,194,040 | 11.1% |
| BINARY_OP | 15,381,780 | 9.4% |


</details>

### BINARY_SUBSCR

<details>
<summary> Successors and predecessors for BINARY_SUBSCR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 420,561,189 | 37.7% |
| LOAD_FAST__LOAD_FAST | 204,668,749 | 18.3% |
| COPY | 109,568,220 | 9.8% |
| BUILD_SLICE | 105,403,380 | 9.4% |
| BINARY_OP_ADD_INT | 88,165,020 | 7.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 413,519,637 | 37.0% |
| LOAD_FAST__LOAD_FAST | 128,271,240 | 11.5% |
| LOAD_FAST__LOAD_CONST | 103,941,420 | 9.3% |
| STORE_FAST__LOAD_FAST | 94,509,760 | 8.5% |
| BINARY_OP_MULTIPLY_FLOAT | 67,701,000 | 6.1% |


</details>

### BINARY_SUBSCR_DICT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_DICT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 204,261,083 | 53.6% |
| LOAD_FAST__LOAD_CONST | 76,425,600 | 20.1% |
| BINARY_SUBSCR | 36,829,920 | 9.7% |
| LOAD_CONST | 21,272,080 | 5.6% |
| LOAD_FAST__LOAD_FAST | 16,571,019 | 4.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RETURN_VALUE | 105,004,109 | 27.5% |
| LOAD_FAST | 50,290,509 | 13.2% |
| LOAD_ATTR_METHOD_NO_DICT | 40,690,500 | 10.7% |
| STORE_FAST | 40,105,297 | 10.5% |
| STORE_FAST__LOAD_FAST | 39,012,780 | 10.2% |


</details>

### BINARY_SUBSCR_GETITEM

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_GETITEM </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 72,509,502 | 48.9% |
| LOAD_FAST__LOAD_CONST | 37,526,540 | 25.3% |
| BUILD_TUPLE | 28,812,000 | 19.4% |
| LOAD_CONST | 4,150,440 | 2.8% |
| LOAD_ATTR_INSTANCE_VALUE | 3,355,020 | 2.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RESUME | 146,819,542 | 98.9% |
| MAKE_CELL | 716,620 | 0.5% |
| POP_JUMP_IF_FALSE | 160,340 | 0.1% |
| LOAD_ATTR_METHOD_NO_DICT | 155,800 | 0.1% |
| GET_ITER | 143,520 | 0.1% |


</details>

### BINARY_SUBSCR_LIST_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_LIST_INT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 302,830,291 | 33.5% |
| COPY | 158,997,820 | 17.6% |
| LOAD_CONST | 147,877,122 | 16.4% |
| LOAD_FAST__LOAD_FAST | 141,639,056 | 15.7% |
| BINARY_OP | 48,349,920 | 5.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 226,613,855 | 25.1% |
| LOAD_CONST | 193,145,340 | 21.4% |
| LOAD_FAST__LOAD_FAST | 104,248,772 | 11.6% |
| RETURN_VALUE | 90,771,321 | 10.1% |
| LOAD_FAST | 39,390,120 | 4.4% |


</details>

### BINARY_SUBSCR_TUPLE_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_TUPLE_INT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_CONST | 135,604,698 | 58.4% |
| LOAD_CONST | 56,611,857 | 24.4% |
| LOAD_FAST | 39,862,529 | 17.2% |
| LOAD_FAST__LOAD_FAST | 3,540 | 0.0% |
| BINARY_SUBSCR | 460 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL | 72,123,680 | 31.1% |
| LOAD_GLOBAL_MODULE | 30,081,740 | 13.0% |
| LOAD_CONST | 24,661,520 | 10.6% |
| LOAD_FAST | 21,994,805 | 9.5% |
| YIELD_VALUE | 19,355,040 | 8.3% |


</details>

### BUILD_CONST_KEY_MAP

<details>
<summary> Successors and predecessors for BUILD_CONST_KEY_MAP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 7,192,500 | 97.5% |
| LOAD_FAST__LOAD_CONST | 181,217 | 2.5% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RETURN_VALUE | 3,976,560 | 53.9% |
| LOAD_FAST | 2,590,860 | 35.1% |
| CALL_NO_KW_METHOD_DESCRIPTOR_O | 383,280 | 5.2% |
| STORE_FAST__LOAD_FAST | 252,377 | 3.4% |
| LOAD_FAST__LOAD_CONST | 91,320 | 1.2% |


</details>

### BUILD_LIST

<details>
<summary> Successors and predecessors for BUILD_LIST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST | 117,193,792 | 38.3% |
| RESUME | 46,668,243 | 15.2% |
| LOAD_ATTR_SLOT | 36,559,315 | 11.9% |
| LOAD_FAST | 25,228,129 | 8.2% |
| LOAD_CONST | 11,615,520 | 3.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 114,929,024 | 37.5% |
| STORE_FAST__LOAD_FAST | 99,911,671 | 32.6% |
| STORE_FAST | 34,480,017 | 11.3% |
| CALL | 11,208,780 | 3.7% |
| RETURN_VALUE | 8,900,044 | 2.9% |


</details>

### BUILD_MAP

<details>
<summary> Successors and predecessors for BUILD_MAP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 18,540,311 | 22.6% |
| RESUME | 14,403,813 | 17.6% |
| BUILD_TUPLE | 11,167,944 | 13.6% |
| STORE_FAST | 9,212,760 | 11.2% |
| POP_JUMP_IF_NOT_NONE | 3,608,463 | 4.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 47,882,471 | 58.4% |
| STORE_FAST__LOAD_FAST | 12,283,203 | 15.0% |
| STORE_FAST | 9,144,276 | 11.1% |
| CALL_NO_KW_BUILTIN_FAST | 4,338,720 | 5.3% |
| CALL_FUNCTION_EX | 3,905,520 | 4.8% |


</details>

### BUILD_SET

<details>
<summary> Successors and predecessors for BUILD_SET </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RESUME | 1,334,100 | 87.8% |
| LOAD_CONST | 82,320 | 5.4% |
| LOAD_FAST | 68,848 | 4.5% |
| CALL_BUILTIN_CLASS | 16,320 | 1.1% |
| LOAD_GLOBAL_MODULE | 9,960 | 0.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 1,334,100 | 87.8% |
| STORE_FAST__LOAD_FAST | 48,240 | 3.2% |
| LOAD_GLOBAL_BUILTIN | 36,600 | 2.4% |
| CALL_PY_EXACT_ARGS | 34,080 | 2.2% |
| LOAD_CONST | 24,600 | 1.6% |


</details>

### BUILD_SLICE

<details>
<summary> Successors and predecessors for BUILD_SLICE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 157,962,780 | 99.6% |
| LOAD_CONST__LOAD_FAST | 433,798 | 0.3% |
| LOAD_FAST | 69,840 | 0.0% |
| LOAD_ATTR_INSTANCE_VALUE | 54,000 | 0.0% |
| LOAD_FAST__LOAD_CONST | 60 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| BINARY_SUBSCR | 105,403,380 | 66.5% |
| DELETE_SUBSCR | 53,117,098 | 33.5% |


</details>

### BUILD_STRING

<details>
<summary> Successors and predecessors for BUILD_STRING </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| FORMAT_VALUE | 49,705,680 | 88.1% |
| LOAD_CONST | 6,705,540 | 11.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_NO_KW_BUILTIN_O | 36,694,920 | 65.0% |
| CALL | 12,312,840 | 21.8% |
| BINARY_OP_ADD_UNICODE | 2,011,200 | 3.6% |
| STORE_FAST | 1,597,740 | 2.8% |
| CALL_NO_KW_LIST_APPEND | 1,398,840 | 2.5% |


</details>

### BUILD_TUPLE

<details>
<summary> Successors and predecessors for BUILD_TUPLE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 164,950,060 | 27.5% |
| LOAD_FAST__LOAD_FAST | 140,606,735 | 23.5% |
| LOAD_FAST | 88,838,854 | 14.8% |
| LOAD_CLOSURE | 78,787,553 | 13.1% |
| CALL | 37,769,860 | 6.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RETURN_VALUE | 337,650,089 | 56.3% |
| LOAD_CONST | 81,178,358 | 13.5% |
| YIELD_VALUE | 32,442,540 | 5.4% |
| BINARY_SUBSCR_GETITEM | 28,812,000 | 4.8% |
| LIST_APPEND | 23,272,524 | 3.9% |


</details>

### CALL

<details>
<summary> Successors and predecessors for CALL </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 213,838,816 | 22.3% |
| KW_NAMES | 162,983,245 | 17.0% |
| LOAD_FAST__LOAD_FAST | 103,712,138 | 10.8% |
| BINARY_SUBSCR_TUPLE_INT | 72,123,680 | 7.5% |
| LOAD_GLOBAL_MODULE | 55,486,349 | 5.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 291,906,849 | 30.4% |
| RESUME | 186,971,844 | 19.5% |
| RETURN_VALUE | 107,919,423 | 11.3% |
| POP_TOP | 50,616,681 | 5.3% |
| LOAD_GLOBAL_MODULE | 39,243,949 | 4.1% |


</details>

### CALL_BOUND_METHOD_EXACT_ARGS

<details>
<summary> Successors and predecessors for CALL_BOUND_METHOD_EXACT_ARGS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 77,585,497 | 33.6% |
| LOAD_FAST | 61,029,008 | 26.5% |
| LOAD_FAST__LOAD_CONST | 27,076,500 | 11.7% |
| LOAD_CONST | 16,715,000 | 7.2% |
| LOAD_ATTR_INSTANCE_VALUE | 8,945,078 | 3.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RESUME | 188,830,691 | 81.9% |
| COPY_FREE_VARS | 37,754,575 | 16.4% |
| POP_TOP | 2,094,280 | 0.9% |
| MAKE_CELL | 1,383,080 | 0.6% |
| CALL_PY_EXACT_ARGS | 510,236 | 0.2% |


</details>

### CALL_BUILTIN_CLASS

<details>
<summary> Successors and predecessors for CALL_BUILTIN_CLASS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_BUILTIN | 83,695,683 | 38.1% |
| LOAD_FAST | 70,132,656 | 32.0% |
| CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS | 8,456,800 | 3.9% |
| LOAD_ATTR_INSTANCE_VALUE | 6,278,437 | 2.9% |
| BINARY_OP_MULTIPLY_INT | 6,174,460 | 2.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR | 111,940,819 | 51.0% |
| GET_ITER | 45,928,882 | 20.9% |
| BINARY_OP_MULTIPLY_FLOAT | 12,782,880 | 5.8% |
| STORE_FAST__LOAD_FAST | 10,242,476 | 4.7% |
| LOAD_FAST | 9,283,920 | 4.2% |


</details>

### CALL_BUILTIN_FAST_WITH_KEYWORDS

<details>
<summary> Successors and predecessors for CALL_BUILTIN_FAST_WITH_KEYWORDS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RETURN_GENERATOR | 33,032,100 | 38.2% |
| KW_NAMES | 24,469,840 | 28.3% |
| LOAD_FAST | 19,452,752 | 22.5% |
| CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS | 5,653,408 | 6.5% |
| LOAD_FAST__LOAD_FAST | 2,692,640 | 3.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_DEREF | 31,295,640 | 36.2% |
| STORE_FAST | 22,180,880 | 25.6% |
| RETURN_VALUE | 13,310,295 | 15.4% |
| POP_TOP | 11,058,947 | 12.8% |
| STORE_FAST__LOAD_FAST | 3,945,432 | 4.6% |


</details>

### CALL_FUNCTION_EX

<details>
<summary> Successors and predecessors for CALL_FUNCTION_EX </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| CALL_INTRINSIC_1 | 43,219,837 | 44.8% |
| DICT_MERGE | 31,382,862 | 32.6% |
| LOAD_FAST | 7,945,526 | 8.2% |
| LOAD_FAST__LOAD_FAST | 5,886,220 | 6.1% |
| BUILD_MAP | 3,905,520 | 4.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_TOP | 45,804,034 | 47.5% |
| STORE_FAST__LOAD_FAST | 21,254,618 | 22.1% |
| UNPACK_SEQUENCE_TWO_TUPLE | 7,720,080 | 8.0% |
| RETURN_VALUE | 7,368,988 | 7.6% |
| LOAD_FAST__LOAD_FAST | 4,982,640 | 5.2% |


</details>

### CALL_INTRINSIC_1

<details>
<summary> Successors and predecessors for CALL_INTRINSIC_1 </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 88,136,760 | 61.7% |
| LIST_EXTEND | 48,723,305 | 34.1% |
| LOAD_ATTR_INSTANCE_VALUE | 6,000,000 | 4.2% |
| RERAISE | 41,160 | 0.0% |
| LIST_APPEND | 11,520 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| YIELD_VALUE | 94,136,760 | 65.9% |
| CALL_FUNCTION_EX | 43,219,837 | 30.2% |
| LOAD_CONST__LOAD_FAST | 3,322,080 | 2.3% |
| BUILD_MAP | 2,119,888 | 1.5% |
| LOAD_CONST | 48,360 | 0.0% |


</details>

### CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 9,725,660 | 40.1% |
| LOAD_FAST | 6,759,182 | 27.8% |
| LOAD_ATTR_METHOD_NO_DICT | 4,481,520 | 18.5% |
| LOAD_DEREF | 2,241,760 | 9.2% |
| LOAD_FAST__LOAD_FAST | 635,923 | 2.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_NO_KW_METHOD_DESCRIPTOR_O | 6,935,320 | 28.6% |
| STORE_FAST | 4,415,080 | 18.2% |
| STORE_FAST__LOAD_FAST | 2,899,543 | 11.9% |
| LOAD_ATTR_METHOD_NO_DICT | 2,436,000 | 10.0% |
| BINARY_OP | 2,151,720 | 8.9% |


</details>

### CALL_NO_KW_BUILTIN_FAST

<details>
<summary> Successors and predecessors for CALL_NO_KW_BUILTIN_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_BUILTIN | 435,765,640 | 44.3% |
| LOAD_CONST | 290,712,040 | 29.6% |
| LOAD_FAST__LOAD_FAST | 83,905,175 | 8.5% |
| LOAD_FAST__LOAD_CONST | 69,931,681 | 7.1% |
| CALL_NO_KW_BUILTIN_FAST | 37,470,460 | 3.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_JUMP_IF_FALSE | 400,893,172 | 40.8% |
| STORE_FAST | 222,602,500 | 22.7% |
| STORE_FAST__LOAD_FAST | 107,877,699 | 11.0% |
| EXTENDED_ARG | 72,007,560 | 7.3% |
| POP_TOP | 47,644,033 | 4.8% |


</details>

### CALL_NO_KW_BUILTIN_O

<details>
<summary> Successors and predecessors for CALL_NO_KW_BUILTIN_O </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 388,769,611 | 45.6% |
| LOAD_FAST__LOAD_FAST | 193,962,903 | 22.8% |
| LOAD_FAST__LOAD_CONST | 85,647,840 | 10.0% |
| RETURN_VALUE | 54,163,500 | 6.4% |
| BUILD_STRING | 36,694,920 | 4.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_TOP | 386,831,386 | 45.4% |
| LOAD_CONST | 172,184,381 | 20.2% |
| STORE_FAST__LOAD_FAST | 169,601,418 | 19.9% |
| RETURN_VALUE | 32,411,100 | 3.8% |
| POP_JUMP_IF_TRUE | 19,459,328 | 2.3% |


</details>

### CALL_NO_KW_ISINSTANCE

<details>
<summary> Successors and predecessors for CALL_NO_KW_ISINSTANCE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_MODULE | 367,534,201 | 51.7% |
| LOAD_GLOBAL_BUILTIN | 222,906,882 | 31.4% |
| LOAD_FAST__LOAD_FAST | 61,917,484 | 8.7% |
| LOAD_ATTR_MODULE | 27,920,400 | 3.9% |
| BUILD_TUPLE | 14,677,756 | 2.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_JUMP_IF_FALSE | 554,306,333 | 78.0% |
| POP_JUMP_IF_TRUE | 121,433,262 | 17.1% |
| UNARY_NOT | 8,059,528 | 1.1% |
| EXTENDED_ARG | 7,452,660 | 1.0% |
| JUMP_IF_FALSE_OR_POP | 7,347,420 | 1.0% |


</details>

### CALL_NO_KW_LEN

<details>
<summary> Successors and predecessors for CALL_NO_KW_LEN </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 221,901,257 | 69.6% |
| LOAD_ATTR_INSTANCE_VALUE | 43,234,975 | 13.6% |
| BINARY_SUBSCR_LIST_INT | 29,548,500 | 9.3% |
| LOAD_ATTR_SLOT | 8,353,520 | 2.6% |
| LOAD_FAST__LOAD_FAST | 3,233,220 | 1.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 130,863,339 | 41.0% |
| LOAD_FAST | 38,888,400 | 12.2% |
| STORE_FAST__LOAD_FAST | 34,972,290 | 11.0% |
| COMPARE_AND_BRANCH_INT | 30,069,992 | 9.4% |
| RETURN_VALUE | 16,745,484 | 5.3% |


</details>

### CALL_NO_KW_LIST_APPEND

<details>
<summary> Successors and predecessors for CALL_NO_KW_LIST_APPEND </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 181,980,857 | 71.0% |
| BINARY_SUBSCR | 20,171,040 | 7.9% |
| BINARY_SLICE | 19,300,980 | 7.5% |
| RETURN_VALUE | 8,211,500 | 3.2% |
| BINARY_OP | 5,899,840 | 2.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 100,823,534 | 39.4% |
| EXTENDED_ARG | 31,389,864 | 12.3% |
| LOAD_FAST__LOAD_FAST | 30,945,600 | 12.1% |
| LOAD_FAST | 28,008,800 | 10.9% |
| RETURN_CONST | 20,589,960 | 8.0% |


</details>

### CALL_NO_KW_METHOD_DESCRIPTOR_FAST

<details>
<summary> Successors and predecessors for CALL_NO_KW_METHOD_DESCRIPTOR_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 159,068,468 | 39.0% |
| LOAD_CONST | 93,393,335 | 22.9% |
| LOAD_FAST__LOAD_FAST | 56,557,800 | 13.9% |
| LOAD_ATTR_METHOD_NO_DICT | 49,732,680 | 12.2% |
| LOAD_GLOBAL_MODULE | 16,437,420 | 4.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 286,231,147 | 70.2% |
| STORE_FAST | 42,434,840 | 10.4% |
| LOAD_FAST | 22,473,365 | 5.5% |
| RETURN_VALUE | 10,298,580 | 2.5% |
| POP_TOP | 9,810,080 | 2.4% |


</details>

### CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS

<details>
<summary> Successors and predecessors for CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_METHOD_NO_DICT | 166,014,337 | 69.6% |
| LOAD_ATTR_METHOD_LAZY_DICT | 53,193,854 | 22.3% |
| LOAD_ATTR | 17,338,012 | 7.3% |
| LOAD_FAST__LOAD_FAST | 1,558,920 | 0.7% |
| CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS | 392,733 | 0.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 51,746,575 | 21.7% |
| POP_JUMP_IF_FALSE | 44,991,018 | 18.9% |
| GET_ITER | 43,108,064 | 18.1% |
| STORE_FAST | 27,146,982 | 11.4% |
| LOAD_GLOBAL_MODULE | 18,682,140 | 7.8% |


</details>

### CALL_NO_KW_METHOD_DESCRIPTOR_O

<details>
<summary> Successors and predecessors for CALL_NO_KW_METHOD_DESCRIPTOR_O </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 166,515,801 | 76.8% |
| CALL | 19,488,270 | 9.0% |
| CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS | 6,935,320 | 3.2% |
| LOAD_GLOBAL_MODULE | 6,146,340 | 2.8% |
| RETURN_VALUE | 3,658,140 | 1.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_TOP | 103,218,340 | 47.6% |
| BINARY_OP | 72,002,140 | 33.2% |
| RETURN_VALUE | 17,462,220 | 8.0% |
| STORE_FAST | 6,524,940 | 3.0% |
| LOAD_FAST | 5,318,760 | 2.5% |


</details>

### CALL_NO_KW_STR_1

<details>
<summary> Successors and predecessors for CALL_NO_KW_STR_1 </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 44,407,143 | 79.3% |
| RETURN_VALUE | 6,551,140 | 11.7% |
| LOAD_FAST__LOAD_FAST | 2,400,000 | 4.3% |
| LOAD_ATTR_INSTANCE_VALUE | 1,228,800 | 2.2% |
| BINARY_SUBSCR_LIST_INT | 1,211,520 | 2.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_NO_KW_BUILTIN_O | 10,852,320 | 19.4% |
| CALL_PY_EXACT_ARGS | 10,848,480 | 19.4% |
| STORE_FAST__LOAD_FAST | 9,079,680 | 16.2% |
| YIELD_VALUE | 7,682,400 | 13.7% |
| BINARY_OP_ADD_UNICODE | 4,820,800 | 8.6% |


</details>

### CALL_NO_KW_TUPLE_1

<details>
<summary> Successors and predecessors for CALL_NO_KW_TUPLE_1 </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 15,250,084 | 58.6% |
| RETURN_GENERATOR | 5,396,980 | 20.7% |
| CALL_BUILTIN_FAST_WITH_KEYWORDS | 3,465,528 | 13.3% |
| LOAD_ATTR_SLOT | 1,098,624 | 4.2% |
| CALL | 436,580 | 1.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 14,315,160 | 55.0% |
| BINARY_OP | 3,468,208 | 13.3% |
| BUILD_TUPLE | 2,902,344 | 11.2% |
| YIELD_VALUE | 2,419,200 | 9.3% |
| STORE_FAST__LOAD_FAST | 645,120 | 2.5% |


</details>

### CALL_NO_KW_TYPE_1

<details>
<summary> Successors and predecessors for CALL_NO_KW_TYPE_1 </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 389,714,234 | 99.1% |
| LOAD_CONST | 3,657,328 | 0.9% |
| LOAD_GLOBAL_BUILTIN | 19,240 | 0.0% |
| CALL | 200 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 249,581,544 | 63.4% |
| STORE_FAST | 44,101,008 | 11.2% |
| LOAD_GLOBAL_BUILTIN | 41,897,164 | 10.7% |
| IS_OP | 25,804,028 | 6.6% |
| LOAD_GLOBAL_MODULE | 13,606,680 | 3.5% |


</details>

### CALL_PY_EXACT_ARGS

<details>
<summary> Successors and predecessors for CALL_PY_EXACT_ARGS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 761,004,042 | 30.7% |
| LOAD_FAST__LOAD_FAST | 663,819,636 | 26.7% |
| LOAD_ATTR_METHOD_WITH_VALUES | 402,379,719 | 16.2% |
| LOAD_ATTR_METHOD_NO_DICT | 124,728,526 | 5.0% |
| GET_ITER | 113,273,138 | 4.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RESUME | 2,232,932,662 | 90.0% |
| RETURN_GENERATOR | 126,796,884 | 5.1% |
| COPY_FREE_VARS | 93,974,368 | 3.8% |
| MAKE_CELL | 26,452,938 | 1.1% |
| CALL_PY_EXACT_ARGS | 1,170,107 | 0.0% |


</details>

### CALL_PY_WITH_DEFAULTS

<details>
<summary> Successors and predecessors for CALL_PY_WITH_DEFAULTS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 89,111,419 | 58.1% |
| LOAD_ATTR_METHOD_NO_DICT | 13,652,345 | 8.9% |
| LOAD_ATTR_METHOD_WITH_VALUES | 12,576,019 | 8.2% |
| LOAD_ATTR | 7,297,094 | 4.8% |
| LOAD_FAST__LOAD_FAST | 4,830,302 | 3.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RESUME | 143,147,232 | 93.3% |
| COPY_FREE_VARS | 4,998,080 | 3.3% |
| RETURN_GENERATOR | 3,419,820 | 2.2% |
| MAKE_CELL | 1,705,172 | 1.1% |
| CALL_PY_EXACT_ARGS | 87,800 | 0.1% |


</details>

### CHECK_EXC_MATCH

<details>
<summary> Successors and predecessors for CHECK_EXC_MATCH </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_BUILTIN | 16,292,560 | 93.9% |
| BUILD_TUPLE | 518,176 | 3.0% |
| LOAD_GLOBAL_MODULE | 496,628 | 2.9% |
| LOAD_ATTR_MODULE | 50,640 | 0.3% |
| LOAD_FAST | 1,200 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_JUMP_IF_FALSE | 17,359,084 | 100.0% |
| EXTENDED_ARG | 120 | 0.0% |


</details>

### CLEANUP_THROW

<details>
<summary> Successors and predecessors for CLEANUP_THROW </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_INTRINSIC_1 | 240 | 100.0% |


</details>

### COMPARE_AND_BRANCH

<details>
<summary> Successors and predecessors for COMPARE_AND_BRANCH </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 53,926,907 | 37.8% |
| LOAD_FAST | 50,275,196 | 35.2% |
| LOAD_ATTR | 8,879,387 | 6.2% |
| LOAD_FAST__LOAD_CONST | 6,219,925 | 4.4% |
| LOAD_GLOBAL_MODULE | 4,707,611 | 3.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 36,400,015 | 25.5% |
| JUMP_BACKWARD | 29,657,262 | 20.8% |
| RETURN_CONST | 24,909,169 | 17.5% |
| LOAD_FAST__LOAD_FAST | 19,525,860 | 13.7% |
| LOAD_GLOBAL_MODULE | 10,661,987 | 7.5% |


</details>

### COMPARE_AND_BRANCH_FLOAT

<details>
<summary> Successors and predecessors for COMPARE_AND_BRANCH_FLOAT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_SUBSCR | 23,382,660 | 37.7% |
| LOAD_ATTR_SLOT | 17,999,820 | 29.0% |
| LOAD_FAST | 6,292,943 | 10.1% |
| LOAD_CONST | 6,004,560 | 9.7% |
| LOAD_GLOBAL_MODULE | 3,632,096 | 5.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 29,182,500 | 47.1% |
| LOAD_FAST | 21,277,150 | 34.3% |
| LOAD_GLOBAL_MODULE | 6,026,760 | 9.7% |
| LOAD_FAST__LOAD_CONST | 4,722,780 | 7.6% |
| PUSH_NULL | 381,336 | 0.6% |


</details>

### COMPARE_AND_BRANCH_INT

<details>
<summary> Successors and predecessors for COMPARE_AND_BRANCH_INT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 341,737,364 | 25.9% |
| LOAD_FAST__LOAD_CONST | 236,156,634 | 17.9% |
| LOAD_FAST | 178,443,729 | 13.5% |
| LOAD_ATTR_INSTANCE_VALUE | 168,159,335 | 12.7% |
| COPY | 102,867,180 | 7.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 552,004,674 | 41.8% |
| LOAD_FAST__LOAD_CONST | 156,788,364 | 11.9% |
| LOAD_FAST__LOAD_FAST | 152,106,248 | 11.5% |
| JUMP_BACKWARD | 115,804,558 | 8.8% |
| JUMP_FORWARD | 96,327,120 | 7.3% |


</details>

### COMPARE_AND_BRANCH_STR

<details>
<summary> Successors and predecessors for COMPARE_AND_BRANCH_STR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 35,652,780 | 39.5% |
| LOAD_FAST__LOAD_CONST | 27,623,399 | 30.6% |
| LOAD_FAST | 16,736,028 | 18.6% |
| LOAD_ATTR_INSTANCE_VALUE | 2,498,700 | 2.8% |
| BINARY_SUBSCR_TUPLE_INT | 2,437,440 | 2.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 22,115,980 | 24.5% |
| LOAD_FAST__LOAD_CONST | 18,194,040 | 20.2% |
| LOAD_GLOBAL_MODULE | 16,681,572 | 18.5% |
| JUMP_BACKWARD | 9,124,670 | 10.1% |
| LOAD_GLOBAL_BUILTIN | 9,108,479 | 10.1% |


</details>

### COMPARE_OP

<details>
<summary> Successors and predecessors for COMPARE_OP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_SLOT | 89,902,702 | 40.0% |
| LOAD_CONST | 37,165,604 | 16.6% |
| LOAD_FAST__LOAD_CONST | 29,743,708 | 13.2% |
| LOAD_FAST__LOAD_FAST | 19,163,470 | 8.5% |
| LOAD_FAST | 12,476,596 | 5.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RETURN_VALUE | 119,071,175 | 53.0% |
| EXTENDED_ARG | 47,112,104 | 21.0% |
| JUMP_IF_FALSE_OR_POP | 12,062,186 | 5.4% |
| LOAD_FAST | 10,600,320 | 4.7% |
| BINARY_OP | 9,899,520 | 4.4% |


</details>

### CONTAINS_OP

<details>
<summary> Successors and predecessors for CONTAINS_OP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_MODULE | 266,981,914 | 36.1% |
| LOAD_FAST__LOAD_FAST | 148,887,727 | 20.1% |
| LOAD_FAST | 142,002,745 | 19.2% |
| LOAD_CONST__LOAD_FAST | 66,590,160 | 9.0% |
| LOAD_ATTR_INSTANCE_VALUE | 43,046,353 | 5.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_JUMP_IF_FALSE | 656,984,897 | 88.8% |
| POP_JUMP_IF_TRUE | 68,231,186 | 9.2% |
| RETURN_VALUE | 5,895,720 | 0.8% |
| EXTENDED_ARG | 4,561,380 | 0.6% |
| JUMP_IF_FALSE_OR_POP | 1,460,640 | 0.2% |


</details>

### COPY

<details>
<summary> Successors and predecessors for COPY </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| COPY | 270,086,400 | 33.3% |
| LOAD_FAST | 134,303,256 | 16.5% |
| SWAP | 128,776,500 | 15.9% |
| LOAD_FAST__LOAD_FAST | 101,528,340 | 12.5% |
| LOAD_FAST__LOAD_CONST | 78,469,140 | 9.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| COPY | 270,086,400 | 33.3% |
| BINARY_SUBSCR_LIST_INT | 158,997,820 | 19.6% |
| BINARY_SUBSCR | 109,568,220 | 13.5% |
| COMPARE_AND_BRANCH_INT | 102,867,180 | 12.7% |
| LOAD_ATTR_INSTANCE_VALUE | 66,090,962 | 8.1% |


</details>

### COPY_FREE_VARS

<details>
<summary> Successors and predecessors for COPY_FREE_VARS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| CALL_PY_EXACT_ARGS | 93,974,368 | 62.2% |
| CALL_BOUND_METHOD_EXACT_ARGS | 37,754,575 | 25.0% |
| CALL | 10,250,286 | 6.8% |
| CALL_PY_WITH_DEFAULTS | 4,998,080 | 3.3% |
| LOAD_ATTR_PROPERTY | 4,032,832 | 2.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RESUME | 209,961,049 | 77.3% |
| RETURN_GENERATOR | 61,646,684 | 22.7% |
| MAKE_CELL | 118,264 | 0.0% |


</details>

### DELETE_ATTR

<details>
<summary> Successors and predecessors for DELETE_ATTR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 8,615,097 | 100.0% |
| LOAD_DEREF | 60 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 6,717,078 | 78.0% |
| NOP | 1,746,820 | 20.3% |
| RETURN_CONST | 150,239 | 1.7% |
| LOAD_GLOBAL_MODULE | 960 | 0.0% |
| LOAD_CONST | 60 | 0.0% |


</details>

### DELETE_DEREF

<details>
<summary> Successors and predecessors for DELETE_DEREF </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_ATTR | 1,200 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| DELETE_FAST | 1,200 | 100.0% |


</details>

### DELETE_FAST

<details>
<summary> Successors and predecessors for DELETE_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| FOR_ITER | 958,080 | 71.1% |
| STORE_FAST | 222,840 | 16.5% |
| CALL | 81,000 | 6.0% |
| POP_EXCEPT | 18,000 | 1.3% |
| STORE_ATTR_INSTANCE_VALUE | 18,000 | 1.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_MODULE | 483,540 | 35.9% |
| BUILD_LIST | 479,040 | 35.6% |
| RERAISE | 151,140 | 11.2% |
| RETURN_VALUE | 138,600 | 10.3% |
| RETURN_CONST | 36,000 | 2.7% |


</details>

### DELETE_SUBSCR

<details>
<summary> Successors and predecessors for DELETE_SUBSCR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 72,992,280 | 55.3% |
| BUILD_SLICE | 53,117,098 | 40.2% |
| LOAD_FAST__LOAD_CONST | 5,558,460 | 4.2% |
| LOAD_FAST | 296,342 | 0.2% |
| CALL | 20,639 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_CONST | 54,070,500 | 41.0% |
| LOAD_FAST | 26,756,998 | 20.3% |
| LOAD_FAST__LOAD_FAST | 26,382,660 | 20.0% |
| LOAD_CONST | 18,042,362 | 13.7% |
| JUMP_FORWARD | 5,280,960 | 4.0% |


</details>

### DICT_MERGE

<details>
<summary> Successors and predecessors for DICT_MERGE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 30,885,919 | 98.4% |
| LOAD_DEREF | 236,360 | 0.8% |
| LOAD_ATTR_INSTANCE_VALUE | 167,883 | 0.5% |
| RETURN_VALUE | 50,880 | 0.2% |
| BUILD_CONST_KEY_MAP | 16,320 | 0.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_FUNCTION_EX | 31,382,862 | 100.0% |


</details>

### DICT_UPDATE

<details>
<summary> Successors and predecessors for DICT_UPDATE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 13,140 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| DICT_MERGE | 13,140 | 100.0% |


</details>

### END_ASYNC_FOR

<details>
<summary> Successors and predecessors for END_ASYNC_FOR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| SEND | 6,000,000 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 3,932,100 | 65.5% |
| RETURN_CONST | 2,067,900 | 34.5% |


</details>

### END_FOR

<details>
<summary> Successors and predecessors for END_FOR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RETURN_CONST | 38,659,026 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 37,036,620 | 95.8% |
| RETURN_CONST | 920,100 | 2.4% |
| LOAD_FAST | 414,726 | 1.1% |
| LOAD_FAST__LOAD_FAST | 93,840 | 0.2% |
| RETURN_VALUE | 80,040 | 0.2% |


</details>

### EXTENDED_ARG

<details>
<summary> Successors and predecessors for EXTENDED_ARG </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| <252> | 99,358,740 | 18.8% |
| JUMP_BACKWARD | 83,347,540 | 15.8% |
| CALL_NO_KW_BUILTIN_FAST | 72,007,560 | 13.6% |
| COMPARE_OP | 47,112,104 | 8.9% |
| LOAD_FAST | 35,258,360 | 6.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_JUMP_IF_FALSE | 160,110,373 | 37.3% |
| JUMP_BACKWARD | 85,306,824 | 19.9% |
| FOR_ITER_LIST | 55,507,028 | 12.9% |
| POP_JUMP_IF_NONE | 37,561,404 | 8.7% |
| POP_JUMP_IF_NOT_NONE | 30,724,260 | 7.2% |


</details>

### FORMAT_VALUE

<details>
<summary> Successors and predecessors for FORMAT_VALUE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST__LOAD_FAST | 51,072,060 | 46.0% |
| LOAD_FAST__LOAD_FAST | 36,024,720 | 32.4% |
| LOAD_ATTR | 13,027,440 | 11.7% |
| LOAD_FAST | 3,107,820 | 2.8% |
| RETURN_VALUE | 2,538,780 | 2.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST__LOAD_FAST | 51,397,560 | 46.3% |
| BUILD_STRING | 49,705,680 | 44.8% |
| LOAD_CONST | 6,745,380 | 6.1% |
| LOAD_FAST | 3,198,180 | 2.9% |
| LOAD_GLOBAL_MODULE | 8,820 | 0.0% |


</details>

### FOR_ITER

<details>
<summary> Successors and predecessors for FOR_ITER </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 270,505,723 | 71.4% |
| GET_ITER | 69,059,296 | 18.2% |
| LOAD_FAST | 21,391,747 | 5.6% |
| EXTENDED_ARG | 17,847,316 | 4.7% |
| FOR_ITER | 142,867 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| UNPACK_SEQUENCE_TWO_TUPLE | 202,571,759 | 53.5% |
| STORE_FAST__LOAD_FAST | 69,714,090 | 18.4% |
| STORE_FAST | 24,304,666 | 6.4% |
| LOAD_FAST | 20,178,294 | 5.3% |
| RETURN_CONST | 19,601,105 | 5.2% |


</details>

### FOR_ITER_GEN

<details>
<summary> Successors and predecessors for FOR_ITER_GEN </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 63,733,872 | 49.7% |
| GET_ITER | 38,319,508 | 29.9% |
| EXTENDED_ARG | 26,083,460 | 20.3% |
| LOAD_FAST | 185,320 | 0.1% |
| FOR_ITER | 2,860 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RESUME | 89,384,172 | 69.7% |
| POP_TOP | 38,787,148 | 30.2% |
| STORE_FAST__LOAD_FAST | 63,160 | 0.0% |
| JUMP_FORWARD | 55,200 | 0.0% |
| RETURN_VALUE | 30,520 | 0.0% |


</details>

### FOR_ITER_LIST

<details>
<summary> Successors and predecessors for FOR_ITER_LIST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 914,687,578 | 73.3% |
| GET_ITER | 196,560,729 | 15.7% |
| LOAD_FAST | 80,275,730 | 6.4% |
| EXTENDED_ARG | 55,507,028 | 4.4% |
| FOR_ITER_TUPLE | 1,244,394 | 0.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 484,768,633 | 38.8% |
| UNPACK_SEQUENCE_TWO_TUPLE | 319,430,100 | 25.6% |
| STORE_FAST | 171,970,437 | 13.8% |
| RETURN_CONST | 107,253,945 | 8.6% |
| LOAD_FAST | 68,357,867 | 5.5% |


</details>

### FOR_ITER_RANGE

<details>
<summary> Successors and predecessors for FOR_ITER_RANGE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 428,472,955 | 92.3% |
| GET_ITER | 25,311,650 | 5.5% |
| LOAD_FAST | 6,810,360 | 1.5% |
| EXTENDED_ARG | 3,539,700 | 0.8% |
| FOR_ITER_LIST | 960 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 161,046,284 | 34.7% |
| LOAD_FAST | 81,936,181 | 17.7% |
| LOAD_DEREF | 64,789,812 | 14.0% |
| LOAD_CONST__LOAD_FAST | 55,903,320 | 12.0% |
| PUSH_NULL | 29,575,472 | 6.4% |


</details>

### FOR_ITER_TUPLE

<details>
<summary> Successors and predecessors for FOR_ITER_TUPLE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 205,160,442 | 69.0% |
| GET_ITER | 84,951,300 | 28.6% |
| LOAD_FAST | 4,611,121 | 1.6% |
| EXTENDED_ARG | 1,392,420 | 0.5% |
| FOR_ITER_LIST | 1,237,804 | 0.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 149,934,498 | 50.4% |
| STORE_FAST | 55,876,349 | 18.8% |
| LOAD_FAST__LOAD_FAST | 40,052,360 | 13.5% |
| LOAD_FAST | 27,483,936 | 9.2% |
| RETURN_CONST | 12,812,329 | 4.3% |


</details>

### GET_AITER

<details>
<summary> Successors and predecessors for GET_AITER </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_INSTANCE_VALUE | 5,999,940 | 100.0% |
| RETURN_VALUE | 60 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| GET_ANEXT | 6,000,000 | 100.0% |


</details>

### GET_ANEXT

<details>
<summary> Successors and predecessors for GET_ANEXT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 94,136,760 | 94.0% |
| GET_AITER | 6,000,000 | 6.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 100,136,760 | 100.0% |


</details>

### GET_AWAITABLE

<details>
<summary> Successors and predecessors for GET_AWAITABLE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RETURN_GENERATOR | 77,837,896 | 92.8% |
| LOAD_FAST | 3,303,060 | 3.9% |
| CALL_FUNCTION_EX | 2,239,620 | 2.7% |
| LOAD_ATTR_INSTANCE_VALUE | 249,238 | 0.3% |
| RETURN_VALUE | 207,120 | 0.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 83,837,114 | 100.0% |


</details>

### GET_ITER

<details>
<summary> Successors and predecessors for GET_ITER </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 100,563,221 | 18.3% |
| LOAD_FAST | 80,846,876 | 14.7% |
| LOAD_ATTR_INSTANCE_VALUE | 79,795,486 | 14.5% |
| RETURN_VALUE | 56,999,798 | 10.4% |
| CALL_BUILTIN_CLASS | 45,928,882 | 8.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| FOR_ITER_LIST | 196,560,729 | 35.8% |
| CALL_PY_EXACT_ARGS | 113,273,138 | 20.7% |
| FOR_ITER_TUPLE | 84,951,300 | 15.5% |
| FOR_ITER | 69,059,296 | 12.6% |
| FOR_ITER_GEN | 38,319,508 | 7.0% |


</details>

### GET_YIELD_FROM_ITER

<details>
<summary> Successors and predecessors for GET_YIELD_FROM_ITER </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_INSTANCE_VALUE | 6,000,480 | 62.8% |
| RETURN_GENERATOR | 3,389,664 | 35.4% |
| BINARY_SUBSCR | 132,060 | 1.4% |
| LOAD_ATTR_SLOT | 33,120 | 0.3% |
| LOAD_FAST | 7,080 | 0.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 9,562,404 | 100.0% |


</details>

### IMPORT_FROM

<details>
<summary> Successors and predecessors for IMPORT_FROM </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| IMPORT_NAME | 8,314,362 | 87.0% |
| STORE_FAST | 1,105,948 | 11.6% |
| STORE_DEREF | 136,424 | 1.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST | 7,999,690 | 83.7% |
| STORE_DEREF | 1,557,044 | 16.3% |


</details>

### IMPORT_NAME

<details>
<summary> Successors and predecessors for IMPORT_NAME </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 8,341,242 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| IMPORT_FROM | 8,314,362 | 99.7% |
| STORE_FAST__LOAD_FAST | 24,240 | 0.3% |
| STORE_FAST | 2,040 | 0.0% |
| STORE_NAME | 360 | 0.0% |
| STORE_DEREF | 240 | 0.0% |


</details>

### INTERPRETER_EXIT

<details>
<summary> Successors and predecessors for INTERPRETER_EXIT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| YIELD_VALUE | 596,523,325 | 36.4% |
| RETURN_CONST | 525,400,243 | 32.0% |
| RETURN_VALUE | 503,693,372 | 30.7% |
| RETURN_GENERATOR | 14,360,980 | 0.9% |

|Successors | Count | Percentage | 
|---|---:|---:|


</details>

### IS_OP

<details>
<summary> Successors and predecessors for IS_OP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR | 228,958,172 | 34.5% |
| LOAD_GLOBAL_MODULE | 177,156,710 | 26.7% |
| LOAD_FAST | 78,967,709 | 11.9% |
| LOAD_FAST__LOAD_FAST | 63,246,408 | 9.5% |
| LOAD_GLOBAL_BUILTIN | 44,298,273 | 6.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_JUMP_IF_FALSE | 559,188,426 | 84.1% |
| POP_JUMP_IF_TRUE | 57,615,466 | 8.7% |
| EXTENDED_ARG | 18,023,280 | 2.7% |
| STORE_FAST__LOAD_FAST | 12,173,460 | 1.8% |
| YIELD_VALUE | 9,829,145 | 1.5% |


</details>

### JUMP_BACKWARD

<details>
<summary> Successors and predecessors for JUMP_BACKWARD </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| POP_TOP | 731,897,375 | 31.0% |
| POP_JUMP_IF_TRUE | 341,166,235 | 14.5% |
| POP_JUMP_IF_FALSE | 183,539,417 | 7.8% |
| STORE_FAST | 175,991,071 | 7.5% |
| LIST_APPEND | 117,835,057 | 5.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| FOR_ITER_LIST | 914,687,578 | 38.8% |
| FOR_ITER_RANGE | 428,472,955 | 18.2% |
| FOR_ITER | 270,505,723 | 11.5% |
| FOR_ITER_TUPLE | 205,160,442 | 8.7% |
| LOAD_FAST__LOAD_FAST | 107,852,520 | 4.6% |


</details>

### JUMP_BACKWARD_NO_INTERRUPT

<details>
<summary> Successors and predecessors for JUMP_BACKWARD_NO_INTERRUPT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RESUME | 125,849,532 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| SEND | 125,849,532 | 100.0% |


</details>

### JUMP_FORWARD

<details>
<summary> Successors and predecessors for JUMP_FORWARD </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST | 151,346,330 | 33.9% |
| COMPARE_AND_BRANCH_INT | 96,327,120 | 21.6% |
| POP_TOP | 54,810,957 | 12.3% |
| POP_JUMP_IF_FALSE | 25,037,260 | 5.6% |
| JUMP_FORWARD | 23,968,740 | 5.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 156,326,703 | 35.0% |
| LOAD_FAST__LOAD_FAST | 78,610,526 | 17.6% |
| LOAD_CONST__LOAD_FAST | 36,260,640 | 8.1% |
| LOAD_FAST__LOAD_CONST | 29,474,414 | 6.6% |
| LOAD_GLOBAL_BUILTIN | 25,642,875 | 5.7% |


</details>

### JUMP_IF_FALSE_OR_POP

<details>
<summary> Successors and predecessors for JUMP_IF_FALSE_OR_POP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 77,685,880 | 52.5% |
| UNARY_NOT | 15,265,157 | 10.3% |
| LOAD_ATTR_INSTANCE_VALUE | 14,784,550 | 10.0% |
| CALL_NO_KW_BUILTIN_FAST | 13,519,860 | 9.1% |
| COMPARE_OP | 12,062,186 | 8.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 104,821,489 | 70.9% |
| RETURN_VALUE | 34,115,864 | 23.1% |
| LOAD_GLOBAL_BUILTIN | 3,574,840 | 2.4% |
| STORE_FAST__LOAD_FAST | 1,601,700 | 1.1% |
| LOAD_GLOBAL_MODULE | 1,580,500 | 1.1% |


</details>

### JUMP_IF_TRUE_OR_POP

<details>
<summary> Successors and predecessors for JUMP_IF_TRUE_OR_POP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_INSTANCE_VALUE | 13,843,923 | 25.2% |
| LOAD_FAST | 12,236,836 | 22.3% |
| COMPARE_OP | 9,473,564 | 17.3% |
| LOAD_ATTR | 7,388,284 | 13.5% |
| RETURN_CONST | 2,773,784 | 5.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 34,197,607 | 62.3% |
| RETURN_VALUE | 8,594,640 | 15.7% |
| STORE_FAST__LOAD_FAST | 3,738,904 | 6.8% |
| LOAD_CONST__LOAD_FAST | 1,410,120 | 2.6% |
| LOAD_GLOBAL_BUILTIN | 1,238,760 | 2.3% |


</details>

### KW_NAMES

<details>
<summary> Successors and predecessors for KW_NAMES </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 43,022,444 | 22.8% |
| LOAD_CONST | 42,797,045 | 22.7% |
| LOAD_FAST | 29,770,518 | 15.8% |
| LOAD_GLOBAL_MODULE | 18,506,376 | 9.8% |
| LOAD_ATTR_INSTANCE_VALUE | 15,392,220 | 8.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL | 162,983,245 | 86.4% |
| CALL_BUILTIN_FAST_WITH_KEYWORDS | 24,469,840 | 13.0% |
| CALL_BUILTIN_CLASS | 1,174,820 | 0.6% |


</details>

### LIST_APPEND

<details>
<summary> Successors and predecessors for LIST_APPEND </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BUILD_TUPLE | 23,272,524 | 19.7% |
| RETURN_VALUE | 22,188,256 | 18.8% |
| BINARY_OP | 20,608,680 | 17.5% |
| LOAD_FAST | 15,913,299 | 13.5% |
| RETURN_GENERATOR | 13,436,700 | 11.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 117,835,057 | 99.9% |
| LOAD_DEREF | 96,000 | 0.1% |
| CALL_INTRINSIC_1 | 11,520 | 0.0% |


</details>

### LIST_EXTEND

<details>
<summary> Successors and predecessors for LIST_EXTEND </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_SLOT | 36,359,815 | 73.5% |
| LOAD_FAST | 12,411,812 | 25.1% |
| LOAD_CONST | 367,320 | 0.7% |
| RETURN_VALUE | 219,622 | 0.4% |
| LOAD_DEREF | 78,000 | 0.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_INTRINSIC_1 | 48,723,305 | 98.5% |
| LOAD_FAST | 174,322 | 0.4% |
| STORE_FAST__LOAD_FAST | 174,022 | 0.4% |
| STORE_FAST | 172,680 | 0.3% |
| UNPACK_SEQUENCE_LIST | 172,560 | 0.3% |


</details>

### LOAD_ATTR

<details>
<summary> Successors and predecessors for LOAD_ATTR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 486,147,313 | 36.3% |
| LOAD_GLOBAL_BUILTIN | 221,414,500 | 16.5% |
| STORE_FAST__LOAD_FAST | 159,425,201 | 11.9% |
| CALL_BUILTIN_CLASS | 111,940,819 | 8.4% |
| LOAD_GLOBAL_MODULE | 101,738,942 | 7.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 283,668,865 | 21.2% |
| IS_OP | 228,958,172 | 17.1% |
| STORE_FAST__LOAD_FAST | 144,943,901 | 10.8% |
| LOAD_FAST__LOAD_FAST | 142,657,286 | 10.6% |
| POP_JUMP_IF_FALSE | 61,706,498 | 4.6% |


</details>

### LOAD_ATTR_CLASS

<details>
<summary> Successors and predecessors for LOAD_ATTR_CLASS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_MODULE | 93,305,618 | 82.1% |
| LOAD_GLOBAL_BUILTIN | 15,500,160 | 13.6% |
| LOAD_FAST | 2,579,140 | 2.3% |
| LOAD_ATTR_MODULE | 1,894,500 | 1.7% |
| STORE_FAST__LOAD_FAST | 179,500 | 0.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| COMPARE_AND_BRANCH_INT | 56,413,440 | 49.7% |
| LOAD_FAST | 23,496,140 | 20.7% |
| LOAD_FAST__LOAD_FAST | 16,266,900 | 14.3% |
| COMPARE_OP | 3,286,560 | 2.9% |
| CALL_BUILTIN_CLASS | 2,841,880 | 2.5% |


</details>

### LOAD_ATTR_INSTANCE_VALUE

<details>
<summary> Successors and predecessors for LOAD_ATTR_INSTANCE_VALUE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 2,804,694,687 | 79.5% |
| STORE_FAST__LOAD_FAST | 242,567,095 | 6.9% |
| LOAD_FAST__LOAD_FAST | 234,899,490 | 6.7% |
| COPY | 66,090,962 | 1.9% |
| LOAD_ATTR_INSTANCE_VALUE | 59,332,172 | 1.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 1,020,380,722 | 28.9% |
| POP_JUMP_IF_FALSE | 539,789,560 | 15.3% |
| LOAD_ATTR_METHOD_NO_DICT | 181,168,263 | 5.1% |
| RETURN_VALUE | 171,645,771 | 4.9% |
| STORE_FAST__LOAD_FAST | 170,939,654 | 4.8% |


</details>

### LOAD_ATTR_METHOD_LAZY_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_LAZY_DICT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 86,785,430 | 60.1% |
| LOAD_ATTR_INSTANCE_VALUE | 36,685,880 | 25.4% |
| STORE_FAST__LOAD_FAST | 20,720,240 | 14.3% |
| LOAD_CONST__LOAD_FAST | 155,598 | 0.1% |
| LOAD_DEREF | 74,547 | 0.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 57,330,936 | 39.7% |
| CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS | 53,193,854 | 36.8% |
| CALL | 27,028,100 | 18.7% |
| LOAD_CONST | 5,260,018 | 3.6% |
| LOAD_FAST__LOAD_FAST | 1,305,960 | 0.9% |


</details>

### LOAD_ATTR_METHOD_NO_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_NO_DICT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 503,234,646 | 37.4% |
| STORE_FAST__LOAD_FAST | 308,892,618 | 23.0% |
| LOAD_ATTR_INSTANCE_VALUE | 181,168,263 | 13.5% |
| LOAD_GLOBAL_MODULE | 55,128,734 | 4.1% |
| LOAD_FAST__LOAD_CONST | 54,128,280 | 4.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 611,370,772 | 45.5% |
| CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS | 166,014,337 | 12.4% |
| LOAD_CONST | 135,330,411 | 10.1% |
| LOAD_FAST__LOAD_FAST | 129,461,045 | 9.6% |
| CALL_PY_EXACT_ARGS | 124,728,526 | 9.3% |


</details>

### LOAD_ATTR_METHOD_WITH_VALUES

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_WITH_VALUES </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 1,099,575,026 | 64.1% |
| STORE_FAST__LOAD_FAST | 389,372,143 | 22.7% |
| LOAD_ATTR_INSTANCE_VALUE | 70,839,677 | 4.1% |
| LOAD_ATTR_SLOT | 45,766,789 | 2.7% |
| LOAD_DEREF | 32,438,176 | 1.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 612,112,823 | 35.7% |
| LOAD_FAST | 546,627,286 | 31.8% |
| CALL_PY_EXACT_ARGS | 402,379,719 | 23.4% |
| LOAD_GLOBAL_MODULE | 48,509,398 | 2.8% |
| LOAD_CONST__LOAD_FAST | 31,056,120 | 1.8% |


</details>

### LOAD_ATTR_MODULE

<details>
<summary> Successors and predecessors for LOAD_ATTR_MODULE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_MODULE | 336,653,087 | 93.1% |
| LOAD_ATTR_MODULE | 11,694,760 | 3.2% |
| LOAD_ATTR | 6,904,551 | 1.9% |
| LOAD_FAST | 3,267,180 | 0.9% |
| LOAD_ATTR_CLASS | 1,887,220 | 0.5% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 125,027,715 | 34.6% |
| LOAD_FAST__LOAD_FAST | 100,547,479 | 27.8% |
| CALL | 30,497,429 | 8.4% |
| CALL_NO_KW_ISINSTANCE | 27,920,400 | 7.7% |
| LOAD_GLOBAL_BUILTIN | 12,459,760 | 3.4% |


</details>

### LOAD_ATTR_PROPERTY

<details>
<summary> Successors and predecessors for LOAD_ATTR_PROPERTY </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 41,149,786 | 62.7% |
| STORE_FAST__LOAD_FAST | 14,332,992 | 21.8% |
| LOAD_ATTR_SLOT | 5,110,965 | 7.8% |
| RETURN_VALUE | 1,738,466 | 2.6% |
| LOAD_DEREF | 1,222,660 | 1.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RESUME | 51,529,602 | 78.5% |
| COPY_FREE_VARS | 4,032,832 | 6.1% |
| POP_JUMP_IF_FALSE | 3,829,483 | 5.8% |
| GET_ITER | 1,442,682 | 2.2% |
| MAKE_CELL | 1,344,060 | 2.0% |


</details>

### LOAD_ATTR_SLOT

<details>
<summary> Successors and predecessors for LOAD_ATTR_SLOT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 1,113,177,368 | 79.0% |
| STORE_FAST__LOAD_FAST | 168,195,721 | 11.9% |
| LOAD_ATTR_SLOT | 41,112,213 | 2.9% |
| COPY | 40,164,120 | 2.9% |
| LOAD_DEREF | 16,015,380 | 1.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 320,971,277 | 22.8% |
| POP_JUMP_IF_FALSE | 148,204,535 | 10.5% |
| COMPARE_OP | 89,902,702 | 6.4% |
| LOAD_ATTR | 85,206,840 | 6.0% |
| STORE_FAST__LOAD_FAST | 58,614,978 | 4.2% |


</details>

### LOAD_ATTR_WITH_HINT

<details>
<summary> Successors and predecessors for LOAD_ATTR_WITH_HINT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 186,560,163 | 57.4% |
| STORE_FAST__LOAD_FAST | 72,981,880 | 22.5% |
| LOAD_ATTR_WITH_HINT | 22,464,774 | 6.9% |
| LOAD_ATTR_INSTANCE_VALUE | 22,337,203 | 6.9% |
| COPY | 12,970,260 | 4.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 78,478,660 | 24.1% |
| STORE_FAST__LOAD_FAST | 42,224,640 | 13.0% |
| COMPARE_AND_BRANCH_INT | 33,680,160 | 10.4% |
| LOAD_ATTR_METHOD_WITH_VALUES | 32,090,542 | 9.9% |
| LOAD_CONST | 27,880,560 | 8.6% |


</details>

### LOAD_BUILD_CLASS

<details>
<summary> Successors and predecessors for LOAD_BUILD_CLASS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| PUSH_NULL | 1,320 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CLOSURE | 1,320 | 100.0% |


</details>

### LOAD_CLASSDEREF

<details>
<summary> Successors and predecessors for LOAD_CLASSDEREF </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CLASSDEREF | 1,200 | 46.5% |
| PUSH_NULL | 1,200 | 46.5% |
| LOAD_NAME | 180 | 7.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CLASSDEREF | 1,200 | 46.5% |
| CALL_PY_EXACT_ARGS | 1,200 | 46.5% |
| LOAD_CONST | 180 | 7.0% |


</details>

### LOAD_CLOSURE

<details>
<summary> Successors and predecessors for LOAD_CLOSURE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_BUILTIN | 61,112,684 | 64.5% |
| LOAD_CLOSURE | 15,939,022 | 16.8% |
| POP_JUMP_IF_TRUE | 3,118,916 | 3.3% |
| LOAD_ATTR_MODULE | 2,239,500 | 2.4% |
| RESUME | 1,952,504 | 2.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| BUILD_TUPLE | 78,787,553 | 83.2% |
| LOAD_CLOSURE | 15,939,022 | 16.8% |


</details>

### LOAD_CONST

<details>
<summary> Successors and predecessors for LOAD_CONST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 458,914,413 | 11.5% |
| STORE_FAST__LOAD_FAST | 455,583,786 | 11.4% |
| LOAD_FAST__LOAD_FAST | 381,508,162 | 9.6% |
| LOAD_FAST__LOAD_CONST | 292,554,746 | 7.3% |
| BINARY_SUBSCR_LIST_INT | 193,145,340 | 4.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 458,914,413 | 11.5% |
| BINARY_OP_ADD_INT | 426,341,962 | 10.7% |
| COMPARE_AND_BRANCH_INT | 341,737,364 | 8.6% |
| STORE_FAST | 314,367,119 | 7.9% |
| CALL_NO_KW_BUILTIN_FAST | 290,712,040 | 7.3% |


</details>

### LOAD_CONST__LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_CONST__LOAD_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_ATTR_SLOT | 216,538,839 | 21.9% |
| POP_JUMP_IF_FALSE | 170,381,669 | 17.2% |
| RESUME | 142,133,752 | 14.4% |
| STORE_ATTR_INSTANCE_VALUE | 65,366,021 | 6.6% |
| FOR_ITER_RANGE | 55,903,320 | 5.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_ATTR_SLOT | 282,953,597 | 28.6% |
| LOAD_FAST | 202,427,095 | 20.4% |
| STORE_ATTR_INSTANCE_VALUE | 106,246,589 | 10.7% |
| SWAP | 78,935,460 | 8.0% |
| CONTAINS_OP | 66,590,160 | 6.7% |


</details>

### LOAD_DEREF

<details>
<summary> Successors and predecessors for LOAD_DEREF </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__STORE_FAST | 228,315,567 | 25.0% |
| STORE_FAST | 96,909,290 | 10.6% |
| FOR_ITER_RANGE | 64,789,812 | 7.1% |
| PUSH_NULL | 56,084,593 | 6.1% |
| LOAD_FAST | 38,804,472 | 4.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 472,217,074 | 51.7% |
| LOAD_ATTR | 78,330,182 | 8.6% |
| LOAD_CONST | 61,361,320 | 6.7% |
| LOAD_ATTR_METHOD_WITH_VALUES | 32,438,176 | 3.5% |
| LOAD_ATTR_INSTANCE_VALUE | 32,164,041 | 3.5% |


</details>

### LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_BUILTIN | 2,320,786,496 | 13.6% |
| RESUME | 1,926,195,654 | 11.3% |
| POP_JUMP_IF_FALSE | 1,813,356,165 | 10.6% |
| LOAD_ATTR_INSTANCE_VALUE | 1,020,380,722 | 6.0% |
| STORE_FAST__LOAD_FAST | 770,073,597 | 4.5% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_INSTANCE_VALUE | 2,804,694,687 | 16.5% |
| LOAD_ATTR_SLOT | 1,113,177,368 | 6.5% |
| LOAD_ATTR_METHOD_WITH_VALUES | 1,099,575,026 | 6.5% |
| LOAD_GLOBAL_BUILTIN | 977,050,361 | 5.7% |
| CALL_PY_EXACT_ARGS | 761,004,042 | 4.5% |


</details>

### LOAD_FAST_CHECK

<details>
<summary> Successors and predecessors for LOAD_FAST_CHECK </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| POP_TOP | 2,085,900 | 37.2% |
| LOAD_ATTR_METHOD_NO_DICT | 1,231,560 | 22.0% |
| POP_JUMP_IF_NONE | 1,211,905 | 21.6% |
| LOAD_GLOBAL_BUILTIN | 456,660 | 8.1% |
| POP_JUMP_IF_FALSE | 282,720 | 5.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_JUMP_IF_NOT_NONE | 1,506,240 | 26.8% |
| CALL_NO_KW_LIST_APPEND | 1,165,440 | 20.8% |
| LOAD_FAST | 1,042,320 | 18.6% |
| UNPACK_SEQUENCE_TWO_TUPLE | 432,000 | 7.7% |
| LOAD_ATTR_METHOD_NO_DICT | 219,620 | 3.9% |


</details>

### LOAD_FAST__LOAD_CONST

<details>
<summary> Successors and predecessors for LOAD_FAST__LOAD_CONST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_BUILTIN | 304,025,889 | 14.8% |
| PUSH_NULL | 181,067,940 | 8.8% |
| LOAD_GLOBAL_MODULE | 163,214,032 | 8.0% |
| COMPARE_AND_BRANCH_INT | 156,788,364 | 7.7% |
| POP_JUMP_IF_FALSE | 121,285,144 | 5.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_ADD_INT | 360,353,640 | 17.6% |
| LOAD_CONST | 292,554,746 | 14.3% |
| COMPARE_AND_BRANCH_INT | 236,156,634 | 11.5% |
| BINARY_OP_SUBTRACT_INT | 145,267,567 | 7.1% |
| BINARY_SUBSCR_TUPLE_INT | 135,604,698 | 6.6% |


</details>

### LOAD_FAST__LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_FAST__LOAD_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 643,351,741 | 11.2% |
| LOAD_ATTR_METHOD_WITH_VALUES | 612,112,823 | 10.7% |
| PUSH_NULL | 480,220,756 | 8.4% |
| POP_JUMP_IF_FALSE | 340,550,175 | 5.9% |
| RESUME | 313,140,747 | 5.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_PY_EXACT_ARGS | 663,819,636 | 11.5% |
| LOAD_FAST__LOAD_FAST | 643,351,741 | 11.2% |
| STORE_ATTR_SLOT | 502,486,513 | 8.7% |
| LOAD_CONST | 381,508,162 | 6.6% |
| LOAD_FAST | 364,617,525 | 6.3% |


</details>

### LOAD_GLOBAL

<details>
<summary> Successors and predecessors for LOAD_GLOBAL </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RETURN_VALUE | 7,284,080 | 49.8% |
| COMPARE_AND_BRANCH | 7,283,705 | 49.8% |
| STORE_FAST | 8,010 | 0.1% |
| RESUME | 7,629 | 0.1% |
| POP_JUMP_IF_FALSE | 3,720 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 14,567,060 | 99.6% |
| LOAD_GLOBAL_MODULE | 33,918 | 0.2% |
| LOAD_GLOBAL_BUILTIN | 15,298 | 0.1% |
| LOAD_ATTR | 1,885 | 0.0% |
| LOAD_GLOBAL | 174 | 0.0% |


</details>

### LOAD_GLOBAL_BUILTIN

<details>
<summary> Successors and predecessors for LOAD_GLOBAL_BUILTIN </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 977,050,361 | 24.2% |
| POP_JUMP_IF_FALSE | 889,952,943 | 22.0% |
| RESUME | 884,055,277 | 21.9% |
| STORE_FAST | 525,411,696 | 13.0% |
| POP_JUMP_IF_NOT_NONE | 123,863,452 | 3.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 2,320,786,496 | 57.5% |
| CALL_NO_KW_BUILTIN_FAST | 435,765,640 | 10.8% |
| LOAD_FAST__LOAD_CONST | 304,025,889 | 7.5% |
| CALL_NO_KW_ISINSTANCE | 222,906,882 | 5.5% |
| LOAD_ATTR | 221,414,500 | 5.5% |


</details>

### LOAD_GLOBAL_MODULE

<details>
<summary> Successors and predecessors for LOAD_GLOBAL_MODULE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 571,294,439 | 22.4% |
| STORE_FAST__LOAD_FAST | 340,415,290 | 13.3% |
| RESUME | 280,831,902 | 11.0% |
| STORE_FAST | 261,904,735 | 10.3% |
| POP_JUMP_IF_FALSE | 139,119,423 | 5.5% |

|Successors | Count | Percentage | 
|---|---:|---:|
| CALL_NO_KW_ISINSTANCE | 367,534,201 | 14.4% |
| LOAD_ATTR_MODULE | 336,653,087 | 13.2% |
| CONTAINS_OP | 266,981,914 | 10.5% |
| LOAD_FAST | 266,684,712 | 10.5% |
| LOAD_FAST__LOAD_FAST | 237,636,205 | 9.3% |


</details>

### LOAD_NAME

<details>
<summary> Successors and predecessors for LOAD_NAME </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| PUSH_NULL | 4,680,900 | 52.0% |
| LOAD_NAME | 4,320,720 | 48.0% |
| RESUME | 1,320 | 0.0% |
| STORE_NAME | 60 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_NAME | 4,320,720 | 48.0% |
| LOAD_CONST | 4,320,720 | 48.0% |
| PUSH_NULL | 360,000 | 4.0% |
| STORE_NAME | 1,320 | 0.0% |
| LOAD_CLASSDEREF | 180 | 0.0% |


</details>

### MAKE_CELL

<details>
<summary> Successors and predecessors for MAKE_CELL </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| MAKE_CELL | 67,489,420 | 60.4% |
| CALL_PY_EXACT_ARGS | 26,452,938 | 23.7% |
| CALL | 12,533,023 | 11.2% |
| CALL_PY_WITH_DEFAULTS | 1,705,172 | 1.5% |
| CALL_BOUND_METHOD_EXACT_ARGS | 1,383,080 | 1.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| MAKE_CELL | 67,489,420 | 55.8% |
| RESUME | 39,502,749 | 32.6% |
| RETURN_GENERATOR | 14,019,840 | 11.6% |


</details>

### MAKE_FUNCTION

<details>
<summary> Successors and predecessors for MAKE_FUNCTION </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 121,904,476 | 99.2% |
| LOAD_FAST__LOAD_CONST | 1,036,260 | 0.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 88,119,763 | 71.7% |
| LOAD_FAST__LOAD_CONST | 11,844,440 | 9.6% |
| LOAD_GLOBAL_BUILTIN | 6,739,268 | 5.5% |
| LOAD_GLOBAL_MODULE | 5,383,787 | 4.4% |
| STORE_FAST | 3,421,016 | 2.8% |


</details>

### MAP_ADD

<details>
<summary> Successors and predecessors for MAP_ADD </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_SLOT | 15,836,160 | 41.9% |
| RETURN_VALUE | 6,247,620 | 16.5% |
| LOAD_FAST__LOAD_FAST | 6,156,028 | 16.3% |
| JUMP_FORWARD | 4,782,720 | 12.7% |
| CALL_BUILTIN_CLASS | 2,461,560 | 6.5% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST__LOAD_FAST | 20,584,800 | 54.5% |
| JUMP_BACKWARD | 15,972,748 | 42.3% |
| CALL_FUNCTION_EX | 1,211,400 | 3.2% |
| LOAD_CONST | 5,940 | 0.0% |


</details>

### NOP

<details>
<summary> Successors and predecessors for NOP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RESUME | 175,726,647 | 34.8% |
| STORE_FAST | 72,826,800 | 14.4% |
| POP_JUMP_IF_FALSE | 56,222,728 | 11.1% |
| STORE_ATTR_INSTANCE_VALUE | 51,434,185 | 10.2% |
| JUMP_BACKWARD | 40,771,839 | 8.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 266,157,610 | 52.7% |
| LOAD_FAST__LOAD_FAST | 73,815,721 | 14.6% |
| PUSH_NULL | 51,345,429 | 10.2% |
| LOAD_GLOBAL_BUILTIN | 33,249,491 | 6.6% |
| LOAD_CONST__LOAD_FAST | 19,662,534 | 3.9% |


</details>

### POP_EXCEPT

<details>
<summary> Successors and predecessors for POP_EXCEPT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| POP_TOP | 8,548,256 | 48.1% |
| SWAP | 3,544,621 | 20.0% |
| STORE_SUBSCR_DICT | 3,075,240 | 17.3% |
| COPY | 1,817,700 | 10.2% |
| STORE_FAST | 544,080 | 3.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RETURN_CONST | 9,362,643 | 52.7% |
| RETURN_VALUE | 3,487,021 | 19.6% |
| RERAISE | 1,817,700 | 10.2% |
| JUMP_FORWARD | 1,718,040 | 9.7% |
| EXTENDED_ARG | 723,580 | 4.1% |


</details>

### POP_JUMP_IF_FALSE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_FALSE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| CONTAINS_OP | 656,984,897 | 15.9% |
| IS_OP | 559,188,426 | 13.5% |
| CALL_NO_KW_ISINSTANCE | 554,306,333 | 13.4% |
| LOAD_ATTR_INSTANCE_VALUE | 539,789,560 | 13.0% |
| CALL_NO_KW_BUILTIN_FAST | 400,893,172 | 9.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 1,813,356,165 | 43.8% |
| LOAD_GLOBAL_BUILTIN | 889,952,943 | 21.5% |
| LOAD_FAST__LOAD_FAST | 340,550,175 | 8.2% |
| RETURN_CONST | 197,369,857 | 4.8% |
| JUMP_BACKWARD | 183,539,417 | 4.4% |


</details>

### POP_JUMP_IF_NONE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_NONE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 158,385,200 | 45.9% |
| LOAD_FAST | 65,761,273 | 19.1% |
| EXTENDED_ARG | 37,561,404 | 10.9% |
| LOAD_ATTR_SLOT | 25,233,420 | 7.3% |
| LOAD_ATTR | 23,643,920 | 6.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 110,932,854 | 32.2% |
| PUSH_NULL | 62,776,027 | 18.2% |
| LOAD_FAST__LOAD_CONST | 36,369,118 | 10.5% |
| JUMP_BACKWARD | 29,141,740 | 8.4% |
| LOAD_DEREF | 27,409,140 | 7.9% |


</details>

### POP_JUMP_IF_NOT_NONE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_NOT_NONE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 250,030,910 | 53.4% |
| STORE_FAST__LOAD_FAST | 134,050,495 | 28.6% |
| EXTENDED_ARG | 30,724,260 | 6.6% |
| LOAD_ATTR_INSTANCE_VALUE | 24,803,801 | 5.3% |
| LOAD_ATTR | 17,768,371 | 3.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 156,956,062 | 33.5% |
| LOAD_GLOBAL_BUILTIN | 123,863,452 | 26.4% |
| LOAD_FAST__LOAD_FAST | 67,544,445 | 14.4% |
| LOAD_GLOBAL_MODULE | 36,474,600 | 7.8% |
| NOP | 18,392,481 | 3.9% |


</details>

### POP_JUMP_IF_TRUE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_TRUE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 540,513,998 | 46.0% |
| STORE_FAST__LOAD_FAST | 179,156,001 | 15.3% |
| CALL_NO_KW_ISINSTANCE | 121,433,262 | 10.3% |
| CONTAINS_OP | 68,231,186 | 5.8% |
| IS_OP | 57,615,466 | 4.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 482,910,872 | 41.1% |
| JUMP_BACKWARD | 341,166,235 | 29.1% |
| LOAD_GLOBAL_BUILTIN | 95,792,122 | 8.2% |
| LOAD_CONST | 61,916,066 | 5.3% |
| NOP | 34,776,046 | 3.0% |


</details>

### POP_TOP

<details>
<summary> Successors and predecessors for POP_TOP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RESUME | 552,814,168 | 27.1% |
| RETURN_CONST | 547,740,410 | 26.9% |
| CALL_NO_KW_BUILTIN_O | 386,831,386 | 19.0% |
| RETURN_VALUE | 109,853,193 | 5.4% |
| CALL_NO_KW_METHOD_DESCRIPTOR_O | 103,218,340 | 5.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 731,897,375 | 33.0% |
| LOAD_FAST | 621,714,371 | 28.0% |
| RESUME | 221,007,648 | 10.0% |
| RETURN_CONST | 170,517,110 | 7.7% |
| LOAD_FAST__LOAD_FAST | 106,539,006 | 4.8% |


</details>

### PUSH_EXC_INFO

<details>
<summary> Successors and predecessors for PUSH_EXC_INFO </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_SUBSCR_DICT | 5,603,357 | 31.6% |
| LOAD_ATTR | 3,318,980 | 18.7% |
| LOAD_ATTR_SLOT | 2,067,300 | 11.7% |
| CALL_NO_KW_BUILTIN_FAST | 1,822,360 | 10.3% |
| RERAISE | 1,716,000 | 9.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_BUILTIN | 16,455,653 | 92.7% |
| LOAD_GLOBAL_MODULE | 877,848 | 4.9% |
| LOAD_FAST | 388,140 | 2.2% |
| WITH_EXCEPT_START | 36,000 | 0.2% |
| LOAD_CONST | 1,440 | 0.0% |


</details>

### PUSH_NULL

<details>
<summary> Successors and predecessors for PUSH_NULL </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST | 287,347,229 | 32.6% |
| POP_JUMP_IF_FALSE | 80,571,182 | 9.1% |
| POP_TOP | 79,748,673 | 9.0% |
| POP_JUMP_IF_NONE | 62,776,027 | 7.1% |
| NOP | 51,345,429 | 5.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 480,220,756 | 54.4% |
| LOAD_FAST__LOAD_CONST | 181,067,940 | 20.5% |
| LOAD_FAST | 152,789,419 | 17.3% |
| LOAD_DEREF | 56,084,593 | 6.4% |
| LOAD_GLOBAL_BUILTIN | 5,562,138 | 0.6% |


</details>

### RAISE_VARARGS

<details>
<summary> Successors and predecessors for RAISE_VARARGS </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 658,020 | 29.2% |
| LOAD_ATTR_MODULE | 583,740 | 25.9% |
| LOAD_GLOBAL_BUILTIN | 559,560 | 24.8% |
| CALL | 186,068 | 8.3% |
| LOAD_FAST | 152,400 | 6.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| COPY | 1,078,680 | 48.2% |
| PUSH_EXC_INFO | 1,006,028 | 45.0% |
| LOAD_CONST | 151,140 | 6.8% |


</details>

### RERAISE

<details>
<summary> Successors and predecessors for RERAISE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| POP_EXCEPT | 1,817,700 | 70.2% |
| POP_TOP | 386,940 | 14.9% |
| POP_JUMP_IF_FALSE | 154,860 | 6.0% |
| DELETE_FAST | 151,140 | 5.8% |
| CALL_INTRINSIC_1 | 41,400 | 1.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| PUSH_EXC_INFO | 1,716,000 | 69.0% |
| COPY | 730,380 | 29.4% |
| CALL_INTRINSIC_1 | 41,160 | 1.7% |


</details>

### RESUME

<details>
<summary> Successors and predecessors for RESUME </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| CALL_PY_EXACT_ARGS | 2,232,932,662 | 63.6% |
| POP_TOP | 221,007,648 | 6.3% |
| COPY_FREE_VARS | 209,961,049 | 6.0% |
| CALL_BOUND_METHOD_EXACT_ARGS | 188,830,691 | 5.4% |
| CALL | 186,971,844 | 5.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 1,926,195,654 | 39.9% |
| LOAD_GLOBAL_BUILTIN | 884,055,277 | 18.3% |
| POP_TOP | 552,814,168 | 11.5% |
| LOAD_FAST__LOAD_FAST | 313,140,747 | 6.5% |
| LOAD_GLOBAL_MODULE | 280,831,902 | 5.8% |


</details>

### RETURN_CONST

<details>
<summary> Successors and predecessors for RETURN_CONST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_ATTR_SLOT | 242,975,227 | 18.2% |
| POP_JUMP_IF_FALSE | 197,369,857 | 14.8% |
| STORE_ATTR_INSTANCE_VALUE | 184,950,087 | 13.8% |
| POP_TOP | 170,517,110 | 12.7% |
| RESUME | 129,946,850 | 9.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_TOP | 547,740,410 | 40.9% |
| INTERPRETER_EXIT | 525,400,243 | 39.3% |
| LOAD_FAST | 52,452,120 | 3.9% |
| POP_JUMP_IF_FALSE | 50,736,773 | 3.8% |
| RETURN_VALUE | 49,790,538 | 3.7% |


</details>

### RETURN_GENERATOR

<details>
<summary> Successors and predecessors for RETURN_GENERATOR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| CALL_PY_EXACT_ARGS | 126,796,884 | 61.4% |
| COPY_FREE_VARS | 61,646,684 | 29.8% |
| MAKE_CELL | 14,019,840 | 6.8% |
| CALL_PY_WITH_DEFAULTS | 3,419,820 | 1.7% |
| CALL | 789,540 | 0.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| GET_AWAITABLE | 77,837,896 | 35.2% |
| GET_ITER | 37,931,880 | 17.2% |
| CALL_BUILTIN_FAST_WITH_KEYWORDS | 33,032,100 | 14.9% |
| CALL | 15,622,820 | 7.1% |
| INTERPRETER_EXIT | 14,360,980 | 6.5% |


</details>

### RETURN_VALUE

<details>
<summary> Successors and predecessors for RETURN_VALUE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 641,512,872 | 22.9% |
| RETURN_VALUE | 439,035,905 | 15.7% |
| BUILD_TUPLE | 337,650,089 | 12.1% |
| LOAD_ATTR_INSTANCE_VALUE | 171,645,771 | 6.1% |
| COMPARE_OP | 119,071,175 | 4.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| INTERPRETER_EXIT | 503,693,372 | 18.0% |
| RETURN_VALUE | 439,035,905 | 15.7% |
| STORE_FAST__LOAD_FAST | 314,435,324 | 11.2% |
| UNPACK_SEQUENCE_TUPLE | 240,156,896 | 8.6% |
| LOAD_FAST | 213,092,070 | 7.6% |


</details>

### SEND

<details>
<summary> Successors and predecessors for SEND </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 193,536,278 | 60.6% |
| JUMP_BACKWARD_NO_INTERRUPT | 125,849,532 | 39.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| YIELD_VALUE | 125,865,516 | 39.4% |
| STORE_FAST__LOAD_FAST | 88,512,238 | 27.7% |
| POP_TOP | 30,022,976 | 9.4% |
| LOAD_GLOBAL_MODULE | 29,134,080 | 9.1% |
| BINARY_OP_ADD_INT | 29,134,080 | 9.1% |


</details>

### SET_ADD

<details>
<summary> Successors and predecessors for SET_ADD </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_ADD_UNICODE | 2,879,280 | 92.5% |
| LOAD_ATTR_INSTANCE_VALUE | 124,560 | 4.0% |
| STORE_FAST__LOAD_FAST | 48,000 | 1.5% |
| LOAD_FAST | 31,380 | 1.0% |
| BINARY_SUBSCR_LIST_INT | 17,520 | 0.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 3,114,300 | 100.0% |


</details>

### SET_UPDATE

<details>
<summary> Successors and predecessors for SET_UPDATE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 16,680 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| COMPARE_AND_BRANCH | 16,320 | 97.8% |
| STORE_FAST | 240 | 1.4% |
| LOAD_GLOBAL_BUILTIN | 120 | 0.7% |


</details>

### STORE_ATTR

<details>
<summary> Successors and predecessors for STORE_ATTR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 18,317,200 | 32.0% |
| LOAD_CONST__LOAD_FAST | 17,052,084 | 29.7% |
| LOAD_FAST__LOAD_FAST | 14,243,792 | 24.8% |
| CALL | 5,419,260 | 9.5% |
| SWAP | 1,379,074 | 2.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 16,427,107 | 28.7% |
| LOAD_DEREF | 13,449,060 | 23.5% |
| RETURN_CONST | 11,515,204 | 20.1% |
| JUMP_BACKWARD | 5,554,200 | 9.7% |
| LOAD_FAST__LOAD_FAST | 4,982,508 | 8.7% |


</details>

### STORE_ATTR_INSTANCE_VALUE

<details>
<summary> Successors and predecessors for STORE_ATTR_INSTANCE_VALUE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 321,911,686 | 39.7% |
| LOAD_FAST | 242,570,418 | 29.9% |
| LOAD_CONST__LOAD_FAST | 106,246,589 | 13.1% |
| SWAP | 66,090,962 | 8.1% |
| BINARY_SUBSCR_LIST_INT | 27,097,200 | 3.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 265,735,218 | 32.7% |
| RETURN_CONST | 184,950,087 | 22.8% |
| LOAD_FAST__LOAD_FAST | 173,968,609 | 21.4% |
| LOAD_CONST__LOAD_FAST | 65,366,021 | 8.1% |
| NOP | 51,434,185 | 6.3% |


</details>

### STORE_ATTR_SLOT

<details>
<summary> Successors and predecessors for STORE_ATTR_SLOT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 502,486,513 | 47.8% |
| LOAD_CONST__LOAD_FAST | 282,953,597 | 26.9% |
| LOAD_FAST | 221,411,313 | 21.1% |
| SWAP | 40,164,120 | 3.8% |
| STORE_ATTR_SLOT | 2,140,270 | 0.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 281,273,578 | 26.8% |
| RETURN_CONST | 242,975,227 | 23.1% |
| LOAD_FAST | 241,313,264 | 23.0% |
| LOAD_CONST__LOAD_FAST | 216,538,839 | 20.6% |
| LOAD_GLOBAL_BUILTIN | 24,870,620 | 2.4% |


</details>

### STORE_ATTR_WITH_HINT

<details>
<summary> Successors and predecessors for STORE_ATTR_WITH_HINT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 21,342,436 | 42.4% |
| SWAP | 12,970,260 | 25.8% |
| LOAD_FAST__LOAD_FAST | 11,671,820 | 23.2% |
| LOAD_CONST__LOAD_FAST | 4,058,301 | 8.1% |
| RETURN_VALUE | 224,100 | 0.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 33,447,440 | 66.5% |
| JUMP_BACKWARD | 5,307,540 | 10.6% |
| RETURN_CONST | 4,207,962 | 8.4% |
| LOAD_CONST__LOAD_FAST | 3,665,340 | 7.3% |
| LOAD_FAST__LOAD_FAST | 2,307,900 | 4.6% |


</details>

### STORE_DEREF

<details>
<summary> Successors and predecessors for STORE_DEREF </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_ADD_INT | 27,675,600 | 41.6% |
| LOAD_CONST | 8,746,320 | 13.2% |
| UNPACK_SEQUENCE_TWO_TUPLE | 7,169,040 | 10.8% |
| RETURN_VALUE | 3,731,172 | 5.6% |
| CALL | 3,375,356 | 5.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_DEREF | 18,353,935 | 27.6% |
| LOAD_FAST__LOAD_FAST | 13,438,200 | 20.2% |
| LOAD_FAST | 8,760,520 | 13.2% |
| LOAD_CONST | 6,911,340 | 10.4% |
| STORE_FAST__LOAD_FAST | 6,144,600 | 9.2% |


</details>

### STORE_FAST

<details>
<summary> Successors and predecessors for STORE_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 314,367,119 | 15.6% |
| CALL_NO_KW_BUILTIN_FAST | 222,602,500 | 11.1% |
| STORE_FAST__STORE_FAST | 213,446,340 | 10.6% |
| FOR_ITER_LIST | 171,970,437 | 8.6% |
| RETURN_VALUE | 158,778,864 | 7.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_GLOBAL_BUILTIN | 525,411,696 | 26.1% |
| PUSH_NULL | 287,347,229 | 14.3% |
| LOAD_GLOBAL_MODULE | 261,904,735 | 13.0% |
| JUMP_BACKWARD | 175,991,071 | 8.8% |
| LOAD_CONST | 174,449,053 | 8.7% |


</details>

### STORE_FAST__LOAD_FAST

<details>
<summary> Successors and predecessors for STORE_FAST__LOAD_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| FOR_ITER_LIST | 484,768,633 | 11.1% |
| RETURN_VALUE | 314,435,324 | 7.2% |
| CALL | 291,906,849 | 6.7% |
| CALL_NO_KW_METHOD_DESCRIPTOR_FAST | 286,231,147 | 6.5% |
| CALL_NO_KW_TYPE_1 | 249,581,544 | 5.7% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 770,073,597 | 17.7% |
| LOAD_CONST | 455,583,786 | 10.5% |
| LOAD_ATTR_METHOD_WITH_VALUES | 389,372,143 | 9.0% |
| POP_JUMP_IF_FALSE | 366,870,075 | 8.5% |
| LOAD_GLOBAL_MODULE | 340,415,290 | 7.8% |


</details>

### STORE_FAST__STORE_FAST

<details>
<summary> Successors and predecessors for STORE_FAST__STORE_FAST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__STORE_FAST | 822,937,356 | 41.0% |
| UNPACK_SEQUENCE_TWO_TUPLE | 586,600,607 | 29.2% |
| UNPACK_SEQUENCE_TUPLE | 391,868,812 | 19.5% |
| UNPACK_SEQUENCE_LIST | 140,351,876 | 7.0% |
| LOAD_ATTR_SLOT | 45,908,040 | 2.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__STORE_FAST | 822,937,356 | 41.0% |
| LOAD_FAST | 445,230,311 | 22.2% |
| LOAD_DEREF | 228,315,567 | 11.4% |
| STORE_FAST | 213,446,340 | 10.6% |
| STORE_FAST__LOAD_FAST | 112,467,656 | 5.6% |


</details>

### STORE_GLOBAL

<details>
<summary> Successors and predecessors for STORE_GLOBAL </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_ADD_INT | 6,147,600 | 99.9% |
| CALL | 3,840 | 0.1% |
| LOAD_ATTR | 540 | 0.0% |
| LOAD_FAST | 300 | 0.0% |
| BUILD_MAP | 60 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 4,864,260 | 79.1% |
| LOAD_GLOBAL_MODULE | 1,285,980 | 20.9% |
| LOAD_CONST | 1,920 | 0.0% |
| RETURN_CONST | 180 | 0.0% |
| BUILD_MAP | 60 | 0.0% |


</details>

### STORE_NAME

<details>
<summary> Successors and predecessors for STORE_NAME </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_NAME | 1,320 | 25.3% |
| LOAD_CONST | 1,320 | 25.3% |
| LOAD_ATTR | 1,200 | 23.0% |
| MAKE_FUNCTION | 660 | 12.6% |
| IMPORT_NAME | 360 | 6.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RETURN_CONST | 2,100 | 40.2% |
| LOAD_CONST | 1,440 | 27.6% |
| PUSH_NULL | 1,380 | 26.4% |
| LOAD_CLOSURE | 120 | 2.3% |
| STORE_NAME | 120 | 2.3% |


</details>

### STORE_SLICE

<details>
<summary> Successors and predecessors for STORE_SLICE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_ADD_INT | 103,909,740 | 88.3% |
| LOAD_CONST | 13,459,080 | 11.4% |
| LOAD_FAST__LOAD_FAST | 258,360 | 0.2% |
| LOAD_ATTR | 8,040 | 0.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_CONST | 103,875,000 | 88.3% |
| RETURN_CONST | 5,855,760 | 5.0% |
| LOAD_FAST__LOAD_FAST | 4,157,040 | 3.5% |
| LOAD_FAST | 3,703,320 | 3.1% |
| JUMP_BACKWARD | 40,320 | 0.0% |


</details>

### STORE_SUBSCR

<details>
<summary> Successors and predecessors for STORE_SUBSCR </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| SWAP | 109,576,100 | 33.0% |
| LOAD_FAST | 89,285,588 | 26.8% |
| BINARY_OP_ADD_INT | 41,532,300 | 12.5% |
| LOAD_FAST__LOAD_FAST | 36,634,860 | 11.0% |
| LOAD_FAST__LOAD_CONST | 36,065,620 | 10.8% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 112,475,280 | 33.8% |
| LOAD_FAST__LOAD_FAST | 104,596,380 | 31.5% |
| RETURN_CONST | 37,815,834 | 11.4% |
| LOAD_GLOBAL_BUILTIN | 27,031,060 | 8.1% |
| LOAD_DEREF | 15,741,300 | 4.7% |


</details>

### STORE_SUBSCR_DICT

<details>
<summary> Successors and predecessors for STORE_SUBSCR_DICT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 119,746,807 | 64.2% |
| LOAD_FAST__LOAD_FAST | 18,710,280 | 10.0% |
| CALL_NO_KW_BUILTIN_O | 13,999,740 | 7.5% |
| LOAD_FAST__LOAD_CONST | 8,221,760 | 4.4% |
| RETURN_VALUE | 8,051,180 | 4.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 73,254,123 | 39.3% |
| LOAD_FAST | 45,335,757 | 24.3% |
| JUMP_BACKWARD | 30,167,700 | 16.2% |
| RETURN_CONST | 17,559,723 | 9.4% |
| LOAD_GLOBAL_MODULE | 7,347,483 | 3.9% |


</details>

### STORE_SUBSCR_LIST_INT

<details>
<summary> Successors and predecessors for STORE_SUBSCR_LIST_INT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| SWAP | 158,997,820 | 50.0% |
| LOAD_FAST__LOAD_FAST | 53,875,464 | 17.0% |
| LOAD_FAST | 40,428,664 | 12.7% |
| LOAD_FAST__LOAD_CONST | 27,444,000 | 8.6% |
| BINARY_SUBSCR_LIST_INT | 20,171,040 | 6.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| JUMP_BACKWARD | 116,881,656 | 36.8% |
| LOAD_FAST__LOAD_FAST | 105,052,952 | 33.1% |
| LOAD_FAST__LOAD_CONST | 87,697,560 | 27.6% |
| RETURN_CONST | 4,685,160 | 1.5% |
| LOAD_FAST | 1,265,480 | 0.4% |


</details>

### SWAP

<details>
<summary> Successors and predecessors for SWAP </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| SWAP | 270,086,400 | 32.1% |
| BINARY_OP_ADD_FLOAT | 116,255,040 | 13.8% |
| LOAD_CONST__LOAD_FAST | 78,935,460 | 9.4% |
| BINARY_OP_ADD_INT | 76,919,273 | 9.2% |
| BINARY_OP_SUBTRACT_INT | 68,066,916 | 8.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| SWAP | 270,086,400 | 32.1% |
| STORE_SUBSCR_LIST_INT | 158,997,820 | 18.9% |
| COPY | 128,776,500 | 15.3% |
| STORE_SUBSCR | 109,576,100 | 13.0% |
| STORE_ATTR_INSTANCE_VALUE | 66,090,962 | 7.9% |


</details>

### UNARY_INVERT

<details>
<summary> Successors and predecessors for UNARY_INVERT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP | 10,521,380 | 88.2% |
| LOAD_ATTR_MODULE | 895,191 | 7.5% |
| LOAD_ATTR | 372,800 | 3.1% |
| LOAD_FAST | 122,040 | 1.0% |
| LOAD_FAST__LOAD_FAST | 17,100 | 0.1% |

|Successors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP | 11,928,511 | 100.0% |


</details>

### UNARY_NEGATIVE

<details>
<summary> Successors and predecessors for UNARY_NEGATIVE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST__LOAD_FAST | 110,875,674 | 91.2% |
| LOAD_GLOBAL_MODULE | 3,059,144 | 2.5% |
| LOAD_FAST | 2,939,722 | 2.4% |
| LOAD_CONST__LOAD_FAST | 2,197,860 | 1.8% |
| BINARY_SUBSCR_TUPLE_INT | 1,205,640 | 1.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| LOAD_CONST | 79,368,240 | 65.2% |
| BINARY_SUBSCR_LIST_INT | 26,768,580 | 22.0% |
| CALL_PY_EXACT_ARGS | 3,191,160 | 2.6% |
| STORE_SUBSCR | 2,419,140 | 2.0% |
| BINARY_SUBSCR | 2,419,140 | 2.0% |


</details>

### UNARY_NOT

<details>
<summary> Successors and predecessors for UNARY_NOT </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_ATTR_INSTANCE_VALUE | 16,889,094 | 36.3% |
| LOAD_FAST | 12,811,560 | 27.5% |
| CALL_NO_KW_ISINSTANCE | 8,059,528 | 17.3% |
| COMPARE_OP | 2,531,390 | 5.4% |
| STORE_FAST__LOAD_FAST | 2,427,596 | 5.2% |

|Successors | Count | Percentage | 
|---|---:|---:|
| RETURN_VALUE | 15,892,267 | 34.2% |
| JUMP_IF_FALSE_OR_POP | 15,265,157 | 32.8% |
| KW_NAMES | 10,565,608 | 22.7% |
| JUMP_IF_TRUE_OR_POP | 1,666,800 | 3.6% |
| STORE_FAST | 1,049,892 | 2.3% |


</details>

### UNPACK_EX

<details>
<summary> Successors and predecessors for UNPACK_EX </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| YIELD_VALUE | 218,520 | 99.2% |
| CALL_INTRINSIC_1 | 960 | 0.4% |
| FOR_ITER | 720 | 0.3% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__STORE_FAST | 220,200 | 100.0% |


</details>

### UNPACK_SEQUENCE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__LOAD_FAST | 170,944 | 42.5% |
| CALL_NO_KW_METHOD_DESCRIPTOR_NOARGS | 96,120 | 23.9% |
| CALL_NO_KW_METHOD_DESCRIPTOR_FAST | 67,940 | 16.9% |
| COPY | 19,920 | 5.0% |
| RETURN_VALUE | 18,660 | 4.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__STORE_FAST | 300,856 | 74.9% |
| STORE_FAST | 96,000 | 23.9% |
| UNPACK_SEQUENCE_TWO_TUPLE | 2,880 | 0.7% |
| UNPACK_SEQUENCE | 1,009 | 0.3% |
| UNPACK_SEQUENCE_TUPLE | 700 | 0.2% |


</details>

### UNPACK_SEQUENCE_LIST

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_LIST </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| LOAD_FAST | 98,505,716 | 70.1% |
| UNPACK_SEQUENCE_TUPLE | 24,026,440 | 17.1% |
| CALL | 10,636,560 | 7.6% |
| STORE_FAST | 6,001,080 | 4.3% |
| CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS | 889,800 | 0.6% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__STORE_FAST | 140,351,876 | 99.9% |
| STORE_DEREF | 83,340 | 0.1% |
| UNPACK_SEQUENCE_TUPLE | 24,040 | 0.0% |
| STORE_FAST | 60 | 0.0% |


</details>

### UNPACK_SEQUENCE_TUPLE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_TUPLE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| RETURN_VALUE | 240,156,896 | 56.2% |
| LOAD_FAST | 103,278,319 | 24.2% |
| YIELD_VALUE | 25,090,720 | 5.9% |
| BINARY_SUBSCR_DICT | 14,268,900 | 3.3% |
| STORE_FAST | 12,341,280 | 2.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__STORE_FAST | 391,868,812 | 91.7% |
| UNPACK_SEQUENCE_LIST | 24,026,440 | 5.6% |
| STORE_FAST | 6,003,000 | 1.4% |
| STORE_FAST__LOAD_FAST | 4,943,598 | 1.2% |
| LOAD_FAST | 290,520 | 0.1% |


</details>

### UNPACK_SEQUENCE_TWO_TUPLE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_TWO_TUPLE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| FOR_ITER_LIST | 319,430,100 | 51.8% |
| FOR_ITER | 202,571,759 | 32.8% |
| LOAD_FAST | 36,686,677 | 5.9% |
| RETURN_VALUE | 25,762,645 | 4.2% |
| BINARY_SUBSCR_LIST_INT | 14,995,572 | 2.4% |

|Successors | Count | Percentage | 
|---|---:|---:|
| STORE_FAST__STORE_FAST | 586,600,607 | 95.1% |
| UNPACK_SEQUENCE_TUPLE | 12,001,200 | 1.9% |
| STORE_FAST__LOAD_FAST | 9,187,080 | 1.5% |
| STORE_DEREF | 7,169,040 | 1.2% |
| LOAD_FAST | 922,740 | 0.1% |


</details>

### WITH_EXCEPT_START

<details>
<summary> Successors and predecessors for WITH_EXCEPT_START </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| PUSH_EXC_INFO | 36,000 | 100.0% |

|Successors | Count | Percentage | 
|---|---:|---:|
| POP_JUMP_IF_TRUE | 36,000 | 100.0% |


</details>

### YIELD_VALUE

<details>
<summary> Successors and predecessors for YIELD_VALUE </summary>

|Predecessors | Count | Percentage | 
|---|---:|---:|
| BINARY_OP_MULTIPLY_FLOAT | 210,931,680 | 30.7% |
| SEND | 125,865,516 | 18.3% |
| CALL_INTRINSIC_1 | 94,136,760 | 13.7% |
| LOAD_FAST | 40,682,716 | 5.9% |
| STORE_FAST__LOAD_FAST | 33,558,540 | 4.9% |

|Successors | Count | Percentage | 
|---|---:|---:|
| INTERPRETER_EXIT | 596,523,325 | 87.0% |
| STORE_FAST__LOAD_FAST | 48,146,754 | 7.0% |
| UNPACK_SEQUENCE_TUPLE | 25,090,720 | 3.7% |
| STORE_FAST | 12,307,740 | 1.8% |
| STORE_DEREF | 2,419,200 | 0.4% |


</details>


</details>

## Specialization stats

<details>
<summary> specialization stats by family </summary>

### BINARY_SUBSCR

<details>
<summary> specialization stats for BINARY_SUBSCR family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |   1116721822 | 40.1% |
| specialization.deopt |        77040 | 0.0% |
|          hit |   1660896520 | 59.7% |
|         miss |      4094815 | 0.1% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 79,136 | 21.3% |
| Failure | 292,353 | 78.7% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| array int | 112,980 | 38.6% |
| other | 86,575 | 29.6% |
| out of range | 25,800 | 8.8% |
| list slice | 25,520 | 8.7% |
| buffer int | 19,600 | 6.7% |
| string int | 17,160 | 5.9% |
| sequence int | 3,118 | 1.1% |
| code complex parameters | 1,340 | 0.5% |
| buffer slice | 180 | 0.1% |
| tuple slice | 60 | 0.0% |
| string slice | 20 | 0.0% |


</details>

### BINARY_SLICE

<details>
<summary> specialization stats for BINARY_SLICE family </summary>

|Kind | Count | Ratio | 
|---|---|---|


</details>

### STORE_SLICE

<details>
<summary> specialization stats for STORE_SLICE family </summary>

|Kind | Count | Ratio | 
|---|---|---|


</details>

### STORE_SUBSCR

<details>
<summary> specialization stats for STORE_SUBSCR family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |    332457161 | 39.7% |
| specialization.deopt |           40 | 0.0% |
|          hit |    504303270 | 60.3% |
|         miss |         2220 | 0.0% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 1,067 | 1.2% |
| Failure | 88,960 | 98.8% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| array int | 45,640 | 51.3% |
| dict subclass no override | 22,000 | 24.7% |
| py simple | 14,380 | 16.2% |
| bytearray int | 5,200 | 5.8% |
| out of range | 1,020 | 1.1% |
| other | 680 | 0.8% |
| list slice | 40 | 0.0% |


</details>

### UNPACK_SEQUENCE

<details>
<summary> specialization stats for UNPACK_SEQUENCE family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |       397216 | 0.0% |
| specialization.deopt |        48080 | 0.0% |
|          hit |   1181759257 | 99.8% |
|         miss |      2547700 | 0.2% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 51,760 | 98.1% |
| Failure | 1,009 | 1.9% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| sequence | 729 | 72.2% |
| iterator | 200 | 19.8% |
| other | 80 | 7.9% |


</details>

### FOR_ITER

<details>
<summary> specialization stats for FOR_ITER family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |    378803256 | 15.0% |
| specialization.deopt |      2508043 | 0.1% |
|          hit |   2005179396 | 79.7% |
|         miss |    132932646 | 5.3% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 2,508,869 | 93.8% |
| Failure | 166,752 | 6.2% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| dict items | 60,346 | 36.2% |
| enumerate | 24,698 | 14.8% |
| other | 19,500 | 11.7% |
| set | 16,248 | 9.7% |
| seq iter | 15,120 | 9.1% |
| dict keys | 7,180 | 4.3% |
| zip | 7,020 | 4.2% |
| dict values | 5,180 | 3.1% |
| reversed list | 4,540 | 2.7% |
| itertools | 3,000 | 1.8% |
| ascii string | 2,820 | 1.7% |
| range | 500 | 0.3% |
| map | 420 | 0.3% |
| callable | 120 | 0.1% |
| bytes | 40 | 0.0% |
| string | 20 | 0.0% |


</details>

### STORE_ATTR

<details>
<summary> specialization stats for STORE_ATTR family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |     57264223 | 2.9% |
| specialization.deopt |      3353951 | 0.2% |
|          hit |   1734977440 | 88.1% |
|         miss |    177766173 | 9.0% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 3,370,518 | 98.7% |
| Failure | 43,806 | 1.3% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| class attr simple | 17,820 | 40.7% |
| not managed dict | 8,382 | 19.1% |
| not in dict | 7,920 | 18.1% |
| overriding descriptor | 5,420 | 12.4% |
| property | 1,060 | 2.4% |
| not in keys | 940 | 2.1% |
| non object slot | 920 | 2.1% |
| overridden | 744 | 1.7% |
| no dict | 360 | 0.8% |
| method | 240 | 0.5% |


</details>

### LOAD_ATTR

<details>
<summary> specialization stats for LOAD_ATTR family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |   1338087228 | 12.9% |
| specialization.deopt |      9143088 | 0.1% |
|          hit |   8521003450 | 82.4% |
|         miss |    484784625 | 4.7% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 9,200,048 | 83.8% |
| Failure | 1,778,501 | 16.2% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| has managed dict | 621,694 | 35.0% |
| class attr simple | 602,046 | 33.9% |
| not managed dict | 287,620 | 16.2% |
| metaclass attribute | 115,004 | 6.5% |
| method | 58,862 | 3.3% |
| overridden | 42,299 | 2.4% |
| mutable class | 20,081 | 1.1% |
| class method obj | 11,902 | 0.7% |
| non object slot | 7,280 | 0.4% |
| non overriding descriptor | 4,044 | 0.2% |
| class attr descriptor | 2,740 | 0.2% |
| shadowed | 2,009 | 0.1% |
| not in keys | 1,680 | 0.1% |
| builtin class method | 840 | 0.0% |
| module attr not found | 400 | 0.0% |


</details>

### COMPARE_OP

<details>
<summary> specialization stats for COMPARE_OP family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |    224516260 | 100.0% |


</details>

### LOAD_GLOBAL

<details>
<summary> specialization stats for LOAD_GLOBAL family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |     14569481 | 0.2% |
| specialization.deopt |          344 | 0.0% |
|          hit |   6590905773 | 99.8% |
|         miss |        22132 | 0.0% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 49,560 | 100.0% |
| Failure | 0 | 0.0% |

|Failure kind | Count | Ratio | 
|---|---:|---:|


</details>

### BINARY_OP

<details>
<summary> specialization stats for BINARY_OP family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |    857818215 | 19.7% |
| specialization.deopt |       712800 | 0.0% |
|          hit |   3462465063 | 79.4% |
|         miss |     37779860 | 0.9% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 716,857 | 39.1% |
| Failure | 1,117,368 | 60.9% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| subtract different types | 579,324 | 51.8% |
| multiply different types | 173,809 | 15.6% |
| add different types | 152,763 | 13.7% |
| remainder | 33,802 | 3.0% |
| floor divide | 32,640 | 2.9% |
| add other | 26,947 | 2.4% |
| and int | 26,033 | 2.3% |
| lshift | 18,700 | 1.7% |
| rshift | 17,554 | 1.6% |
| true divide different types | 15,300 | 1.4% |
| xor | 10,739 | 1.0% |
| subtract other | 8,320 | 0.7% |
| true divide float | 6,640 | 0.6% |
| or | 5,526 | 0.5% |
| power | 4,480 | 0.4% |
| multiply other | 2,560 | 0.2% |
| true divide other | 1,120 | 0.1% |
| and other | 1,011 | 0.1% |
| and different types | 100 | 0.0% |


</details>

### COMPARE_AND_BRANCH

<details>
<summary> specialization stats for COMPARE_AND_BRANCH family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |    142556398 | 8.8% |
| specialization.deopt |        23885 | 0.0% |
|          hit |   1470855206 | 91.1% |
|         miss |      1268302 | 0.1% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 27,919 | 19.6% |
| Failure | 114,368 | 80.4% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| big int | 50,327 | 44.0% |
| different types | 29,205 | 25.5% |
| float long | 8,913 | 7.8% |
| baseobject | 7,800 | 6.8% |
| set | 6,821 | 6.0% |
| other | 4,038 | 3.5% |
| tuple | 3,435 | 3.0% |
| bool | 1,749 | 1.5% |
| bytes | 940 | 0.8% |
| list | 900 | 0.8% |
| long float | 160 | 0.1% |
| string | 80 | 0.1% |


</details>

### CALL

<details>
<summary> specialization stats for CALL family </summary>

|Kind | Count | Ratio | 
|---|---|---|
| specialization.deferred |    958759360 | 10.8% |
| specialization.deopt |      3536317 | 0.0% |
|          hit |   7696734532 | 87.0% |
|         miss |    187540052 | 2.1% |

#### Specialization attempts

| | Count | Ratio | 
|---|---:|---:|
| Success | 3,581,140 | 89.0% |
| Failure | 444,311 | 11.0% |

|Failure kind | Count | Ratio | 
|---|---:|---:|
| python class | 106,656 | 24.0% |
| meth descr method fastcall keywords | 67,320 | 15.2% |
| kwnames | 57,515 | 12.9% |
| code complex parameters | 50,645 | 11.4% |
| class no vectorcall | 33,729 | 7.6% |
| cfunc varargs keywords | 25,280 | 5.7% |
| class mutable | 24,651 | 5.5% |
| cfunc noargs | 22,835 | 5.1% |
| meth descr varargs | 18,853 | 4.2% |
| other | 9,975 | 2.2% |
| meth descr varargs keywords | 8,144 | 1.8% |
| bound method | 6,808 | 1.5% |
| cmethod | 4,480 | 1.0% |
| cfunc varargs | 3,780 | 0.9% |
| method wrapper | 1,740 | 0.4% |
| str | 1,260 | 0.3% |
| operator wrapper | 640 | 0.1% |


</details>


</details>

## Specialization effectiveness

<details>
<summary> specialization effectiveness </summary>

|Instructions | Count | Ratio | 
|---|---:|---:|
| Basic | 71,143,832,540 | 63.2% |
| Not specialized | 6,735,925,649 | 6.0% |
| Specialized | 34,600,630,329 | 30.8% |

### Deferred by instruction

<details>
<summary> deferred by instruction </summary>

|Name | Count | Ratio | 
|---|---:|---:|
| LOAD_ATTR | 1,338,087,228 | 24.7% |
| BINARY_SUBSCR | 1,116,721,822 | 20.6% |
| CALL | 958,759,360 | 17.7% |
| BINARY_OP | 857,818,215 | 15.8% |
| FOR_ITER | 378,803,256 | 7.0% |
| STORE_SUBSCR | 332,457,161 | 6.1% |
| COMPARE_OP | 224,516,260 | 4.1% |
| COMPARE_AND_BRANCH | 142,556,398 | 2.6% |
| STORE_ATTR | 57,264,223 | 1.1% |
| LOAD_GLOBAL | 14,569,481 | 0.3% |


</details>

### Misses by instruction

<details>
<summary> misses by instruction </summary>

|Name | Count | Ratio | 
|---|---:|---:|
| LOAD_ATTR_INSTANCE_VALUE | 184,405,824 | 17.9% |
| LOAD_ATTR_METHOD_WITH_VALUES | 143,362,070 | 13.9% |
| STORE_ATTR_SLOT | 113,424,018 | 11.0% |
| CALL_PY_EXACT_ARGS | 94,164,509 | 9.2% |
| LOAD_ATTR_SLOT | 86,891,088 | 8.4% |
| FOR_ITER_LIST | 66,547,223 | 6.5% |
| FOR_ITER_TUPLE | 66,180,823 | 6.4% |
| STORE_ATTR_INSTANCE_VALUE | 63,354,359 | 6.2% |
| LOAD_ATTR_METHOD_NO_DICT | 52,259,073 | 5.1% |
| CALL_NO_KW_METHOD_DESCRIPTOR_FAST | 32,833,867 | 3.2% |


</details>


</details>

## Call stats

<details>
<summary> Inlined calls and frame stats </summary>

| | Count | Ratio | 
|---|---:|---:|
| Calls to PyEval_EvalDefault | 1,642,298,388 | 32.5% |
| Calls to Python functions inlined | 3,404,865,291 | 67.5% |
| Calls via PyEval_EvalFrame (total) | 1,642,298,388 | 32.5% |
| Calls via PyEval_EvalFrame (vector) | 870,756,960 | 17.3% |
| Calls via PyEval_EvalFrame (generator) | 771,541,428 | 15.3% |
| Calls via PyEval_EvalFrame (legacy) | 3,964,560 | 0.1% |
| Calls via PyEval_EvalFrame (function vectorcall) | 866,791,080 | 17.2% |
| Calls via PyEval_EvalFrame (build class) | 1,320 | 0.0% |
| Calls via PyEval_EvalFrame (slot) | 206,980,367 | 4.1% |
| Calls via PyEval_EvalFrame (function ex) | 22,166,893 | 0.4% |
| Calls via PyEval_EvalFrame (api) | 171,983,221 | 3.4% |
| Calls via PyEval_EvalFrame (method) | 60,614,702 | 1.2% |
| Frames pushed | 4,147,467,251 | 82.2% |
| Frame objects created | 46,308,794 | 0.9% |


</details>

## Object stats

<details>
<summary> allocations, frees and dict materializatons </summary>

| | Count | Ratio | 
|---|---:|---:|
| Allocations from freelist | 4,987,003,474 | 43.0% |
| Frees to freelist | 4,990,843,747 |  |
| Allocations | 6,617,023,862 | 57.0% |
| Allocations to 512 bytes | 6,540,767,678 | 56.4% |
| Allocations to 4 kbytes | 65,796,634 | 0.6% |
| Allocations over 4 kbytes | 10,459,550 | 0.1% |
| Frees | 6,866,252,280 |  |
| New values | 134,897,363 |  |
| Interpreter increfs | 80,683,650,401 | 67.6% |
| Interpreter decrefs | 92,172,038,250 | 70.9% |
| Increfs | 38,659,001,451 | 32.4% |
| Decrefs | 37,874,987,771 | 29.1% |
| Materialize dict (on request) | 3,699,120 | 2.7% |
| Materialize dict (new key) | 58,320 | 0.0% |
| Materialize dict (too big) | 0 | 0.0% |
| Materialize dict (str subclass) | 0 | 0.0% |
| Method cache hits | 2,050,068,374 |  |
| Method cache misses | 66,588,448 |  |
| Method cache collisions | 73,501,980 |  |
| Method cache dunder hits | 2,481,590,737 |  |
| Method cache dunder misses | 7,167,414 |  |


</details>

## Meta stats

<details>
<summary> Meta statistics </summary>

| | Count | 
|---|---:|
| Number of data files | 8,643 |


</details>

---
Stats gathered on: 2023-02-08
