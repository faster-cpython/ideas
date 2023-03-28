
# Results vs. 3.11.0

- fork: python
- ref: 3b9d793efcfd2c00c14f
- machine: linux-x86_64
- commit hash: 3b9d793
- commit date: 2022-11-14
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 245 ms: 1.05x faster                                                  |
| chameleon      | 6.52 ms                                                             | 6.30 ms: 1.03x faster                                                 |
| docutils       | 2.59 sec                                                            | 2.50 sec: 1.04x faster                                                |
| html5lib       | 64.0 ms                                                             | 58.9 ms: 1.09x faster                                                 |
| tornado_http   | 96.7 ms                                                             | 93.1 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                               | 1.05x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.0 ms                                                             | 72.0 ms: 1.05x faster                                                 |
| pidigits       | 197 ms                                                              | 189 ms: 1.04x faster                                                  |
| nbody          | 96.7 ms                                                             | 93.9 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                               | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                              | 127 ms: 1.08x faster                                                  |
| regex_v8       | 22.0 ms                                                             | 21.1 ms: 1.04x faster                                                 |
| regex_effbot   | 3.32 ms                                                             | 3.47 ms: 1.04x slower                                                 |
| regex_dna      | 196 ms                                                              | 208 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                               | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.66 ms: 1.30x faster                                                 |
| unpickle_pure_python | 228 us                                                              | 200 us: 1.14x faster                                                  |
| json_loads           | 26.2 us                                                             | 23.9 us: 1.10x faster                                                 |
| xml_etree_parse      | 162 ms                                                              | 149 ms: 1.09x faster                                                  |
| pickle_pure_python   | 307 us                                                              | 283 us: 1.08x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                              | 103 ms: 1.05x faster                                                  |
| unpickle             | 13.2 us                                                             | 12.9 us: 1.02x faster                                                 |
| pickle_dict          | 30.9 us                                                             | 30.8 us: 1.01x faster                                                 |
| xml_etree_process    | 54.1 ms                                                             | 53.9 ms: 1.00x faster                                                 |
| pickle_list          | 4.03 us                                                             | 4.06 us: 1.01x slower                                                 |
| xml_etree_generate   | 76.5 ms                                                             | 77.2 ms: 1.01x slower                                                 |
| pickle               | 9.79 us                                                             | 9.88 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.06x faster                                                          |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.58 ms: 1.01x slower                                                 |
| python_startup_no_site | 5.98 ms                                                             | 6.12 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 51.8 ms                                                             | 47.0 ms: 1.10x faster                                                 |
| genshi_text    | 21.8 ms                                                             | 20.2 ms: 1.08x faster                                                 |
| mako           | 9.82 ms                                                             | 9.39 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                               | 1.06x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps              | 12.5 ms                                                             | 9.66 ms: 1.30x faster                                                 |
| mypy2                   | 422 ms                                                              | 325 ms: 1.30x faster                                                  |
| unpickle_pure_python    | 228 us                                                              | 200 us: 1.14x faster                                                  |
| deltablue               | 3.66 ms                                                             | 3.22 ms: 1.14x faster                                                 |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.00 ms: 1.12x faster                                                 |
| genshi_xml              | 51.8 ms                                                             | 47.0 ms: 1.10x faster                                                 |
| json_loads              | 26.2 us                                                             | 23.9 us: 1.10x faster                                                 |
| scimark_sor             | 115 ms                                                              | 105 ms: 1.09x faster                                                  |
| richards                | 45.7 ms                                                             | 41.8 ms: 1.09x faster                                                 |
| xml_etree_parse         | 162 ms                                                              | 149 ms: 1.09x faster                                                  |
| html5lib                | 64.0 ms                                                             | 58.9 ms: 1.09x faster                                                 |
| genshi_text             | 21.8 ms                                                             | 20.2 ms: 1.08x faster                                                 |
| pickle_pure_python      | 307 us                                                              | 283 us: 1.08x faster                                                  |
| unpack_sequence         | 49.5 ns                                                             | 45.7 ns: 1.08x faster                                                 |
| deepcopy_memo           | 36.4 us                                                             | 33.6 us: 1.08x faster                                                 |
| regex_compile           | 137 ms                                                              | 127 ms: 1.08x faster                                                  |
| hexiom                  | 6.48 ms                                                             | 6.04 ms: 1.07x faster                                                 |
| logging_simple          | 6.09 us                                                             | 5.70 us: 1.07x faster                                                 |
| pycparser               | 1.14 sec                                                            | 1.08 sec: 1.06x faster                                                |
| scimark_fft             | 328 ms                                                              | 309 ms: 1.06x faster                                                  |
| mdp                     | 2.64 sec                                                            | 2.48 sec: 1.06x faster                                                |
| coroutines              | 26.3 ms                                                             | 24.7 ms: 1.06x faster                                                 |
| logging_silent          | 98.7 ns                                                             | 93.4 ns: 1.06x faster                                                 |
| raytrace                | 292 ms                                                              | 277 ms: 1.06x faster                                                  |
| aiohttp                 | 1.05 ms                                                             | 999 us: 1.06x faster                                                  |
| float                   | 76.0 ms                                                             | 72.0 ms: 1.05x faster                                                 |
| logging_format          | 6.64 us                                                             | 6.30 us: 1.05x faster                                                 |
| bench_thread_pool       | 820 us                                                              | 780 us: 1.05x faster                                                  |
| spectral_norm           | 99.5 ms                                                             | 94.9 ms: 1.05x faster                                                 |
| 2to3                    | 257 ms                                                              | 245 ms: 1.05x faster                                                  |
| gunicorn                | 1.13 ms                                                             | 1.08 ms: 1.05x faster                                                 |
| mako                    | 9.82 ms                                                             | 9.39 ms: 1.05x faster                                                 |
| sqlglot_optimize        | 53.4 ms                                                             | 51.0 ms: 1.05x faster                                                 |
| sympy_expand            | 477 ms                                                              | 456 ms: 1.05x faster                                                  |
| xml_etree_iterparse     | 108 ms                                                              | 103 ms: 1.05x faster                                                  |
| json                    | 4.86 ms                                                             | 4.65 ms: 1.04x faster                                                 |
| pprint_pformat          | 1.45 sec                                                            | 1.39 sec: 1.04x faster                                                |
| regex_v8                | 22.0 ms                                                             | 21.1 ms: 1.04x faster                                                 |
| meteor_contest          | 106 ms                                                              | 102 ms: 1.04x faster                                                  |
| pidigits                | 197 ms                                                              | 189 ms: 1.04x faster                                                  |
| fannkuch                | 384 ms                                                              | 369 ms: 1.04x faster                                                  |
| tornado_http            | 96.7 ms                                                             | 93.1 ms: 1.04x faster                                                 |
| docutils                | 2.59 sec                                                            | 2.50 sec: 1.04x faster                                                |
| nqueens                 | 84.0 ms                                                             | 81.1 ms: 1.04x faster                                                 |
| chameleon               | 6.52 ms                                                             | 6.30 ms: 1.03x faster                                                 |
| deepcopy                | 339 us                                                              | 328 us: 1.03x faster                                                  |
| sympy_integrate         | 21.0 ms                                                             | 20.4 ms: 1.03x faster                                                 |
| sympy_str               | 291 ms                                                              | 282 ms: 1.03x faster                                                  |
| telco                   | 6.59 ms                                                             | 6.38 ms: 1.03x faster                                                 |
| chaos                   | 68.0 ms                                                             | 65.8 ms: 1.03x faster                                                 |
| nbody                   | 96.7 ms                                                             | 93.9 ms: 1.03x faster                                                 |
| dulwich_log             | 63.6 ms                                                             | 61.8 ms: 1.03x faster                                                 |
| go                      | 138 ms                                                              | 135 ms: 1.03x faster                                                  |
| sqlglot_normalize       | 108 ms                                                              | 105 ms: 1.03x faster                                                  |
| pyflate                 | 414 ms                                                              | 402 ms: 1.03x faster                                                  |
| pathlib                 | 18.2 ms                                                             | 17.7 ms: 1.03x faster                                                 |
| deepcopy_reduce         | 2.96 us                                                             | 2.89 us: 1.02x faster                                                 |
| thrift                  | 766 us                                                              | 748 us: 1.02x faster                                                  |
| pprint_safe_repr        | 701 ms                                                              | 685 ms: 1.02x faster                                                  |
| sqlglot_parse           | 1.36 ms                                                             | 1.33 ms: 1.02x faster                                                 |
| sqlglot_transpile       | 1.65 ms                                                             | 1.62 ms: 1.02x faster                                                 |
| dask                    | 368 ms                                                              | 360 ms: 1.02x faster                                                  |
| unpickle                | 13.2 us                                                             | 12.9 us: 1.02x faster                                                 |
| async_generators        | 361 ms                                                              | 355 ms: 1.02x faster                                                  |
| sympy_sum               | 167 ms                                                              | 165 ms: 1.02x faster                                                  |
| create_gc_cycles        | 1.48 ms                                                             | 1.46 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed | 736 ms                                                              | 730 ms: 1.01x faster                                                  |
| pickle_dict             | 30.9 us                                                             | 30.8 us: 1.01x faster                                                 |
| asyncio_tcp             | 888 ms                                                              | 884 ms: 1.00x faster                                                  |
| xml_etree_process       | 54.1 ms                                                             | 53.9 ms: 1.00x faster                                                 |
| pickle_list             | 4.03 us                                                             | 4.06 us: 1.01x slower                                                 |
| xml_etree_generate      | 76.5 ms                                                             | 77.2 ms: 1.01x slower                                                 |
| pickle                  | 9.79 us                                                             | 9.88 us: 1.01x slower                                                 |
| python_startup          | 8.49 ms                                                             | 8.58 ms: 1.01x slower                                                 |
| crypto_pyaes            | 73.8 ms                                                             | 74.6 ms: 1.01x slower                                                 |
| python_startup_no_site  | 5.98 ms                                                             | 6.12 ms: 1.02x slower                                                 |
| async_tree_io           | 1.28 sec                                                            | 1.32 sec: 1.03x slower                                                |
| sqlite_synth            | 2.51 us                                                             | 2.60 us: 1.04x slower                                                 |
| gc_traversal            | 3.63 ms                                                             | 3.77 ms: 1.04x slower                                                 |
| regex_effbot            | 3.32 ms                                                             | 3.47 ms: 1.04x slower                                                 |
| async_tree_memoization  | 621 ms                                                              | 653 ms: 1.05x slower                                                  |
| generators              | 73.4 ms                                                             | 77.4 ms: 1.05x slower                                                 |
| comprehensions          | 22.2 us                                                             | 23.4 us: 1.05x slower                                                 |
| regex_dna               | 196 ms                                                              | 208 ms: 1.06x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.04x faster                                                          |

Benchmark hidden because not significant (8): coverage, scimark_lu, django_template, bench_mp_pool, scimark_monte_carlo, async_tree_none, unpickle_list, djangocms
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
