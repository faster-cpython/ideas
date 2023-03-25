
# Results vs. 3.11.0

- fork: python
- ref: ef7c2bfcf1fd618438f9
- machine: linux-x86_64
- commit hash: ef7c2bf
- commit date: 2023-02-05
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf2-x86_64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 281 ms: 1.03x faster                                                         |
| chameleon      | 7.50 ms                                                                   | 7.63 ms: 1.02x slower                                                        |
| docutils       | 2.86 sec                                                                  | 2.75 sec: 1.04x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 66.2 ms: 1.06x faster                                                        |
| tornado_http   | 125 ms                                                                    | 120 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf2-x86_64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 71.5 ms: 1.06x faster                                                        |
| nbody          | 92.1 ms                                                                   | 89.9 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf2-x86_64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 22.1 ms: 1.11x faster                                                        |
| regex_compile  | 154 ms                                                                    | 145 ms: 1.06x faster                                                         |
| regex_dna      | 225 ms                                                                    | 222 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                                 |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf2-x86_64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.0 ms: 1.33x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.1 us: 1.18x faster                                                        |
| unpickle_pure_python | 238 us                                                                    | 208 us: 1.15x faster                                                         |
| xml_etree_parse      | 161 ms                                                                    | 143 ms: 1.12x faster                                                         |
| pickle_pure_python   | 319 us                                                                    | 307 us: 1.04x faster                                                         |
| unpickle_list        | 4.52 us                                                                   | 4.36 us: 1.04x faster                                                        |
| pickle               | 9.92 us                                                                   | 10.1 us: 1.02x slower                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 81.1 ms: 1.02x slower                                                        |
| unpickle             | 13.0 us                                                                   | 13.5 us: 1.04x slower                                                        |
| pickle_list          | 3.78 us                                                                   | 3.95 us: 1.05x slower                                                        |
| pickle_dict          | 31.1 us                                                                   | 32.6 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.05x faster                                                                 |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf2-x86_64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.2 ms: 1.04x slower                                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.26 ms: 1.07x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.06x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf2-x86_64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|-----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 54.1 ms: 1.07x faster                                                        |
| mako            | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| genshi_text     | 26.3 ms                                                                   | 24.9 ms: 1.05x faster                                                        |
| django_template | 39.6 ms                                                                   | 38.3 ms: 1.03x faster                                                        |
| Geometric mean  | (ref)                                                                     | 1.06x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf2-x86_64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 387 ms: 1.95x faster                                                         |
| json_dumps              | 13.4 ms                                                                   | 10.0 ms: 1.33x faster                                                        |
| mypy2                   | 446 ms                                                                    | 374 ms: 1.19x faster                                                         |
| json_loads              | 28.4 us                                                                   | 24.1 us: 1.18x faster                                                        |
| comprehensions          | 24.7 us                                                                   | 21.5 us: 1.15x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 208 us: 1.15x faster                                                         |
| deltablue               | 3.99 ms                                                                   | 3.49 ms: 1.14x faster                                                        |
| chaos                   | 76.2 ms                                                                   | 67.4 ms: 1.13x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.59 ms: 1.13x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 143 ms: 1.12x faster                                                         |
| gc_traversal            | 4.22 ms                                                                   | 3.76 ms: 1.12x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 102 ms: 1.12x faster                                                         |
| fannkuch                | 449 ms                                                                    | 404 ms: 1.11x faster                                                         |
| regex_v8                | 24.4 ms                                                                   | 22.1 ms: 1.11x faster                                                        |
| json                    | 5.59 ms                                                                   | 5.07 ms: 1.10x faster                                                        |
| hexiom                  | 7.00 ms                                                                   | 6.43 ms: 1.09x faster                                                        |
| pycparser               | 1.30 sec                                                                  | 1.21 sec: 1.07x faster                                                       |
| logging_silent          | 103 ns                                                                    | 95.9 ns: 1.07x faster                                                        |
| sympy_str               | 333 ms                                                                    | 311 ms: 1.07x faster                                                         |
| genshi_xml              | 57.8 ms                                                                   | 54.1 ms: 1.07x faster                                                        |
| mako                    | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| unpack_sequence         | 45.9 ns                                                                   | 43.2 ns: 1.06x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 80.0 ms: 1.06x faster                                                        |
| html5lib                | 70.2 ms                                                                   | 66.2 ms: 1.06x faster                                                        |
| float                   | 75.7 ms                                                                   | 71.5 ms: 1.06x faster                                                        |
| regex_compile           | 154 ms                                                                    | 145 ms: 1.06x faster                                                         |
| sympy_sum               | 182 ms                                                                    | 172 ms: 1.06x faster                                                         |
| thrift                  | 942 us                                                                    | 892 us: 1.06x faster                                                         |
| richards                | 49.1 ms                                                                   | 46.5 ms: 1.06x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 24.9 ms: 1.05x faster                                                        |
| dulwich_log             | 69.1 ms                                                                   | 65.6 ms: 1.05x faster                                                        |
| async_tree_memoization  | 639 ms                                                                    | 608 ms: 1.05x faster                                                         |
| coverage                | 86.0 ms                                                                   | 82.2 ms: 1.05x faster                                                        |
| tornado_http            | 125 ms                                                                    | 120 ms: 1.04x faster                                                         |
| sympy_integrate         | 25.3 ms                                                                   | 24.3 ms: 1.04x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 508 ms: 1.04x faster                                                         |
| raytrace                | 303 ms                                                                    | 291 ms: 1.04x faster                                                         |
| pickle_pure_python      | 319 us                                                                    | 307 us: 1.04x faster                                                         |
| docutils                | 2.86 sec                                                                  | 2.75 sec: 1.04x faster                                                       |
| unpickle_list           | 4.52 us                                                                   | 4.36 us: 1.04x faster                                                        |
| sympy_expand            | 547 ms                                                                    | 528 ms: 1.03x faster                                                         |
| django_template         | 39.6 ms                                                                   | 38.3 ms: 1.03x faster                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.28 us: 1.03x faster                                                        |
| bench_thread_pool       | 990 us                                                                    | 959 us: 1.03x faster                                                         |
| 2to3                    | 289 ms                                                                    | 281 ms: 1.03x faster                                                         |
| create_gc_cycles        | 1.65 ms                                                                   | 1.60 ms: 1.03x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.64 us: 1.03x faster                                                        |
| nbody                   | 92.1 ms                                                                   | 89.9 ms: 1.02x faster                                                        |
| go                      | 158 ms                                                                    | 155 ms: 1.02x faster                                                         |
| sqlglot_normalize       | 122 ms                                                                    | 119 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 739 ms: 1.02x faster                                                         |
| scimark_sor             | 109 ms                                                                    | 107 ms: 1.02x faster                                                         |
| scimark_fft             | 276 ms                                                                    | 271 ms: 1.02x faster                                                         |
| pathlib                 | 19.2 ms                                                                   | 18.9 ms: 1.02x faster                                                        |
| regex_dna               | 225 ms                                                                    | 222 ms: 1.02x faster                                                         |
| pyflate                 | 438 ms                                                                    | 431 ms: 1.02x faster                                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.58 sec: 1.02x faster                                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 66.9 ms: 1.01x faster                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 57.8 ms: 1.01x faster                                                        |
| telco                   | 6.70 ms                                                                   | 6.61 ms: 1.01x faster                                                        |
| meteor_contest          | 129 ms                                                                    | 128 ms: 1.01x faster                                                         |
| deepcopy                | 384 us                                                                    | 380 us: 1.01x faster                                                         |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 29.2 ms: 1.01x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 36.8 us: 1.00x faster                                                        |
| async_generators        | 318 ms                                                                    | 322 ms: 1.01x slower                                                         |
| chameleon               | 7.50 ms                                                                   | 7.63 ms: 1.02x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.1 us: 1.02x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 81.1 ms: 1.02x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.56 us: 1.03x slower                                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.58 ms: 1.03x slower                                                        |
| unpickle                | 13.0 us                                                                   | 13.5 us: 1.04x slower                                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.95 ms: 1.04x slower                                                        |
| python_startup          | 10.7 ms                                                                   | 11.2 ms: 1.04x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 3.95 us: 1.05x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 32.6 us: 1.05x slower                                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 4.80 ms: 1.06x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.26 ms: 1.07x slower                                                        |
| generators              | 56.0 ms                                                                   | 60.8 ms: 1.09x slower                                                        |
| dask                    | 418 ms                                                                    | 568 ms: 1.36x slower                                                         |
| Geometric mean          | (ref)                                                                     | 1.04x faster                                                                 |

Benchmark hidden because not significant (9): nqueens, logging_simple, xml_etree_process, pprint_safe_repr, pidigits, mdp, regex_effbot, spectral_norm, xml_etree_iterparse
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
