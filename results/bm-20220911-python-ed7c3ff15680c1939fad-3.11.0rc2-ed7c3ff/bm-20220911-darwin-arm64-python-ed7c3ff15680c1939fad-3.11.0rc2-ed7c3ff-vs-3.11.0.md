Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| chameleon      | 4.61 ms                                                             | 4.63 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 51.7 ms                                                             | 52.9 ms: 1.02x slower                                                  |
| nbody          | 65.2 ms                                                             | 65.5 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                               | 1.01x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 151 ms                                                              | 152 ms: 1.00x slower                                                   |
| regex_v8       | 16.5 ms                                                             | 16.4 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                               | 1.00x slower                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 7.58 ms: 1.01x faster                                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                                  |
| pickle_pure_python   | 200 us                                                              | 199 us: 1.00x faster                                                   |
| unpickle_pure_python | 159 us                                                              | 159 us: 1.00x faster                                                   |
| xml_etree_generate   | 48.4 ms                                                             | 48.3 ms: 1.00x faster                                                  |
| Geometric mean       | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (8): json_loads, pickle, pickle_list, unpickle, unpickle_list, xml_etree_parse, xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.21 ms: 1.00x slower                                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.27 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                               | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.1 ms: 1.00x slower                                                  |
| genshi_text     | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                                  |
| genshi_xml      | 30.5 ms                                                             | 30.1 ms: 1.01x faster                                                  |
| Geometric mean  | (ref)                                                               | 1.01x faster                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators        | 195 ms                                                              | 195 ms: 1.00x faster                                                   |
| chameleon               | 4.61 ms                                                             | 4.63 ms: 1.00x slower                                                  |
| coroutines              | 17.8 ms                                                             | 17.6 ms: 1.01x faster                                                  |
| crypto_pyaes            | 51.7 ms                                                             | 51.8 ms: 1.00x slower                                                  |
| deepcopy_memo           | 26.2 us                                                             | 26.3 us: 1.01x slower                                                  |
| django_template         | 21.1 ms                                                             | 21.1 ms: 1.00x slower                                                  |
| dulwich_log             | 29.1 ms                                                             | 29.0 ms: 1.00x faster                                                  |
| fannkuch                | 262 ms                                                              | 263 ms: 1.00x slower                                                   |
| float                   | 51.7 ms                                                             | 52.9 ms: 1.02x slower                                                  |
| genshi_text             | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                                  |
| genshi_xml              | 30.5 ms                                                             | 30.1 ms: 1.01x faster                                                  |
| go                      | 109 ms                                                              | 109 ms: 1.00x faster                                                   |
| hexiom                  | 4.73 ms                                                             | 4.72 ms: 1.00x faster                                                  |
| json_dumps              | 7.67 ms                                                             | 7.58 ms: 1.01x faster                                                  |
| logging_simple          | 3.47 us                                                             | 3.45 us: 1.00x faster                                                  |
| mdp                     | 1.54 sec                                                            | 1.54 sec: 1.00x faster                                                 |
| nbody                   | 65.2 ms                                                             | 65.5 ms: 1.00x slower                                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                                  |
| pickle_pure_python      | 200 us                                                              | 199 us: 1.00x faster                                                   |
| pyflate                 | 313 ms                                                              | 313 ms: 1.00x slower                                                   |
| python_startup          | 9.19 ms                                                             | 9.21 ms: 1.00x slower                                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.27 ms: 1.00x slower                                                  |
| raytrace                | 207 ms                                                              | 207 ms: 1.00x faster                                                   |
| regex_dna               | 151 ms                                                              | 152 ms: 1.00x slower                                                   |
| regex_v8                | 16.5 ms                                                             | 16.4 ms: 1.00x faster                                                  |
| scimark_fft             | 201 ms                                                              | 201 ms: 1.00x slower                                                   |
| scimark_monte_carlo     | 46.9 ms                                                             | 46.8 ms: 1.00x faster                                                  |
| scimark_sor             | 83.3 ms                                                             | 83.0 ms: 1.00x faster                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.24 ms: 1.01x slower                                                  |
| sqlglot_parse           | 948 us                                                              | 953 us: 1.01x slower                                                   |
| sqlglot_optimize        | 31.3 ms                                                             | 31.2 ms: 1.00x faster                                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.5 ms: 1.00x faster                                                  |
| telco                   | 3.39 ms                                                             | 3.40 ms: 1.00x slower                                                  |
| unpack_sequence         | 33.1 ns                                                             | 33.1 ns: 1.00x slower                                                  |
| unpickle_pure_python    | 159 us                                                              | 159 us: 1.00x faster                                                   |
| xml_etree_generate      | 48.4 ms                                                             | 48.3 ms: 1.00x faster                                                  |
| Geometric mean          | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (53): 2to3, aiohttp, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, chaos, bench_mp_pool, bench_thread_pool, deepcopy, deepcopy_reduce, deltablue, docutils, flaskblogging, generators, gunicorn, html5lib, json, json_loads, logging_format, logging_silent, mako, meteor_contest, mypy, nqueens, pathlib, pickle, pickle_list, pidigits, pprint_safe_repr, pprint_pformat, pycparser, pylint, regex_compile, regex_effbot, richards, scimark_lu, spectral_norm, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_transpile, sqlglot_normalize, sqlite_synth, sympy_expand, sympy_sum, sympy_str, thrift, tornado_http, unpickle, unpickle_list, xml_etree_parse, xml_etree_iterparse, xml_etree_process
Ignored benchmarks (1) of public/results/bm-20221024-python-deaf509e8fc6e0363bd6-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: coverage
