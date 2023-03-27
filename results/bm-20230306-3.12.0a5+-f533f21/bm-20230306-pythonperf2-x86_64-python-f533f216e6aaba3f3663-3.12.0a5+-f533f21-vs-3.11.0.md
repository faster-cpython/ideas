
# Results vs. 3.11.0

- fork: python
- ref: f533f216e6aaba3f3663
- machine: linux-x86_64
- commit hash: f533f21
- commit date: 2023-03-06
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 284 ms: 1.02x faster                                                         |
| chameleon      | 7.50 ms                                                                   | 7.24 ms: 1.04x faster                                                        |
| docutils       | 2.86 sec                                                                  | 2.81 sec: 1.02x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 66.8 ms: 1.05x faster                                                        |
| tornado_http   | 125 ms                                                                    | 116 ms: 1.08x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 73.5 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                    | 148 ms: 1.04x faster                                                         |
| regex_v8       | 24.4 ms                                                                   | 24.1 ms: 1.02x faster                                                        |
| regex_dna      | 225 ms                                                                    | 232 ms: 1.03x slower                                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.62 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.2 ms: 1.31x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.0 us: 1.19x faster                                                        |
| unpickle_pure_python | 238 us                                                                    | 202 us: 1.18x faster                                                         |
| xml_etree_parse      | 161 ms                                                                    | 143 ms: 1.12x faster                                                         |
| pickle_pure_python   | 319 us                                                                    | 305 us: 1.05x faster                                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 104 ms: 1.01x faster                                                         |
| pickle_list          | 3.78 us                                                                   | 3.85 us: 1.02x slower                                                        |
| pickle               | 9.92 us                                                                   | 10.2 us: 1.02x slower                                                        |
| xml_etree_process    | 55.8 ms                                                                   | 57.4 ms: 1.03x slower                                                        |
| pickle_dict          | 31.1 us                                                                   | 32.2 us: 1.03x slower                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 83.5 ms: 1.06x slower                                                        |
| unpickle             | 13.0 us                                                                   | 13.8 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.04x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.3 ms: 1.05x slower                                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.34 ms: 1.08x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.07x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|-----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| genshi_xml      | 57.8 ms                                                                   | 54.9 ms: 1.05x faster                                                        |
| genshi_text     | 26.3 ms                                                                   | 25.5 ms: 1.03x faster                                                        |
| django_template | 39.6 ms                                                                   | 39.1 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                                     | 1.04x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 386 ms: 1.95x faster                                                         |
| generators              | 56.0 ms                                                                   | 38.2 ms: 1.47x faster                                                        |
| json_dumps              | 13.4 ms                                                                   | 10.2 ms: 1.31x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 24.8 ms: 1.19x faster                                                        |
| deltablue               | 3.99 ms                                                                   | 3.35 ms: 1.19x faster                                                        |
| mypy2                   | 446 ms                                                                    | 375 ms: 1.19x faster                                                         |
| json_loads              | 28.4 us                                                                   | 24.0 us: 1.19x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 202 us: 1.18x faster                                                         |
| json                    | 5.59 ms                                                                   | 4.97 ms: 1.12x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 143 ms: 1.12x faster                                                         |
| richards                | 49.1 ms                                                                   | 44.0 ms: 1.12x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 103 ms: 1.10x faster                                                         |
| tornado_http            | 125 ms                                                                    | 116 ms: 1.08x faster                                                         |
| dulwich_log             | 69.1 ms                                                                   | 64.3 ms: 1.07x faster                                                        |
| logging_silent          | 103 ns                                                                    | 95.6 ns: 1.07x faster                                                        |
| fannkuch                | 449 ms                                                                    | 419 ms: 1.07x faster                                                         |
| mako                    | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| hexiom                  | 7.00 ms                                                                   | 6.55 ms: 1.07x faster                                                        |
| genshi_xml              | 57.8 ms                                                                   | 54.9 ms: 1.05x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.45 us: 1.05x faster                                                        |
| async_tree_memoization  | 639 ms                                                                    | 607 ms: 1.05x faster                                                         |
| html5lib                | 70.2 ms                                                                   | 66.8 ms: 1.05x faster                                                        |
| pickle_pure_python      | 319 us                                                                    | 305 us: 1.05x faster                                                         |
| logging_simple          | 6.95 us                                                                   | 6.66 us: 1.04x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 507 ms: 1.04x faster                                                         |
| regex_compile           | 154 ms                                                                    | 148 ms: 1.04x faster                                                         |
| coverage                | 86.0 ms                                                                   | 82.8 ms: 1.04x faster                                                        |
| pathlib                 | 19.2 ms                                                                   | 18.5 ms: 1.04x faster                                                        |
| chameleon               | 7.50 ms                                                                   | 7.24 ms: 1.04x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 82.3 ms: 1.03x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 35.8 us: 1.03x faster                                                        |
| pycparser               | 1.30 sec                                                                  | 1.26 sec: 1.03x faster                                                       |
| mdp                     | 2.73 sec                                                                  | 2.64 sec: 1.03x faster                                                       |
| go                      | 158 ms                                                                    | 153 ms: 1.03x faster                                                         |
| float                   | 75.7 ms                                                                   | 73.5 ms: 1.03x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 25.5 ms: 1.03x faster                                                        |
| chaos                   | 76.2 ms                                                                   | 74.1 ms: 1.03x faster                                                        |
| raytrace                | 303 ms                                                                    | 295 ms: 1.03x faster                                                         |
| bench_thread_pool       | 990 us                                                                    | 965 us: 1.03x faster                                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.57 sec: 1.02x faster                                                       |
| sympy_expand            | 547 ms                                                                    | 535 ms: 1.02x faster                                                         |
| scimark_sor             | 109 ms                                                                    | 107 ms: 1.02x faster                                                         |
| sqlglot_normalize       | 122 ms                                                                    | 120 ms: 1.02x faster                                                         |
| unpack_sequence         | 45.9 ns                                                                   | 45.0 ns: 1.02x faster                                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.16 sec: 1.02x faster                                                       |
| 2to3                    | 289 ms                                                                    | 284 ms: 1.02x faster                                                         |
| regex_v8                | 24.4 ms                                                                   | 24.1 ms: 1.02x faster                                                        |
| docutils                | 2.86 sec                                                                  | 2.81 sec: 1.02x faster                                                       |
| sympy_integrate         | 25.3 ms                                                                   | 24.9 ms: 1.01x faster                                                        |
| django_template         | 39.6 ms                                                                   | 39.1 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 744 ms: 1.01x faster                                                         |
| xml_etree_iterparse     | 106 ms                                                                    | 104 ms: 1.01x faster                                                         |
| spectral_norm           | 95.1 ms                                                                   | 94.0 ms: 1.01x faster                                                        |
| pyflate                 | 438 ms                                                                    | 435 ms: 1.01x faster                                                         |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.2 ms: 1.01x faster                                                        |
| pprint_safe_repr        | 768 ms                                                                    | 764 ms: 1.01x faster                                                         |
| meteor_contest          | 129 ms                                                                    | 129 ms: 1.00x faster                                                         |
| sympy_str               | 333 ms                                                                    | 332 ms: 1.00x faster                                                         |
| gc_traversal            | 4.22 ms                                                                   | 4.26 ms: 1.01x slower                                                        |
| deepcopy                | 384 us                                                                    | 390 us: 1.02x slower                                                         |
| pickle_list             | 3.78 us                                                                   | 3.85 us: 1.02x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 282 ms: 1.02x slower                                                         |
| sympy_sum               | 182 ms                                                                    | 186 ms: 1.02x slower                                                         |
| create_gc_cycles        | 1.65 ms                                                                   | 1.68 ms: 1.02x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 69.4 ms: 1.02x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.2 us: 1.02x slower                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 57.4 ms: 1.03x slower                                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.58 ms: 1.03x slower                                                        |
| thrift                  | 942 us                                                                    | 972 us: 1.03x slower                                                         |
| regex_dna               | 225 ms                                                                    | 232 ms: 1.03x slower                                                         |
| telco                   | 6.70 ms                                                                   | 6.92 ms: 1.03x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 32.2 us: 1.03x slower                                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.95 ms: 1.04x slower                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.26 ms: 1.05x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.62 us: 1.05x slower                                                        |
| python_startup          | 10.7 ms                                                                   | 11.3 ms: 1.05x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 83.5 ms: 1.06x slower                                                        |
| unpickle                | 13.0 us                                                                   | 13.8 us: 1.06x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 26.4 us: 1.07x slower                                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 4.87 ms: 1.07x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.34 ms: 1.08x slower                                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.62 ms: 1.09x slower                                                        |
| async_generators        | 318 ms                                                                    | 389 ms: 1.22x slower                                                         |
| dask                    | 418 ms                                                                    | 566 ms: 1.35x slower                                                         |
| Geometric mean          | (ref)                                                                     | 1.03x faster                                                                 |

Benchmark hidden because not significant (5): nbody, nqueens, unpickle_list, pidigits, deepcopy_reduce
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
