
# Results vs. 3.11.0

- fork: python
- ref: f9774e57d84162ff0cba
- machine: linux-x86_64
- commit hash: f9774e5
- commit date: 2023-03-07
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf2-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 284 ms: 1.02x faster                                                        |
| chameleon      | 7.50 ms                                                                   | 6.94 ms: 1.08x faster                                                       |
| docutils       | 2.86 sec                                                                  | 2.79 sec: 1.02x faster                                                      |
| html5lib       | 70.2 ms                                                                   | 65.9 ms: 1.07x faster                                                       |
| tornado_http   | 125 ms                                                                    | 115 ms: 1.09x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.05x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf2-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 73.9 ms: 1.02x faster                                                       |
| pidigits       | 252 ms                                                                    | 251 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf2-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 22.8 ms: 1.07x faster                                                       |
| regex_compile  | 154 ms                                                                    | 146 ms: 1.06x faster                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.36 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf2-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.2 ms: 1.30x faster                                                       |
| unpickle_pure_python | 238 us                                                                    | 202 us: 1.18x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.4 us: 1.16x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 144 ms: 1.11x faster                                                        |
| pickle_pure_python   | 319 us                                                                    | 306 us: 1.04x faster                                                        |
| xml_etree_iterparse  | 106 ms                                                                    | 103 ms: 1.02x faster                                                        |
| unpickle_list        | 4.52 us                                                                   | 4.44 us: 1.02x faster                                                       |
| pickle               | 9.92 us                                                                   | 10.0 us: 1.01x slower                                                       |
| pickle_dict          | 31.1 us                                                                   | 31.8 us: 1.02x slower                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 57.3 ms: 1.03x slower                                                       |
| unpickle             | 13.0 us                                                                   | 13.4 us: 1.03x slower                                                       |
| xml_etree_generate   | 79.1 ms                                                                   | 83.5 ms: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.05x faster                                                                |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf2-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.3 ms: 1.05x slower                                                       |
| python_startup_no_site | 7.73 ms                                                                   | 8.34 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                                     | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf2-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 53.0 ms: 1.09x faster                                                       |
| mako            | 10.9 ms                                                                   | 10.0 ms: 1.08x faster                                                       |
| genshi_text     | 26.3 ms                                                                   | 24.6 ms: 1.07x faster                                                       |
| django_template | 39.6 ms                                                                   | 39.1 ms: 1.01x faster                                                       |
| Geometric mean  | (ref)                                                                     | 1.06x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf2-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 382 ms: 1.97x faster                                                        |
| generators              | 56.0 ms                                                                   | 38.4 ms: 1.46x faster                                                       |
| json_dumps              | 13.4 ms                                                                   | 10.2 ms: 1.30x faster                                                       |
| deltablue               | 3.99 ms                                                                   | 3.33 ms: 1.20x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 24.7 ms: 1.19x faster                                                       |
| mypy2                   | 446 ms                                                                    | 377 ms: 1.18x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 202 us: 1.18x faster                                                        |
| json_loads              | 28.4 us                                                                   | 24.4 us: 1.16x faster                                                       |
| json                    | 5.59 ms                                                                   | 5.00 ms: 1.12x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 144 ms: 1.11x faster                                                        |
| fannkuch                | 449 ms                                                                    | 408 ms: 1.10x faster                                                        |
| genshi_xml              | 57.8 ms                                                                   | 53.0 ms: 1.09x faster                                                       |
| scimark_lu              | 114 ms                                                                    | 105 ms: 1.09x faster                                                        |
| logging_silent          | 103 ns                                                                    | 94.5 ns: 1.09x faster                                                       |
| tornado_http            | 125 ms                                                                    | 115 ms: 1.09x faster                                                        |
| dulwich_log             | 69.1 ms                                                                   | 63.7 ms: 1.09x faster                                                       |
| mako                    | 10.9 ms                                                                   | 10.0 ms: 1.08x faster                                                       |
| hexiom                  | 7.00 ms                                                                   | 6.46 ms: 1.08x faster                                                       |
| chameleon               | 7.50 ms                                                                   | 6.94 ms: 1.08x faster                                                       |
| chaos                   | 76.2 ms                                                                   | 70.9 ms: 1.08x faster                                                       |
| regex_v8                | 24.4 ms                                                                   | 22.8 ms: 1.07x faster                                                       |
| mdp                     | 2.73 sec                                                                  | 2.54 sec: 1.07x faster                                                      |
| genshi_text             | 26.3 ms                                                                   | 24.6 ms: 1.07x faster                                                       |
| html5lib                | 70.2 ms                                                                   | 65.9 ms: 1.07x faster                                                       |
| richards                | 49.1 ms                                                                   | 46.4 ms: 1.06x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.99 ms: 1.06x faster                                                       |
| pycparser               | 1.30 sec                                                                  | 1.23 sec: 1.06x faster                                                      |
| regex_compile           | 154 ms                                                                    | 146 ms: 1.06x faster                                                        |
| go                      | 158 ms                                                                    | 151 ms: 1.05x faster                                                        |
| raytrace                | 303 ms                                                                    | 290 ms: 1.05x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 35.4 us: 1.05x faster                                                       |
| async_tree_memoization  | 639 ms                                                                    | 611 ms: 1.05x faster                                                        |
| coverage                | 86.0 ms                                                                   | 82.2 ms: 1.05x faster                                                       |
| pickle_pure_python      | 319 us                                                                    | 306 us: 1.04x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 81.5 ms: 1.04x faster                                                       |
| nqueens                 | 101 ms                                                                    | 96.9 ms: 1.04x faster                                                       |
| scimark_sor             | 109 ms                                                                    | 105 ms: 1.04x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 510 ms: 1.04x faster                                                        |
| thrift                  | 942 us                                                                    | 909 us: 1.04x faster                                                        |
| pathlib                 | 19.2 ms                                                                   | 18.5 ms: 1.04x faster                                                       |
| logging_format          | 7.84 us                                                                   | 7.59 us: 1.03x faster                                                       |
| unpack_sequence         | 45.9 ns                                                                   | 44.4 ns: 1.03x faster                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.55 sec: 1.03x faster                                                      |
| float                   | 75.7 ms                                                                   | 73.9 ms: 1.02x faster                                                       |
| logging_simple          | 6.95 us                                                                   | 6.79 us: 1.02x faster                                                       |
| docutils                | 2.86 sec                                                                  | 2.79 sec: 1.02x faster                                                      |
| xml_etree_iterparse     | 106 ms                                                                    | 103 ms: 1.02x faster                                                        |
| 2to3                    | 289 ms                                                                    | 284 ms: 1.02x faster                                                        |
| unpickle_list           | 4.52 us                                                                   | 4.44 us: 1.02x faster                                                       |
| deepcopy_reduce         | 3.39 us                                                                   | 3.33 us: 1.02x faster                                                       |
| deepcopy                | 384 us                                                                    | 377 us: 1.02x faster                                                        |
| sympy_expand            | 547 ms                                                                    | 538 ms: 1.02x faster                                                        |
| sqlglot_normalize       | 122 ms                                                                    | 120 ms: 1.02x faster                                                        |
| sympy_str               | 333 ms                                                                    | 328 ms: 1.01x faster                                                        |
| pyflate                 | 438 ms                                                                    | 432 ms: 1.01x faster                                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                      |
| django_template         | 39.6 ms                                                                   | 39.1 ms: 1.01x faster                                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 745 ms: 1.01x faster                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.0 ms: 1.01x faster                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 762 ms: 1.01x faster                                                        |
| meteor_contest          | 129 ms                                                                    | 128 ms: 1.01x faster                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.2 ms: 1.01x faster                                                       |
| pidigits                | 252 ms                                                                    | 251 ms: 1.00x faster                                                        |
| spectral_norm           | 95.1 ms                                                                   | 95.6 ms: 1.01x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 278 ms: 1.01x slower                                                        |
| sympy_sum               | 182 ms                                                                    | 184 ms: 1.01x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.0 us: 1.01x slower                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.36 ms: 1.02x slower                                                       |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.14 ms: 1.02x slower                                                       |
| pickle_dict             | 31.1 us                                                                   | 31.8 us: 1.02x slower                                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 69.5 ms: 1.02x slower                                                       |
| xml_etree_process       | 55.8 ms                                                                   | 57.3 ms: 1.03x slower                                                       |
| unpickle                | 13.0 us                                                                   | 13.4 us: 1.03x slower                                                       |
| telco                   | 6.70 ms                                                                   | 6.90 ms: 1.03x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 1.58 ms: 1.03x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.94 ms: 1.03x slower                                                       |
| python_startup          | 10.7 ms                                                                   | 11.3 ms: 1.05x slower                                                       |
| xml_etree_generate      | 79.1 ms                                                                   | 83.5 ms: 1.06x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.63 us: 1.06x slower                                                       |
| bench_mp_pool           | 4.54 ms                                                                   | 4.84 ms: 1.07x slower                                                       |
| python_startup_no_site  | 7.73 ms                                                                   | 8.34 ms: 1.08x slower                                                       |
| comprehensions          | 24.7 us                                                                   | 26.7 us: 1.08x slower                                                       |
| async_generators        | 318 ms                                                                    | 385 ms: 1.21x slower                                                        |
| dask                    | 418 ms                                                                    | 560 ms: 1.34x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.04x faster                                                                |

Benchmark hidden because not significant (5): bench_thread_pool, nbody, create_gc_cycles, regex_dna, pickle_list
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
