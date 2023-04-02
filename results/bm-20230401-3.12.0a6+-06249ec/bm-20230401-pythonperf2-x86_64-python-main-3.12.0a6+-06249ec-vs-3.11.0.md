
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 06249ec
- commit date: 2023-04-01
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 288 ms: 1.01x faster                                         |
| chameleon      | 7.50 ms                                                                   | 7.16 ms: 1.05x faster                                        |
| docutils       | 2.86 sec                                                                  | 2.82 sec: 1.01x faster                                       |
| tornado_http   | 125 ms                                                                    | 113 ms: 1.10x faster                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 92.1 ms                                                                   | 86.8 ms: 1.06x faster                                        |
| float          | 75.7 ms                                                                   | 73.7 ms: 1.03x faster                                        |
| pidigits       | 252 ms                                                                    | 260 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 23.4 ms: 1.05x faster                                        |
| regex_compile  | 154 ms                                                                    | 150 ms: 1.03x faster                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.38 ms: 1.02x slower                                        |
| regex_dna      | 225 ms                                                                    | 231 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6+-06249ec |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.4 ms: 1.28x faster                                        |
| json_loads           | 28.4 us                                                                   | 23.9 us: 1.19x faster                                        |
| xml_etree_parse      | 161 ms                                                                    | 143 ms: 1.12x faster                                         |
| unpickle_pure_python | 238 us                                                                    | 215 us: 1.11x faster                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 103 ms: 1.02x faster                                         |
| pickle_dict          | 31.1 us                                                                   | 31.5 us: 1.01x slower                                        |
| pickle_list          | 3.78 us                                                                   | 3.90 us: 1.03x slower                                        |
| pickle               | 9.92 us                                                                   | 10.3 us: 1.04x slower                                        |
| xml_etree_process    | 55.8 ms                                                                   | 60.0 ms: 1.07x slower                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 86.2 ms: 1.09x slower                                        |
| Geometric mean       | (ref)                                                                     | 1.03x faster                                                 |

Benchmark hidden because not significant (3): unpickle, pickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6+-06249ec |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.0 ms: 1.03x slower                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.31 ms: 1.08x slower                                        |
| Geometric mean         | (ref)                                                                     | 1.05x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6+-06249ec |
|-----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 10.9 ms                                                                   | 10.1 ms: 1.08x faster                                        |
| genshi_xml      | 57.8 ms                                                                   | 56.5 ms: 1.02x faster                                        |
| django_template | 39.6 ms                                                                   | 39.9 ms: 1.01x slower                                        |
| Geometric mean  | (ref)                                                                     | 1.02x faster                                                 |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6+-06249ec |
|-------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 385 ms: 1.95x faster                                         |
| generators              | 56.0 ms                                                                   | 38.7 ms: 1.45x faster                                        |
| json_dumps              | 13.4 ms                                                                   | 10.4 ms: 1.28x faster                                        |
| json_loads              | 28.4 us                                                                   | 23.9 us: 1.19x faster                                        |
| mypy2                   | 446 ms                                                                    | 386 ms: 1.16x faster                                         |
| scimark_lu              | 114 ms                                                                    | 101 ms: 1.13x faster                                         |
| coroutines              | 29.5 ms                                                                   | 26.2 ms: 1.13x faster                                        |
| xml_etree_parse         | 161 ms                                                                    | 143 ms: 1.12x faster                                         |
| unpickle_pure_python    | 238 us                                                                    | 215 us: 1.11x faster                                         |
| json                    | 5.59 ms                                                                   | 5.05 ms: 1.11x faster                                        |
| tornado_http            | 125 ms                                                                    | 113 ms: 1.10x faster                                         |
| deltablue               | 3.99 ms                                                                   | 3.63 ms: 1.10x faster                                        |
| logging_silent          | 103 ns                                                                    | 94.8 ns: 1.08x faster                                        |
| mako                    | 10.9 ms                                                                   | 10.1 ms: 1.08x faster                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.78 ms: 1.07x faster                                        |
| chaos                   | 76.2 ms                                                                   | 71.4 ms: 1.07x faster                                        |
| mdp                     | 2.73 sec                                                                  | 2.57 sec: 1.06x faster                                       |
| nbody                   | 92.1 ms                                                                   | 86.8 ms: 1.06x faster                                        |
| chameleon               | 7.50 ms                                                                   | 7.16 ms: 1.05x faster                                        |
| scimark_fft             | 276 ms                                                                    | 264 ms: 1.05x faster                                         |
| regex_v8                | 24.4 ms                                                                   | 23.4 ms: 1.05x faster                                        |
| gc_traversal            | 4.22 ms                                                                   | 4.04 ms: 1.04x faster                                        |
| unpack_sequence         | 45.9 ns                                                                   | 44.0 ns: 1.04x faster                                        |
| dulwich_log             | 69.1 ms                                                                   | 66.4 ms: 1.04x faster                                        |
| async_tree_memoization  | 639 ms                                                                    | 614 ms: 1.04x faster                                         |
| pycparser               | 1.30 sec                                                                  | 1.26 sec: 1.03x faster                                       |
| hexiom                  | 7.00 ms                                                                   | 6.77 ms: 1.03x faster                                        |
| regex_compile           | 154 ms                                                                    | 150 ms: 1.03x faster                                         |
| float                   | 75.7 ms                                                                   | 73.7 ms: 1.03x faster                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 103 ms: 1.02x faster                                         |
| async_tree_none         | 529 ms                                                                    | 516 ms: 1.02x faster                                         |
| raytrace                | 303 ms                                                                    | 296 ms: 1.02x faster                                         |
| genshi_xml              | 57.8 ms                                                                   | 56.5 ms: 1.02x faster                                        |
| deepcopy_memo           | 37.0 us                                                                   | 36.2 us: 1.02x faster                                        |
| coverage                | 86.0 ms                                                                   | 84.4 ms: 1.02x faster                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 83.5 ms: 1.02x faster                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.57 sec: 1.02x faster                                       |
| docutils                | 2.86 sec                                                                  | 2.82 sec: 1.01x faster                                       |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                       |
| spectral_norm           | 95.1 ms                                                                   | 94.1 ms: 1.01x faster                                        |
| sympy_expand            | 547 ms                                                                    | 541 ms: 1.01x faster                                         |
| fannkuch                | 449 ms                                                                    | 445 ms: 1.01x faster                                         |
| meteor_contest          | 129 ms                                                                    | 128 ms: 1.01x faster                                         |
| sqlglot_normalize       | 122 ms                                                                    | 121 ms: 1.01x faster                                         |
| 2to3                    | 289 ms                                                                    | 288 ms: 1.01x faster                                         |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.8 ms: 1.00x slower                                        |
| sympy_str               | 333 ms                                                                    | 334 ms: 1.01x slower                                         |
| django_template         | 39.6 ms                                                                   | 39.9 ms: 1.01x slower                                        |
| logging_simple          | 6.95 us                                                                   | 7.03 us: 1.01x slower                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.6 ms: 1.01x slower                                        |
| pickle_dict             | 31.1 us                                                                   | 31.5 us: 1.01x slower                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.38 ms: 1.02x slower                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.68 ms: 1.02x slower                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 4.65 ms: 1.02x slower                                        |
| regex_dna               | 225 ms                                                                    | 231 ms: 1.03x slower                                         |
| logging_format          | 7.84 us                                                                   | 8.05 us: 1.03x slower                                        |
| pathlib                 | 19.2 ms                                                                   | 19.7 ms: 1.03x slower                                        |
| sympy_sum               | 182 ms                                                                    | 188 ms: 1.03x slower                                         |
| python_startup          | 10.7 ms                                                                   | 11.0 ms: 1.03x slower                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.50 us: 1.03x slower                                        |
| pickle_list             | 3.78 us                                                                   | 3.90 us: 1.03x slower                                        |
| telco                   | 6.70 ms                                                                   | 6.93 ms: 1.03x slower                                        |
| pidigits                | 252 ms                                                                    | 260 ms: 1.03x slower                                         |
| pickle                  | 9.92 us                                                                   | 10.3 us: 1.04x slower                                        |
| deepcopy                | 384 us                                                                    | 398 us: 1.04x slower                                         |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.96 ms: 1.04x slower                                        |
| scimark_sor             | 109 ms                                                                    | 114 ms: 1.04x slower                                         |
| sqlglot_parse           | 1.53 ms                                                                   | 1.60 ms: 1.05x slower                                        |
| pyflate                 | 438 ms                                                                    | 459 ms: 1.05x slower                                         |
| sqlite_synth            | 2.49 us                                                                   | 2.62 us: 1.05x slower                                        |
| nqueens                 | 101 ms                                                                    | 106 ms: 1.05x slower                                         |
| xml_etree_process       | 55.8 ms                                                                   | 60.0 ms: 1.07x slower                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.31 ms: 1.08x slower                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 86.2 ms: 1.09x slower                                        |
| go                      | 158 ms                                                                    | 173 ms: 1.09x slower                                         |
| comprehensions          | 24.7 us                                                                   | 27.7 us: 1.12x slower                                        |
| async_generators        | 318 ms                                                                    | 391 ms: 1.23x slower                                         |
| dask                    | 418 ms                                                                    | 577 ms: 1.38x slower                                         |
| Geometric mean          | (ref)                                                                     | 1.02x faster                                                 |

Benchmark hidden because not significant (11): scimark_monte_carlo, unpickle, bench_thread_pool, pickle_pure_python, unpickle_list, thrift, richards, async_tree_cpu_io_mixed, genshi_text, pprint_safe_repr, html5lib
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
