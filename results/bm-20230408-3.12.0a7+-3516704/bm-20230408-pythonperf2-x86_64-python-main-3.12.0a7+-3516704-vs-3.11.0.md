
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3516704
- commit date: 2023-04-08
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 284 ms: 1.02x faster                                         |
| chameleon      | 7.50 ms                                                                   | 7.03 ms: 1.07x faster                                        |
| docutils       | 2.86 sec                                                                  | 2.81 sec: 1.02x faster                                       |
| html5lib       | 70.2 ms                                                                   | 67.1 ms: 1.05x faster                                        |
| tornado_http   | 125 ms                                                                    | 115 ms: 1.09x faster                                         |
| Geometric mean | (ref)                                                                     | 1.05x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 92.1 ms                                                                   | 84.0 ms: 1.10x faster                                        |
| float          | 75.7 ms                                                                   | 72.6 ms: 1.04x faster                                        |
| pidigits       | 252 ms                                                                    | 260 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 23.5 ms: 1.04x faster                                        |
| regex_compile  | 154 ms                                                                    | 149 ms: 1.04x faster                                         |
| regex_dna      | 225 ms                                                                    | 235 ms: 1.05x slower                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.48 ms: 1.05x slower                                        |
| Geometric mean | (ref)                                                                     | 1.00x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7+-3516704 |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.5 ms: 1.28x faster                                        |
| json_loads           | 28.4 us                                                                   | 24.2 us: 1.17x faster                                        |
| unpickle_pure_python | 238 us                                                                    | 205 us: 1.16x faster                                         |
| xml_etree_parse      | 161 ms                                                                    | 145 ms: 1.11x faster                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 103 ms: 1.02x faster                                         |
| pickle_dict          | 31.1 us                                                                   | 30.5 us: 1.02x faster                                        |
| pickle_pure_python   | 319 us                                                                    | 314 us: 1.02x faster                                         |
| unpickle_list        | 4.52 us                                                                   | 4.59 us: 1.02x slower                                        |
| xml_etree_process    | 55.8 ms                                                                   | 56.8 ms: 1.02x slower                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 82.6 ms: 1.04x slower                                        |
| unpickle             | 13.0 us                                                                   | 14.0 us: 1.07x slower                                        |
| Geometric mean       | (ref)                                                                     | 1.04x faster                                                 |

Benchmark hidden because not significant (2): pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7+-3516704 |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.0 ms: 1.03x slower                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.29 ms: 1.07x slower                                        |
| Geometric mean         | (ref)                                                                     | 1.05x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7+-3516704 |
|-----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 52.7 ms: 1.10x faster                                        |
| mako            | 10.9 ms                                                                   | 10.1 ms: 1.08x faster                                        |
| genshi_text     | 26.3 ms                                                                   | 24.8 ms: 1.06x faster                                        |
| django_template | 39.6 ms                                                                   | 38.9 ms: 1.02x faster                                        |
| Geometric mean  | (ref)                                                                     | 1.06x faster                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7+-3516704 |
|-------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 384 ms: 1.96x faster                                         |
| generators              | 56.0 ms                                                                   | 37.6 ms: 1.49x faster                                        |
| json_dumps              | 13.4 ms                                                                   | 10.5 ms: 1.28x faster                                        |
| mypy2                   | 446 ms                                                                    | 378 ms: 1.18x faster                                         |
| deltablue               | 3.99 ms                                                                   | 3.40 ms: 1.17x faster                                        |
| json_loads              | 28.4 us                                                                   | 24.2 us: 1.17x faster                                        |
| coroutines              | 29.5 ms                                                                   | 25.2 ms: 1.17x faster                                        |
| unpickle_pure_python    | 238 us                                                                    | 205 us: 1.16x faster                                         |
| sqlglot_parse           | 1.53 ms                                                                   | 1.35 ms: 1.14x faster                                        |
| gc_traversal            | 4.22 ms                                                                   | 3.77 ms: 1.12x faster                                        |
| xml_etree_parse         | 161 ms                                                                    | 145 ms: 1.11x faster                                         |
| genshi_xml              | 57.8 ms                                                                   | 52.7 ms: 1.10x faster                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.71 ms: 1.10x faster                                        |
| nbody                   | 92.1 ms                                                                   | 84.0 ms: 1.10x faster                                        |
| scimark_lu              | 114 ms                                                                    | 104 ms: 1.10x faster                                         |
| json                    | 5.59 ms                                                                   | 5.13 ms: 1.09x faster                                        |
| tornado_http            | 125 ms                                                                    | 115 ms: 1.09x faster                                         |
| logging_format          | 7.84 us                                                                   | 7.26 us: 1.08x faster                                        |
| mako                    | 10.9 ms                                                                   | 10.1 ms: 1.08x faster                                        |
| mdp                     | 2.73 sec                                                                  | 2.54 sec: 1.07x faster                                       |
| logging_silent          | 103 ns                                                                    | 96.0 ns: 1.07x faster                                        |
| dulwich_log             | 69.1 ms                                                                   | 64.7 ms: 1.07x faster                                        |
| chameleon               | 7.50 ms                                                                   | 7.03 ms: 1.07x faster                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.81 ms: 1.06x faster                                        |
| async_tree_memoization  | 639 ms                                                                    | 601 ms: 1.06x faster                                         |
| deepcopy_memo           | 37.0 us                                                                   | 34.8 us: 1.06x faster                                        |
| hexiom                  | 7.00 ms                                                                   | 6.60 ms: 1.06x faster                                        |
| coverage                | 86.0 ms                                                                   | 81.2 ms: 1.06x faster                                        |
| chaos                   | 76.2 ms                                                                   | 72.0 ms: 1.06x faster                                        |
| genshi_text             | 26.3 ms                                                                   | 24.8 ms: 1.06x faster                                        |
| thrift                  | 942 us                                                                    | 891 us: 1.06x faster                                         |
| logging_simple          | 6.95 us                                                                   | 6.58 us: 1.06x faster                                        |
| pycparser               | 1.30 sec                                                                  | 1.24 sec: 1.05x faster                                       |
| raytrace                | 303 ms                                                                    | 288 ms: 1.05x faster                                         |
| async_tree_none         | 529 ms                                                                    | 503 ms: 1.05x faster                                         |
| html5lib                | 70.2 ms                                                                   | 67.1 ms: 1.05x faster                                        |
| float                   | 75.7 ms                                                                   | 72.6 ms: 1.04x faster                                        |
| spectral_norm           | 95.1 ms                                                                   | 91.2 ms: 1.04x faster                                        |
| regex_v8                | 24.4 ms                                                                   | 23.5 ms: 1.04x faster                                        |
| fannkuch                | 449 ms                                                                    | 432 ms: 1.04x faster                                         |
| async_tree_io           | 1.18 sec                                                                  | 1.14 sec: 1.04x faster                                       |
| bench_thread_pool       | 990 us                                                                    | 955 us: 1.04x faster                                         |
| regex_compile           | 154 ms                                                                    | 149 ms: 1.04x faster                                         |
| richards                | 49.1 ms                                                                   | 47.4 ms: 1.04x faster                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.59 ms: 1.03x faster                                        |
| unpack_sequence         | 45.9 ns                                                                   | 44.4 ns: 1.03x faster                                        |
| sqlglot_normalize       | 122 ms                                                                    | 118 ms: 1.03x faster                                         |
| deepcopy_reduce         | 3.39 us                                                                   | 3.30 us: 1.03x faster                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 735 ms: 1.02x faster                                         |
| xml_etree_iterparse     | 106 ms                                                                    | 103 ms: 1.02x faster                                         |
| 2to3                    | 289 ms                                                                    | 284 ms: 1.02x faster                                         |
| deepcopy                | 384 us                                                                    | 376 us: 1.02x faster                                         |
| scimark_fft             | 276 ms                                                                    | 271 ms: 1.02x faster                                         |
| django_template         | 39.6 ms                                                                   | 38.9 ms: 1.02x faster                                        |
| pickle_dict             | 31.1 us                                                                   | 30.5 us: 1.02x faster                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 57.5 ms: 1.02x faster                                        |
| pickle_pure_python      | 319 us                                                                    | 314 us: 1.02x faster                                         |
| docutils                | 2.86 sec                                                                  | 2.81 sec: 1.02x faster                                       |
| sympy_expand            | 547 ms                                                                    | 538 ms: 1.02x faster                                         |
| sympy_integrate         | 25.3 ms                                                                   | 25.0 ms: 1.01x faster                                        |
| meteor_contest          | 129 ms                                                                    | 128 ms: 1.01x faster                                         |
| sympy_str               | 333 ms                                                                    | 330 ms: 1.01x faster                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.59 sec: 1.01x faster                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 67.4 ms: 1.01x faster                                        |
| sympy_sum               | 182 ms                                                                    | 183 ms: 1.01x slower                                         |
| crypto_pyaes            | 85.0 ms                                                                   | 85.9 ms: 1.01x slower                                        |
| go                      | 158 ms                                                                    | 160 ms: 1.01x slower                                         |
| pprint_safe_repr        | 768 ms                                                                    | 780 ms: 1.02x slower                                         |
| unpickle_list           | 4.52 us                                                                   | 4.59 us: 1.02x slower                                        |
| xml_etree_process       | 55.8 ms                                                                   | 56.8 ms: 1.02x slower                                        |
| telco                   | 6.70 ms                                                                   | 6.82 ms: 1.02x slower                                        |
| pyflate                 | 438 ms                                                                    | 446 ms: 1.02x slower                                         |
| python_startup          | 10.7 ms                                                                   | 11.0 ms: 1.03x slower                                        |
| scimark_sor             | 109 ms                                                                    | 113 ms: 1.03x slower                                         |
| pathlib                 | 19.2 ms                                                                   | 19.8 ms: 1.03x slower                                        |
| pidigits                | 252 ms                                                                    | 260 ms: 1.03x slower                                         |
| xml_etree_generate      | 79.1 ms                                                                   | 82.6 ms: 1.04x slower                                        |
| regex_dna               | 225 ms                                                                    | 235 ms: 1.05x slower                                         |
| regex_effbot            | 3.31 ms                                                                   | 3.48 ms: 1.05x slower                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.62 us: 1.05x slower                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 4.82 ms: 1.06x slower                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.29 ms: 1.07x slower                                        |
| unpickle                | 13.0 us                                                                   | 14.0 us: 1.07x slower                                        |
| async_generators        | 318 ms                                                                    | 381 ms: 1.20x slower                                         |
| dask                    | 418 ms                                                                    | 566 ms: 1.36x slower                                         |
| Geometric mean          | (ref)                                                                     | 1.04x faster                                                 |

Benchmark hidden because not significant (4): pickle_list, comprehensions, pickle, nqueens
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
