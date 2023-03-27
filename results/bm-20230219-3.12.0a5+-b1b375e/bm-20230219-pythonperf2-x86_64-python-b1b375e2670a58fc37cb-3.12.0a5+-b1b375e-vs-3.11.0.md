
# Results vs. 3.11.0

- fork: python
- ref: b1b375e2670a58fc37cb
- machine: linux-x86_64
- commit hash: b1b375e
- commit date: 2023-02-19
- overall geometric mean: 1.05x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf2-x86_64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 279 ms: 1.04x faster                                                         |
| chameleon      | 7.50 ms                                                                   | 7.14 ms: 1.05x faster                                                        |
| docutils       | 2.86 sec                                                                  | 2.80 sec: 1.02x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 68.0 ms: 1.03x faster                                                        |
| tornado_http   | 125 ms                                                                    | 117 ms: 1.07x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf2-x86_64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 70.9 ms: 1.07x faster                                                        |
| nbody          | 92.1 ms                                                                   | 90.4 ms: 1.02x faster                                                        |
| pidigits       | 252 ms                                                                    | 252 ms: 1.00x slower                                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf2-x86_64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                    | 142 ms: 1.08x faster                                                         |
| regex_v8       | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.42 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf2-x86_64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.2 ms: 1.31x faster                                                        |
| json_loads           | 28.4 us                                                                   | 23.9 us: 1.19x faster                                                        |
| unpickle_pure_python | 238 us                                                                    | 206 us: 1.15x faster                                                         |
| xml_etree_parse      | 161 ms                                                                    | 141 ms: 1.14x faster                                                         |
| pickle_pure_python   | 319 us                                                                    | 305 us: 1.05x faster                                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 101 ms: 1.04x faster                                                         |
| unpickle_list        | 4.52 us                                                                   | 4.44 us: 1.02x faster                                                        |
| unpickle             | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                        |
| xml_etree_process    | 55.8 ms                                                                   | 57.1 ms: 1.02x slower                                                        |
| pickle               | 9.92 us                                                                   | 10.3 us: 1.03x slower                                                        |
| pickle_dict          | 31.1 us                                                                   | 32.3 us: 1.04x slower                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 83.2 ms: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.05x faster                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf2-x86_64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.2 ms: 1.05x slower                                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.28 ms: 1.07x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.06x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf2-x86_64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.9 ms                                                                   | 9.92 ms: 1.10x faster                                                        |
| genshi_xml      | 57.8 ms                                                                   | 53.6 ms: 1.08x faster                                                        |
| genshi_text     | 26.3 ms                                                                   | 24.7 ms: 1.06x faster                                                        |
| django_template | 39.6 ms                                                                   | 38.3 ms: 1.03x faster                                                        |
| Geometric mean  | (ref)                                                                     | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf2-x86_64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 386 ms: 1.95x faster                                                         |
| generators              | 56.0 ms                                                                   | 39.9 ms: 1.40x faster                                                        |
| json_dumps              | 13.4 ms                                                                   | 10.2 ms: 1.31x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 24.0 ms: 1.23x faster                                                        |
| mypy2                   | 446 ms                                                                    | 368 ms: 1.21x faster                                                         |
| deltablue               | 3.99 ms                                                                   | 3.32 ms: 1.20x faster                                                        |
| json_loads              | 28.4 us                                                                   | 23.9 us: 1.19x faster                                                        |
| gc_traversal            | 4.22 ms                                                                   | 3.57 ms: 1.18x faster                                                        |
| comprehensions          | 24.7 us                                                                   | 21.1 us: 1.17x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 206 us: 1.15x faster                                                         |
| scimark_lu              | 114 ms                                                                    | 99.6 ms: 1.15x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 141 ms: 1.14x faster                                                         |
| json                    | 5.59 ms                                                                   | 5.00 ms: 1.12x faster                                                        |
| logging_silent          | 103 ns                                                                    | 92.7 ns: 1.11x faster                                                        |
| mako                    | 10.9 ms                                                                   | 9.92 ms: 1.10x faster                                                        |
| richards                | 49.1 ms                                                                   | 44.8 ms: 1.10x faster                                                        |
| hexiom                  | 7.00 ms                                                                   | 6.39 ms: 1.10x faster                                                        |
| regex_compile           | 154 ms                                                                    | 142 ms: 1.08x faster                                                         |
| pycparser               | 1.30 sec                                                                  | 1.21 sec: 1.08x faster                                                       |
| genshi_xml              | 57.8 ms                                                                   | 53.6 ms: 1.08x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.78 ms: 1.07x faster                                                        |
| tornado_http            | 125 ms                                                                    | 117 ms: 1.07x faster                                                         |
| float                   | 75.7 ms                                                                   | 70.9 ms: 1.07x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 24.7 ms: 1.06x faster                                                        |
| chaos                   | 76.2 ms                                                                   | 71.8 ms: 1.06x faster                                                        |
| dulwich_log             | 69.1 ms                                                                   | 65.2 ms: 1.06x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 35.0 us: 1.06x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 80.4 ms: 1.06x faster                                                        |
| sympy_str               | 333 ms                                                                    | 315 ms: 1.06x faster                                                         |
| fannkuch                | 449 ms                                                                    | 426 ms: 1.06x faster                                                         |
| go                      | 158 ms                                                                    | 150 ms: 1.05x faster                                                         |
| chameleon               | 7.50 ms                                                                   | 7.14 ms: 1.05x faster                                                        |
| pickle_pure_python      | 319 us                                                                    | 305 us: 1.05x faster                                                         |
| xml_etree_iterparse     | 106 ms                                                                    | 101 ms: 1.04x faster                                                         |
| async_tree_none         | 529 ms                                                                    | 507 ms: 1.04x faster                                                         |
| async_tree_memoization  | 639 ms                                                                    | 613 ms: 1.04x faster                                                         |
| mdp                     | 2.73 sec                                                                  | 2.62 sec: 1.04x faster                                                       |
| nqueens                 | 101 ms                                                                    | 96.9 ms: 1.04x faster                                                        |
| 2to3                    | 289 ms                                                                    | 279 ms: 1.04x faster                                                         |
| sympy_sum               | 182 ms                                                                    | 176 ms: 1.04x faster                                                         |
| scimark_sor             | 109 ms                                                                    | 105 ms: 1.04x faster                                                         |
| raytrace                | 303 ms                                                                    | 293 ms: 1.03x faster                                                         |
| bench_thread_pool       | 990 us                                                                    | 956 us: 1.03x faster                                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.55 sec: 1.03x faster                                                       |
| sympy_integrate         | 25.3 ms                                                                   | 24.5 ms: 1.03x faster                                                        |
| django_template         | 39.6 ms                                                                   | 38.3 ms: 1.03x faster                                                        |
| unpack_sequence         | 45.9 ns                                                                   | 44.4 ns: 1.03x faster                                                        |
| html5lib                | 70.2 ms                                                                   | 68.0 ms: 1.03x faster                                                        |
| thrift                  | 942 us                                                                    | 915 us: 1.03x faster                                                         |
| sympy_expand            | 547 ms                                                                    | 535 ms: 1.02x faster                                                         |
| docutils                | 2.86 sec                                                                  | 2.80 sec: 1.02x faster                                                       |
| nbody                   | 92.1 ms                                                                   | 90.4 ms: 1.02x faster                                                        |
| sqlglot_normalize       | 122 ms                                                                    | 120 ms: 1.02x faster                                                         |
| unpickle_list           | 4.52 us                                                                   | 4.44 us: 1.02x faster                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.34 us: 1.02x faster                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 57.6 ms: 1.02x faster                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.62 ms: 1.02x faster                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 66.8 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 744 ms: 1.01x faster                                                         |
| pprint_safe_repr        | 768 ms                                                                    | 759 ms: 1.01x faster                                                         |
| coverage                | 86.0 ms                                                                   | 85.0 ms: 1.01x faster                                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                       |
| meteor_contest          | 129 ms                                                                    | 128 ms: 1.01x faster                                                         |
| pyflate                 | 438 ms                                                                    | 434 ms: 1.01x faster                                                         |
| spectral_norm           | 95.1 ms                                                                   | 94.6 ms: 1.01x faster                                                        |
| pidigits                | 252 ms                                                                    | 252 ms: 1.00x slower                                                         |
| telco                   | 6.70 ms                                                                   | 6.73 ms: 1.00x slower                                                        |
| pathlib                 | 19.2 ms                                                                   | 19.4 ms: 1.01x slower                                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.55 ms: 1.01x slower                                                        |
| unpickle                | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 282 ms: 1.02x slower                                                         |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.92 ms: 1.02x slower                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 57.1 ms: 1.02x slower                                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.42 ms: 1.03x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.3 us: 1.03x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 32.3 us: 1.04x slower                                                        |
| python_startup          | 10.7 ms                                                                   | 11.2 ms: 1.05x slower                                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 4.77 ms: 1.05x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 83.2 ms: 1.05x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.63 us: 1.06x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.28 ms: 1.07x slower                                                        |
| async_generators        | 318 ms                                                                    | 375 ms: 1.18x slower                                                         |
| dask                    | 418 ms                                                                    | 558 ms: 1.34x slower                                                         |
| Geometric mean          | (ref)                                                                     | 1.05x faster                                                                 |

Benchmark hidden because not significant (5): logging_format, regex_dna, logging_simple, deepcopy, pickle_list
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
