
# Results vs. 3.11.0

- fork: python
- ref: 7c12e4835ebe52287acd
- machine: linux-x86_64
- commit hash: 7c12e48
- commit date: 2021-10-05
- overall geometric mean: 1.16x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 329 ms: 1.28x slower                                                        |
| chameleon      | 6.52 ms                                                             | 8.97 ms: 1.38x slower                                                       |
| docutils       | 2.59 sec                                                            | 3.22 sec: 1.24x slower                                                      |
| html5lib       | 64.0 ms                                                             | 83.0 ms: 1.30x slower                                                       |
| tornado_http   | 96.7 ms                                                             | 136 ms: 1.41x slower                                                        |
| Geometric mean | (ref)                                                               | 1.32x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 76.0 ms                                                             | 86.6 ms: 1.14x slower                                                       |
| pidigits       | 197 ms                                                              | 266 ms: 1.35x slower                                                        |
| nbody          | 96.7 ms                                                             | 132 ms: 1.36x slower                                                        |
| Geometric mean | (ref)                                                               | 1.28x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.32 ms                                                             | 3.05 ms: 1.09x faster                                                       |
| regex_v8       | 22.0 ms                                                             | 25.6 ms: 1.17x slower                                                       |
| regex_compile  | 137 ms                                                              | 169 ms: 1.24x slower                                                        |
| regex_dna      | 196 ms                                                              | 262 ms: 1.33x slower                                                        |
| Geometric mean | (ref)                                                               | 1.15x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list        | 4.96 us                                                             | 4.54 us: 1.09x faster                                                       |
| xml_etree_parse      | 162 ms                                                              | 158 ms: 1.02x faster                                                        |
| pickle_dict          | 30.9 us                                                             | 31.5 us: 1.02x slower                                                       |
| pickle_list          | 4.03 us                                                             | 4.14 us: 1.03x slower                                                       |
| json_loads           | 26.2 us                                                             | 27.0 us: 1.03x slower                                                       |
| xml_etree_iterparse  | 108 ms                                                              | 111 ms: 1.03x slower                                                        |
| unpickle             | 13.2 us                                                             | 13.7 us: 1.03x slower                                                       |
| pickle               | 9.79 us                                                             | 10.4 us: 1.06x slower                                                       |
| json_dumps           | 12.5 ms                                                             | 13.6 ms: 1.09x slower                                                       |
| xml_etree_generate   | 76.5 ms                                                             | 86.0 ms: 1.12x slower                                                       |
| xml_etree_process    | 54.1 ms                                                             | 64.1 ms: 1.18x slower                                                       |
| pickle_pure_python   | 307 us                                                              | 394 us: 1.28x slower                                                        |
| unpickle_pure_python | 228 us                                                              | 293 us: 1.28x slower                                                        |
| Geometric mean       | (ref)                                                               | 1.08x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 5.98 ms                                                             | 7.57 ms: 1.27x slower                                                       |
| python_startup         | 8.49 ms                                                             | 11.8 ms: 1.39x slower                                                       |
| Geometric mean         | (ref)                                                               | 1.33x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 59.9 ms: 1.16x slower                                                       |
| genshi_text     | 21.8 ms                                                             | 28.3 ms: 1.29x slower                                                       |
| mako            | 9.82 ms                                                             | 13.1 ms: 1.33x slower                                                       |
| django_template | 32.9 ms                                                             | 47.5 ms: 1.44x slower                                                       |
| Geometric mean  | (ref)                                                               | 1.30x slower                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| bench_mp_pool           | 24.0 ms                                                             | 5.14 ms: 4.67x faster                                                       |
| flaskblogging           | 7.09 ms                                                             | 4.88 ms: 1.45x faster                                                       |
| coverage                | 101 ms                                                              | 72.0 ms: 1.40x faster                                                       |
| generators              | 73.4 ms                                                             | 52.5 ms: 1.40x faster                                                       |
| gunicorn                | 1.13 ms                                                             | 988 us: 1.14x faster                                                        |
| unpickle_list           | 4.96 us                                                             | 4.54 us: 1.09x faster                                                       |
| regex_effbot            | 3.32 ms                                                             | 3.05 ms: 1.09x faster                                                       |
| unpack_sequence         | 49.5 ns                                                             | 46.5 ns: 1.06x faster                                                       |
| async_tree_io           | 1.28 sec                                                            | 1.24 sec: 1.03x faster                                                      |
| xml_etree_parse         | 162 ms                                                              | 158 ms: 1.02x faster                                                        |
| gc_traversal            | 3.63 ms                                                             | 3.55 ms: 1.02x faster                                                       |
| async_tree_none         | 525 ms                                                              | 515 ms: 1.02x faster                                                        |
| async_generators        | 361 ms                                                              | 356 ms: 1.01x faster                                                        |
| telco                   | 6.59 ms                                                             | 6.66 ms: 1.01x slower                                                       |
| scimark_fft             | 328 ms                                                              | 333 ms: 1.02x slower                                                        |
| pickle_dict             | 30.9 us                                                             | 31.5 us: 1.02x slower                                                       |
| pickle_list             | 4.03 us                                                             | 4.14 us: 1.03x slower                                                       |
| json_loads              | 26.2 us                                                             | 27.0 us: 1.03x slower                                                       |
| xml_etree_iterparse     | 108 ms                                                              | 111 ms: 1.03x slower                                                        |
| unpickle                | 13.2 us                                                             | 13.7 us: 1.03x slower                                                       |
| async_tree_memoization  | 621 ms                                                              | 660 ms: 1.06x slower                                                        |
| pickle                  | 9.79 us                                                             | 10.4 us: 1.06x slower                                                       |
| mdp                     | 2.64 sec                                                            | 2.84 sec: 1.08x slower                                                      |
| async_tree_cpu_io_mixed | 736 ms                                                              | 796 ms: 1.08x slower                                                        |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.84 ms: 1.08x slower                                                       |
| coroutines              | 26.3 ms                                                             | 28.5 ms: 1.08x slower                                                       |
| json_dumps              | 12.5 ms                                                             | 13.6 ms: 1.09x slower                                                       |
| sqlite_synth            | 2.51 us                                                             | 2.76 us: 1.10x slower                                                       |
| logging_format          | 6.64 us                                                             | 7.28 us: 1.10x slower                                                       |
| logging_simple          | 6.09 us                                                             | 6.69 us: 1.10x slower                                                       |
| sympy_sum               | 167 ms                                                              | 184 ms: 1.10x slower                                                        |
| json                    | 4.86 ms                                                             | 5.40 ms: 1.11x slower                                                       |
| xml_etree_generate      | 76.5 ms                                                             | 86.0 ms: 1.12x slower                                                       |
| float                   | 76.0 ms                                                             | 86.6 ms: 1.14x slower                                                       |
| pathlib                 | 18.2 ms                                                             | 20.9 ms: 1.15x slower                                                       |
| genshi_xml              | 51.8 ms                                                             | 59.9 ms: 1.16x slower                                                       |
| dulwich_log             | 63.6 ms                                                             | 74.2 ms: 1.17x slower                                                       |
| regex_v8                | 22.0 ms                                                             | 25.6 ms: 1.17x slower                                                       |
| dask                    | 368 ms                                                              | 433 ms: 1.18x slower                                                        |
| sympy_str               | 291 ms                                                              | 343 ms: 1.18x slower                                                        |
| xml_etree_process       | 54.1 ms                                                             | 64.1 ms: 1.18x slower                                                       |
| sympy_expand            | 477 ms                                                              | 573 ms: 1.20x slower                                                        |
| spectral_norm           | 99.5 ms                                                             | 120 ms: 1.21x slower                                                        |
| nqueens                 | 84.0 ms                                                             | 103 ms: 1.22x slower                                                        |
| deepcopy_memo           | 36.4 us                                                             | 44.7 us: 1.23x slower                                                       |
| fannkuch                | 384 ms                                                              | 472 ms: 1.23x slower                                                        |
| pycparser               | 1.14 sec                                                            | 1.41 sec: 1.23x slower                                                      |
| regex_compile           | 137 ms                                                              | 169 ms: 1.24x slower                                                        |
| docutils                | 2.59 sec                                                            | 3.22 sec: 1.24x slower                                                      |
| sqlglot_normalize       | 108 ms                                                              | 135 ms: 1.25x slower                                                        |
| sqlglot_optimize        | 53.4 ms                                                             | 66.6 ms: 1.25x slower                                                       |
| deepcopy_reduce         | 2.96 us                                                             | 3.70 us: 1.25x slower                                                       |
| meteor_contest          | 106 ms                                                              | 133 ms: 1.25x slower                                                        |
| pprint_safe_repr        | 701 ms                                                              | 879 ms: 1.25x slower                                                        |
| hexiom                  | 6.48 ms                                                             | 8.15 ms: 1.26x slower                                                       |
| deepcopy                | 339 us                                                              | 427 us: 1.26x slower                                                        |
| pprint_pformat          | 1.45 sec                                                            | 1.83 sec: 1.26x slower                                                      |
| python_startup_no_site  | 5.98 ms                                                             | 7.57 ms: 1.27x slower                                                       |
| raytrace                | 292 ms                                                              | 371 ms: 1.27x slower                                                        |
| sympy_integrate         | 21.0 ms                                                             | 26.8 ms: 1.27x slower                                                       |
| 2to3                    | 257 ms                                                              | 329 ms: 1.28x slower                                                        |
| scimark_sor             | 115 ms                                                              | 147 ms: 1.28x slower                                                        |
| pickle_pure_python      | 307 us                                                              | 394 us: 1.28x slower                                                        |
| unpickle_pure_python    | 228 us                                                              | 293 us: 1.28x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                             | 87.3 ms: 1.29x slower                                                       |
| chaos                   | 68.0 ms                                                             | 87.5 ms: 1.29x slower                                                       |
| create_gc_cycles        | 1.48 ms                                                             | 1.90 ms: 1.29x slower                                                       |
| genshi_text             | 21.8 ms                                                             | 28.3 ms: 1.29x slower                                                       |
| html5lib                | 64.0 ms                                                             | 83.0 ms: 1.30x slower                                                       |
| bench_thread_pool       | 820 us                                                              | 1.07 ms: 1.30x slower                                                       |
| comprehensions          | 22.2 us                                                             | 29.5 us: 1.33x slower                                                       |
| thrift                  | 766 us                                                              | 1.02 ms: 1.33x slower                                                       |
| mako                    | 9.82 ms                                                             | 13.1 ms: 1.33x slower                                                       |
| regex_dna               | 196 ms                                                              | 262 ms: 1.33x slower                                                        |
| scimark_lu              | 108 ms                                                              | 145 ms: 1.34x slower                                                        |
| pidigits                | 197 ms                                                              | 266 ms: 1.35x slower                                                        |
| logging_silent          | 98.7 ns                                                             | 134 ns: 1.36x slower                                                        |
| nbody                   | 96.7 ms                                                             | 132 ms: 1.36x slower                                                        |
| chameleon               | 6.52 ms                                                             | 8.97 ms: 1.38x slower                                                       |
| crypto_pyaes            | 73.8 ms                                                             | 102 ms: 1.38x slower                                                        |
| python_startup          | 8.49 ms                                                             | 11.8 ms: 1.39x slower                                                       |
| tornado_http            | 96.7 ms                                                             | 136 ms: 1.41x slower                                                        |
| richards                | 45.7 ms                                                             | 64.9 ms: 1.42x slower                                                       |
| django_template         | 32.9 ms                                                             | 47.5 ms: 1.44x slower                                                       |
| pyflate                 | 414 ms                                                              | 615 ms: 1.49x slower                                                        |
| go                      | 138 ms                                                              | 211 ms: 1.53x slower                                                        |
| deltablue               | 3.66 ms                                                             | 5.73 ms: 1.57x slower                                                       |
| sqlglot_transpile       | 1.65 ms                                                             | 2.76 ms: 1.67x slower                                                       |
| sqlglot_parse           | 1.36 ms                                                             | 2.37 ms: 1.74x slower                                                       |
| Geometric mean          | (ref)                                                               | 1.16x slower                                                                |
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, asyncio_tcp, djangocms, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
