
# Results vs. 3.11.0

- fork: python
- ref: 2e91dba437fe5c56c6f8
- machine: linux-x86_64
- commit hash: 2e91dba
- commit date: 2021-12-08
- overall geometric mean: 1.10x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 293 ms: 1.14x slower                                                        |
| chameleon      | 6.52 ms                                                             | 8.85 ms: 1.36x slower                                                       |
| docutils       | 2.59 sec                                                            | 3.02 sec: 1.17x slower                                                      |
| html5lib       | 64.0 ms                                                             | 75.1 ms: 1.17x slower                                                       |
| tornado_http   | 96.7 ms                                                             | 135 ms: 1.39x slower                                                        |
| Geometric mean | (ref)                                                               | 1.24x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 76.0 ms                                                             | 80.9 ms: 1.07x slower                                                       |
| nbody          | 96.7 ms                                                             | 109 ms: 1.12x slower                                                        |
| pidigits       | 197 ms                                                              | 253 ms: 1.28x slower                                                        |
| Geometric mean | (ref)                                                               | 1.15x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.32 ms                                                             | 3.10 ms: 1.07x faster                                                       |
| regex_compile  | 137 ms                                                              | 153 ms: 1.12x slower                                                        |
| regex_v8       | 22.0 ms                                                             | 25.7 ms: 1.17x slower                                                       |
| regex_dna      | 196 ms                                                              | 261 ms: 1.33x slower                                                        |
| Geometric mean | (ref)                                                               | 1.13x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list        | 4.96 us                                                             | 4.53 us: 1.09x faster                                                       |
| xml_etree_parse      | 162 ms                                                              | 155 ms: 1.04x faster                                                        |
| json_loads           | 26.2 us                                                             | 25.3 us: 1.03x faster                                                       |
| xml_etree_iterparse  | 108 ms                                                              | 110 ms: 1.02x slower                                                        |
| pickle               | 9.79 us                                                             | 10.2 us: 1.05x slower                                                       |
| pickle_dict          | 30.9 us                                                             | 33.0 us: 1.07x slower                                                       |
| pickle_list          | 4.03 us                                                             | 4.32 us: 1.07x slower                                                       |
| xml_etree_generate   | 76.5 ms                                                             | 82.8 ms: 1.08x slower                                                       |
| json_dumps           | 12.5 ms                                                             | 14.1 ms: 1.12x slower                                                       |
| xml_etree_process    | 54.1 ms                                                             | 60.9 ms: 1.13x slower                                                       |
| unpickle_pure_python | 228 us                                                              | 265 us: 1.16x slower                                                        |
| pickle_pure_python   | 307 us                                                              | 366 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                               | 1.05x slower                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 10.1 ms: 1.19x slower                                                       |
| python_startup_no_site | 5.98 ms                                                             | 7.14 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                               | 1.19x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 59.7 ms: 1.15x slower                                                       |
| genshi_text     | 21.8 ms                                                             | 28.2 ms: 1.29x slower                                                       |
| mako            | 9.82 ms                                                             | 12.9 ms: 1.31x slower                                                       |
| django_template | 32.9 ms                                                             | 44.9 ms: 1.37x slower                                                       |
| Geometric mean  | (ref)                                                               | 1.28x slower                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| bench_mp_pool           | 24.0 ms                                                             | 4.90 ms: 4.90x faster                                                       |
| generators              | 73.4 ms                                                             | 50.1 ms: 1.47x faster                                                       |
| flaskblogging           | 7.09 ms                                                             | 4.95 ms: 1.43x faster                                                       |
| coverage                | 101 ms                                                              | 72.1 ms: 1.40x faster                                                       |
| async_generators        | 361 ms                                                              | 319 ms: 1.13x faster                                                        |
| gunicorn                | 1.13 ms                                                             | 1.00 ms: 1.13x faster                                                       |
| unpickle_list           | 4.96 us                                                             | 4.53 us: 1.09x faster                                                       |
| regex_effbot            | 3.32 ms                                                             | 3.10 ms: 1.07x faster                                                       |
| unpack_sequence         | 49.5 ns                                                             | 46.3 ns: 1.07x faster                                                       |
| scimark_fft             | 328 ms                                                              | 314 ms: 1.04x faster                                                        |
| xml_etree_parse         | 162 ms                                                              | 155 ms: 1.04x faster                                                        |
| json_loads              | 26.2 us                                                             | 25.3 us: 1.03x faster                                                       |
| scimark_sor             | 115 ms                                                              | 115 ms: 1.01x slower                                                        |
| scimark_lu              | 108 ms                                                              | 110 ms: 1.01x slower                                                        |
| xml_etree_iterparse     | 108 ms                                                              | 110 ms: 1.02x slower                                                        |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.58 ms: 1.03x slower                                                       |
| coroutines              | 26.3 ms                                                             | 27.0 ms: 1.03x slower                                                       |
| async_tree_io           | 1.28 sec                                                            | 1.32 sec: 1.03x slower                                                      |
| async_tree_none         | 525 ms                                                              | 545 ms: 1.04x slower                                                        |
| pickle                  | 9.79 us                                                             | 10.2 us: 1.05x slower                                                       |
| mdp                     | 2.64 sec                                                            | 2.76 sec: 1.05x slower                                                      |
| float                   | 76.0 ms                                                             | 80.9 ms: 1.07x slower                                                       |
| pickle_dict             | 30.9 us                                                             | 33.0 us: 1.07x slower                                                       |
| pickle_list             | 4.03 us                                                             | 4.32 us: 1.07x slower                                                       |
| gc_traversal            | 3.63 ms                                                             | 3.89 ms: 1.07x slower                                                       |
| sqlite_synth            | 2.51 us                                                             | 2.70 us: 1.07x slower                                                       |
| json                    | 4.86 ms                                                             | 5.24 ms: 1.08x slower                                                       |
| telco                   | 6.59 ms                                                             | 7.11 ms: 1.08x slower                                                       |
| xml_etree_generate      | 76.5 ms                                                             | 82.8 ms: 1.08x slower                                                       |
| pathlib                 | 18.2 ms                                                             | 19.9 ms: 1.09x slower                                                       |
| async_tree_cpu_io_mixed | 736 ms                                                              | 811 ms: 1.10x slower                                                        |
| async_tree_memoization  | 621 ms                                                              | 686 ms: 1.10x slower                                                        |
| fannkuch                | 384 ms                                                              | 428 ms: 1.12x slower                                                        |
| regex_compile           | 137 ms                                                              | 153 ms: 1.12x slower                                                        |
| json_dumps              | 12.5 ms                                                             | 14.1 ms: 1.12x slower                                                       |
| create_gc_cycles        | 1.48 ms                                                             | 1.66 ms: 1.12x slower                                                       |
| nbody                   | 96.7 ms                                                             | 109 ms: 1.12x slower                                                        |
| xml_etree_process       | 54.1 ms                                                             | 60.9 ms: 1.13x slower                                                       |
| sympy_sum               | 167 ms                                                              | 189 ms: 1.13x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                             | 76.7 ms: 1.13x slower                                                       |
| deepcopy_memo           | 36.4 us                                                             | 41.5 us: 1.14x slower                                                       |
| 2to3                    | 257 ms                                                              | 293 ms: 1.14x slower                                                        |
| hexiom                  | 6.48 ms                                                             | 7.41 ms: 1.14x slower                                                       |
| dulwich_log             | 63.6 ms                                                             | 73.0 ms: 1.15x slower                                                       |
| chaos                   | 68.0 ms                                                             | 78.3 ms: 1.15x slower                                                       |
| genshi_xml              | 51.8 ms                                                             | 59.7 ms: 1.15x slower                                                       |
| logging_simple          | 6.09 us                                                             | 7.04 us: 1.16x slower                                                       |
| logging_format          | 6.64 us                                                             | 7.70 us: 1.16x slower                                                       |
| unpickle_pure_python    | 228 us                                                              | 265 us: 1.16x slower                                                        |
| docutils                | 2.59 sec                                                            | 3.02 sec: 1.17x slower                                                      |
| regex_v8                | 22.0 ms                                                             | 25.7 ms: 1.17x slower                                                       |
| html5lib                | 64.0 ms                                                             | 75.1 ms: 1.17x slower                                                       |
| logging_silent          | 98.7 ns                                                             | 116 ns: 1.17x slower                                                        |
| pycparser               | 1.14 sec                                                            | 1.35 sec: 1.18x slower                                                      |
| dask                    | 368 ms                                                              | 435 ms: 1.18x slower                                                        |
| pprint_safe_repr        | 701 ms                                                              | 832 ms: 1.19x slower                                                        |
| raytrace                | 292 ms                                                              | 347 ms: 1.19x slower                                                        |
| python_startup          | 8.49 ms                                                             | 10.1 ms: 1.19x slower                                                       |
| pickle_pure_python      | 307 us                                                              | 366 us: 1.19x slower                                                        |
| python_startup_no_site  | 5.98 ms                                                             | 7.14 ms: 1.19x slower                                                       |
| pprint_pformat          | 1.45 sec                                                            | 1.74 sec: 1.20x slower                                                      |
| deepcopy_reduce         | 2.96 us                                                             | 3.55 us: 1.20x slower                                                       |
| sympy_str               | 291 ms                                                              | 350 ms: 1.20x slower                                                        |
| sqlglot_optimize        | 53.4 ms                                                             | 64.7 ms: 1.21x slower                                                       |
| sympy_expand            | 477 ms                                                              | 579 ms: 1.22x slower                                                        |
| meteor_contest          | 106 ms                                                              | 129 ms: 1.22x slower                                                        |
| sqlglot_normalize       | 108 ms                                                              | 133 ms: 1.22x slower                                                        |
| nqueens                 | 84.0 ms                                                             | 103 ms: 1.23x slower                                                        |
| deepcopy                | 339 us                                                              | 418 us: 1.23x slower                                                        |
| richards                | 45.7 ms                                                             | 56.7 ms: 1.24x slower                                                       |
| go                      | 138 ms                                                              | 173 ms: 1.25x slower                                                        |
| sympy_integrate         | 21.0 ms                                                             | 26.5 ms: 1.26x slower                                                       |
| pyflate                 | 414 ms                                                              | 525 ms: 1.27x slower                                                        |
| pidigits                | 197 ms                                                              | 253 ms: 1.28x slower                                                        |
| crypto_pyaes            | 73.8 ms                                                             | 94.7 ms: 1.28x slower                                                       |
| bench_thread_pool       | 820 us                                                              | 1.06 ms: 1.29x slower                                                       |
| genshi_text             | 21.8 ms                                                             | 28.2 ms: 1.29x slower                                                       |
| thrift                  | 766 us                                                              | 995 us: 1.30x slower                                                        |
| deltablue               | 3.66 ms                                                             | 4.78 ms: 1.31x slower                                                       |
| mako                    | 9.82 ms                                                             | 12.9 ms: 1.31x slower                                                       |
| regex_dna               | 196 ms                                                              | 261 ms: 1.33x slower                                                        |
| chameleon               | 6.52 ms                                                             | 8.85 ms: 1.36x slower                                                       |
| django_template         | 32.9 ms                                                             | 44.9 ms: 1.37x slower                                                       |
| comprehensions          | 22.2 us                                                             | 30.6 us: 1.37x slower                                                       |
| tornado_http            | 96.7 ms                                                             | 135 ms: 1.39x slower                                                        |
| sqlglot_transpile       | 1.65 ms                                                             | 2.60 ms: 1.57x slower                                                       |
| sqlglot_parse           | 1.36 ms                                                             | 2.21 ms: 1.62x slower                                                       |
| Geometric mean          | (ref)                                                               | 1.10x slower                                                                |

Benchmark hidden because not significant (2): unpickle, spectral_norm
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, asyncio_tcp, djangocms, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
