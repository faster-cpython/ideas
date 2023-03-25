
# Results vs. 3.11.0

- fork: python
- ref: ed7c3ff15680c1939fad
- machine: linux-x86_64
- commit hash: ed7c3ff
- commit date: 2022-09-11
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf2-x86_64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 287 ms: 1.01x faster                                                         |
| html5lib       | 70.2 ms                                                                   | 73.2 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                                 |

Benchmark hidden because not significant (3): chameleon, docutils, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf2-x86_64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.1 ms                                                                   | 89.6 ms: 1.03x faster                                                        |
| float          | 75.7 ms                                                                   | 75.1 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf2-x86_64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 24.3 ms: 1.01x faster                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.29 ms: 1.01x faster                                                        |
| regex_compile  | 154 ms                                                                    | 157 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                     | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf2-x86_64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle               | 9.92 us                                                                   | 9.61 us: 1.03x faster                                                        |
| xml_etree_iterparse  | 106 ms                                                                    | 104 ms: 1.02x faster                                                         |
| pickle_dict          | 31.1 us                                                                   | 30.7 us: 1.01x faster                                                        |
| json_dumps           | 13.4 ms                                                                   | 13.5 ms: 1.01x slower                                                        |
| pickle_pure_python   | 319 us                                                                    | 324 us: 1.01x slower                                                         |
| xml_etree_process    | 55.8 ms                                                                   | 57.0 ms: 1.02x slower                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 80.8 ms: 1.02x slower                                                        |
| unpickle_list        | 4.52 us                                                                   | 4.72 us: 1.04x slower                                                        |
| unpickle_pure_python | 238 us                                                                    | 250 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                                     | 1.01x slower                                                                 |

Benchmark hidden because not significant (4): pickle_list, xml_etree_parse, unpickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf2-x86_64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup | 10.7 ms                                                                   | 10.7 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf2-x86_64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text    | 26.3 ms                                                                   | 26.1 ms: 1.01x faster                                                        |
| genshi_xml     | 57.8 ms                                                                   | 59.2 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.00x slower                                                                 |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf2-x86_64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| gc_traversal            | 4.22 ms                                                                   | 3.63 ms: 1.16x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 27.9 ms: 1.06x faster                                                        |
| thrift                  | 942 us                                                                    | 906 us: 1.04x faster                                                         |
| pickle                  | 9.92 us                                                                   | 9.61 us: 1.03x faster                                                        |
| generators              | 56.0 ms                                                                   | 54.2 ms: 1.03x faster                                                        |
| nbody                   | 92.1 ms                                                                   | 89.6 ms: 1.03x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 517 ms: 1.02x faster                                                         |
| xml_etree_iterparse     | 106 ms                                                                    | 104 ms: 1.02x faster                                                         |
| fannkuch                | 449 ms                                                                    | 441 ms: 1.02x faster                                                         |
| logging_silent          | 103 ns                                                                    | 101 ns: 1.02x faster                                                         |
| pickle_dict             | 31.1 us                                                                   | 30.7 us: 1.01x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.01 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 746 ms: 1.01x faster                                                         |
| 2to3                    | 289 ms                                                                    | 287 ms: 1.01x faster                                                         |
| genshi_text             | 26.3 ms                                                                   | 26.1 ms: 1.01x faster                                                        |
| float                   | 75.7 ms                                                                   | 75.1 ms: 1.01x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 84.3 ms: 1.01x faster                                                        |
| sqlglot_normalize       | 122 ms                                                                    | 121 ms: 1.01x faster                                                         |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                       |
| regex_v8                | 24.4 ms                                                                   | 24.3 ms: 1.01x faster                                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.29 ms: 1.01x faster                                                        |
| mdp                     | 2.73 sec                                                                  | 2.72 sec: 1.00x faster                                                       |
| python_startup          | 10.7 ms                                                                   | 10.7 ms: 1.00x faster                                                        |
| scimark_fft             | 276 ms                                                                    | 277 ms: 1.00x slower                                                         |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.8 ms: 1.00x slower                                                        |
| spectral_norm           | 95.1 ms                                                                   | 95.5 ms: 1.00x slower                                                        |
| sympy_sum               | 182 ms                                                                    | 183 ms: 1.00x slower                                                         |
| gunicorn                | 936 us                                                                    | 941 us: 1.00x slower                                                         |
| scimark_sor             | 109 ms                                                                    | 110 ms: 1.01x slower                                                         |
| sqlalchemy_imperative   | 19.8 ms                                                                   | 19.9 ms: 1.01x slower                                                        |
| dulwich_log             | 69.1 ms                                                                   | 69.6 ms: 1.01x slower                                                        |
| json_dumps              | 13.4 ms                                                                   | 13.5 ms: 1.01x slower                                                        |
| aiohttp                 | 959 us                                                                    | 966 us: 1.01x slower                                                         |
| sympy_expand            | 547 ms                                                                    | 553 ms: 1.01x slower                                                         |
| scimark_monte_carlo     | 67.8 ms                                                                   | 68.7 ms: 1.01x slower                                                        |
| sympy_str               | 333 ms                                                                    | 337 ms: 1.01x slower                                                         |
| pickle_pure_python      | 319 us                                                                    | 324 us: 1.01x slower                                                         |
| raytrace                | 303 ms                                                                    | 307 ms: 1.01x slower                                                         |
| hexiom                  | 7.00 ms                                                                   | 7.12 ms: 1.02x slower                                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.56 ms: 1.02x slower                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 57.0 ms: 1.02x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 80.8 ms: 1.02x slower                                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.92 ms: 1.02x slower                                                        |
| regex_compile           | 154 ms                                                                    | 157 ms: 1.02x slower                                                         |
| meteor_contest          | 129 ms                                                                    | 132 ms: 1.02x slower                                                         |
| genshi_xml              | 57.8 ms                                                                   | 59.2 ms: 1.02x slower                                                        |
| logging_format          | 7.84 us                                                                   | 8.03 us: 1.02x slower                                                        |
| deltablue               | 3.99 ms                                                                   | 4.09 ms: 1.03x slower                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.9 ms: 1.03x slower                                                        |
| telco                   | 6.70 ms                                                                   | 6.88 ms: 1.03x slower                                                        |
| pycparser               | 1.30 sec                                                                  | 1.34 sec: 1.03x slower                                                       |
| pyflate                 | 438 ms                                                                    | 450 ms: 1.03x slower                                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.65 sec: 1.03x slower                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 791 ms: 1.03x slower                                                         |
| async_generators        | 318 ms                                                                    | 328 ms: 1.03x slower                                                         |
| comprehensions          | 24.7 us                                                                   | 25.5 us: 1.03x slower                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.51 us: 1.04x slower                                                        |
| html5lib                | 70.2 ms                                                                   | 73.2 ms: 1.04x slower                                                        |
| unpickle_list           | 4.52 us                                                                   | 4.72 us: 1.04x slower                                                        |
| unpickle_pure_python    | 238 us                                                                    | 250 us: 1.05x slower                                                         |
| deepcopy                | 384 us                                                                    | 407 us: 1.06x slower                                                         |
| chaos                   | 76.2 ms                                                                   | 81.4 ms: 1.07x slower                                                        |
| logging_simple          | 6.95 us                                                                   | 7.43 us: 1.07x slower                                                        |
| go                      | 158 ms                                                                    | 172 ms: 1.09x slower                                                         |
| richards                | 49.1 ms                                                                   | 53.5 ms: 1.09x slower                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 41.0 us: 1.11x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.01x slower                                                                 |

Benchmark hidden because not significant (28): async_tree_memoization, unpack_sequence, pickle_list, xml_etree_parse, pathlib, scimark_lu, flaskblogging, unpickle, json, sqlalchemy_declarative, bench_mp_pool, sqlite_synth, pidigits, regex_dna, python_startup_no_site, json_loads, chameleon, docutils, asyncio_tcp, mako, django_template, nqueens, tornado_http, dask, pylint, create_gc_cycles, mypy2, bench_thread_pool
Ignored benchmarks (1) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: coverage
