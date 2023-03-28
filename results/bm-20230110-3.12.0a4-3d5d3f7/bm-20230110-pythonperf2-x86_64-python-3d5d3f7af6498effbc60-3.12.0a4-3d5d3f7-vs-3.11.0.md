
# Results vs. 3.11.0

- fork: python
- ref: 3d5d3f7af6498effbc60
- machine: linux-x86_64
- commit hash: 3d5d3f7
- commit date: 2023-01-10
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf2-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 286 ms: 1.01x faster                                                        |
| chameleon      | 7.50 ms                                                                   | 7.31 ms: 1.03x faster                                                       |
| docutils       | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                      |
| html5lib       | 70.2 ms                                                                   | 66.8 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf2-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 72.4 ms: 1.05x faster                                                       |
| pidigits       | 252 ms                                                                    | 252 ms: 1.00x slower                                                        |
| nbody          | 92.1 ms                                                                   | 98.1 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf2-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 23.0 ms: 1.06x faster                                                       |
| regex_compile  | 154 ms                                                                    | 149 ms: 1.03x faster                                                        |
| regex_dna      | 225 ms                                                                    | 229 ms: 1.02x slower                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.43 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf2-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.1 ms: 1.32x faster                                                       |
| json_loads           | 28.4 us                                                                   | 24.0 us: 1.18x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 144 ms: 1.12x faster                                                        |
| unpickle_pure_python | 238 us                                                                    | 214 us: 1.11x faster                                                        |
| pickle_list          | 3.78 us                                                                   | 3.70 us: 1.02x faster                                                       |
| pickle               | 9.92 us                                                                   | 9.71 us: 1.02x faster                                                       |
| pickle_pure_python   | 319 us                                                                    | 313 us: 1.02x faster                                                        |
| xml_etree_iterparse  | 106 ms                                                                    | 104 ms: 1.01x faster                                                        |
| unpickle_list        | 4.52 us                                                                   | 4.48 us: 1.01x faster                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 55.4 ms: 1.01x faster                                                       |
| xml_etree_generate   | 79.1 ms                                                                   | 80.3 ms: 1.01x slower                                                       |
| unpickle             | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.06x faster                                                                |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf2-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.8 ms: 1.00x slower                                                       |
| python_startup_no_site | 7.73 ms                                                                   | 7.87 ms: 1.02x slower                                                       |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf2-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 53.7 ms: 1.08x faster                                                       |
| mako            | 10.9 ms                                                                   | 10.2 ms: 1.06x faster                                                       |
| genshi_text     | 26.3 ms                                                                   | 24.8 ms: 1.06x faster                                                       |
| django_template | 39.6 ms                                                                   | 39.2 ms: 1.01x faster                                                       |
| Geometric mean  | (ref)                                                                     | 1.05x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf2-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 386 ms: 1.95x faster                                                        |
| json_dumps              | 13.4 ms                                                                   | 10.1 ms: 1.32x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.54 ms: 1.19x faster                                                       |
| json_loads              | 28.4 us                                                                   | 24.0 us: 1.18x faster                                                       |
| fannkuch                | 449 ms                                                                    | 380 ms: 1.18x faster                                                        |
| mypy2                   | 446 ms                                                                    | 380 ms: 1.17x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 101 ms: 1.13x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 144 ms: 1.12x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 214 us: 1.11x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.70 ms: 1.10x faster                                                       |
| deltablue               | 3.99 ms                                                                   | 3.69 ms: 1.08x faster                                                       |
| genshi_xml              | 57.8 ms                                                                   | 53.7 ms: 1.08x faster                                                       |
| chaos                   | 76.2 ms                                                                   | 70.9 ms: 1.08x faster                                                       |
| nqueens                 | 101 ms                                                                    | 94.0 ms: 1.07x faster                                                       |
| json                    | 5.59 ms                                                                   | 5.24 ms: 1.07x faster                                                       |
| mako                    | 10.9 ms                                                                   | 10.2 ms: 1.06x faster                                                       |
| regex_v8                | 24.4 ms                                                                   | 23.0 ms: 1.06x faster                                                       |
| genshi_text             | 26.3 ms                                                                   | 24.8 ms: 1.06x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 27.9 ms: 1.06x faster                                                       |
| async_tree_memoization  | 639 ms                                                                    | 608 ms: 1.05x faster                                                        |
| html5lib                | 70.2 ms                                                                   | 66.8 ms: 1.05x faster                                                       |
| crypto_pyaes            | 85.0 ms                                                                   | 81.1 ms: 1.05x faster                                                       |
| richards                | 49.1 ms                                                                   | 46.9 ms: 1.05x faster                                                       |
| async_tree_none         | 529 ms                                                                    | 505 ms: 1.05x faster                                                        |
| float                   | 75.7 ms                                                                   | 72.4 ms: 1.05x faster                                                       |
| unpack_sequence         | 45.9 ns                                                                   | 44.0 ns: 1.04x faster                                                       |
| create_gc_cycles        | 1.65 ms                                                                   | 1.58 ms: 1.04x faster                                                       |
| thrift                  | 942 us                                                                    | 908 us: 1.04x faster                                                        |
| hexiom                  | 7.00 ms                                                                   | 6.77 ms: 1.03x faster                                                       |
| pycparser               | 1.30 sec                                                                  | 1.26 sec: 1.03x faster                                                      |
| regex_compile           | 154 ms                                                                    | 149 ms: 1.03x faster                                                        |
| go                      | 158 ms                                                                    | 153 ms: 1.03x faster                                                        |
| docutils                | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                      |
| chameleon               | 7.50 ms                                                                   | 7.31 ms: 1.03x faster                                                       |
| async_tree_io           | 1.18 sec                                                                  | 1.15 sec: 1.02x faster                                                      |
| dulwich_log             | 69.1 ms                                                                   | 67.5 ms: 1.02x faster                                                       |
| logging_format          | 7.84 us                                                                   | 7.66 us: 1.02x faster                                                       |
| dask                    | 418 ms                                                                    | 408 ms: 1.02x faster                                                        |
| pickle_list             | 3.78 us                                                                   | 3.70 us: 1.02x faster                                                       |
| pickle                  | 9.92 us                                                                   | 9.71 us: 1.02x faster                                                       |
| pickle_pure_python      | 319 us                                                                    | 313 us: 1.02x faster                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 66.6 ms: 1.02x faster                                                       |
| sympy_expand            | 547 ms                                                                    | 537 ms: 1.02x faster                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.33 us: 1.02x faster                                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 742 ms: 1.02x faster                                                        |
| raytrace                | 303 ms                                                                    | 299 ms: 1.01x faster                                                        |
| deepcopy                | 384 us                                                                    | 379 us: 1.01x faster                                                        |
| 2to3                    | 289 ms                                                                    | 286 ms: 1.01x faster                                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 104 ms: 1.01x faster                                                        |
| django_template         | 39.6 ms                                                                   | 39.2 ms: 1.01x faster                                                       |
| pyflate                 | 438 ms                                                                    | 433 ms: 1.01x faster                                                        |
| scimark_sor             | 109 ms                                                                    | 108 ms: 1.01x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 36.7 us: 1.01x faster                                                       |
| unpickle_list           | 4.52 us                                                                   | 4.48 us: 1.01x faster                                                       |
| xml_etree_process       | 55.8 ms                                                                   | 55.4 ms: 1.01x faster                                                       |
| pidigits                | 252 ms                                                                    | 252 ms: 1.00x slower                                                        |
| python_startup          | 10.7 ms                                                                   | 10.8 ms: 1.00x slower                                                       |
| sqlglot_normalize       | 122 ms                                                                    | 123 ms: 1.01x slower                                                        |
| sympy_str               | 333 ms                                                                    | 335 ms: 1.01x slower                                                        |
| mdp                     | 2.73 sec                                                                  | 2.75 sec: 1.01x slower                                                      |
| sympy_integrate         | 25.3 ms                                                                   | 25.6 ms: 1.01x slower                                                       |
| pathlib                 | 19.2 ms                                                                   | 19.4 ms: 1.01x slower                                                       |
| async_generators        | 318 ms                                                                    | 322 ms: 1.01x slower                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 59.3 ms: 1.01x slower                                                       |
| meteor_contest          | 129 ms                                                                    | 131 ms: 1.01x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 80.3 ms: 1.01x slower                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.63 sec: 1.02x slower                                                      |
| regex_dna               | 225 ms                                                                    | 229 ms: 1.02x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.87 ms: 1.02x slower                                                       |
| sympy_sum               | 182 ms                                                                    | 186 ms: 1.02x slower                                                        |
| unpickle                | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 283 ms: 1.02x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.56 us: 1.03x slower                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 794 ms: 1.03x slower                                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.43 ms: 1.04x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 1.59 ms: 1.04x slower                                                       |
| coverage                | 86.0 ms                                                                   | 89.3 ms: 1.04x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.95 ms: 1.04x slower                                                       |
| spectral_norm           | 95.1 ms                                                                   | 101 ms: 1.06x slower                                                        |
| nbody                   | 92.1 ms                                                                   | 98.1 ms: 1.07x slower                                                       |
| generators              | 56.0 ms                                                                   | 60.5 ms: 1.08x slower                                                       |
| bench_mp_pool           | 4.54 ms                                                                   | 4.94 ms: 1.09x slower                                                       |
| comprehensions          | 24.7 us                                                                   | 27.1 us: 1.09x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.03x faster                                                                |

Benchmark hidden because not significant (5): logging_silent, bench_thread_pool, telco, logging_simple, pickle_dict
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
