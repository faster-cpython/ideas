
# Results vs. 3.11.0

- fork: python
- ref: 3c67ec394faac79d2608
- machine: darwin-arm64
- commit hash: 3c67ec3
- commit date: 2023-02-07
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 162 ms: 1.01x slower                                                  |
| chameleon      | 4.55 ms                                                             | 4.61 ms: 1.01x slower                                                 |
| docutils       | 1.47 sec                                                            | 1.46 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                               | 1.00x faster                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 65.5 ms                                                             | 64.1 ms: 1.02x faster                                                 |
| float          | 53.0 ms                                                             | 52.1 ms: 1.02x faster                                                 |
| pidigits       | 281 ms                                                              | 281 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                               | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 76.6 ms                                                             | 72.3 ms: 1.06x faster                                                 |
| regex_v8       | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                                 |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.62 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                               | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.10 ms: 1.24x faster                                                 |
| xml_etree_parse      | 106 ms                                                              | 96.4 ms: 1.10x faster                                                 |
| pickle_pure_python   | 198 us                                                              | 192 us: 1.03x faster                                                  |
| pickle_list          | 2.83 us                                                             | 2.76 us: 1.02x faster                                                 |
| unpickle_pure_python | 158 us                                                              | 157 us: 1.01x faster                                                  |
| xml_etree_process    | 35.0 ms                                                             | 34.6 ms: 1.01x faster                                                 |
| xml_etree_generate   | 48.2 ms                                                             | 48.3 ms: 1.00x slower                                                 |
| pickle_dict          | 17.9 us                                                             | 17.9 us: 1.01x slower                                                 |
| json_loads           | 16.0 us                                                             | 16.2 us: 1.01x slower                                                 |
| xml_etree_iterparse  | 69.2 ms                                                             | 70.1 ms: 1.01x slower                                                 |
| unpickle             | 9.66 us                                                             | 9.82 us: 1.02x slower                                                 |
| unpickle_list        | 2.63 us                                                             | 2.68 us: 1.02x slower                                                 |
| pickle               | 7.17 us                                                             | 7.47 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 12.4 ms: 1.01x slower                                                 |
| python_startup_no_site | 10.1 ms                                                             | 10.3 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 8.42 ms                                                             | 7.19 ms: 1.17x faster                                                 |
| genshi_text     | 15.3 ms                                                             | 14.2 ms: 1.08x faster                                                 |
| genshi_xml      | 29.9 ms                                                             | 28.2 ms: 1.06x faster                                                 |
| django_template | 21.1 ms                                                             | 21.1 ms: 1.00x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.07x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp             | 651 ms                                                              | 436 ms: 1.49x faster                                                  |
| json_dumps              | 7.59 ms                                                             | 6.10 ms: 1.24x faster                                                 |
| mako                    | 8.42 ms                                                             | 7.19 ms: 1.17x faster                                                 |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.80 ms: 1.14x faster                                                 |
| xml_etree_parse         | 106 ms                                                              | 96.4 ms: 1.10x faster                                                 |
| hexiom                  | 4.73 ms                                                             | 4.32 ms: 1.10x faster                                                 |
| deltablue               | 2.81 ms                                                             | 2.57 ms: 1.09x faster                                                 |
| richards                | 32.2 ms                                                             | 29.8 ms: 1.08x faster                                                 |
| chaos                   | 49.4 ms                                                             | 45.7 ms: 1.08x faster                                                 |
| genshi_text             | 15.3 ms                                                             | 14.2 ms: 1.08x faster                                                 |
| comprehensions          | 16.1 us                                                             | 15.1 us: 1.07x faster                                                 |
| genshi_xml              | 29.9 ms                                                             | 28.2 ms: 1.06x faster                                                 |
| regex_compile           | 76.6 ms                                                             | 72.3 ms: 1.06x faster                                                 |
| sympy_sum               | 86.0 ms                                                             | 82.1 ms: 1.05x faster                                                 |
| pycparser               | 695 ms                                                              | 664 ms: 1.05x faster                                                  |
| create_gc_cycles        | 722 us                                                              | 695 us: 1.04x faster                                                  |
| scimark_fft             | 200 ms                                                              | 192 ms: 1.04x faster                                                  |
| sympy_str               | 151 ms                                                              | 146 ms: 1.04x faster                                                  |
| sqlalchemy_imperative   | 7.26 ms                                                             | 7.01 ms: 1.04x faster                                                 |
| logging_silent          | 68.0 ns                                                             | 65.8 ns: 1.03x faster                                                 |
| async_tree_memoization  | 338 ms                                                              | 327 ms: 1.03x faster                                                  |
| pickle_pure_python      | 198 us                                                              | 192 us: 1.03x faster                                                  |
| nqueens                 | 62.4 ms                                                             | 60.6 ms: 1.03x faster                                                 |
| coverage                | 58.4 ms                                                             | 56.8 ms: 1.03x faster                                                 |
| pathlib                 | 28.3 ms                                                             | 27.5 ms: 1.03x faster                                                 |
| sympy_integrate         | 11.5 ms                                                             | 11.2 ms: 1.03x faster                                                 |
| regex_v8                | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                                 |
| pickle_list             | 2.83 us                                                             | 2.76 us: 1.02x faster                                                 |
| unpack_sequence         | 33.5 ns                                                             | 32.7 ns: 1.02x faster                                                 |
| bench_thread_pool       | 474 us                                                              | 463 us: 1.02x faster                                                  |
| nbody                   | 65.5 ms                                                             | 64.1 ms: 1.02x faster                                                 |
| float                   | 53.0 ms                                                             | 52.1 ms: 1.02x faster                                                 |
| scimark_lu              | 72.2 ms                                                             | 70.9 ms: 1.02x faster                                                 |
| fannkuch                | 260 ms                                                              | 256 ms: 1.02x faster                                                  |
| deepcopy                | 224 us                                                              | 220 us: 1.02x faster                                                  |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| deepcopy_memo           | 26.3 us                                                             | 26.0 us: 1.01x faster                                                 |
| unpickle_pure_python    | 158 us                                                              | 157 us: 1.01x faster                                                  |
| xml_etree_process       | 35.0 ms                                                             | 34.6 ms: 1.01x faster                                                 |
| dulwich_log             | 29.7 ms                                                             | 29.4 ms: 1.01x faster                                                 |
| mdp                     | 1.54 sec                                                            | 1.53 sec: 1.01x faster                                                |
| docutils                | 1.47 sec                                                            | 1.46 sec: 1.01x faster                                                |
| regex_effbot            | 2.63 ms                                                             | 2.62 ms: 1.00x faster                                                 |
| pidigits                | 281 ms                                                              | 281 ms: 1.00x slower                                                  |
| sqlglot_normalize       | 171 ms                                                              | 172 ms: 1.00x slower                                                  |
| django_template         | 21.1 ms                                                             | 21.1 ms: 1.00x slower                                                 |
| xml_etree_generate      | 48.2 ms                                                             | 48.3 ms: 1.00x slower                                                 |
| go                      | 109 ms                                                              | 110 ms: 1.00x slower                                                  |
| gc_traversal            | 2.41 ms                                                             | 2.42 ms: 1.00x slower                                                 |
| pickle_dict             | 17.9 us                                                             | 17.9 us: 1.01x slower                                                 |
| sqlalchemy_declarative  | 62.6 ms                                                             | 62.9 ms: 1.01x slower                                                 |
| python_startup          | 12.3 ms                                                             | 12.4 ms: 1.01x slower                                                 |
| json                    | 2.77 ms                                                             | 2.79 ms: 1.01x slower                                                 |
| sqlglot_optimize        | 31.2 ms                                                             | 31.4 ms: 1.01x slower                                                 |
| 2to3                    | 161 ms                                                              | 162 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed | 534 ms                                                              | 538 ms: 1.01x slower                                                  |
| json_loads              | 16.0 us                                                             | 16.2 us: 1.01x slower                                                 |
| telco                   | 3.40 ms                                                             | 3.43 ms: 1.01x slower                                                 |
| deepcopy_reduce         | 1.91 us                                                             | 1.93 us: 1.01x slower                                                 |
| chameleon               | 4.55 ms                                                             | 4.61 ms: 1.01x slower                                                 |
| pprint_safe_repr        | 463 ms                                                              | 469 ms: 1.01x slower                                                  |
| xml_etree_iterparse     | 69.2 ms                                                             | 70.1 ms: 1.01x slower                                                 |
| unpickle                | 9.66 us                                                             | 9.82 us: 1.02x slower                                                 |
| pprint_pformat          | 946 ms                                                              | 963 ms: 1.02x slower                                                  |
| crypto_pyaes            | 51.8 ms                                                             | 52.8 ms: 1.02x slower                                                 |
| bench_mp_pool           | 43.8 ms                                                             | 44.6 ms: 1.02x slower                                                 |
| unpickle_list           | 2.63 us                                                             | 2.68 us: 1.02x slower                                                 |
| python_startup_no_site  | 10.1 ms                                                             | 10.3 ms: 1.02x slower                                                 |
| thrift                  | 431 us                                                              | 442 us: 1.02x slower                                                  |
| async_generators        | 195 ms                                                              | 200 ms: 1.03x slower                                                  |
| scimark_sor             | 82.9 ms                                                             | 85.3 ms: 1.03x slower                                                 |
| meteor_contest          | 73.3 ms                                                             | 75.6 ms: 1.03x slower                                                 |
| logging_format          | 3.77 us                                                             | 3.91 us: 1.04x slower                                                 |
| logging_simple          | 3.49 us                                                             | 3.64 us: 1.04x slower                                                 |
| pickle                  | 7.17 us                                                             | 7.47 us: 1.04x slower                                                 |
| async_tree_io           | 707 ms                                                              | 742 ms: 1.05x slower                                                  |
| coroutines              | 17.7 ms                                                             | 18.8 ms: 1.06x slower                                                 |
| sqlglot_transpile       | 1.12 ms                                                             | 1.19 ms: 1.06x slower                                                 |
| sqlite_synth            | 1.28 us                                                             | 1.37 us: 1.07x slower                                                 |
| sqlglot_parse           | 956 us                                                              | 1.02 ms: 1.07x slower                                                 |
| raytrace                | 207 ms                                                              | 221 ms: 1.07x slower                                                  |
| pyflate                 | 309 ms                                                              | 331 ms: 1.07x slower                                                  |
| scimark_monte_carlo     | 46.5 ms                                                             | 50.0 ms: 1.08x slower                                                 |
| generators              | 28.6 ms                                                             | 34.3 ms: 1.20x slower                                                 |
| dask                    | 226 ms                                                              | 323 ms: 1.43x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.01x faster                                                          |

Benchmark hidden because not significant (6): tornado_http, async_tree_none, html5lib, spectral_norm, sympy_expand, mypy2
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint
