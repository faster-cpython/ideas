
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4fe1c4b
- commit date: 2023-04-15
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 284 ms: 1.02x faster                                         |
| docutils       | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                       |
| html5lib       | 70.2 ms                                                                   | 68.4 ms: 1.03x faster                                        |
| tornado_http   | 125 ms                                                                    | 114 ms: 1.10x faster                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                 |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 92.1 ms                                                                   | 78.5 ms: 1.17x faster                                        |
| float          | 75.7 ms                                                                   | 70.4 ms: 1.08x faster                                        |
| pidigits       | 252 ms                                                                    | 260 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                                     | 1.07x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                    | 148 ms: 1.04x faster                                         |
| regex_v8       | 24.4 ms                                                                   | 23.9 ms: 1.02x faster                                        |
| regex_dna      | 225 ms                                                                    | 234 ms: 1.04x slower                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.44 ms: 1.04x slower                                        |
| Geometric mean | (ref)                                                                     | 1.00x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.3 ms: 1.29x faster                                        |
| json_loads           | 28.4 us                                                                   | 24.0 us: 1.19x faster                                        |
| unpickle_pure_python | 238 us                                                                    | 211 us: 1.13x faster                                         |
| xml_etree_parse      | 161 ms                                                                    | 146 ms: 1.10x faster                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 101 ms: 1.05x faster                                         |
| pickle_dict          | 31.1 us                                                                   | 30.2 us: 1.03x faster                                        |
| pickle               | 9.92 us                                                                   | 9.98 us: 1.01x slower                                        |
| xml_etree_process    | 55.8 ms                                                                   | 57.0 ms: 1.02x slower                                        |
| unpickle_list        | 4.52 us                                                                   | 4.63 us: 1.02x slower                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 82.4 ms: 1.04x slower                                        |
| unpickle             | 13.0 us                                                                   | 14.2 us: 1.09x slower                                        |
| Geometric mean       | (ref)                                                                     | 1.04x faster                                                 |

Benchmark hidden because not significant (2): pickle_list, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7+-4fe1c4b |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.1 ms: 1.03x slower                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.34 ms: 1.08x slower                                        |
| Geometric mean         | (ref)                                                                     | 1.06x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7+-4fe1c4b |
|-----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 10.9 ms                                                                   | 9.90 ms: 1.10x faster                                        |
| genshi_xml      | 57.8 ms                                                                   | 53.7 ms: 1.08x faster                                        |
| genshi_text     | 26.3 ms                                                                   | 25.8 ms: 1.02x faster                                        |
| django_template | 39.6 ms                                                                   | 41.3 ms: 1.04x slower                                        |
| Geometric mean  | (ref)                                                                     | 1.04x faster                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7+-4fe1c4b |
|-------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 383 ms: 1.96x faster                                         |
| generators              | 56.0 ms                                                                   | 35.6 ms: 1.57x faster                                        |
| json_dumps              | 13.4 ms                                                                   | 10.3 ms: 1.29x faster                                        |
| coroutines              | 29.5 ms                                                                   | 24.7 ms: 1.20x faster                                        |
| gc_traversal            | 4.22 ms                                                                   | 3.55 ms: 1.19x faster                                        |
| json_loads              | 28.4 us                                                                   | 24.0 us: 1.19x faster                                        |
| deltablue               | 3.99 ms                                                                   | 3.39 ms: 1.18x faster                                        |
| mypy2                   | 446 ms                                                                    | 379 ms: 1.18x faster                                         |
| nbody                   | 92.1 ms                                                                   | 78.5 ms: 1.17x faster                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.34 ms: 1.14x faster                                        |
| scimark_lu              | 114 ms                                                                    | 100.0 ms: 1.14x faster                                       |
| fannkuch                | 449 ms                                                                    | 395 ms: 1.14x faster                                         |
| unpickle_pure_python    | 238 us                                                                    | 211 us: 1.13x faster                                         |
| json                    | 5.59 ms                                                                   | 5.03 ms: 1.11x faster                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.70 ms: 1.11x faster                                        |
| mako                    | 10.9 ms                                                                   | 9.90 ms: 1.10x faster                                        |
| xml_etree_parse         | 161 ms                                                                    | 146 ms: 1.10x faster                                         |
| tornado_http            | 125 ms                                                                    | 114 ms: 1.10x faster                                         |
| logging_silent          | 103 ns                                                                    | 94.1 ns: 1.09x faster                                        |
| mdp                     | 2.73 sec                                                                  | 2.52 sec: 1.08x faster                                       |
| genshi_xml              | 57.8 ms                                                                   | 53.7 ms: 1.08x faster                                        |
| float                   | 75.7 ms                                                                   | 70.4 ms: 1.08x faster                                        |
| pylint                  | 517 ms                                                                    | 484 ms: 1.07x faster                                         |
| dulwich_log             | 69.1 ms                                                                   | 64.7 ms: 1.07x faster                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.80 ms: 1.07x faster                                        |
| spectral_norm           | 95.1 ms                                                                   | 89.6 ms: 1.06x faster                                        |
| deepcopy_memo           | 37.0 us                                                                   | 34.9 us: 1.06x faster                                        |
| scimark_fft             | 276 ms                                                                    | 261 ms: 1.06x faster                                         |
| hexiom                  | 7.00 ms                                                                   | 6.63 ms: 1.06x faster                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 101 ms: 1.05x faster                                         |
| thrift                  | 942 us                                                                    | 899 us: 1.05x faster                                         |
| chaos                   | 76.2 ms                                                                   | 72.9 ms: 1.05x faster                                        |
| regex_compile           | 154 ms                                                                    | 148 ms: 1.04x faster                                         |
| richards                | 49.1 ms                                                                   | 47.3 ms: 1.04x faster                                        |
| async_tree_memoization  | 639 ms                                                                    | 617 ms: 1.04x faster                                         |
| pathlib                 | 19.2 ms                                                                   | 18.5 ms: 1.04x faster                                        |
| sqlglot_normalize       | 122 ms                                                                    | 118 ms: 1.03x faster                                         |
| pickle_dict             | 31.1 us                                                                   | 30.2 us: 1.03x faster                                        |
| meteor_contest          | 129 ms                                                                    | 126 ms: 1.03x faster                                         |
| bench_thread_pool       | 990 us                                                                    | 962 us: 1.03x faster                                         |
| raytrace                | 303 ms                                                                    | 295 ms: 1.03x faster                                         |
| async_tree_none         | 529 ms                                                                    | 515 ms: 1.03x faster                                         |
| docutils                | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                       |
| crypto_pyaes            | 85.0 ms                                                                   | 82.8 ms: 1.03x faster                                        |
| html5lib                | 70.2 ms                                                                   | 68.4 ms: 1.03x faster                                        |
| regex_v8                | 24.4 ms                                                                   | 23.9 ms: 1.02x faster                                        |
| unpack_sequence         | 45.9 ns                                                                   | 45.0 ns: 1.02x faster                                        |
| genshi_text             | 26.3 ms                                                                   | 25.8 ms: 1.02x faster                                        |
| 2to3                    | 289 ms                                                                    | 284 ms: 1.02x faster                                         |
| sympy_expand            | 547 ms                                                                    | 537 ms: 1.02x faster                                         |
| deepcopy                | 384 us                                                                    | 377 us: 1.02x faster                                         |
| async_tree_io           | 1.18 sec                                                                  | 1.16 sec: 1.02x faster                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 66.9 ms: 1.01x faster                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 57.8 ms: 1.01x faster                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.58 sec: 1.01x faster                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 749 ms: 1.01x faster                                         |
| logging_format          | 7.84 us                                                                   | 7.80 us: 1.01x faster                                        |
| sympy_str               | 333 ms                                                                    | 331 ms: 1.01x faster                                         |
| sympy_sum               | 182 ms                                                                    | 183 ms: 1.00x slower                                         |
| pickle                  | 9.92 us                                                                   | 9.98 us: 1.01x slower                                        |
| pprint_safe_repr        | 768 ms                                                                    | 773 ms: 1.01x slower                                         |
| telco                   | 6.70 ms                                                                   | 6.76 ms: 1.01x slower                                        |
| scimark_sor             | 109 ms                                                                    | 110 ms: 1.01x slower                                         |
| xml_etree_process       | 55.8 ms                                                                   | 57.0 ms: 1.02x slower                                        |
| unpickle_list           | 4.52 us                                                                   | 4.63 us: 1.02x slower                                        |
| python_startup          | 10.7 ms                                                                   | 11.1 ms: 1.03x slower                                        |
| pidigits                | 252 ms                                                                    | 260 ms: 1.03x slower                                         |
| regex_dna               | 225 ms                                                                    | 234 ms: 1.04x slower                                         |
| sqlite_synth            | 2.49 us                                                                   | 2.58 us: 1.04x slower                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.44 ms: 1.04x slower                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 82.4 ms: 1.04x slower                                        |
| django_template         | 39.6 ms                                                                   | 41.3 ms: 1.04x slower                                        |
| coverage                | 86.0 ms                                                                   | 91.1 ms: 1.06x slower                                        |
| pyflate                 | 438 ms                                                                    | 469 ms: 1.07x slower                                         |
| python_startup_no_site  | 7.73 ms                                                                   | 8.34 ms: 1.08x slower                                        |
| go                      | 158 ms                                                                    | 172 ms: 1.09x slower                                         |
| unpickle                | 13.0 us                                                                   | 14.2 us: 1.09x slower                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 5.44 ms: 1.20x slower                                        |
| async_generators        | 318 ms                                                                    | 388 ms: 1.22x slower                                         |
| dask                    | 418 ms                                                                    | 564 ms: 1.35x slower                                         |
| Geometric mean          | (ref)                                                                     | 1.04x faster                                                 |

Benchmark hidden because not significant (10): pickle_list, nqueens, logging_simple, create_gc_cycles, chameleon, sympy_integrate, pycparser, comprehensions, pickle_pure_python, deepcopy_reduce
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
