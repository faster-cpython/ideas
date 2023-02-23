
# Results vs. base

- fork: carljm
- ref: inlinecomp2
- machine: linux-x86_64
- commit hash: 9f0fc5b
- commit date: 2023-02-20
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5+-022b44f | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 248 ms: 1.00x faster                                          |
| chameleon      | 6.47 ms                                                                | 6.32 ms: 1.02x faster                                         |
| docutils       | 2.56 sec                                                               | 2.53 sec: 1.01x faster                                        |
| html5lib       | 61.6 ms                                                                | 60.4 ms: 1.02x faster                                         |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5+-022b44f | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 189 ms: 1.04x faster                                          |
| nbody          | 95.4 ms                                                                | 94.0 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5+-022b44f | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_dna      | 211 ms                                                                 | 207 ms: 1.02x faster                                          |
| regex_compile  | 128 ms                                                                 | 127 ms: 1.01x faster                                          |
| regex_v8       | 21.9 ms                                                                | 21.8 ms: 1.00x faster                                         |
| regex_effbot   | 3.46 ms                                                                | 3.69 ms: 1.07x slower                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5+-022b44f | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pickle_list          | 4.09 us                                                                | 3.97 us: 1.03x faster                                         |
| pickle               | 10.3 us                                                                | 10.0 us: 1.03x faster                                         |
| pickle_dict          | 30.6 us                                                                | 30.0 us: 1.02x faster                                         |
| xml_etree_generate   | 80.4 ms                                                                | 80.6 ms: 1.00x slower                                         |
| unpickle_pure_python | 195 us                                                                 | 197 us: 1.01x slower                                          |
| json_dumps           | 9.27 ms                                                                | 9.49 ms: 1.02x slower                                         |
| unpickle             | 13.1 us                                                                | 13.4 us: 1.03x slower                                         |
| unpickle_list        | 5.00 us                                                                | 5.13 us: 1.03x slower                                         |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (5): pickle_pure_python, xml_etree_parse, xml_etree_iterparse, json_loads, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5+-022b44f | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 8.94 ms                                                                | 8.96 ms: 1.00x slower                                         |
| python_startup_no_site | 6.48 ms                                                                | 6.50 ms: 1.00x slower                                         |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5+-022b44f | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| mako           | 9.86 ms                                                                | 9.83 ms: 1.00x faster                                         |
| genshi_xml     | 47.3 ms                                                                | 47.9 ms: 1.01x slower                                         |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark              | bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5+-022b44f | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| mdp                    | 2.67 sec                                                               | 2.48 sec: 1.08x faster                                        |
| async_tree_io          | 1.32 sec                                                               | 1.26 sec: 1.04x faster                                        |
| pidigits               | 197 ms                                                                 | 189 ms: 1.04x faster                                          |
| async_tree_none        | 525 ms                                                                 | 505 ms: 1.04x faster                                          |
| sqlglot_normalize      | 103 ms                                                                 | 99.8 ms: 1.03x faster                                         |
| coroutines             | 22.6 ms                                                                | 21.8 ms: 1.03x faster                                         |
| pickle_list            | 4.09 us                                                                | 3.97 us: 1.03x faster                                         |
| pickle                 | 10.3 us                                                                | 10.0 us: 1.03x faster                                         |
| thrift                 | 763 us                                                                 | 742 us: 1.03x faster                                          |
| sympy_expand           | 455 ms                                                                 | 444 ms: 1.03x faster                                          |
| chaos                  | 65.1 ms                                                                | 63.5 ms: 1.02x faster                                         |
| chameleon              | 6.47 ms                                                                | 6.32 ms: 1.02x faster                                         |
| richards               | 42.2 ms                                                                | 41.3 ms: 1.02x faster                                         |
| pickle_dict            | 30.6 us                                                                | 30.0 us: 1.02x faster                                         |
| html5lib               | 61.6 ms                                                                | 60.4 ms: 1.02x faster                                         |
| pycparser              | 1.13 sec                                                               | 1.11 sec: 1.02x faster                                        |
| sqlglot_optimize       | 50.6 ms                                                                | 49.7 ms: 1.02x faster                                         |
| regex_dna              | 211 ms                                                                 | 207 ms: 1.02x faster                                          |
| hexiom                 | 6.04 ms                                                                | 5.94 ms: 1.02x faster                                         |
| mypy2                  | 332 ms                                                                 | 326 ms: 1.02x faster                                          |
| sqlalchemy_imperative  | 17.8 ms                                                                | 17.5 ms: 1.02x faster                                         |
| gunicorn               | 1.09 ms                                                                | 1.07 ms: 1.02x faster                                         |
| sympy_str              | 282 ms                                                                 | 278 ms: 1.02x faster                                          |
| nbody                  | 95.4 ms                                                                | 94.0 ms: 1.01x faster                                         |
| pyflate                | 404 ms                                                                 | 398 ms: 1.01x faster                                          |
| sympy_sum              | 166 ms                                                                 | 164 ms: 1.01x faster                                          |
| sympy_integrate        | 20.3 ms                                                                | 20.1 ms: 1.01x faster                                         |
| docutils               | 2.56 sec                                                               | 2.53 sec: 1.01x faster                                        |
| logging_simple         | 5.79 us                                                                | 5.73 us: 1.01x faster                                         |
| bench_thread_pool      | 789 us                                                                 | 783 us: 1.01x faster                                          |
| pprint_pformat         | 1.38 sec                                                               | 1.37 sec: 1.01x faster                                        |
| deepcopy               | 330 us                                                                 | 328 us: 1.01x faster                                          |
| scimark_monte_carlo    | 65.1 ms                                                                | 64.7 ms: 1.01x faster                                         |
| regex_compile          | 128 ms                                                                 | 127 ms: 1.01x faster                                          |
| aiohttp                | 1.01 ms                                                                | 1.00 ms: 1.00x faster                                         |
| regex_v8               | 21.9 ms                                                                | 21.8 ms: 1.00x faster                                         |
| coverage               | 96.6 ms                                                                | 96.1 ms: 1.00x faster                                         |
| logging_format         | 6.36 us                                                                | 6.33 us: 1.00x faster                                         |
| pprint_safe_repr       | 674 ms                                                                 | 671 ms: 1.00x faster                                          |
| mako                   | 9.86 ms                                                                | 9.83 ms: 1.00x faster                                         |
| 2to3                   | 248 ms                                                                 | 248 ms: 1.00x faster                                          |
| python_startup         | 8.94 ms                                                                | 8.96 ms: 1.00x slower                                         |
| xml_etree_generate     | 80.4 ms                                                                | 80.6 ms: 1.00x slower                                         |
| python_startup_no_site | 6.48 ms                                                                | 6.50 ms: 1.00x slower                                         |
| crypto_pyaes           | 73.2 ms                                                                | 73.7 ms: 1.01x slower                                         |
| unpickle_pure_python   | 195 us                                                                 | 197 us: 1.01x slower                                          |
| genshi_xml             | 47.3 ms                                                                | 47.9 ms: 1.01x slower                                         |
| deepcopy_reduce        | 2.92 us                                                                | 2.96 us: 1.01x slower                                         |
| async_generators       | 412 ms                                                                 | 417 ms: 1.01x slower                                          |
| dulwich_log            | 62.8 ms                                                                | 63.6 ms: 1.01x slower                                         |
| spectral_norm          | 94.9 ms                                                                | 96.2 ms: 1.01x slower                                         |
| sqlglot_transpile      | 1.70 ms                                                                | 1.72 ms: 1.01x slower                                         |
| nqueens                | 79.1 ms                                                                | 80.3 ms: 1.01x slower                                         |
| deltablue              | 3.11 ms                                                                | 3.16 ms: 1.02x slower                                         |
| pathlib                | 17.9 ms                                                                | 18.3 ms: 1.02x slower                                         |
| unpack_sequence        | 42.1 ns                                                                | 42.9 ns: 1.02x slower                                         |
| scimark_fft            | 303 ms                                                                 | 309 ms: 1.02x slower                                          |
| generators             | 29.3 ms                                                                | 29.9 ms: 1.02x slower                                         |
| sqlglot_parse          | 1.41 ms                                                                | 1.44 ms: 1.02x slower                                         |
| json_dumps             | 9.27 ms                                                                | 9.49 ms: 1.02x slower                                         |
| unpickle               | 13.1 us                                                                | 13.4 us: 1.03x slower                                         |
| unpickle_list          | 5.00 us                                                                | 5.13 us: 1.03x slower                                         |
| scimark_sor            | 104 ms                                                                 | 107 ms: 1.03x slower                                          |
| fannkuch               | 356 ms                                                                 | 368 ms: 1.03x slower                                          |
| regex_effbot           | 3.46 ms                                                                | 3.69 ms: 1.07x slower                                         |
| gc_traversal           | 3.84 ms                                                                | 4.18 ms: 1.09x slower                                         |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (27): async_tree_memoization, logging_silent, meteor_contest, deepcopy_memo, dask, tornado_http, go, django_template, genshi_text, pickle_pure_python, float, create_gc_cycles, bench_mp_pool, xml_etree_parse, djangocms, asyncio_tcp, xml_etree_iterparse, json_loads, xml_etree_process, scimark_sparse_mat_mult, telco, sqlalchemy_declarative, async_tree_cpu_io_mixed, sqlite_synth, scimark_lu, json, raytrace
