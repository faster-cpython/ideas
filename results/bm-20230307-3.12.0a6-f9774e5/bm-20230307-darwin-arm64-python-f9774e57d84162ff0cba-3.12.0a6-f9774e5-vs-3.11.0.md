
# Results vs. 3.11.0

- fork: python
- ref: f9774e57d84162ff0cba
- machine: darwin-arm64
- commit hash: f9774e5
- commit date: 2023-03-07
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 165 ms: 1.02x slower                                                  |
| chameleon      | 4.55 ms                                                             | 4.48 ms: 1.01x faster                                                 |
| docutils       | 1.47 sec                                                            | 1.49 sec: 1.01x slower                                                |
| html5lib       | 34.8 ms                                                             | 35.4 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                               | 1.00x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 281 ms                                                              | 281 ms: 1.00x slower                                                  |
| nbody          | 65.5 ms                                                             | 66.1 ms: 1.01x slower                                                 |
| float          | 53.0 ms                                                             | 53.5 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                               | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 76.6 ms                                                             | 75.4 ms: 1.02x faster                                                 |
| regex_v8       | 16.1 ms                                                             | 16.2 ms: 1.01x slower                                                 |
| regex_dna      | 151 ms                                                              | 153 ms: 1.01x slower                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.69 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                               | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.18 ms: 1.23x faster                                                 |
| unpickle_pure_python | 158 us                                                              | 145 us: 1.09x faster                                                  |
| xml_etree_parse      | 106 ms                                                              | 97.9 ms: 1.08x faster                                                 |
| pickle_pure_python   | 198 us                                                              | 191 us: 1.04x faster                                                  |
| json_loads           | 16.0 us                                                             | 16.1 us: 1.00x slower                                                 |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.01x slower                                                 |
| unpickle_list        | 2.63 us                                                             | 2.65 us: 1.01x slower                                                 |
| xml_etree_iterparse  | 69.2 ms                                                             | 71.1 ms: 1.03x slower                                                 |
| pickle               | 7.17 us                                                             | 7.47 us: 1.04x slower                                                 |
| xml_etree_process    | 35.0 ms                                                             | 37.0 ms: 1.06x slower                                                 |
| xml_etree_generate   | 48.2 ms                                                             | 51.1 ms: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                          |

Benchmark hidden because not significant (2): pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 12.5 ms: 1.01x slower                                                 |
| python_startup_no_site | 10.1 ms                                                             | 10.4 ms: 1.03x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 8.42 ms                                                             | 7.44 ms: 1.13x faster                                                 |
| genshi_text     | 15.3 ms                                                             | 14.7 ms: 1.04x faster                                                 |
| genshi_xml      | 29.9 ms                                                             | 29.2 ms: 1.02x faster                                                 |
| django_template | 21.1 ms                                                             | 21.6 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp             | 651 ms                                                              | 473 ms: 1.38x faster                                                  |
| json_dumps              | 7.59 ms                                                             | 6.18 ms: 1.23x faster                                                 |
| mako                    | 8.42 ms                                                             | 7.44 ms: 1.13x faster                                                 |
| unpickle_pure_python    | 158 us                                                              | 145 us: 1.09x faster                                                  |
| deltablue               | 2.81 ms                                                             | 2.59 ms: 1.09x faster                                                 |
| xml_etree_parse         | 106 ms                                                              | 97.9 ms: 1.08x faster                                                 |
| hexiom                  | 4.73 ms                                                             | 4.46 ms: 1.06x faster                                                 |
| richards                | 32.2 ms                                                             | 30.5 ms: 1.06x faster                                                 |
| genshi_text             | 15.3 ms                                                             | 14.7 ms: 1.04x faster                                                 |
| pickle_pure_python      | 198 us                                                              | 191 us: 1.04x faster                                                  |
| chaos                   | 49.4 ms                                                             | 47.8 ms: 1.03x faster                                                 |
| mdp                     | 1.54 sec                                                            | 1.50 sec: 1.03x faster                                                |
| pycparser               | 695 ms                                                              | 674 ms: 1.03x faster                                                  |
| pathlib                 | 28.3 ms                                                             | 27.5 ms: 1.03x faster                                                 |
| create_gc_cycles        | 722 us                                                              | 702 us: 1.03x faster                                                  |
| generators              | 28.6 ms                                                             | 27.9 ms: 1.03x faster                                                 |
| genshi_xml              | 29.9 ms                                                             | 29.2 ms: 1.02x faster                                                 |
| scimark_fft             | 200 ms                                                              | 196 ms: 1.02x faster                                                  |
| unpack_sequence         | 33.5 ns                                                             | 32.9 ns: 1.02x faster                                                 |
| regex_compile           | 76.6 ms                                                             | 75.4 ms: 1.02x faster                                                 |
| chameleon               | 4.55 ms                                                             | 4.48 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 3.17 ms: 1.01x faster                                                 |
| sqlalchemy_imperative   | 7.26 ms                                                             | 7.21 ms: 1.01x faster                                                 |
| fannkuch                | 260 ms                                                              | 258 ms: 1.01x faster                                                  |
| deepcopy                | 224 us                                                              | 222 us: 1.01x faster                                                  |
| meteor_contest          | 73.3 ms                                                             | 72.9 ms: 1.01x faster                                                 |
| dulwich_log             | 29.7 ms                                                             | 29.6 ms: 1.01x faster                                                 |
| bench_thread_pool       | 474 us                                                              | 472 us: 1.00x faster                                                  |
| pidigits                | 281 ms                                                              | 281 ms: 1.00x slower                                                  |
| json_loads              | 16.0 us                                                             | 16.1 us: 1.00x slower                                                 |
| deepcopy_memo           | 26.3 us                                                             | 26.4 us: 1.00x slower                                                 |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.01x slower                                                 |
| regex_v8                | 16.1 ms                                                             | 16.2 ms: 1.01x slower                                                 |
| unpickle_list           | 2.63 us                                                             | 2.65 us: 1.01x slower                                                 |
| gc_traversal            | 2.41 ms                                                             | 2.43 ms: 1.01x slower                                                 |
| nbody                   | 65.5 ms                                                             | 66.1 ms: 1.01x slower                                                 |
| float                   | 53.0 ms                                                             | 53.5 ms: 1.01x slower                                                 |
| python_startup          | 12.3 ms                                                             | 12.5 ms: 1.01x slower                                                 |
| regex_dna               | 151 ms                                                              | 153 ms: 1.01x slower                                                  |
| go                      | 109 ms                                                              | 111 ms: 1.01x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.7 ms: 1.01x slower                                                 |
| docutils                | 1.47 sec                                                            | 1.49 sec: 1.01x slower                                                |
| async_tree_none         | 285 ms                                                              | 289 ms: 1.02x slower                                                  |
| html5lib                | 34.8 ms                                                             | 35.4 ms: 1.02x slower                                                 |
| sympy_expand            | 243 ms                                                              | 248 ms: 1.02x slower                                                  |
| logging_silent          | 68.0 ns                                                             | 69.3 ns: 1.02x slower                                                 |
| sqlalchemy_declarative  | 62.6 ms                                                             | 63.8 ms: 1.02x slower                                                 |
| sympy_str               | 151 ms                                                              | 155 ms: 1.02x slower                                                  |
| 2to3                    | 161 ms                                                              | 165 ms: 1.02x slower                                                  |
| sqlglot_normalize       | 171 ms                                                              | 175 ms: 1.02x slower                                                  |
| coverage                | 58.4 ms                                                             | 59.6 ms: 1.02x slower                                                 |
| coroutines              | 17.7 ms                                                             | 18.1 ms: 1.02x slower                                                 |
| regex_effbot            | 2.63 ms                                                             | 2.69 ms: 1.02x slower                                                 |
| deepcopy_reduce         | 1.91 us                                                             | 1.95 us: 1.02x slower                                                 |
| async_tree_cpu_io_mixed | 534 ms                                                              | 547 ms: 1.02x slower                                                  |
| pprint_pformat          | 946 ms                                                              | 970 ms: 1.02x slower                                                  |
| sympy_sum               | 86.0 ms                                                             | 88.2 ms: 1.02x slower                                                 |
| django_template         | 21.1 ms                                                             | 21.6 ms: 1.03x slower                                                 |
| telco                   | 3.40 ms                                                             | 3.49 ms: 1.03x slower                                                 |
| xml_etree_iterparse     | 69.2 ms                                                             | 71.1 ms: 1.03x slower                                                 |
| scimark_lu              | 72.2 ms                                                             | 74.2 ms: 1.03x slower                                                 |
| pprint_safe_repr        | 463 ms                                                              | 477 ms: 1.03x slower                                                  |
| sqlglot_optimize        | 31.2 ms                                                             | 32.1 ms: 1.03x slower                                                 |
| python_startup_no_site  | 10.1 ms                                                             | 10.4 ms: 1.03x slower                                                 |
| crypto_pyaes            | 51.8 ms                                                             | 53.5 ms: 1.03x slower                                                 |
| spectral_norm           | 72.5 ms                                                             | 74.9 ms: 1.03x slower                                                 |
| pickle                  | 7.17 us                                                             | 7.47 us: 1.04x slower                                                 |
| logging_simple          | 3.49 us                                                             | 3.66 us: 1.05x slower                                                 |
| logging_format          | 3.77 us                                                             | 3.95 us: 1.05x slower                                                 |
| thrift                  | 431 us                                                              | 453 us: 1.05x slower                                                  |
| async_tree_io           | 707 ms                                                              | 744 ms: 1.05x slower                                                  |
| xml_etree_process       | 35.0 ms                                                             | 37.0 ms: 1.06x slower                                                 |
| scimark_sor             | 82.9 ms                                                             | 87.7 ms: 1.06x slower                                                 |
| xml_etree_generate      | 48.2 ms                                                             | 51.1 ms: 1.06x slower                                                 |
| bench_mp_pool           | 43.8 ms                                                             | 46.5 ms: 1.06x slower                                                 |
| sqlite_synth            | 1.28 us                                                             | 1.37 us: 1.07x slower                                                 |
| pyflate                 | 309 ms                                                              | 331 ms: 1.07x slower                                                  |
| sqlglot_transpile       | 1.12 ms                                                             | 1.22 ms: 1.09x slower                                                 |
| scimark_monte_carlo     | 46.5 ms                                                             | 51.0 ms: 1.10x slower                                                 |
| sqlglot_parse           | 956 us                                                              | 1.05 ms: 1.10x slower                                                 |
| comprehensions          | 16.1 us                                                             | 17.7 us: 1.10x slower                                                 |
| raytrace                | 207 ms                                                              | 229 ms: 1.11x slower                                                  |
| async_generators        | 195 ms                                                              | 272 ms: 1.39x slower                                                  |
| dask                    | 226 ms                                                              | 325 ms: 1.44x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (7): tornado_http, async_tree_memoization, pickle_list, unpickle, json, nqueens, mypy2
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint
