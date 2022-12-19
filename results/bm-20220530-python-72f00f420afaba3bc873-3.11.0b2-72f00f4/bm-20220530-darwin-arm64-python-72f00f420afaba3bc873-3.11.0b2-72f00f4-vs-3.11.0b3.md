Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 182 ms: 1.00x faster                                                  |
| chameleon      | 4.73 ms                                                               | 4.71 ms: 1.01x faster                                                 |
| docutils       | 1.46 sec                                                              | 1.46 sec: 1.00x faster                                                |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 55.0 ms: 1.01x faster                                                 |
| pidigits       | 282 ms                                                                | 282 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 77.4 ms: 1.00x faster                                                 |
| regex_effbot   | 2.40 ms                                                               | 2.39 ms: 1.00x faster                                                 |
| regex_v8       | 16.8 ms                                                               | 16.6 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|--------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps         | 7.69 ms                                                               | 7.63 ms: 1.01x faster                                                 |
| json_loads         | 16.4 us                                                               | 16.3 us: 1.01x faster                                                 |
| pickle_dict        | 17.6 us                                                               | 17.2 us: 1.02x faster                                                 |
| pickle_list        | 2.73 us                                                               | 2.71 us: 1.01x faster                                                 |
| pickle_pure_python | 222 us                                                                | 223 us: 1.00x slower                                                  |
| unpickle_list      | 2.77 us                                                               | 2.71 us: 1.02x faster                                                 |
| xml_etree_parse    | 99.1 ms                                                               | 99.3 ms: 1.00x slower                                                 |
| xml_etree_generate | 48.0 ms                                                               | 48.2 ms: 1.00x slower                                                 |
| xml_etree_process  | 34.8 ms                                                               | 34.7 ms: 1.00x faster                                                 |
| Geometric mean     | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (4): pickle, unpickle, unpickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.15 ms: 1.01x faster                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.20 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.0 ms: 1.00x faster                                                 |
| genshi_text     | 15.5 ms                                                               | 15.4 ms: 1.01x faster                                                 |
| mako            | 8.44 ms                                                               | 8.38 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 182 ms: 1.00x faster                                                  |
| async_generators        | 197 ms                                                                | 198 ms: 1.00x slower                                                  |
| chameleon               | 4.73 ms                                                               | 4.71 ms: 1.01x faster                                                 |
| chaos                   | 49.5 ms                                                               | 49.4 ms: 1.00x faster                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 51.6 ms: 1.00x faster                                                 |
| deepcopy                | 237 us                                                                | 239 us: 1.00x slower                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 2.05 us: 1.01x slower                                                 |
| deepcopy_memo           | 28.7 us                                                               | 28.5 us: 1.01x faster                                                 |
| deltablue               | 2.83 ms                                                               | 2.84 ms: 1.01x slower                                                 |
| django_template         | 21.0 ms                                                               | 21.0 ms: 1.00x faster                                                 |
| docutils                | 1.46 sec                                                              | 1.46 sec: 1.00x faster                                                |
| fannkuch                | 261 ms                                                                | 260 ms: 1.00x faster                                                  |
| float                   | 55.7 ms                                                               | 55.0 ms: 1.01x faster                                                 |
| generators              | 27.7 ms                                                               | 27.6 ms: 1.00x faster                                                 |
| genshi_text             | 15.5 ms                                                               | 15.4 ms: 1.01x faster                                                 |
| go                      | 106 ms                                                                | 108 ms: 1.01x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.70 ms: 1.00x faster                                                 |
| json_dumps              | 7.69 ms                                                               | 7.63 ms: 1.01x faster                                                 |
| json_loads              | 16.4 us                                                               | 16.3 us: 1.01x faster                                                 |
| logging_silent          | 65.7 ns                                                               | 65.4 ns: 1.00x faster                                                 |
| logging_simple          | 3.44 us                                                               | 3.46 us: 1.01x slower                                                 |
| mako                    | 8.44 ms                                                               | 8.38 ms: 1.01x faster                                                 |
| mdp                     | 1.53 sec                                                              | 1.53 sec: 1.00x slower                                                |
| meteor_contest          | 77.8 ms                                                               | 77.4 ms: 1.00x faster                                                 |
| pathlib                 | 20.8 ms                                                               | 20.6 ms: 1.01x faster                                                 |
| pickle_dict             | 17.6 us                                                               | 17.2 us: 1.02x faster                                                 |
| pickle_list             | 2.73 us                                                               | 2.71 us: 1.01x faster                                                 |
| pickle_pure_python      | 222 us                                                                | 223 us: 1.00x slower                                                  |
| pidigits                | 282 ms                                                                | 282 ms: 1.00x slower                                                  |
| pprint_safe_repr        | 488 ms                                                                | 490 ms: 1.01x slower                                                  |
| pyflate                 | 318 ms                                                                | 316 ms: 1.01x faster                                                  |
| python_startup          | 9.25 ms                                                               | 9.15 ms: 1.01x faster                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.20 ms: 1.01x faster                                                 |
| raytrace                | 208 ms                                                                | 210 ms: 1.01x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 77.4 ms: 1.00x faster                                                 |
| regex_effbot            | 2.40 ms                                                               | 2.39 ms: 1.00x faster                                                 |
| regex_v8                | 16.8 ms                                                               | 16.6 ms: 1.01x faster                                                 |
| richards                | 33.3 ms                                                               | 33.5 ms: 1.01x slower                                                 |
| scimark_fft             | 199 ms                                                                | 200 ms: 1.00x slower                                                  |
| scimark_lu              | 71.8 ms                                                               | 71.4 ms: 1.01x faster                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 48.7 ms: 1.00x faster                                                 |
| scimark_sor             | 77.6 ms                                                               | 75.5 ms: 1.03x faster                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.20 ms: 1.00x faster                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 61.5 ms: 1.00x faster                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.26 ms: 1.00x faster                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 31.4 ms: 1.00x slower                                                 |
| sympy_integrate         | 11.6 ms                                                               | 11.5 ms: 1.00x faster                                                 |
| sympy_str               | 151 ms                                                                | 150 ms: 1.00x faster                                                  |
| telco                   | 3.42 ms                                                               | 3.41 ms: 1.00x faster                                                 |
| thrift                  | 435 us                                                                | 437 us: 1.00x slower                                                  |
| unpack_sequence         | 32.2 ns                                                               | 32.2 ns: 1.00x slower                                                 |
| unpickle_list           | 2.77 us                                                               | 2.71 us: 1.02x faster                                                 |
| xml_etree_parse         | 99.1 ms                                                               | 99.3 ms: 1.00x slower                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 48.2 ms: 1.00x slower                                                 |
| xml_etree_process       | 34.8 ms                                                               | 34.7 ms: 1.00x faster                                                 |
| Geometric mean          | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (33): aiohttp, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, bench_mp_pool, bench_thread_pool, coroutines, dulwich_log, genshi_xml, gunicorn, html5lib, json, logging_format, mypy, nbody, nqueens, pickle, pprint_pformat, pycparser, pylint, regex_dna, spectral_norm, sqlglot_parse, sqlglot_transpile, sqlglot_normalize, sqlite_synth, sympy_expand, sympy_sum, tornado_http, unpickle, unpickle_pure_python, xml_etree_iterparse
Ignored benchmarks (1) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: flaskblogging
