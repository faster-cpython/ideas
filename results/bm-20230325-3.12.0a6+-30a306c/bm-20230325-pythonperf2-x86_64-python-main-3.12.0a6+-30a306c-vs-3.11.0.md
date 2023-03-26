
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 30a306c
- commit date: 2023-03-25
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 285 ms: 1.02x faster                                         |
| docutils       | 2.86 sec                                                                  | 2.81 sec: 1.02x faster                                       |
| html5lib       | 70.2 ms                                                                   | 68.9 ms: 1.02x faster                                        |
| tornado_http   | 125 ms                                                                    | 114 ms: 1.10x faster                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                 |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 92.1 ms                                                                   | 84.6 ms: 1.09x faster                                        |
| float          | 75.7 ms                                                                   | 71.4 ms: 1.06x faster                                        |
| pidigits       | 252 ms                                                                    | 261 ms: 1.04x slower                                         |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 23.2 ms: 1.05x faster                                        |
| regex_compile  | 154 ms                                                                    | 147 ms: 1.05x faster                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.43 ms: 1.04x slower                                        |
| regex_dna      | 225 ms                                                                    | 235 ms: 1.04x slower                                         |
| Geometric mean | (ref)                                                                     | 1.00x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6+-30a306c |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.2 ms: 1.30x faster                                        |
| json_loads           | 28.4 us                                                                   | 24.2 us: 1.18x faster                                        |
| unpickle_pure_python | 238 us                                                                    | 206 us: 1.16x faster                                         |
| xml_etree_parse      | 161 ms                                                                    | 142 ms: 1.13x faster                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 102 ms: 1.04x faster                                         |
| pickle               | 9.92 us                                                                   | 10.1 us: 1.02x slower                                        |
| pickle_dict          | 31.1 us                                                                   | 31.8 us: 1.02x slower                                        |
| xml_etree_process    | 55.8 ms                                                                   | 57.5 ms: 1.03x slower                                        |
| unpickle             | 13.0 us                                                                   | 13.4 us: 1.03x slower                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 83.6 ms: 1.06x slower                                        |
| Geometric mean       | (ref)                                                                     | 1.05x faster                                                 |

Benchmark hidden because not significant (3): pickle_list, pickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6+-30a306c |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.0 ms: 1.03x slower                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.32 ms: 1.08x slower                                        |
| Geometric mean         | (ref)                                                                     | 1.05x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6+-30a306c |
|-----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 10.9 ms                                                                   | 10.0 ms: 1.08x faster                                        |
| genshi_xml      | 57.8 ms                                                                   | 55.3 ms: 1.05x faster                                        |
| genshi_text     | 26.3 ms                                                                   | 25.2 ms: 1.04x faster                                        |
| django_template | 39.6 ms                                                                   | 40.8 ms: 1.03x slower                                        |
| Geometric mean  | (ref)                                                                     | 1.03x faster                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6+-30a306c |
|-------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 387 ms: 1.94x faster                                         |
| generators              | 56.0 ms                                                                   | 37.9 ms: 1.48x faster                                        |
| json_dumps              | 13.4 ms                                                                   | 10.2 ms: 1.30x faster                                        |
| coroutines              | 29.5 ms                                                                   | 24.8 ms: 1.19x faster                                        |
| mypy2                   | 446 ms                                                                    | 379 ms: 1.18x faster                                         |
| json_loads              | 28.4 us                                                                   | 24.2 us: 1.18x faster                                        |
| gc_traversal            | 4.22 ms                                                                   | 3.59 ms: 1.17x faster                                        |
| deltablue               | 3.99 ms                                                                   | 3.44 ms: 1.16x faster                                        |
| unpickle_pure_python    | 238 us                                                                    | 206 us: 1.16x faster                                         |
| scimark_lu              | 114 ms                                                                    | 101 ms: 1.13x faster                                         |
| xml_etree_parse         | 161 ms                                                                    | 142 ms: 1.13x faster                                         |
| json                    | 5.59 ms                                                                   | 5.03 ms: 1.11x faster                                        |
| tornado_http            | 125 ms                                                                    | 114 ms: 1.10x faster                                         |
| nbody                   | 92.1 ms                                                                   | 84.6 ms: 1.09x faster                                        |
| mako                    | 10.9 ms                                                                   | 10.0 ms: 1.08x faster                                        |
| mdp                     | 2.73 sec                                                                  | 2.53 sec: 1.08x faster                                       |
| hexiom                  | 7.00 ms                                                                   | 6.50 ms: 1.08x faster                                        |
| deepcopy_memo           | 37.0 us                                                                   | 34.6 us: 1.07x faster                                        |
| chaos                   | 76.2 ms                                                                   | 71.5 ms: 1.07x faster                                        |
| pycparser               | 1.30 sec                                                                  | 1.23 sec: 1.06x faster                                       |
| float                   | 75.7 ms                                                                   | 71.4 ms: 1.06x faster                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.83 ms: 1.06x faster                                        |
| regex_v8                | 24.4 ms                                                                   | 23.2 ms: 1.05x faster                                        |
| async_tree_memoization  | 639 ms                                                                    | 607 ms: 1.05x faster                                         |
| dulwich_log             | 69.1 ms                                                                   | 65.7 ms: 1.05x faster                                        |
| regex_compile           | 154 ms                                                                    | 147 ms: 1.05x faster                                         |
| logging_silent          | 103 ns                                                                    | 97.9 ns: 1.05x faster                                        |
| unpack_sequence         | 45.9 ns                                                                   | 43.8 ns: 1.05x faster                                        |
| richards                | 49.1 ms                                                                   | 46.9 ms: 1.05x faster                                        |
| raytrace                | 303 ms                                                                    | 290 ms: 1.05x faster                                         |
| genshi_xml              | 57.8 ms                                                                   | 55.3 ms: 1.05x faster                                        |
| genshi_text             | 26.3 ms                                                                   | 25.2 ms: 1.04x faster                                        |
| nqueens                 | 101 ms                                                                    | 97.0 ms: 1.04x faster                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 102 ms: 1.04x faster                                         |
| async_tree_none         | 529 ms                                                                    | 510 ms: 1.04x faster                                         |
| spectral_norm           | 95.1 ms                                                                   | 92.1 ms: 1.03x faster                                        |
| logging_format          | 7.84 us                                                                   | 7.62 us: 1.03x faster                                        |
| pathlib                 | 19.2 ms                                                                   | 18.7 ms: 1.03x faster                                        |
| thrift                  | 942 us                                                                    | 919 us: 1.03x faster                                         |
| bench_thread_pool       | 990 us                                                                    | 966 us: 1.03x faster                                         |
| docutils                | 2.86 sec                                                                  | 2.81 sec: 1.02x faster                                       |
| html5lib                | 70.2 ms                                                                   | 68.9 ms: 1.02x faster                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 741 ms: 1.02x faster                                         |
| fannkuch                | 449 ms                                                                    | 442 ms: 1.02x faster                                         |
| 2to3                    | 289 ms                                                                    | 285 ms: 1.02x faster                                         |
| crypto_pyaes            | 85.0 ms                                                                   | 83.6 ms: 1.02x faster                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.62 ms: 1.02x faster                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.16 sec: 1.02x faster                                       |
| sympy_expand            | 547 ms                                                                    | 538 ms: 1.02x faster                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.58 sec: 1.01x faster                                       |
| deepcopy                | 384 us                                                                    | 380 us: 1.01x faster                                         |
| scimark_fft             | 276 ms                                                                    | 274 ms: 1.01x faster                                         |
| sympy_str               | 333 ms                                                                    | 330 ms: 1.01x faster                                         |
| sqlglot_normalize       | 122 ms                                                                    | 121 ms: 1.01x faster                                         |
| sympy_integrate         | 25.3 ms                                                                   | 25.2 ms: 1.01x faster                                        |
| meteor_contest          | 129 ms                                                                    | 129 ms: 1.00x faster                                         |
| scimark_sor             | 109 ms                                                                    | 111 ms: 1.01x slower                                         |
| telco                   | 6.70 ms                                                                   | 6.78 ms: 1.01x slower                                        |
| logging_simple          | 6.95 us                                                                   | 7.04 us: 1.01x slower                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.55 ms: 1.02x slower                                        |
| sympy_sum               | 182 ms                                                                    | 185 ms: 1.02x slower                                         |
| pyflate                 | 438 ms                                                                    | 446 ms: 1.02x slower                                         |
| scimark_monte_carlo     | 67.8 ms                                                                   | 69.1 ms: 1.02x slower                                        |
| pickle                  | 9.92 us                                                                   | 10.1 us: 1.02x slower                                        |
| pickle_dict             | 31.1 us                                                                   | 31.8 us: 1.02x slower                                        |
| go                      | 158 ms                                                                    | 162 ms: 1.02x slower                                         |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.92 ms: 1.02x slower                                        |
| python_startup          | 10.7 ms                                                                   | 11.0 ms: 1.03x slower                                        |
| xml_etree_process       | 55.8 ms                                                                   | 57.5 ms: 1.03x slower                                        |
| django_template         | 39.6 ms                                                                   | 40.8 ms: 1.03x slower                                        |
| unpickle                | 13.0 us                                                                   | 13.4 us: 1.03x slower                                        |
| pidigits                | 252 ms                                                                    | 261 ms: 1.04x slower                                         |
| regex_effbot            | 3.31 ms                                                                   | 3.43 ms: 1.04x slower                                        |
| regex_dna               | 225 ms                                                                    | 235 ms: 1.04x slower                                         |
| coverage                | 86.0 ms                                                                   | 90.5 ms: 1.05x slower                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 83.6 ms: 1.06x slower                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.63 us: 1.06x slower                                        |
| comprehensions          | 24.7 us                                                                   | 26.4 us: 1.07x slower                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 4.86 ms: 1.07x slower                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.32 ms: 1.08x slower                                        |
| async_generators        | 318 ms                                                                    | 377 ms: 1.18x slower                                         |
| dask                    | 418 ms                                                                    | 568 ms: 1.36x slower                                         |
| Geometric mean          | (ref)                                                                     | 1.03x faster                                                 |

Benchmark hidden because not significant (7): pickle_list, chameleon, pickle_pure_python, sqlglot_optimize, pprint_safe_repr, unpickle_list, deepcopy_reduce
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
