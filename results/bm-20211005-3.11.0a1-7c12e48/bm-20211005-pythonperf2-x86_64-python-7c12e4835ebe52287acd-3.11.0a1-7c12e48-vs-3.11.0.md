
# Results vs. 3.11.0

- fork: python
- ref: 7c12e4835ebe52287acd
- machine: linux-x86_64
- commit hash: 7c12e48
- commit date: 2021-10-05
- overall geometric mean: 1.11x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 329 ms: 1.14x slower                                                        |
| chameleon      | 7.50 ms                                                                   | 8.97 ms: 1.20x slower                                                       |
| docutils       | 2.86 sec                                                                  | 3.22 sec: 1.13x slower                                                      |
| html5lib       | 70.2 ms                                                                   | 83.0 ms: 1.18x slower                                                       |
| tornado_http   | 125 ms                                                                    | 136 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.14x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 252 ms                                                                    | 266 ms: 1.06x slower                                                        |
| float          | 75.7 ms                                                                   | 86.6 ms: 1.14x slower                                                       |
| nbody          | 92.1 ms                                                                   | 132 ms: 1.43x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.20x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.31 ms                                                                   | 3.05 ms: 1.08x faster                                                       |
| regex_v8       | 24.4 ms                                                                   | 25.6 ms: 1.05x slower                                                       |
| regex_compile  | 154 ms                                                                    | 169 ms: 1.10x slower                                                        |
| regex_dna      | 225 ms                                                                    | 262 ms: 1.16x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.05x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                   | 27.0 us: 1.05x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 158 ms: 1.01x faster                                                        |
| pickle_dict          | 31.1 us                                                                   | 31.5 us: 1.01x slower                                                       |
| json_dumps           | 13.4 ms                                                                   | 13.6 ms: 1.02x slower                                                       |
| unpickle             | 13.0 us                                                                   | 13.7 us: 1.05x slower                                                       |
| pickle               | 9.92 us                                                                   | 10.4 us: 1.05x slower                                                       |
| xml_etree_iterparse  | 106 ms                                                                    | 111 ms: 1.05x slower                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 86.0 ms: 1.09x slower                                                       |
| pickle_list          | 3.78 us                                                                   | 4.14 us: 1.09x slower                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 64.1 ms: 1.15x slower                                                       |
| unpickle_pure_python | 238 us                                                                    | 293 us: 1.23x slower                                                        |
| pickle_pure_python   | 319 us                                                                    | 394 us: 1.23x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.07x slower                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                                   | 7.57 ms: 1.02x faster                                                       |
| python_startup         | 10.7 ms                                                                   | 11.8 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                                     | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 59.9 ms: 1.04x slower                                                       |
| genshi_text     | 26.3 ms                                                                   | 28.3 ms: 1.08x slower                                                       |
| django_template | 39.6 ms                                                                   | 47.5 ms: 1.20x slower                                                       |
| mako            | 10.9 ms                                                                   | 13.1 ms: 1.20x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.13x slower                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| coverage                | 86.0 ms                                                                   | 72.0 ms: 1.19x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.55 ms: 1.19x faster                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.05 ms: 1.08x faster                                                       |
| logging_format          | 7.84 us                                                                   | 7.28 us: 1.08x faster                                                       |
| generators              | 56.0 ms                                                                   | 52.5 ms: 1.07x faster                                                       |
| json_loads              | 28.4 us                                                                   | 27.0 us: 1.05x faster                                                       |
| logging_simple          | 6.95 us                                                                   | 6.69 us: 1.04x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 28.5 ms: 1.03x faster                                                       |
| json                    | 5.59 ms                                                                   | 5.40 ms: 1.03x faster                                                       |
| async_tree_none         | 529 ms                                                                    | 515 ms: 1.03x faster                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.57 ms: 1.02x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 158 ms: 1.01x faster                                                        |
| telco                   | 6.70 ms                                                                   | 6.66 ms: 1.01x faster                                                       |
| sympy_sum               | 182 ms                                                                    | 184 ms: 1.01x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 31.5 us: 1.01x slower                                                       |
| nqueens                 | 101 ms                                                                    | 103 ms: 1.02x slower                                                        |
| json_dumps              | 13.4 ms                                                                   | 13.6 ms: 1.02x slower                                                       |
| meteor_contest          | 129 ms                                                                    | 133 ms: 1.03x slower                                                        |
| sympy_str               | 333 ms                                                                    | 343 ms: 1.03x slower                                                        |
| async_tree_memoization  | 639 ms                                                                    | 660 ms: 1.03x slower                                                        |
| dask                    | 418 ms                                                                    | 433 ms: 1.04x slower                                                        |
| genshi_xml              | 57.8 ms                                                                   | 59.9 ms: 1.04x slower                                                       |
| mdp                     | 2.73 sec                                                                  | 2.84 sec: 1.04x slower                                                      |
| unpickle                | 13.0 us                                                                   | 13.7 us: 1.05x slower                                                       |
| regex_v8                | 24.4 ms                                                                   | 25.6 ms: 1.05x slower                                                       |
| sympy_expand            | 547 ms                                                                    | 573 ms: 1.05x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.4 us: 1.05x slower                                                       |
| fannkuch                | 449 ms                                                                    | 472 ms: 1.05x slower                                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 111 ms: 1.05x slower                                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.24 sec: 1.05x slower                                                      |
| gunicorn                | 936 us                                                                    | 988 us: 1.06x slower                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 796 ms: 1.06x slower                                                        |
| pidigits                | 252 ms                                                                    | 266 ms: 1.06x slower                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 26.8 ms: 1.06x slower                                                       |
| dulwich_log             | 69.1 ms                                                                   | 74.2 ms: 1.07x slower                                                       |
| genshi_text             | 26.3 ms                                                                   | 28.3 ms: 1.08x slower                                                       |
| bench_thread_pool       | 990 us                                                                    | 1.07 ms: 1.08x slower                                                       |
| thrift                  | 942 us                                                                    | 1.02 ms: 1.08x slower                                                       |
| pycparser               | 1.30 sec                                                                  | 1.41 sec: 1.08x slower                                                      |
| xml_etree_generate      | 79.1 ms                                                                   | 86.0 ms: 1.09x slower                                                       |
| tornado_http            | 125 ms                                                                    | 136 ms: 1.09x slower                                                        |
| pathlib                 | 19.2 ms                                                                   | 20.9 ms: 1.09x slower                                                       |
| deepcopy_reduce         | 3.39 us                                                                   | 3.70 us: 1.09x slower                                                       |
| pickle_list             | 3.78 us                                                                   | 4.14 us: 1.09x slower                                                       |
| python_startup          | 10.7 ms                                                                   | 11.8 ms: 1.10x slower                                                       |
| regex_compile           | 154 ms                                                                    | 169 ms: 1.10x slower                                                        |
| sqlglot_normalize       | 122 ms                                                                    | 135 ms: 1.11x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.76 us: 1.11x slower                                                       |
| deepcopy                | 384 us                                                                    | 427 us: 1.11x slower                                                        |
| async_generators        | 318 ms                                                                    | 356 ms: 1.12x slower                                                        |
| docutils                | 2.86 sec                                                                  | 3.22 sec: 1.13x slower                                                      |
| bench_mp_pool           | 4.54 ms                                                                   | 5.14 ms: 1.13x slower                                                       |
| 2to3                    | 289 ms                                                                    | 329 ms: 1.14x slower                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 66.6 ms: 1.14x slower                                                       |
| float                   | 75.7 ms                                                                   | 86.6 ms: 1.14x slower                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.83 sec: 1.14x slower                                                      |
| pprint_safe_repr        | 768 ms                                                                    | 879 ms: 1.14x slower                                                        |
| chaos                   | 76.2 ms                                                                   | 87.5 ms: 1.15x slower                                                       |
| xml_etree_process       | 55.8 ms                                                                   | 64.1 ms: 1.15x slower                                                       |
| create_gc_cycles        | 1.65 ms                                                                   | 1.90 ms: 1.16x slower                                                       |
| regex_dna               | 225 ms                                                                    | 262 ms: 1.16x slower                                                        |
| hexiom                  | 7.00 ms                                                                   | 8.15 ms: 1.16x slower                                                       |
| html5lib                | 70.2 ms                                                                   | 83.0 ms: 1.18x slower                                                       |
| comprehensions          | 24.7 us                                                                   | 29.5 us: 1.19x slower                                                       |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.84 ms: 1.19x slower                                                       |
| chameleon               | 7.50 ms                                                                   | 8.97 ms: 1.20x slower                                                       |
| crypto_pyaes            | 85.0 ms                                                                   | 102 ms: 1.20x slower                                                        |
| django_template         | 39.6 ms                                                                   | 47.5 ms: 1.20x slower                                                       |
| mako                    | 10.9 ms                                                                   | 13.1 ms: 1.20x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 333 ms: 1.21x slower                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 44.7 us: 1.21x slower                                                       |
| raytrace                | 303 ms                                                                    | 371 ms: 1.22x slower                                                        |
| unpickle_pure_python    | 238 us                                                                    | 293 us: 1.23x slower                                                        |
| pickle_pure_python      | 319 us                                                                    | 394 us: 1.23x slower                                                        |
| spectral_norm           | 95.1 ms                                                                   | 120 ms: 1.26x slower                                                        |
| scimark_lu              | 114 ms                                                                    | 145 ms: 1.27x slower                                                        |
| flaskblogging           | 3.81 ms                                                                   | 4.88 ms: 1.28x slower                                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 87.3 ms: 1.29x slower                                                       |
| logging_silent          | 103 ns                                                                    | 134 ns: 1.31x slower                                                        |
| richards                | 49.1 ms                                                                   | 64.9 ms: 1.32x slower                                                       |
| go                      | 158 ms                                                                    | 211 ms: 1.34x slower                                                        |
| scimark_sor             | 109 ms                                                                    | 147 ms: 1.34x slower                                                        |
| pyflate                 | 438 ms                                                                    | 615 ms: 1.41x slower                                                        |
| nbody                   | 92.1 ms                                                                   | 132 ms: 1.43x slower                                                        |
| deltablue               | 3.99 ms                                                                   | 5.73 ms: 1.43x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.76 ms: 1.47x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 2.37 ms: 1.55x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.11x slower                                                                |

Benchmark hidden because not significant (2): unpickle_list, unpack_sequence
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, asyncio_tcp, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
