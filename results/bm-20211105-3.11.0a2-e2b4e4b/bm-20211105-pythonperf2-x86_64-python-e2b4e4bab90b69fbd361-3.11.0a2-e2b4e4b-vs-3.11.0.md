
# Results vs. 3.11.0

- fork: python
- ref: e2b4e4bab90b69fbd361
- machine: linux-x86_64
- commit hash: e2b4e4b
- commit date: 2021-11-05
- overall geometric mean: 1.08x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 299 ms: 1.03x slower                                                        |
| chameleon      | 7.50 ms                                                                   | 9.27 ms: 1.24x slower                                                       |
| docutils       | 2.86 sec                                                                  | 3.05 sec: 1.07x slower                                                      |
| html5lib       | 70.2 ms                                                                   | 80.0 ms: 1.14x slower                                                       |
| tornado_http   | 125 ms                                                                    | 136 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.11x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 252 ms                                                                    | 264 ms: 1.05x slower                                                        |
| float          | 75.7 ms                                                                   | 86.1 ms: 1.14x slower                                                       |
| nbody          | 92.1 ms                                                                   | 113 ms: 1.23x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.14x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.31 ms                                                                   | 3.06 ms: 1.08x faster                                                       |
| regex_compile  | 154 ms                                                                    | 158 ms: 1.03x slower                                                        |
| regex_v8       | 24.4 ms                                                                   | 25.8 ms: 1.06x slower                                                       |
| regex_dna      | 225 ms                                                                    | 262 ms: 1.16x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.04x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                   | 24.7 us: 1.15x faster                                                       |
| pickle_dict          | 31.1 us                                                                   | 30.2 us: 1.03x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 157 ms: 1.02x faster                                                        |
| json_dumps           | 13.4 ms                                                                   | 13.4 ms: 1.01x slower                                                       |
| xml_etree_iterparse  | 106 ms                                                                    | 107 ms: 1.01x slower                                                        |
| unpickle             | 13.0 us                                                                   | 13.4 us: 1.03x slower                                                       |
| pickle               | 9.92 us                                                                   | 10.3 us: 1.03x slower                                                       |
| xml_etree_generate   | 79.1 ms                                                                   | 85.8 ms: 1.08x slower                                                       |
| pickle_list          | 3.78 us                                                                   | 4.17 us: 1.10x slower                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 61.7 ms: 1.11x slower                                                       |
| unpickle_pure_python | 238 us                                                                    | 277 us: 1.16x slower                                                        |
| pickle_pure_python   | 319 us                                                                    | 386 us: 1.21x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.04x slower                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                                   | 7.43 ms: 1.04x faster                                                       |
| python_startup         | 10.7 ms                                                                   | 11.2 ms: 1.04x slower                                                       |
| Geometric mean         | (ref)                                                                     | 1.00x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 26.3 ms                                                                   | 28.2 ms: 1.07x slower                                                       |
| mako            | 10.9 ms                                                                   | 12.9 ms: 1.19x slower                                                       |
| django_template | 39.6 ms                                                                   | 47.4 ms: 1.20x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.11x slower                                                                |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| coverage                | 86.0 ms                                                                   | 68.7 ms: 1.25x faster                                                       |
| json_loads              | 28.4 us                                                                   | 24.7 us: 1.15x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.77 ms: 1.12x faster                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.06 ms: 1.08x faster                                                       |
| json                    | 5.59 ms                                                                   | 5.19 ms: 1.08x faster                                                       |
| generators              | 56.0 ms                                                                   | 52.7 ms: 1.06x faster                                                       |
| python_startup_no_site  | 7.73 ms                                                                   | 7.43 ms: 1.04x faster                                                       |
| pickle_dict             | 31.1 us                                                                   | 30.2 us: 1.03x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 157 ms: 1.02x faster                                                        |
| meteor_contest          | 129 ms                                                                    | 128 ms: 1.01x faster                                                        |
| json_dumps              | 13.4 ms                                                                   | 13.4 ms: 1.01x slower                                                       |
| sympy_sum               | 182 ms                                                                    | 183 ms: 1.01x slower                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.67 ms: 1.01x slower                                                       |
| xml_etree_iterparse     | 106 ms                                                                    | 107 ms: 1.01x slower                                                        |
| telco                   | 6.70 ms                                                                   | 6.81 ms: 1.02x slower                                                       |
| fannkuch                | 449 ms                                                                    | 458 ms: 1.02x slower                                                        |
| thrift                  | 942 us                                                                    | 961 us: 1.02x slower                                                        |
| async_generators        | 318 ms                                                                    | 325 ms: 1.02x slower                                                        |
| sympy_str               | 333 ms                                                                    | 340 ms: 1.02x slower                                                        |
| unpickle                | 13.0 us                                                                   | 13.4 us: 1.03x slower                                                       |
| regex_compile           | 154 ms                                                                    | 158 ms: 1.03x slower                                                        |
| logging_format          | 7.84 us                                                                   | 8.08 us: 1.03x slower                                                       |
| sympy_expand            | 547 ms                                                                    | 563 ms: 1.03x slower                                                        |
| 2to3                    | 289 ms                                                                    | 299 ms: 1.03x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.3 us: 1.03x slower                                                       |
| chaos                   | 76.2 ms                                                                   | 79.2 ms: 1.04x slower                                                       |
| python_startup          | 10.7 ms                                                                   | 11.2 ms: 1.04x slower                                                       |
| pathlib                 | 19.2 ms                                                                   | 20.0 ms: 1.04x slower                                                       |
| async_tree_memoization  | 639 ms                                                                    | 668 ms: 1.04x slower                                                        |
| gunicorn                | 936 us                                                                    | 980 us: 1.05x slower                                                        |
| dulwich_log             | 69.1 ms                                                                   | 72.4 ms: 1.05x slower                                                       |
| sympy_integrate         | 25.3 ms                                                                   | 26.5 ms: 1.05x slower                                                       |
| pidigits                | 252 ms                                                                    | 264 ms: 1.05x slower                                                        |
| mdp                     | 2.73 sec                                                                  | 2.87 sec: 1.05x slower                                                      |
| regex_v8                | 24.4 ms                                                                   | 25.8 ms: 1.06x slower                                                       |
| logging_simple          | 6.95 us                                                                   | 7.35 us: 1.06x slower                                                       |
| bench_thread_pool       | 990 us                                                                    | 1.05 ms: 1.06x slower                                                       |
| dask                    | 418 ms                                                                    | 445 ms: 1.07x slower                                                        |
| docutils                | 2.86 sec                                                                  | 3.05 sec: 1.07x slower                                                      |
| async_tree_io           | 1.18 sec                                                                  | 1.27 sec: 1.07x slower                                                      |
| genshi_text             | 26.3 ms                                                                   | 28.2 ms: 1.07x slower                                                       |
| tornado_http            | 125 ms                                                                    | 136 ms: 1.08x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 85.8 ms: 1.08x slower                                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 818 ms: 1.09x slower                                                        |
| sqlglot_normalize       | 122 ms                                                                    | 132 ms: 1.09x slower                                                        |
| spectral_norm           | 95.1 ms                                                                   | 104 ms: 1.10x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 4.17 us: 1.10x slower                                                       |
| bench_mp_pool           | 4.54 ms                                                                   | 5.01 ms: 1.10x slower                                                       |
| xml_etree_process       | 55.8 ms                                                                   | 61.7 ms: 1.11x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.75 us: 1.11x slower                                                       |
| sqlglot_optimize        | 58.6 ms                                                                   | 64.9 ms: 1.11x slower                                                       |
| deepcopy                | 384 us                                                                    | 428 us: 1.12x slower                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 94.9 ms: 1.12x slower                                                       |
| hexiom                  | 7.00 ms                                                                   | 7.87 ms: 1.12x slower                                                       |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.56 ms: 1.12x slower                                                       |
| deepcopy_reduce         | 3.39 us                                                                   | 3.81 us: 1.12x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 311 ms: 1.12x slower                                                        |
| float                   | 75.7 ms                                                                   | 86.1 ms: 1.14x slower                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.82 sec: 1.14x slower                                                      |
| pycparser               | 1.30 sec                                                                  | 1.48 sec: 1.14x slower                                                      |
| html5lib                | 70.2 ms                                                                   | 80.0 ms: 1.14x slower                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 877 ms: 1.14x slower                                                        |
| raytrace                | 303 ms                                                                    | 349 ms: 1.15x slower                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 42.9 us: 1.16x slower                                                       |
| scimark_lu              | 114 ms                                                                    | 132 ms: 1.16x slower                                                        |
| regex_dna               | 225 ms                                                                    | 262 ms: 1.16x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 28.8 us: 1.16x slower                                                       |
| unpickle_pure_python    | 238 us                                                                    | 277 us: 1.16x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 79.5 ms: 1.17x slower                                                       |
| logging_silent          | 103 ns                                                                    | 121 ns: 1.18x slower                                                        |
| mako                    | 10.9 ms                                                                   | 12.9 ms: 1.19x slower                                                       |
| django_template         | 39.6 ms                                                                   | 47.4 ms: 1.20x slower                                                       |
| richards                | 49.1 ms                                                                   | 59.0 ms: 1.20x slower                                                       |
| pickle_pure_python      | 319 us                                                                    | 386 us: 1.21x slower                                                        |
| nbody                   | 92.1 ms                                                                   | 113 ms: 1.23x slower                                                        |
| go                      | 158 ms                                                                    | 194 ms: 1.23x slower                                                        |
| chameleon               | 7.50 ms                                                                   | 9.27 ms: 1.24x slower                                                       |
| deltablue               | 3.99 ms                                                                   | 5.07 ms: 1.27x slower                                                       |
| flaskblogging           | 3.81 ms                                                                   | 4.84 ms: 1.27x slower                                                       |
| scimark_sor             | 109 ms                                                                    | 140 ms: 1.28x slower                                                        |
| pyflate                 | 438 ms                                                                    | 582 ms: 1.33x slower                                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.63 ms: 1.40x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 2.24 ms: 1.47x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.08x slower                                                                |

Benchmark hidden because not significant (6): coroutines, genshi_xml, unpack_sequence, unpickle_list, async_tree_none, nqueens
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, asyncio_tcp, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
