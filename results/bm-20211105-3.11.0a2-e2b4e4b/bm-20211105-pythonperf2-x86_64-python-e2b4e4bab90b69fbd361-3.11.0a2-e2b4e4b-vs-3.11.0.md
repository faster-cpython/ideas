
# Results vs. 3.11.0

- fork: python
- ref: e2b4e4bab90b69fbd361
- machine: linux-x86_64
- commit hash: e2b4e4b
- commit date: 2021-11-05
- overall geometric mean: 1.12x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 299 ms: 1.16x slower                                                        |
| chameleon      | 6.52 ms                                                             | 9.27 ms: 1.42x slower                                                       |
| docutils       | 2.59 sec                                                            | 3.05 sec: 1.18x slower                                                      |
| html5lib       | 64.0 ms                                                             | 80.0 ms: 1.25x slower                                                       |
| tornado_http   | 96.7 ms                                                             | 136 ms: 1.40x slower                                                        |
| Geometric mean | (ref)                                                               | 1.28x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 76.0 ms                                                             | 86.1 ms: 1.13x slower                                                       |
| nbody          | 96.7 ms                                                             | 113 ms: 1.17x slower                                                        |
| pidigits       | 197 ms                                                              | 264 ms: 1.34x slower                                                        |
| Geometric mean | (ref)                                                               | 1.21x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.32 ms                                                             | 3.06 ms: 1.08x faster                                                       |
| regex_compile  | 137 ms                                                              | 158 ms: 1.16x slower                                                        |
| regex_v8       | 22.0 ms                                                             | 25.8 ms: 1.18x slower                                                       |
| regex_dna      | 196 ms                                                              | 262 ms: 1.33x slower                                                        |
| Geometric mean | (ref)                                                               | 1.14x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list        | 4.96 us                                                             | 4.55 us: 1.09x faster                                                       |
| json_loads           | 26.2 us                                                             | 24.7 us: 1.06x faster                                                       |
| xml_etree_parse      | 162 ms                                                              | 157 ms: 1.03x faster                                                        |
| pickle_dict          | 30.9 us                                                             | 30.2 us: 1.02x faster                                                       |
| xml_etree_iterparse  | 108 ms                                                              | 107 ms: 1.00x faster                                                        |
| unpickle             | 13.2 us                                                             | 13.4 us: 1.01x slower                                                       |
| pickle_list          | 4.03 us                                                             | 4.17 us: 1.04x slower                                                       |
| pickle               | 9.79 us                                                             | 10.3 us: 1.05x slower                                                       |
| json_dumps           | 12.5 ms                                                             | 13.4 ms: 1.07x slower                                                       |
| xml_etree_generate   | 76.5 ms                                                             | 85.8 ms: 1.12x slower                                                       |
| xml_etree_process    | 54.1 ms                                                             | 61.7 ms: 1.14x slower                                                       |
| unpickle_pure_python | 228 us                                                              | 277 us: 1.21x slower                                                        |
| pickle_pure_python   | 307 us                                                              | 386 us: 1.26x slower                                                        |
| Geometric mean       | (ref)                                                               | 1.05x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 5.98 ms                                                             | 7.43 ms: 1.24x slower                                                       |
| python_startup         | 8.49 ms                                                             | 11.2 ms: 1.31x slower                                                       |
| Geometric mean         | (ref)                                                               | 1.28x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 57.9 ms: 1.12x slower                                                       |
| genshi_text     | 21.8 ms                                                             | 28.2 ms: 1.29x slower                                                       |
| mako            | 9.82 ms                                                             | 12.9 ms: 1.31x slower                                                       |
| django_template | 32.9 ms                                                             | 47.4 ms: 1.44x slower                                                       |
| Geometric mean  | (ref)                                                               | 1.29x slower                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| bench_mp_pool           | 24.0 ms                                                             | 5.01 ms: 4.79x faster                                                       |
| coverage                | 101 ms                                                              | 68.7 ms: 1.47x faster                                                       |
| flaskblogging           | 7.09 ms                                                             | 4.84 ms: 1.46x faster                                                       |
| generators              | 73.4 ms                                                             | 52.7 ms: 1.39x faster                                                       |
| gunicorn                | 1.13 ms                                                             | 980 us: 1.15x faster                                                        |
| async_generators        | 361 ms                                                              | 325 ms: 1.11x faster                                                        |
| unpickle_list           | 4.96 us                                                             | 4.55 us: 1.09x faster                                                       |
| regex_effbot            | 3.32 ms                                                             | 3.06 ms: 1.08x faster                                                       |
| unpack_sequence         | 49.5 ns                                                             | 46.0 ns: 1.07x faster                                                       |
| json_loads              | 26.2 us                                                             | 24.7 us: 1.06x faster                                                       |
| scimark_fft             | 328 ms                                                              | 311 ms: 1.05x faster                                                        |
| xml_etree_parse         | 162 ms                                                              | 157 ms: 1.03x faster                                                        |
| pickle_dict             | 30.9 us                                                             | 30.2 us: 1.02x faster                                                       |
| async_tree_io           | 1.28 sec                                                            | 1.27 sec: 1.01x faster                                                      |
| xml_etree_iterparse     | 108 ms                                                              | 107 ms: 1.00x faster                                                        |
| unpickle                | 13.2 us                                                             | 13.4 us: 1.01x slower                                                       |
| async_tree_none         | 525 ms                                                              | 532 ms: 1.01x slower                                                        |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.56 ms: 1.02x slower                                                       |
| telco                   | 6.59 ms                                                             | 6.81 ms: 1.03x slower                                                       |
| pickle_list             | 4.03 us                                                             | 4.17 us: 1.04x slower                                                       |
| gc_traversal            | 3.63 ms                                                             | 3.77 ms: 1.04x slower                                                       |
| spectral_norm           | 99.5 ms                                                             | 104 ms: 1.05x slower                                                        |
| pickle                  | 9.79 us                                                             | 10.3 us: 1.05x slower                                                       |
| json                    | 4.86 ms                                                             | 5.19 ms: 1.07x slower                                                       |
| json_dumps              | 12.5 ms                                                             | 13.4 ms: 1.07x slower                                                       |
| async_tree_memoization  | 621 ms                                                              | 668 ms: 1.08x slower                                                        |
| mdp                     | 2.64 sec                                                            | 2.87 sec: 1.09x slower                                                      |
| sqlite_synth            | 2.51 us                                                             | 2.75 us: 1.09x slower                                                       |
| sympy_sum               | 167 ms                                                              | 183 ms: 1.10x slower                                                        |
| pathlib                 | 18.2 ms                                                             | 20.0 ms: 1.10x slower                                                       |
| async_tree_cpu_io_mixed | 736 ms                                                              | 818 ms: 1.11x slower                                                        |
| genshi_xml              | 51.8 ms                                                             | 57.9 ms: 1.12x slower                                                       |
| xml_etree_generate      | 76.5 ms                                                             | 85.8 ms: 1.12x slower                                                       |
| coroutines              | 26.3 ms                                                             | 29.5 ms: 1.12x slower                                                       |
| create_gc_cycles        | 1.48 ms                                                             | 1.67 ms: 1.13x slower                                                       |
| float                   | 76.0 ms                                                             | 86.1 ms: 1.13x slower                                                       |
| dulwich_log             | 63.6 ms                                                             | 72.4 ms: 1.14x slower                                                       |
| xml_etree_process       | 54.1 ms                                                             | 61.7 ms: 1.14x slower                                                       |
| regex_compile           | 137 ms                                                              | 158 ms: 1.16x slower                                                        |
| 2to3                    | 257 ms                                                              | 299 ms: 1.16x slower                                                        |
| chaos                   | 68.0 ms                                                             | 79.2 ms: 1.17x slower                                                       |
| nbody                   | 96.7 ms                                                             | 113 ms: 1.17x slower                                                        |
| sympy_str               | 291 ms                                                              | 340 ms: 1.17x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                             | 79.5 ms: 1.17x slower                                                       |
| regex_v8                | 22.0 ms                                                             | 25.8 ms: 1.18x slower                                                       |
| docutils                | 2.59 sec                                                            | 3.05 sec: 1.18x slower                                                      |
| deepcopy_memo           | 36.4 us                                                             | 42.9 us: 1.18x slower                                                       |
| sympy_expand            | 477 ms                                                              | 563 ms: 1.18x slower                                                        |
| fannkuch                | 384 ms                                                              | 458 ms: 1.19x slower                                                        |
| raytrace                | 292 ms                                                              | 349 ms: 1.20x slower                                                        |
| logging_simple          | 6.09 us                                                             | 7.35 us: 1.21x slower                                                       |
| meteor_contest          | 106 ms                                                              | 128 ms: 1.21x slower                                                        |
| dask                    | 368 ms                                                              | 445 ms: 1.21x slower                                                        |
| nqueens                 | 84.0 ms                                                             | 102 ms: 1.21x slower                                                        |
| hexiom                  | 6.48 ms                                                             | 7.87 ms: 1.21x slower                                                       |
| unpickle_pure_python    | 228 us                                                              | 277 us: 1.21x slower                                                        |
| scimark_sor             | 115 ms                                                              | 140 ms: 1.22x slower                                                        |
| sqlglot_optimize        | 53.4 ms                                                             | 64.9 ms: 1.22x slower                                                       |
| logging_format          | 6.64 us                                                             | 8.08 us: 1.22x slower                                                       |
| scimark_lu              | 108 ms                                                              | 132 ms: 1.22x slower                                                        |
| sqlglot_normalize       | 108 ms                                                              | 132 ms: 1.22x slower                                                        |
| logging_silent          | 98.7 ns                                                             | 121 ns: 1.22x slower                                                        |
| python_startup_no_site  | 5.98 ms                                                             | 7.43 ms: 1.24x slower                                                       |
| html5lib                | 64.0 ms                                                             | 80.0 ms: 1.25x slower                                                       |
| pprint_safe_repr        | 701 ms                                                              | 877 ms: 1.25x slower                                                        |
| pprint_pformat          | 1.45 sec                                                            | 1.82 sec: 1.25x slower                                                      |
| thrift                  | 766 us                                                              | 961 us: 1.26x slower                                                        |
| pickle_pure_python      | 307 us                                                              | 386 us: 1.26x slower                                                        |
| sympy_integrate         | 21.0 ms                                                             | 26.5 ms: 1.26x slower                                                       |
| deepcopy                | 339 us                                                              | 428 us: 1.26x slower                                                        |
| bench_thread_pool       | 820 us                                                              | 1.05 ms: 1.28x slower                                                       |
| crypto_pyaes            | 73.8 ms                                                             | 94.9 ms: 1.29x slower                                                       |
| deepcopy_reduce         | 2.96 us                                                             | 3.81 us: 1.29x slower                                                       |
| genshi_text             | 21.8 ms                                                             | 28.2 ms: 1.29x slower                                                       |
| richards                | 45.7 ms                                                             | 59.0 ms: 1.29x slower                                                       |
| comprehensions          | 22.2 us                                                             | 28.8 us: 1.29x slower                                                       |
| pycparser               | 1.14 sec                                                            | 1.48 sec: 1.30x slower                                                      |
| mako                    | 9.82 ms                                                             | 12.9 ms: 1.31x slower                                                       |
| python_startup          | 8.49 ms                                                             | 11.2 ms: 1.31x slower                                                       |
| regex_dna               | 196 ms                                                              | 262 ms: 1.33x slower                                                        |
| pidigits                | 197 ms                                                              | 264 ms: 1.34x slower                                                        |
| deltablue               | 3.66 ms                                                             | 5.07 ms: 1.39x slower                                                       |
| tornado_http            | 96.7 ms                                                             | 136 ms: 1.40x slower                                                        |
| go                      | 138 ms                                                              | 194 ms: 1.40x slower                                                        |
| pyflate                 | 414 ms                                                              | 582 ms: 1.41x slower                                                        |
| chameleon               | 6.52 ms                                                             | 9.27 ms: 1.42x slower                                                       |
| django_template         | 32.9 ms                                                             | 47.4 ms: 1.44x slower                                                       |
| sqlglot_transpile       | 1.65 ms                                                             | 2.63 ms: 1.59x slower                                                       |
| sqlglot_parse           | 1.36 ms                                                             | 2.24 ms: 1.65x slower                                                       |
| Geometric mean          | (ref)                                                               | 1.12x slower                                                                |
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, asyncio_tcp, djangocms, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
