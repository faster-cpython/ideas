
# Results vs. 3.11.0

- fork: python
- ref: 2e91dba437fe5c56c6f8
- machine: linux-x86_64
- commit hash: 2e91dba
- commit date: 2021-12-08
- overall geometric mean: 1.06x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 293 ms: 1.01x slower                                                        |
| chameleon      | 7.50 ms                                                                   | 8.85 ms: 1.18x slower                                                       |
| docutils       | 2.86 sec                                                                  | 3.02 sec: 1.06x slower                                                      |
| html5lib       | 70.2 ms                                                                   | 75.1 ms: 1.07x slower                                                       |
| tornado_http   | 125 ms                                                                    | 135 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.08x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 252 ms                                                                    | 253 ms: 1.01x slower                                                        |
| float          | 75.7 ms                                                                   | 80.9 ms: 1.07x slower                                                       |
| nbody          | 92.1 ms                                                                   | 109 ms: 1.18x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.08x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.31 ms                                                                   | 3.10 ms: 1.07x faster                                                       |
| regex_compile  | 154 ms                                                                    | 153 ms: 1.01x faster                                                        |
| regex_v8       | 24.4 ms                                                                   | 25.7 ms: 1.05x slower                                                       |
| regex_dna      | 225 ms                                                                    | 261 ms: 1.16x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.03x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                   | 25.3 us: 1.12x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 155 ms: 1.03x faster                                                        |
| unpickle             | 13.0 us                                                                   | 13.2 us: 1.01x slower                                                       |
| pickle               | 9.92 us                                                                   | 10.2 us: 1.03x slower                                                       |
| xml_etree_iterparse  | 106 ms                                                                    | 110 ms: 1.04x slower                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 82.8 ms: 1.05x slower                                                       |
| json_dumps           | 13.4 ms                                                                   | 14.1 ms: 1.05x slower                                                       |
| pickle_dict          | 31.1 us                                                                   | 33.0 us: 1.06x slower                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 60.9 ms: 1.09x slower                                                       |
| unpickle_pure_python | 238 us                                                                    | 265 us: 1.11x slower                                                        |
| pickle_list          | 3.78 us                                                                   | 4.32 us: 1.14x slower                                                       |
| pickle_pure_python   | 319 us                                                                    | 366 us: 1.15x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.04x slower                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                                   | 7.14 ms: 1.08x faster                                                       |
| python_startup         | 10.7 ms                                                                   | 10.1 ms: 1.06x faster                                                       |
| Geometric mean         | (ref)                                                                     | 1.07x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 59.7 ms: 1.03x slower                                                       |
| genshi_text     | 26.3 ms                                                                   | 28.2 ms: 1.07x slower                                                       |
| django_template | 39.6 ms                                                                   | 44.9 ms: 1.13x slower                                                       |
| mako            | 10.9 ms                                                                   | 12.9 ms: 1.18x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.10x slower                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| coverage                | 86.0 ms                                                                   | 72.1 ms: 1.19x faster                                                       |
| json_loads              | 28.4 us                                                                   | 25.3 us: 1.12x faster                                                       |
| generators              | 56.0 ms                                                                   | 50.1 ms: 1.12x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 27.0 ms: 1.09x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.89 ms: 1.08x faster                                                       |
| python_startup_no_site  | 7.73 ms                                                                   | 7.14 ms: 1.08x faster                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.10 ms: 1.07x faster                                                       |
| json                    | 5.59 ms                                                                   | 5.24 ms: 1.07x faster                                                       |
| python_startup          | 10.7 ms                                                                   | 10.1 ms: 1.06x faster                                                       |
| fannkuch                | 449 ms                                                                    | 428 ms: 1.05x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 110 ms: 1.04x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 155 ms: 1.03x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.70 us: 1.02x faster                                                       |
| regex_compile           | 154 ms                                                                    | 153 ms: 1.01x faster                                                        |
| meteor_contest          | 129 ms                                                                    | 129 ms: 1.00x faster                                                        |
| async_generators        | 318 ms                                                                    | 319 ms: 1.00x slower                                                        |
| pidigits                | 252 ms                                                                    | 253 ms: 1.01x slower                                                        |
| unpickle                | 13.0 us                                                                   | 13.2 us: 1.01x slower                                                       |
| logging_simple          | 6.95 us                                                                   | 7.04 us: 1.01x slower                                                       |
| 2to3                    | 289 ms                                                                    | 293 ms: 1.01x slower                                                        |
| mdp                     | 2.73 sec                                                                  | 2.76 sec: 1.01x slower                                                      |
| nqueens                 | 101 ms                                                                    | 103 ms: 1.02x slower                                                        |
| chaos                   | 76.2 ms                                                                   | 78.3 ms: 1.03x slower                                                       |
| async_tree_none         | 529 ms                                                                    | 545 ms: 1.03x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.2 us: 1.03x slower                                                       |
| genshi_xml              | 57.8 ms                                                                   | 59.7 ms: 1.03x slower                                                       |
| pycparser               | 1.30 sec                                                                  | 1.35 sec: 1.03x slower                                                      |
| sympy_sum               | 182 ms                                                                    | 189 ms: 1.04x slower                                                        |
| pathlib                 | 19.2 ms                                                                   | 19.9 ms: 1.04x slower                                                       |
| xml_etree_iterparse     | 106 ms                                                                    | 110 ms: 1.04x slower                                                        |
| dask                    | 418 ms                                                                    | 435 ms: 1.04x slower                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.55 us: 1.05x slower                                                       |
| xml_etree_generate      | 79.1 ms                                                                   | 82.8 ms: 1.05x slower                                                       |
| sympy_integrate         | 25.3 ms                                                                   | 26.5 ms: 1.05x slower                                                       |
| spectral_norm           | 95.1 ms                                                                   | 99.9 ms: 1.05x slower                                                       |
| json_dumps              | 13.4 ms                                                                   | 14.1 ms: 1.05x slower                                                       |
| regex_v8                | 24.4 ms                                                                   | 25.7 ms: 1.05x slower                                                       |
| sympy_str               | 333 ms                                                                    | 350 ms: 1.05x slower                                                        |
| dulwich_log             | 69.1 ms                                                                   | 73.0 ms: 1.06x slower                                                       |
| thrift                  | 942 us                                                                    | 995 us: 1.06x slower                                                        |
| scimark_sor             | 109 ms                                                                    | 115 ms: 1.06x slower                                                        |
| docutils                | 2.86 sec                                                                  | 3.02 sec: 1.06x slower                                                      |
| hexiom                  | 7.00 ms                                                                   | 7.41 ms: 1.06x slower                                                       |
| sympy_expand            | 547 ms                                                                    | 579 ms: 1.06x slower                                                        |
| telco                   | 6.70 ms                                                                   | 7.11 ms: 1.06x slower                                                       |
| pickle_dict             | 31.1 us                                                                   | 33.0 us: 1.06x slower                                                       |
| float                   | 75.7 ms                                                                   | 80.9 ms: 1.07x slower                                                       |
| bench_thread_pool       | 990 us                                                                    | 1.06 ms: 1.07x slower                                                       |
| html5lib                | 70.2 ms                                                                   | 75.1 ms: 1.07x slower                                                       |
| gunicorn                | 936 us                                                                    | 1.00 ms: 1.07x slower                                                       |
| async_tree_memoization  | 639 ms                                                                    | 686 ms: 1.07x slower                                                        |
| genshi_text             | 26.3 ms                                                                   | 28.2 ms: 1.07x slower                                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 811 ms: 1.08x slower                                                        |
| tornado_http            | 125 ms                                                                    | 135 ms: 1.08x slower                                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 4.90 ms: 1.08x slower                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 832 ms: 1.08x slower                                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.74 sec: 1.09x slower                                                      |
| sqlite_synth            | 2.49 us                                                                   | 2.70 us: 1.09x slower                                                       |
| sqlglot_normalize       | 122 ms                                                                    | 133 ms: 1.09x slower                                                        |
| deepcopy                | 384 us                                                                    | 418 us: 1.09x slower                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 60.9 ms: 1.09x slower                                                       |
| go                      | 158 ms                                                                    | 173 ms: 1.09x slower                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 64.7 ms: 1.10x slower                                                       |
| async_tree_io           | 1.18 sec                                                                  | 1.32 sec: 1.11x slower                                                      |
| crypto_pyaes            | 85.0 ms                                                                   | 94.7 ms: 1.11x slower                                                       |
| unpickle_pure_python    | 238 us                                                                    | 265 us: 1.11x slower                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 41.5 us: 1.12x slower                                                       |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.58 ms: 1.13x slower                                                       |
| logging_silent          | 103 ns                                                                    | 116 ns: 1.13x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 76.7 ms: 1.13x slower                                                       |
| django_template         | 39.6 ms                                                                   | 44.9 ms: 1.13x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 314 ms: 1.14x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 4.32 us: 1.14x slower                                                       |
| raytrace                | 303 ms                                                                    | 347 ms: 1.14x slower                                                        |
| pickle_pure_python      | 319 us                                                                    | 366 us: 1.15x slower                                                        |
| richards                | 49.1 ms                                                                   | 56.7 ms: 1.15x slower                                                       |
| regex_dna               | 225 ms                                                                    | 261 ms: 1.16x slower                                                        |
| nbody                   | 92.1 ms                                                                   | 109 ms: 1.18x slower                                                        |
| chameleon               | 7.50 ms                                                                   | 8.85 ms: 1.18x slower                                                       |
| mako                    | 10.9 ms                                                                   | 12.9 ms: 1.18x slower                                                       |
| deltablue               | 3.99 ms                                                                   | 4.78 ms: 1.20x slower                                                       |
| pyflate                 | 438 ms                                                                    | 525 ms: 1.20x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 30.6 us: 1.24x slower                                                       |
| flaskblogging           | 3.81 ms                                                                   | 4.95 ms: 1.30x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.60 ms: 1.38x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 2.21 ms: 1.44x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.06x slower                                                                |

Benchmark hidden because not significant (3): unpickle_list, create_gc_cycles, unpack_sequence
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, asyncio_tcp, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
