
# Results vs. 3.11.0

- fork: python
- ref: edfbf56f4ca6588dfd20
- machine: linux-x86_64
- commit hash: edfbf56
- commit date: 2023-01-01
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 284 ms: 1.02x faster                                                         |
| chameleon      | 7.50 ms                                                                   | 7.29 ms: 1.03x faster                                                        |
| docutils       | 2.86 sec                                                                  | 2.76 sec: 1.03x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 66.2 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 72.5 ms: 1.04x faster                                                        |
| nbody          | 92.1 ms                                                                   | 90.4 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                        |
| regex_compile  | 154 ms                                                                    | 149 ms: 1.03x faster                                                         |
| regex_dna      | 225 ms                                                                    | 229 ms: 1.02x slower                                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.40 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.2 ms: 1.31x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.1 us: 1.18x faster                                                        |
| xml_etree_parse      | 161 ms                                                                    | 141 ms: 1.14x faster                                                         |
| unpickle_pure_python | 238 us                                                                    | 210 us: 1.14x faster                                                         |
| xml_etree_process    | 55.8 ms                                                                   | 54.1 ms: 1.03x faster                                                        |
| pickle_pure_python   | 319 us                                                                    | 313 us: 1.02x faster                                                         |
| unpickle_list        | 4.52 us                                                                   | 4.43 us: 1.02x faster                                                        |
| xml_etree_iterparse  | 106 ms                                                                    | 104 ms: 1.02x faster                                                         |
| xml_etree_generate   | 79.1 ms                                                                   | 78.0 ms: 1.01x faster                                                        |
| unpickle             | 13.0 us                                                                   | 12.9 us: 1.01x faster                                                        |
| pickle               | 9.92 us                                                                   | 9.84 us: 1.01x faster                                                        |
| pickle_list          | 3.78 us                                                                   | 3.83 us: 1.01x slower                                                        |
| pickle_dict          | 31.1 us                                                                   | 31.7 us: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.06x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                                   | 7.83 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.9 ms                                                                   | 10.1 ms: 1.08x faster                                                        |
| genshi_xml     | 57.8 ms                                                                   | 53.9 ms: 1.07x faster                                                        |
| genshi_text    | 26.3 ms                                                                   | 25.1 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.05x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 391 ms: 1.93x faster                                                         |
| json_dumps              | 13.4 ms                                                                   | 10.2 ms: 1.31x faster                                                        |
| mypy2                   | 446 ms                                                                    | 378 ms: 1.18x faster                                                         |
| json_loads              | 28.4 us                                                                   | 24.1 us: 1.18x faster                                                        |
| fannkuch                | 449 ms                                                                    | 392 ms: 1.15x faster                                                         |
| scimark_lu              | 114 ms                                                                    | 100 ms: 1.14x faster                                                         |
| xml_etree_parse         | 161 ms                                                                    | 141 ms: 1.14x faster                                                         |
| unpickle_pure_python    | 238 us                                                                    | 210 us: 1.14x faster                                                         |
| gc_traversal            | 4.22 ms                                                                   | 3.78 ms: 1.12x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.66 ms: 1.11x faster                                                        |
| json                    | 5.59 ms                                                                   | 5.08 ms: 1.10x faster                                                        |
| deltablue               | 3.99 ms                                                                   | 3.64 ms: 1.10x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 27.2 ms: 1.09x faster                                                        |
| mako                    | 10.9 ms                                                                   | 10.1 ms: 1.08x faster                                                        |
| genshi_xml              | 57.8 ms                                                                   | 53.9 ms: 1.07x faster                                                        |
| nqueens                 | 101 ms                                                                    | 94.4 ms: 1.07x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                        |
| thrift                  | 942 us                                                                    | 885 us: 1.07x faster                                                         |
| dulwich_log             | 69.1 ms                                                                   | 65.1 ms: 1.06x faster                                                        |
| richards                | 49.1 ms                                                                   | 46.3 ms: 1.06x faster                                                        |
| html5lib                | 70.2 ms                                                                   | 66.2 ms: 1.06x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 80.5 ms: 1.06x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 25.1 ms: 1.05x faster                                                        |
| chaos                   | 76.2 ms                                                                   | 72.8 ms: 1.05x faster                                                        |
| float                   | 75.7 ms                                                                   | 72.5 ms: 1.04x faster                                                        |
| async_tree_memoization  | 639 ms                                                                    | 613 ms: 1.04x faster                                                         |
| create_gc_cycles        | 1.65 ms                                                                   | 1.58 ms: 1.04x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 510 ms: 1.04x faster                                                         |
| docutils                | 2.86 sec                                                                  | 2.76 sec: 1.03x faster                                                       |
| deepcopy_memo           | 37.0 us                                                                   | 35.7 us: 1.03x faster                                                        |
| regex_compile           | 154 ms                                                                    | 149 ms: 1.03x faster                                                         |
| xml_etree_process       | 55.8 ms                                                                   | 54.1 ms: 1.03x faster                                                        |
| unpack_sequence         | 45.9 ns                                                                   | 44.5 ns: 1.03x faster                                                        |
| chameleon               | 7.50 ms                                                                   | 7.29 ms: 1.03x faster                                                        |
| sqlglot_normalize       | 122 ms                                                                    | 119 ms: 1.03x faster                                                         |
| scimark_monte_carlo     | 67.8 ms                                                                   | 66.1 ms: 1.03x faster                                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.56 sec: 1.03x faster                                                       |
| sympy_expand            | 547 ms                                                                    | 533 ms: 1.03x faster                                                         |
| deepcopy_reduce         | 3.39 us                                                                   | 3.32 us: 1.02x faster                                                        |
| pickle_pure_python      | 319 us                                                                    | 313 us: 1.02x faster                                                         |
| pycparser               | 1.30 sec                                                                  | 1.28 sec: 1.02x faster                                                       |
| hexiom                  | 7.00 ms                                                                   | 6.86 ms: 1.02x faster                                                        |
| pyflate                 | 438 ms                                                                    | 429 ms: 1.02x faster                                                         |
| unpickle_list           | 4.52 us                                                                   | 4.43 us: 1.02x faster                                                        |
| 2to3                    | 289 ms                                                                    | 284 ms: 1.02x faster                                                         |
| scimark_sor             | 109 ms                                                                    | 107 ms: 1.02x faster                                                         |
| nbody                   | 92.1 ms                                                                   | 90.4 ms: 1.02x faster                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 57.5 ms: 1.02x faster                                                        |
| logging_silent          | 103 ns                                                                    | 101 ns: 1.02x faster                                                         |
| async_tree_io           | 1.18 sec                                                                  | 1.16 sec: 1.02x faster                                                       |
| xml_etree_iterparse     | 106 ms                                                                    | 104 ms: 1.02x faster                                                         |
| xml_etree_generate      | 79.1 ms                                                                   | 78.0 ms: 1.01x faster                                                        |
| pprint_safe_repr        | 768 ms                                                                    | 758 ms: 1.01x faster                                                         |
| unpickle                | 13.0 us                                                                   | 12.9 us: 1.01x faster                                                        |
| raytrace                | 303 ms                                                                    | 300 ms: 1.01x faster                                                         |
| dask                    | 418 ms                                                                    | 413 ms: 1.01x faster                                                         |
| spectral_norm           | 95.1 ms                                                                   | 94.2 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 747 ms: 1.01x faster                                                         |
| deepcopy                | 384 us                                                                    | 380 us: 1.01x faster                                                         |
| sympy_str               | 333 ms                                                                    | 330 ms: 1.01x faster                                                         |
| pickle                  | 9.92 us                                                                   | 9.84 us: 1.01x faster                                                        |
| meteor_contest          | 129 ms                                                                    | 129 ms: 1.01x faster                                                         |
| scimark_fft             | 276 ms                                                                    | 275 ms: 1.00x faster                                                         |
| sympy_sum               | 182 ms                                                                    | 183 ms: 1.00x slower                                                         |
| go                      | 158 ms                                                                    | 159 ms: 1.01x slower                                                         |
| pickle_list             | 3.78 us                                                                   | 3.83 us: 1.01x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.83 ms: 1.01x slower                                                        |
| regex_dna               | 225 ms                                                                    | 229 ms: 1.02x slower                                                         |
| pickle_dict             | 31.1 us                                                                   | 31.7 us: 1.02x slower                                                        |
| async_generators        | 318 ms                                                                    | 326 ms: 1.02x slower                                                         |
| regex_effbot            | 3.31 ms                                                                   | 3.40 ms: 1.03x slower                                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.57 ms: 1.03x slower                                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.93 ms: 1.03x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.57 us: 1.03x slower                                                        |
| mdp                     | 2.73 sec                                                                  | 2.83 sec: 1.04x slower                                                       |
| bench_mp_pool           | 4.54 ms                                                                   | 4.74 ms: 1.04x slower                                                        |
| generators              | 56.0 ms                                                                   | 59.9 ms: 1.07x slower                                                        |
| coverage                | 86.0 ms                                                                   | 93.0 ms: 1.08x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 27.2 us: 1.10x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.04x faster                                                                 |

Benchmark hidden because not significant (9): bench_thread_pool, logging_format, django_template, pidigits, sympy_integrate, python_startup, pathlib, logging_simple, telco
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
