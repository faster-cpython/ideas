Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 184 ms: 1.01x slower                                                  |
| chameleon      | 4.61 ms                                                             | 4.75 ms: 1.03x slower                                                 |
| docutils       | 1.46 sec                                                            | 1.45 sec: 1.01x faster                                                |
| html5lib       | 34.7 ms                                                             | 33.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                               | 1.00x faster                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 51.7 ms                                                             | 51.4 ms: 1.01x faster                                                 |
| nbody          | 65.2 ms                                                             | 64.0 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                               | 1.01x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 78.4 ms: 1.03x slower                                                 |
| regex_dna      | 151 ms                                                              | 140 ms: 1.08x faster                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.03 ms: 1.30x faster                                                 |
| regex_v8       | 16.5 ms                                                             | 15.8 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                               | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 7.77 ms: 1.01x slower                                                 |
| json_loads           | 16.1 us                                                             | 16.4 us: 1.01x slower                                                 |
| pickle               | 7.21 us                                                             | 7.17 us: 1.00x faster                                                 |
| pickle_dict          | 17.9 us                                                             | 17.1 us: 1.05x faster                                                 |
| pickle_list          | 2.86 us                                                             | 2.71 us: 1.05x faster                                                 |
| pickle_pure_python   | 200 us                                                              | 212 us: 1.06x slower                                                  |
| unpickle             | 9.68 us                                                             | 9.91 us: 1.02x slower                                                 |
| unpickle_list        | 2.64 us                                                             | 2.61 us: 1.01x faster                                                 |
| unpickle_pure_python | 159 us                                                              | 181 us: 1.14x slower                                                  |
| xml_etree_generate   | 48.4 ms                                                             | 49.0 ms: 1.01x slower                                                 |
| xml_etree_process    | 35.1 ms                                                             | 35.9 ms: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.22 ms: 1.00x slower                                                 |
| python_startup_no_site | 7.24 ms                                                             | 7.24 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.5 ms: 1.02x slower                                                 |
| genshi_xml      | 30.5 ms                                                             | 31.6 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 184 ms: 1.01x slower                                                  |
| aiohttp                 | 1.06 ms                                                             | 1.03 ms: 1.03x faster                                                 |
| async_generators        | 195 ms                                                              | 200 ms: 1.02x slower                                                  |
| async_tree_none         | 281 ms                                                              | 286 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 534 ms: 1.01x slower                                                  |
| async_tree_io           | 696 ms                                                              | 705 ms: 1.01x slower                                                  |
| async_tree_memoization  | 317 ms                                                              | 356 ms: 1.12x slower                                                  |
| chameleon               | 4.61 ms                                                             | 4.75 ms: 1.03x slower                                                 |
| chaos                   | 49.3 ms                                                             | 50.6 ms: 1.03x slower                                                 |
| bench_thread_pool       | 457 us                                                              | 482 us: 1.05x slower                                                  |
| coroutines              | 17.8 ms                                                             | 18.8 ms: 1.06x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                             | 52.1 ms: 1.01x slower                                                 |
| deepcopy_memo           | 26.2 us                                                             | 26.2 us: 1.00x slower                                                 |
| deltablue               | 2.82 ms                                                             | 2.74 ms: 1.03x faster                                                 |
| django_template         | 21.1 ms                                                             | 21.5 ms: 1.02x slower                                                 |
| docutils                | 1.46 sec                                                            | 1.45 sec: 1.01x faster                                                |
| dulwich_log             | 29.1 ms                                                             | 29.5 ms: 1.02x slower                                                 |
| fannkuch                | 262 ms                                                              | 261 ms: 1.00x faster                                                  |
| float                   | 51.7 ms                                                             | 51.4 ms: 1.01x faster                                                 |
| generators              | 28.4 ms                                                             | 28.6 ms: 1.01x slower                                                 |
| genshi_xml              | 30.5 ms                                                             | 31.6 ms: 1.03x slower                                                 |
| go                      | 109 ms                                                              | 110 ms: 1.01x slower                                                  |
| hexiom                  | 4.73 ms                                                             | 4.92 ms: 1.04x slower                                                 |
| html5lib                | 34.7 ms                                                             | 33.2 ms: 1.04x faster                                                 |
| json                    | 2.83 ms                                                             | 2.92 ms: 1.03x slower                                                 |
| json_dumps              | 7.67 ms                                                             | 7.77 ms: 1.01x slower                                                 |
| json_loads              | 16.1 us                                                             | 16.4 us: 1.01x slower                                                 |
| logging_format          | 3.73 us                                                             | 3.90 us: 1.04x slower                                                 |
| logging_simple          | 3.47 us                                                             | 3.60 us: 1.04x slower                                                 |
| mdp                     | 1.54 sec                                                            | 1.56 sec: 1.02x slower                                                |
| meteor_contest          | 73.9 ms                                                             | 76.8 ms: 1.04x slower                                                 |
| nbody                   | 65.2 ms                                                             | 64.0 ms: 1.02x faster                                                 |
| nqueens                 | 59.5 ms                                                             | 60.4 ms: 1.02x slower                                                 |
| pickle                  | 7.21 us                                                             | 7.17 us: 1.00x faster                                                 |
| pickle_dict             | 17.9 us                                                             | 17.1 us: 1.05x faster                                                 |
| pickle_list             | 2.86 us                                                             | 2.71 us: 1.05x faster                                                 |
| pickle_pure_python      | 200 us                                                              | 212 us: 1.06x slower                                                  |
| pprint_safe_repr        | 467 ms                                                              | 470 ms: 1.01x slower                                                  |
| pprint_pformat          | 953 ms                                                              | 966 ms: 1.01x slower                                                  |
| pycparser               | 694 ms                                                              | 709 ms: 1.02x slower                                                  |
| pyflate                 | 313 ms                                                              | 322 ms: 1.03x slower                                                  |
| python_startup          | 9.19 ms                                                             | 9.22 ms: 1.00x slower                                                 |
| python_startup_no_site  | 7.24 ms                                                             | 7.24 ms: 1.00x slower                                                 |
| raytrace                | 207 ms                                                              | 207 ms: 1.00x faster                                                  |
| regex_compile           | 76.3 ms                                                             | 78.4 ms: 1.03x slower                                                 |
| regex_dna               | 151 ms                                                              | 140 ms: 1.08x faster                                                  |
| regex_effbot            | 2.63 ms                                                             | 2.03 ms: 1.30x faster                                                 |
| regex_v8                | 16.5 ms                                                             | 15.8 ms: 1.04x faster                                                 |
| richards                | 32.7 ms                                                             | 33.8 ms: 1.03x slower                                                 |
| scimark_fft             | 201 ms                                                              | 201 ms: 1.00x slower                                                  |
| scimark_lu              | 72.2 ms                                                             | 73.7 ms: 1.02x slower                                                 |
| scimark_monte_carlo     | 46.9 ms                                                             | 48.9 ms: 1.04x slower                                                 |
| scimark_sor             | 83.3 ms                                                             | 79.2 ms: 1.05x faster                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.23 ms: 1.01x slower                                                 |
| spectral_norm           | 72.7 ms                                                             | 71.7 ms: 1.01x faster                                                 |
| sqlalchemy_declarative  | 62.4 ms                                                             | 62.8 ms: 1.01x slower                                                 |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.44 ms: 1.03x slower                                                 |
| sqlglot_parse           | 948 us                                                              | 1.21 ms: 1.28x slower                                                 |
| sqlglot_transpile       | 1.11 ms                                                             | 1.38 ms: 1.24x slower                                                 |
| sqlglot_optimize        | 31.3 ms                                                             | 33.0 ms: 1.05x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 179 ms: 1.05x slower                                                  |
| sqlite_synth            | 1.29 us                                                             | 1.32 us: 1.02x slower                                                 |
| sympy_expand            | 242 ms                                                              | 249 ms: 1.03x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.7 ms: 1.02x slower                                                 |
| sympy_sum               | 85.5 ms                                                             | 83.6 ms: 1.02x faster                                                 |
| sympy_str               | 151 ms                                                              | 153 ms: 1.01x slower                                                  |
| telco                   | 3.39 ms                                                             | 3.41 ms: 1.01x slower                                                 |
| thrift                  | 429 us                                                              | 443 us: 1.03x slower                                                  |
| unpack_sequence         | 33.1 ns                                                             | 32.3 ns: 1.02x faster                                                 |
| unpickle                | 9.68 us                                                             | 9.91 us: 1.02x slower                                                 |
| unpickle_list           | 2.64 us                                                             | 2.61 us: 1.01x faster                                                 |
| unpickle_pure_python    | 159 us                                                              | 181 us: 1.14x slower                                                  |
| xml_etree_generate      | 48.4 ms                                                             | 49.0 ms: 1.01x slower                                                 |
| xml_etree_process       | 35.1 ms                                                             | 35.9 ms: 1.02x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (15): bench_mp_pool, deepcopy, deepcopy_reduce, flaskblogging, genshi_text, gunicorn, logging_silent, mako, mypy, pathlib, pidigits, pylint, tornado_http, xml_etree_parse, xml_etree_iterparse
Ignored benchmarks (1) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: coverage
