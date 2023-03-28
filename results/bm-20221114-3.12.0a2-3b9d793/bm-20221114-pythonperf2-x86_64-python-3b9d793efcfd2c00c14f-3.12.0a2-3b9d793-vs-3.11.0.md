
# Results vs. 3.11.0

- fork: python
- ref: 3b9d793efcfd2c00c14f
- machine: linux-x86_64
- commit hash: 3b9d793
- commit date: 2022-11-14
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf2-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 282 ms: 1.02x faster                                                        |
| chameleon      | 7.50 ms                                                                   | 7.19 ms: 1.04x faster                                                       |
| docutils       | 2.86 sec                                                                  | 2.77 sec: 1.03x faster                                                      |
| html5lib       | 70.2 ms                                                                   | 66.7 ms: 1.05x faster                                                       |
| tornado_http   | 125 ms                                                                    | 115 ms: 1.08x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.05x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf2-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 73.2 ms: 1.03x faster                                                       |
| nbody          | 92.1 ms                                                                   | 90.9 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf2-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 23.2 ms: 1.06x faster                                                       |
| regex_compile  | 154 ms                                                                    | 147 ms: 1.05x faster                                                        |
| regex_dna      | 225 ms                                                                    | 227 ms: 1.01x slower                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.45 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf2-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.2 ms: 1.31x faster                                                       |
| json_loads           | 28.4 us                                                                   | 23.7 us: 1.20x faster                                                       |
| unpickle_pure_python | 238 us                                                                    | 209 us: 1.14x faster                                                        |
| xml_etree_parse      | 161 ms                                                                    | 143 ms: 1.13x faster                                                        |
| pickle_list          | 3.78 us                                                                   | 3.65 us: 1.04x faster                                                       |
| unpickle             | 13.0 us                                                                   | 12.6 us: 1.03x faster                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 54.8 ms: 1.02x faster                                                       |
| pickle_pure_python   | 319 us                                                                    | 314 us: 1.02x faster                                                        |
| pickle               | 9.92 us                                                                   | 10.1 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 106 ms                                                                    | 108 ms: 1.02x slower                                                        |
| pickle_dict          | 31.1 us                                                                   | 33.4 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.05x faster                                                                |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf2-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.8 ms: 1.01x slower                                                       |
| python_startup_no_site | 7.73 ms                                                                   | 7.87 ms: 1.02x slower                                                       |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf2-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml     | 57.8 ms                                                                   | 54.0 ms: 1.07x faster                                                       |
| mako           | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                       |
| genshi_text    | 26.3 ms                                                                   | 25.2 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                                |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf2-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 13.4 ms                                                                   | 10.2 ms: 1.31x faster                                                       |
| json_loads              | 28.4 us                                                                   | 23.7 us: 1.20x faster                                                       |
| mypy2                   | 446 ms                                                                    | 374 ms: 1.19x faster                                                        |
| fannkuch                | 449 ms                                                                    | 391 ms: 1.15x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 209 us: 1.14x faster                                                        |
| json                    | 5.59 ms                                                                   | 4.95 ms: 1.13x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 143 ms: 1.13x faster                                                        |
| deltablue               | 3.99 ms                                                                   | 3.64 ms: 1.10x faster                                                       |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.74 ms: 1.09x faster                                                       |
| tornado_http            | 125 ms                                                                    | 115 ms: 1.08x faster                                                        |
| richards                | 49.1 ms                                                                   | 45.4 ms: 1.08x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.92 ms: 1.08x faster                                                       |
| genshi_xml              | 57.8 ms                                                                   | 54.0 ms: 1.07x faster                                                       |
| mako                    | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                       |
| aiohttp                 | 959 us                                                                    | 904 us: 1.06x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 27.9 ms: 1.06x faster                                                       |
| gunicorn                | 936 us                                                                    | 886 us: 1.06x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 23.2 ms: 1.06x faster                                                       |
| crypto_pyaes            | 85.0 ms                                                                   | 80.7 ms: 1.05x faster                                                       |
| html5lib                | 70.2 ms                                                                   | 66.7 ms: 1.05x faster                                                       |
| regex_compile           | 154 ms                                                                    | 147 ms: 1.05x faster                                                        |
| pycparser               | 1.30 sec                                                                  | 1.24 sec: 1.05x faster                                                      |
| chaos                   | 76.2 ms                                                                   | 72.9 ms: 1.05x faster                                                       |
| genshi_text             | 26.3 ms                                                                   | 25.2 ms: 1.04x faster                                                       |
| chameleon               | 7.50 ms                                                                   | 7.19 ms: 1.04x faster                                                       |
| pickle_list             | 3.78 us                                                                   | 3.65 us: 1.04x faster                                                       |
| hexiom                  | 7.00 ms                                                                   | 6.76 ms: 1.04x faster                                                       |
| logging_silent          | 103 ns                                                                    | 99.2 ns: 1.03x faster                                                       |
| float                   | 75.7 ms                                                                   | 73.2 ms: 1.03x faster                                                       |
| docutils                | 2.86 sec                                                                  | 2.77 sec: 1.03x faster                                                      |
| unpickle                | 13.0 us                                                                   | 12.6 us: 1.03x faster                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.55 sec: 1.03x faster                                                      |
| thrift                  | 942 us                                                                    | 913 us: 1.03x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.60 us: 1.03x faster                                                       |
| async_tree_memoization  | 639 ms                                                                    | 621 ms: 1.03x faster                                                        |
| dulwich_log             | 69.1 ms                                                                   | 67.2 ms: 1.03x faster                                                       |
| create_gc_cycles        | 1.65 ms                                                                   | 1.60 ms: 1.03x faster                                                       |
| scimark_lu              | 114 ms                                                                    | 111 ms: 1.03x faster                                                        |
| scimark_sor             | 109 ms                                                                    | 106 ms: 1.03x faster                                                        |
| logging_simple          | 6.95 us                                                                   | 6.78 us: 1.03x faster                                                       |
| 2to3                    | 289 ms                                                                    | 282 ms: 1.02x faster                                                        |
| pprint_safe_repr        | 768 ms                                                                    | 752 ms: 1.02x faster                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 66.4 ms: 1.02x faster                                                       |
| spectral_norm           | 95.1 ms                                                                   | 93.2 ms: 1.02x faster                                                       |
| xml_etree_process       | 55.8 ms                                                                   | 54.8 ms: 1.02x faster                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 1.50 ms: 1.02x faster                                                       |
| telco                   | 6.70 ms                                                                   | 6.58 ms: 1.02x faster                                                       |
| pickle_pure_python      | 319 us                                                                    | 314 us: 1.02x faster                                                        |
| dask                    | 418 ms                                                                    | 410 ms: 1.02x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 520 ms: 1.02x faster                                                        |
| nbody                   | 92.1 ms                                                                   | 90.9 ms: 1.01x faster                                                       |
| scimark_fft             | 276 ms                                                                    | 273 ms: 1.01x faster                                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                      |
| deepcopy_memo           | 37.0 us                                                                   | 36.7 us: 1.01x faster                                                       |
| meteor_contest          | 129 ms                                                                    | 129 ms: 1.01x faster                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.2 ms: 1.01x faster                                                       |
| asyncio_tcp             | 752 ms                                                                    | 749 ms: 1.00x faster                                                        |
| mdp                     | 2.73 sec                                                                  | 2.73 sec: 1.00x slower                                                      |
| pathlib                 | 19.2 ms                                                                   | 19.3 ms: 1.01x slower                                                       |
| sympy_expand            | 547 ms                                                                    | 550 ms: 1.01x slower                                                        |
| regex_dna               | 225 ms                                                                    | 227 ms: 1.01x slower                                                        |
| python_startup          | 10.7 ms                                                                   | 10.8 ms: 1.01x slower                                                       |
| raytrace                | 303 ms                                                                    | 305 ms: 1.01x slower                                                        |
| deepcopy                | 384 us                                                                    | 387 us: 1.01x slower                                                        |
| async_generators        | 318 ms                                                                    | 321 ms: 1.01x slower                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.5 ms: 1.01x slower                                                       |
| coverage                | 86.0 ms                                                                   | 86.9 ms: 1.01x slower                                                       |
| sympy_sum               | 182 ms                                                                    | 184 ms: 1.01x slower                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 762 ms: 1.01x slower                                                        |
| sympy_str               | 333 ms                                                                    | 337 ms: 1.01x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.1 us: 1.01x slower                                                       |
| go                      | 158 ms                                                                    | 160 ms: 1.02x slower                                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 108 ms: 1.02x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.87 ms: 1.02x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.57 us: 1.03x slower                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.45 ms: 1.04x slower                                                       |
| pickle_dict             | 31.1 us                                                                   | 33.4 us: 1.07x slower                                                       |
| comprehensions          | 24.7 us                                                                   | 26.9 us: 1.09x slower                                                       |
| generators              | 56.0 ms                                                                   | 61.2 ms: 1.09x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.03x faster                                                                |

Benchmark hidden because not significant (12): bench_thread_pool, pyflate, sqlglot_transpile, unpack_sequence, unpickle_list, deepcopy_reduce, pidigits, sqlglot_normalize, xml_etree_generate, django_template, bench_mp_pool, nqueens
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
