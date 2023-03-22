
# Results vs. 3.11.0

- fork: python
- ref: ed7c3ff15680c1939fad
- machine: darwin-arm64
- commit hash: ed7c3ff
- commit date: 2022-09-11
- overall geometric mean: 1.00x faster

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
| nbody          | 65.2 ms                                                             | 65.5 ms: 1.00x slower                                                  |
| float          | 51.7 ms                                                             | 52.9 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                               | 1.01x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 16.5 ms                                                             | 16.4 ms: 1.00x faster                                                  |
| regex_dna      | 151 ms                                                              | 152 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                               | 1.00x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 7.58 ms: 1.01x faster                                                  |
| unpickle_pure_python | 159 us                                                              | 159 us: 1.00x faster                                                   |
| pickle_pure_python   | 200 us                                                              | 199 us: 1.00x faster                                                   |
| xml_etree_generate   | 48.4 ms                                                             | 48.3 ms: 1.00x faster                                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (8): pickle_list, xml_etree_parse, xml_etree_process, xml_etree_iterparse, json_loads, unpickle_list, pickle, unpickle

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
| genshi_xml      | 30.5 ms                                                             | 30.1 ms: 1.01x faster                                                  |
| genshi_text     | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                                  |
| django_template | 21.1 ms                                                             | 21.1 ms: 1.00x slower                                                  |
| Geometric mean  | (ref)                                                               | 1.01x faster                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml              | 30.5 ms                                                             | 30.1 ms: 1.01x faster                                                  |
| json_dumps              | 7.67 ms                                                             | 7.58 ms: 1.01x faster                                                  |
| genshi_text             | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                                  |
| coroutines              | 17.8 ms                                                             | 17.6 ms: 1.01x faster                                                  |
| logging_simple          | 3.47 us                                                             | 3.45 us: 1.00x faster                                                  |
| go                      | 109 ms                                                              | 109 ms: 1.00x faster                                                   |
| dulwich_log             | 29.1 ms                                                             | 29.0 ms: 1.00x faster                                                  |
| async_generators        | 195 ms                                                              | 195 ms: 1.00x faster                                                   |
| unpickle_pure_python    | 159 us                                                              | 159 us: 1.00x faster                                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.5 ms: 1.00x faster                                                  |
| pickle_pure_python      | 200 us                                                              | 199 us: 1.00x faster                                                   |
| scimark_monte_carlo     | 46.9 ms                                                             | 46.8 ms: 1.00x faster                                                  |
| scimark_sor             | 83.3 ms                                                             | 83.0 ms: 1.00x faster                                                  |
| raytrace                | 207 ms                                                              | 207 ms: 1.00x faster                                                   |
| mdp                     | 1.54 sec                                                            | 1.54 sec: 1.00x faster                                                 |
| hexiom                  | 4.73 ms                                                             | 4.72 ms: 1.00x faster                                                  |
| xml_etree_generate      | 48.4 ms                                                             | 48.3 ms: 1.00x faster                                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 31.2 ms: 1.00x faster                                                  |
| regex_v8                | 16.5 ms                                                             | 16.4 ms: 1.00x faster                                                  |
| unpack_sequence         | 33.1 ns                                                             | 33.1 ns: 1.00x slower                                                  |
| regex_dna               | 151 ms                                                              | 152 ms: 1.00x slower                                                   |
| crypto_pyaes            | 51.7 ms                                                             | 51.8 ms: 1.00x slower                                                  |
| pyflate                 | 313 ms                                                              | 313 ms: 1.00x slower                                                   |
| python_startup          | 9.19 ms                                                             | 9.21 ms: 1.00x slower                                                  |
| django_template         | 21.1 ms                                                             | 21.1 ms: 1.00x slower                                                  |
| telco                   | 3.39 ms                                                             | 3.40 ms: 1.00x slower                                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                                  |
| scimark_fft             | 201 ms                                                              | 201 ms: 1.00x slower                                                   |
| fannkuch                | 262 ms                                                              | 263 ms: 1.00x slower                                                   |
| nbody                   | 65.2 ms                                                             | 65.5 ms: 1.00x slower                                                  |
| chameleon               | 4.61 ms                                                             | 4.63 ms: 1.00x slower                                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.27 ms: 1.00x slower                                                  |
| deepcopy_memo           | 26.2 us                                                             | 26.3 us: 1.01x slower                                                  |
| sqlglot_parse           | 948 us                                                              | 953 us: 1.01x slower                                                   |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.24 ms: 1.01x slower                                                  |
| float                   | 51.7 ms                                                             | 52.9 ms: 1.02x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (53): aiohttp, gunicorn, tornado_http, mypy, flaskblogging, pylint, pickle_list, logging_format, xml_etree_parse, mako, deepcopy, thrift, sympy_str, pprint_safe_repr, sympy_expand, spectral_norm, docutils, 2to3, sqlite_synth, regex_effbot, async_tree_none, sqlglot_normalize, xml_etree_process, chaos, sqlalchemy_declarative, sympy_sum, meteor_contest, deltablue, nqueens, pidigits, async_tree_cpu_io_mixed, scimark_lu, json, pprint_pformat, async_tree_memoization, regex_compile, generators, xml_etree_iterparse, json_loads, logging_silent, unpickle_list, sqlglot_transpile, bench_thread_pool, pickle, async_tree_io, deepcopy_reduce, pycparser, html5lib, sqlalchemy_imperative, richards, unpickle, pathlib, bench_mp_pool
Ignored benchmarks (1) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: coverage
