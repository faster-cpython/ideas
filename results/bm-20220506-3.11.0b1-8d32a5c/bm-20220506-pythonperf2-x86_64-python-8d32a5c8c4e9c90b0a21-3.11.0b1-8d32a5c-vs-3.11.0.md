
# Results vs. 3.11.0

- fork: python
- ref: 8d32a5c8c4e9c90b0a21
- machine: linux-x86_64
- commit hash: 8d32a5c
- commit date: 2022-05-06
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf2-x86_64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 281 ms: 1.03x faster                                                        |
| docutils       | 2.86 sec                                                                  | 2.82 sec: 1.01x faster                                                      |
| html5lib       | 70.2 ms                                                                   | 69.0 ms: 1.02x faster                                                       |
| tornado_http   | 125 ms                                                                    | 121 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf2-x86_64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 74.7 ms: 1.01x faster                                                       |
| nbody          | 92.1 ms                                                                   | 100 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.02x slower                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf2-x86_64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.31 ms                                                                   | 2.97 ms: 1.12x faster                                                       |
| regex_v8       | 24.4 ms                                                                   | 22.8 ms: 1.07x faster                                                       |
| regex_compile  | 154 ms                                                                    | 153 ms: 1.01x faster                                                        |
| regex_dna      | 225 ms                                                                    | 232 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf2-x86_64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                   | 24.6 us: 1.15x faster                                                       |
| pickle_dict          | 31.1 us                                                                   | 29.9 us: 1.04x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 155 ms: 1.03x faster                                                        |
| pickle               | 9.92 us                                                                   | 9.62 us: 1.03x faster                                                       |
| unpickle_pure_python | 238 us                                                                    | 233 us: 1.02x faster                                                        |
| xml_etree_iterparse  | 106 ms                                                                    | 105 ms: 1.01x faster                                                        |
| xml_etree_process    | 55.8 ms                                                                   | 56.1 ms: 1.00x slower                                                       |
| unpickle_list        | 4.52 us                                                                   | 4.56 us: 1.01x slower                                                       |
| json_dumps           | 13.4 ms                                                                   | 13.5 ms: 1.01x slower                                                       |
| xml_etree_generate   | 79.1 ms                                                                   | 80.3 ms: 1.02x slower                                                       |
| unpickle             | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.02x faster                                                                |

Benchmark hidden because not significant (2): pickle_pure_python, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf2-x86_64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.5 ms: 1.02x faster                                                       |
| python_startup_no_site | 7.73 ms                                                                   | 7.68 ms: 1.01x faster                                                       |
| Geometric mean         | (ref)                                                                     | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf2-x86_64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 26.3 ms                                                                   | 25.4 ms: 1.03x faster                                                       |
| genshi_xml      | 57.8 ms                                                                   | 56.7 ms: 1.02x faster                                                       |
| django_template | 39.6 ms                                                                   | 41.3 ms: 1.04x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.00x faster                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf2-x86_64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads              | 28.4 us                                                                   | 24.6 us: 1.15x faster                                                       |
| regex_effbot            | 3.31 ms                                                                   | 2.97 ms: 1.12x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.85 ms: 1.10x faster                                                       |
| json                    | 5.59 ms                                                                   | 5.14 ms: 1.09x faster                                                       |
| fannkuch                | 449 ms                                                                    | 418 ms: 1.07x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 22.8 ms: 1.07x faster                                                       |
| nqueens                 | 101 ms                                                                    | 95.8 ms: 1.05x faster                                                       |
| chaos                   | 76.2 ms                                                                   | 72.4 ms: 1.05x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 28.0 ms: 1.05x faster                                                       |
| pickle_dict             | 31.1 us                                                                   | 29.9 us: 1.04x faster                                                       |
| pycparser               | 1.30 sec                                                                  | 1.26 sec: 1.03x faster                                                      |
| genshi_text             | 26.3 ms                                                                   | 25.4 ms: 1.03x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 155 ms: 1.03x faster                                                        |
| thrift                  | 942 us                                                                    | 913 us: 1.03x faster                                                        |
| tornado_http            | 125 ms                                                                    | 121 ms: 1.03x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 82.3 ms: 1.03x faster                                                       |
| pickle                  | 9.92 us                                                                   | 9.62 us: 1.03x faster                                                       |
| 2to3                    | 289 ms                                                                    | 281 ms: 1.03x faster                                                        |
| logging_silent          | 103 ns                                                                    | 99.8 ns: 1.03x faster                                                       |
| sqlglot_normalize       | 122 ms                                                                    | 119 ms: 1.03x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 516 ms: 1.03x faster                                                        |
| async_tree_memoization  | 639 ms                                                                    | 624 ms: 1.02x faster                                                        |
| pylint                  | 517 ms                                                                    | 505 ms: 1.02x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.67 us: 1.02x faster                                                       |
| sympy_sum               | 182 ms                                                                    | 178 ms: 1.02x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 233 us: 1.02x faster                                                        |
| spectral_norm           | 95.1 ms                                                                   | 93.1 ms: 1.02x faster                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.57 sec: 1.02x faster                                                      |
| pathlib                 | 19.2 ms                                                                   | 18.8 ms: 1.02x faster                                                       |
| genshi_xml              | 57.8 ms                                                                   | 56.7 ms: 1.02x faster                                                       |
| python_startup          | 10.7 ms                                                                   | 10.5 ms: 1.02x faster                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 755 ms: 1.02x faster                                                        |
| html5lib                | 70.2 ms                                                                   | 69.0 ms: 1.02x faster                                                       |
| dulwich_log             | 69.1 ms                                                                   | 68.0 ms: 1.02x faster                                                       |
| sqlalchemy_imperative   | 19.8 ms                                                                   | 19.5 ms: 1.02x faster                                                       |
| deltablue               | 3.99 ms                                                                   | 3.93 ms: 1.02x faster                                                       |
| aiohttp                 | 959 us                                                                    | 945 us: 1.01x faster                                                        |
| hexiom                  | 7.00 ms                                                                   | 6.91 ms: 1.01x faster                                                       |
| float                   | 75.7 ms                                                                   | 74.7 ms: 1.01x faster                                                       |
| sqlalchemy_declarative  | 156 ms                                                                    | 153 ms: 1.01x faster                                                        |
| sympy_expand            | 547 ms                                                                    | 540 ms: 1.01x faster                                                        |
| docutils                | 2.86 sec                                                                  | 2.82 sec: 1.01x faster                                                      |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                      |
| go                      | 158 ms                                                                    | 156 ms: 1.01x faster                                                        |
| pyflate                 | 438 ms                                                                    | 433 ms: 1.01x faster                                                        |
| sympy_str               | 333 ms                                                                    | 329 ms: 1.01x faster                                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 105 ms: 1.01x faster                                                        |
| regex_compile           | 154 ms                                                                    | 153 ms: 1.01x faster                                                        |
| gunicorn                | 936 us                                                                    | 928 us: 1.01x faster                                                        |
| generators              | 56.0 ms                                                                   | 55.5 ms: 1.01x faster                                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 748 ms: 1.01x faster                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.68 ms: 1.01x faster                                                       |
| sympy_integrate         | 25.3 ms                                                                   | 25.2 ms: 1.00x faster                                                       |
| asyncio_tcp             | 752 ms                                                                    | 749 ms: 1.00x faster                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 56.1 ms: 1.00x slower                                                       |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.9 ms: 1.01x slower                                                       |
| scimark_sor             | 109 ms                                                                    | 110 ms: 1.01x slower                                                        |
| unpickle_list           | 4.52 us                                                                   | 4.56 us: 1.01x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.51 us: 1.01x slower                                                       |
| json_dumps              | 13.4 ms                                                                   | 13.5 ms: 1.01x slower                                                       |
| meteor_contest          | 129 ms                                                                    | 131 ms: 1.02x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 80.3 ms: 1.02x slower                                                       |
| deepcopy_memo           | 37.0 us                                                                   | 37.6 us: 1.02x slower                                                       |
| unpickle                | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                       |
| raytrace                | 303 ms                                                                    | 309 ms: 1.02x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 69.2 ms: 1.02x slower                                                       |
| richards                | 49.1 ms                                                                   | 50.1 ms: 1.02x slower                                                       |
| mdp                     | 2.73 sec                                                                  | 2.78 sec: 1.02x slower                                                      |
| deepcopy                | 384 us                                                                    | 394 us: 1.03x slower                                                        |
| regex_dna               | 225 ms                                                                    | 232 ms: 1.03x slower                                                        |
| bench_thread_pool       | 990 us                                                                    | 1.02 ms: 1.03x slower                                                       |
| django_template         | 39.6 ms                                                                   | 41.3 ms: 1.04x slower                                                       |
| telco                   | 6.70 ms                                                                   | 6.99 ms: 1.04x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 294 ms: 1.06x slower                                                        |
| nbody                   | 92.1 ms                                                                   | 100 ms: 1.09x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 28.2 us: 1.14x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.30 ms: 1.23x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 1.95 ms: 1.27x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.01x faster                                                                |

Benchmark hidden because not significant (16): mypy2, logging_simple, create_gc_cycles, scimark_lu, async_generators, pidigits, scimark_sparse_mat_mult, dask, flaskblogging, mako, pickle_pure_python, bench_mp_pool, chameleon, unpack_sequence, pickle_list, deepcopy_reduce
Ignored benchmarks (1) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: coverage
