
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 0fd3891
- commit date: 2023-04-22
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 284 ms: 1.02x faster                                         |
| html5lib       | 70.2 ms                                                                   | 67.8 ms: 1.04x faster                                        |
| tornado_http   | 125 ms                                                                    | 119 ms: 1.05x faster                                         |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                 |

Benchmark hidden because not significant (2): chameleon, docutils

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 92.1 ms                                                                   | 86.6 ms: 1.06x faster                                        |
| pidigits       | 252 ms                                                                    | 260 ms: 1.03x slower                                         |
| float          | 75.7 ms                                                                   | 79.1 ms: 1.04x slower                                        |
| Geometric mean | (ref)                                                                     | 1.00x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                    | 143 ms: 1.08x faster                                         |
| regex_v8       | 24.4 ms                                                                   | 24.1 ms: 1.02x faster                                        |
| regex_dna      | 225 ms                                                                    | 232 ms: 1.03x slower                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.53 ms: 1.07x slower                                        |
| Geometric mean | (ref)                                                                     | 1.00x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.1 ms: 1.32x faster                                        |
| json_loads           | 28.4 us                                                                   | 24.5 us: 1.16x faster                                        |
| unpickle_pure_python | 238 us                                                                    | 205 us: 1.16x faster                                         |
| xml_etree_parse      | 161 ms                                                                    | 145 ms: 1.11x faster                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 104 ms: 1.02x faster                                         |
| pickle_pure_python   | 319 us                                                                    | 315 us: 1.01x faster                                         |
| pickle_dict          | 31.1 us                                                                   | 30.9 us: 1.01x faster                                        |
| pickle               | 9.92 us                                                                   | 10.2 us: 1.03x slower                                        |
| xml_etree_process    | 55.8 ms                                                                   | 58.2 ms: 1.04x slower                                        |
| unpickle_list        | 4.52 us                                                                   | 4.72 us: 1.04x slower                                        |
| pickle_list          | 3.78 us                                                                   | 3.96 us: 1.05x slower                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 84.5 ms: 1.07x slower                                        |
| unpickle             | 13.0 us                                                                   | 14.2 us: 1.09x slower                                        |
| Geometric mean       | (ref)                                                                     | 1.03x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7+-0fd3891 |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.1 ms: 1.04x slower                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.33 ms: 1.08x slower                                        |
| Geometric mean         | (ref)                                                                     | 1.06x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7+-0fd3891 |
|-----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 10.9 ms                                                                   | 9.92 ms: 1.10x faster                                        |
| genshi_xml      | 57.8 ms                                                                   | 54.1 ms: 1.07x faster                                        |
| genshi_text     | 26.3 ms                                                                   | 24.9 ms: 1.06x faster                                        |
| django_template | 39.6 ms                                                                   | 38.6 ms: 1.03x faster                                        |
| Geometric mean  | (ref)                                                                     | 1.06x faster                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7+-0fd3891 |
|-------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 376 ms: 2.00x faster                                         |
| generators              | 56.0 ms                                                                   | 36.4 ms: 1.54x faster                                        |
| fannkuch                | 449 ms                                                                    | 341 ms: 1.32x faster                                         |
| json_dumps              | 13.4 ms                                                                   | 10.1 ms: 1.32x faster                                        |
| coroutines              | 29.5 ms                                                                   | 22.6 ms: 1.30x faster                                        |
| deltablue               | 3.99 ms                                                                   | 3.30 ms: 1.21x faster                                        |
| scimark_lu              | 114 ms                                                                    | 94.7 ms: 1.21x faster                                        |
| hexiom                  | 7.00 ms                                                                   | 5.84 ms: 1.20x faster                                        |
| gc_traversal            | 4.22 ms                                                                   | 3.56 ms: 1.19x faster                                        |
| json_loads              | 28.4 us                                                                   | 24.5 us: 1.16x faster                                        |
| unpickle_pure_python    | 238 us                                                                    | 205 us: 1.16x faster                                         |
| mypy2                   | 446 ms                                                                    | 387 ms: 1.15x faster                                         |
| chaos                   | 76.2 ms                                                                   | 66.4 ms: 1.15x faster                                        |
| nqueens                 | 101 ms                                                                    | 89.0 ms: 1.13x faster                                        |
| richards                | 49.1 ms                                                                   | 43.3 ms: 1.13x faster                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.38 ms: 1.11x faster                                        |
| xml_etree_parse         | 161 ms                                                                    | 145 ms: 1.11x faster                                         |
| json                    | 5.59 ms                                                                   | 5.05 ms: 1.11x faster                                        |
| spectral_norm           | 95.1 ms                                                                   | 86.5 ms: 1.10x faster                                        |
| mako                    | 10.9 ms                                                                   | 9.92 ms: 1.10x faster                                        |
| logging_format          | 7.84 us                                                                   | 7.15 us: 1.10x faster                                        |
| logging_silent          | 103 ns                                                                    | 94.2 ns: 1.09x faster                                        |
| go                      | 158 ms                                                                    | 145 ms: 1.09x faster                                         |
| async_tree_memoization  | 639 ms                                                                    | 587 ms: 1.09x faster                                         |
| regex_compile           | 154 ms                                                                    | 143 ms: 1.08x faster                                         |
| logging_simple          | 6.95 us                                                                   | 6.49 us: 1.07x faster                                        |
| genshi_xml              | 57.8 ms                                                                   | 54.1 ms: 1.07x faster                                        |
| dulwich_log             | 69.1 ms                                                                   | 64.9 ms: 1.07x faster                                        |
| nbody                   | 92.1 ms                                                                   | 86.6 ms: 1.06x faster                                        |
| async_tree_none         | 529 ms                                                                    | 498 ms: 1.06x faster                                         |
| mdp                     | 2.73 sec                                                                  | 2.57 sec: 1.06x faster                                       |
| crypto_pyaes            | 85.0 ms                                                                   | 80.4 ms: 1.06x faster                                        |
| genshi_text             | 26.3 ms                                                                   | 24.9 ms: 1.06x faster                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.78 ms: 1.05x faster                                        |
| pylint                  | 517 ms                                                                    | 491 ms: 1.05x faster                                         |
| tornado_http            | 125 ms                                                                    | 119 ms: 1.05x faster                                         |
| sympy_expand            | 547 ms                                                                    | 524 ms: 1.04x faster                                         |
| pathlib                 | 19.2 ms                                                                   | 18.4 ms: 1.04x faster                                        |
| thrift                  | 942 us                                                                    | 906 us: 1.04x faster                                         |
| html5lib                | 70.2 ms                                                                   | 67.8 ms: 1.04x faster                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.14 sec: 1.03x faster                                       |
| pycparser               | 1.30 sec                                                                  | 1.26 sec: 1.03x faster                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 733 ms: 1.03x faster                                         |
| sympy_str               | 333 ms                                                                    | 324 ms: 1.03x faster                                         |
| django_template         | 39.6 ms                                                                   | 38.6 ms: 1.03x faster                                        |
| bench_thread_pool       | 990 us                                                                    | 964 us: 1.03x faster                                         |
| create_gc_cycles        | 1.65 ms                                                                   | 1.61 ms: 1.02x faster                                        |
| 2to3                    | 289 ms                                                                    | 284 ms: 1.02x faster                                         |
| xml_etree_iterparse     | 106 ms                                                                    | 104 ms: 1.02x faster                                         |
| regex_v8                | 24.4 ms                                                                   | 24.1 ms: 1.02x faster                                        |
| pickle_pure_python      | 319 us                                                                    | 315 us: 1.01x faster                                         |
| raytrace                | 303 ms                                                                    | 300 ms: 1.01x faster                                         |
| deepcopy_memo           | 37.0 us                                                                   | 36.7 us: 1.01x faster                                        |
| pickle_dict             | 31.1 us                                                                   | 30.9 us: 1.01x faster                                        |
| scimark_sor             | 109 ms                                                                    | 109 ms: 1.00x faster                                         |
| comprehensions          | 24.7 us                                                                   | 25.0 us: 1.01x slower                                        |
| deepcopy                | 384 us                                                                    | 388 us: 1.01x slower                                         |
| deepcopy_reduce         | 3.39 us                                                                   | 3.45 us: 1.02x slower                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 59.6 ms: 1.02x slower                                        |
| pickle                  | 9.92 us                                                                   | 10.2 us: 1.03x slower                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 69.8 ms: 1.03x slower                                        |
| regex_dna               | 225 ms                                                                    | 232 ms: 1.03x slower                                         |
| pidigits                | 252 ms                                                                    | 260 ms: 1.03x slower                                         |
| python_startup          | 10.7 ms                                                                   | 11.1 ms: 1.04x slower                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.66 sec: 1.04x slower                                       |
| scimark_fft             | 276 ms                                                                    | 288 ms: 1.04x slower                                         |
| xml_etree_process       | 55.8 ms                                                                   | 58.2 ms: 1.04x slower                                        |
| unpickle_list           | 4.52 us                                                                   | 4.72 us: 1.04x slower                                        |
| float                   | 75.7 ms                                                                   | 79.1 ms: 1.04x slower                                        |
| pickle_list             | 3.78 us                                                                   | 3.96 us: 1.05x slower                                        |
| telco                   | 6.70 ms                                                                   | 7.05 ms: 1.05x slower                                        |
| coverage                | 86.0 ms                                                                   | 90.9 ms: 1.06x slower                                        |
| meteor_contest          | 129 ms                                                                    | 137 ms: 1.06x slower                                         |
| pprint_safe_repr        | 768 ms                                                                    | 815 ms: 1.06x slower                                         |
| sqlite_synth            | 2.49 us                                                                   | 2.65 us: 1.07x slower                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.53 ms: 1.07x slower                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 84.5 ms: 1.07x slower                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.35 ms: 1.07x slower                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.33 ms: 1.08x slower                                        |
| unpickle                | 13.0 us                                                                   | 14.2 us: 1.09x slower                                        |
| unpack_sequence         | 45.9 ns                                                                   | 52.6 ns: 1.15x slower                                        |
| async_generators        | 318 ms                                                                    | 386 ms: 1.21x slower                                         |
| dask                    | 418 ms                                                                    | 560 ms: 1.34x slower                                         |
| bench_mp_pool           | 4.54 ms                                                                   | 7.21 ms: 1.59x slower                                        |
| Geometric mean          | (ref)                                                                     | 1.04x faster                                                 |

Benchmark hidden because not significant (6): chameleon, pyflate, sympy_sum, sqlglot_normalize, sympy_integrate, docutils
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
