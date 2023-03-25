
# Results vs. 3.11.0

- fork: python
- ref: 2e49bd06c5ffab7d1540
- machine: linux-x86_64
- commit hash: 2e49bd0
- commit date: 2022-04-05
- overall geometric mean: 1.02x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220405-pythonperf2-x86_64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 293 ms: 1.01x slower                                                        |
| chameleon      | 7.50 ms                                                                   | 7.97 ms: 1.06x slower                                                       |
| docutils       | 2.86 sec                                                                  | 2.92 sec: 1.02x slower                                                      |
| html5lib       | 70.2 ms                                                                   | 75.0 ms: 1.07x slower                                                       |
| tornado_http   | 125 ms                                                                    | 123 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.03x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220405-pythonperf2-x86_64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 252 ms                                                                    | 251 ms: 1.00x faster                                                        |
| nbody          | 92.1 ms                                                                   | 93.6 ms: 1.02x slower                                                       |
| float          | 75.7 ms                                                                   | 78.4 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.02x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220405-pythonperf2-x86_64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.31 ms                                                                   | 3.13 ms: 1.06x faster                                                       |
| regex_compile  | 154 ms                                                                    | 159 ms: 1.03x slower                                                        |
| regex_v8       | 24.4 ms                                                                   | 26.6 ms: 1.09x slower                                                       |
| regex_dna      | 225 ms                                                                    | 253 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.05x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220405-pythonperf2-x86_64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                   | 24.5 us: 1.16x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 157 ms: 1.02x faster                                                        |
| pickle               | 9.92 us                                                                   | 9.88 us: 1.00x faster                                                       |
| json_dumps           | 13.4 ms                                                                   | 13.5 ms: 1.01x slower                                                       |
| unpickle_pure_python | 238 us                                                                    | 242 us: 1.02x slower                                                        |
| pickle_pure_python   | 319 us                                                                    | 331 us: 1.04x slower                                                        |
| xml_etree_process    | 55.8 ms                                                                   | 58.3 ms: 1.04x slower                                                       |
| xml_etree_generate   | 79.1 ms                                                                   | 82.8 ms: 1.05x slower                                                       |
| pickle_list          | 3.78 us                                                                   | 4.12 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.00x slower                                                                |

Benchmark hidden because not significant (4): unpickle, unpickle_list, xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220405-pythonperf2-x86_64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                                   | 7.46 ms: 1.04x faster                                                       |
| python_startup         | 10.7 ms                                                                   | 10.4 ms: 1.04x faster                                                       |
| Geometric mean         | (ref)                                                                     | 1.04x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220405-pythonperf2-x86_64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 26.3 ms                                                                   | 26.8 ms: 1.02x slower                                                       |
| django_template | 39.6 ms                                                                   | 40.7 ms: 1.03x slower                                                       |
| mako            | 10.9 ms                                                                   | 11.2 ms: 1.03x slower                                                       |
| genshi_xml      | 57.8 ms                                                                   | 59.7 ms: 1.03x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.03x slower                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220405-pythonperf2-x86_64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal            | 4.22 ms                                                                   | 3.58 ms: 1.18x faster                                                       |
| json_loads              | 28.4 us                                                                   | 24.5 us: 1.16x faster                                                       |
| dask                    | 418 ms                                                                    | 367 ms: 1.14x faster                                                        |
| json                    | 5.59 ms                                                                   | 5.17 ms: 1.08x faster                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.13 ms: 1.06x faster                                                       |
| chaos                   | 76.2 ms                                                                   | 73.4 ms: 1.04x faster                                                       |
| logging_simple          | 6.95 us                                                                   | 6.69 us: 1.04x faster                                                       |
| python_startup_no_site  | 7.73 ms                                                                   | 7.46 ms: 1.04x faster                                                       |
| python_startup          | 10.7 ms                                                                   | 10.4 ms: 1.04x faster                                                       |
| logging_format          | 7.84 us                                                                   | 7.59 us: 1.03x faster                                                       |
| sympy_sum               | 182 ms                                                                    | 177 ms: 1.03x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 157 ms: 1.02x faster                                                        |
| generators              | 56.0 ms                                                                   | 54.7 ms: 1.02x faster                                                       |
| fannkuch                | 449 ms                                                                    | 442 ms: 1.02x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 29.0 ms: 1.02x faster                                                       |
| thrift                  | 942 us                                                                    | 928 us: 1.01x faster                                                        |
| tornado_http            | 125 ms                                                                    | 123 ms: 1.01x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 523 ms: 1.01x faster                                                        |
| asyncio_tcp             | 752 ms                                                                    | 746 ms: 1.01x faster                                                        |
| sympy_str               | 333 ms                                                                    | 330 ms: 1.01x faster                                                        |
| pickle                  | 9.92 us                                                                   | 9.88 us: 1.00x faster                                                       |
| pidigits                | 252 ms                                                                    | 251 ms: 1.00x faster                                                        |
| sympy_expand            | 547 ms                                                                    | 549 ms: 1.00x slower                                                        |
| pathlib                 | 19.2 ms                                                                   | 19.3 ms: 1.01x slower                                                       |
| dulwich_log             | 69.1 ms                                                                   | 69.8 ms: 1.01x slower                                                       |
| json_dumps              | 13.4 ms                                                                   | 13.5 ms: 1.01x slower                                                       |
| 2to3                    | 289 ms                                                                    | 293 ms: 1.01x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.52 us: 1.01x slower                                                       |
| mdp                     | 2.73 sec                                                                  | 2.76 sec: 1.01x slower                                                      |
| telco                   | 6.70 ms                                                                   | 6.79 ms: 1.01x slower                                                       |
| nbody                   | 92.1 ms                                                                   | 93.6 ms: 1.02x slower                                                       |
| unpickle_pure_python    | 238 us                                                                    | 242 us: 1.02x slower                                                        |
| logging_silent          | 103 ns                                                                    | 105 ns: 1.02x slower                                                        |
| pycparser               | 1.30 sec                                                                  | 1.33 sec: 1.02x slower                                                      |
| genshi_text             | 26.3 ms                                                                   | 26.8 ms: 1.02x slower                                                       |
| aiohttp                 | 959 us                                                                    | 978 us: 1.02x slower                                                        |
| docutils                | 2.86 sec                                                                  | 2.92 sec: 1.02x slower                                                      |
| deepcopy_reduce         | 3.39 us                                                                   | 3.48 us: 1.02x slower                                                       |
| bench_thread_pool       | 990 us                                                                    | 1.02 ms: 1.03x slower                                                       |
| django_template         | 39.6 ms                                                                   | 40.7 ms: 1.03x slower                                                       |
| meteor_contest          | 129 ms                                                                    | 133 ms: 1.03x slower                                                        |
| sqlalchemy_declarative  | 156 ms                                                                    | 160 ms: 1.03x slower                                                        |
| flaskblogging           | 3.81 ms                                                                   | 3.92 ms: 1.03x slower                                                       |
| scimark_sor             | 109 ms                                                                    | 112 ms: 1.03x slower                                                        |
| unpack_sequence         | 45.9 ns                                                                   | 47.3 ns: 1.03x slower                                                       |
| mako                    | 10.9 ms                                                                   | 11.2 ms: 1.03x slower                                                       |
| regex_compile           | 154 ms                                                                    | 159 ms: 1.03x slower                                                        |
| genshi_xml              | 57.8 ms                                                                   | 59.7 ms: 1.03x slower                                                       |
| gunicorn                | 936 us                                                                    | 968 us: 1.03x slower                                                        |
| float                   | 75.7 ms                                                                   | 78.4 ms: 1.03x slower                                                       |
| sqlalchemy_imperative   | 19.8 ms                                                                   | 20.5 ms: 1.04x slower                                                       |
| sqlglot_normalize       | 122 ms                                                                    | 127 ms: 1.04x slower                                                        |
| pickle_pure_python      | 319 us                                                                    | 331 us: 1.04x slower                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 58.3 ms: 1.04x slower                                                       |
| xml_etree_generate      | 79.1 ms                                                                   | 82.8 ms: 1.05x slower                                                       |
| deepcopy_memo           | 37.0 us                                                                   | 38.8 us: 1.05x slower                                                       |
| go                      | 158 ms                                                                    | 166 ms: 1.05x slower                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 89.5 ms: 1.05x slower                                                       |
| scimark_lu              | 114 ms                                                                    | 120 ms: 1.05x slower                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 61.9 ms: 1.06x slower                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.69 sec: 1.06x slower                                                      |
| deltablue               | 3.99 ms                                                                   | 4.23 ms: 1.06x slower                                                       |
| pyflate                 | 438 ms                                                                    | 464 ms: 1.06x slower                                                        |
| chameleon               | 7.50 ms                                                                   | 7.97 ms: 1.06x slower                                                       |
| raytrace                | 303 ms                                                                    | 322 ms: 1.06x slower                                                        |
| pprint_safe_repr        | 768 ms                                                                    | 818 ms: 1.07x slower                                                        |
| html5lib                | 70.2 ms                                                                   | 75.0 ms: 1.07x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 297 ms: 1.07x slower                                                        |
| richards                | 49.1 ms                                                                   | 52.8 ms: 1.08x slower                                                       |
| regex_v8                | 24.4 ms                                                                   | 26.6 ms: 1.09x slower                                                       |
| pickle_list             | 3.78 us                                                                   | 4.12 us: 1.09x slower                                                       |
| hexiom                  | 7.00 ms                                                                   | 7.66 ms: 1.09x slower                                                       |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.51 ms: 1.11x slower                                                       |
| regex_dna               | 225 ms                                                                    | 253 ms: 1.12x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 27.8 us: 1.12x slower                                                       |
| spectral_norm           | 95.1 ms                                                                   | 107 ms: 1.13x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 77.1 ms: 1.14x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.38 ms: 1.27x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 2.04 ms: 1.33x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.02x slower                                                                |

Benchmark hidden because not significant (15): async_tree_io, unpickle, create_gc_cycles, unpickle_list, async_tree_cpu_io_mixed, sympy_integrate, xml_etree_iterparse, pylint, async_generators, pickle_dict, async_tree_memoization, deepcopy, nqueens, bench_mp_pool, mypy2
Ignored benchmarks (1) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: coverage
