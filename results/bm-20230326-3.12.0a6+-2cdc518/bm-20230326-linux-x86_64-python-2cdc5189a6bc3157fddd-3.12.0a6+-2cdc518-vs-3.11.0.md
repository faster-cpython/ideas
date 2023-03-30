
# Results vs. 3.11.0

- fork: python
- ref: 2cdc5189a6bc3157fddd
- machine: linux-x86_64
- commit hash: 2cdc518
- commit date: 2023-03-26
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 253 ms: 1.02x faster                                                   |
| docutils       | 2.59 sec                                                            | 2.55 sec: 1.02x faster                                                 |
| html5lib       | 64.0 ms                                                             | 62.3 ms: 1.03x faster                                                  |
| tornado_http   | 96.7 ms                                                             | 91.1 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.7 ms                                                             | 87.8 ms: 1.10x faster                                                  |
| pidigits       | 197 ms                                                              | 188 ms: 1.05x faster                                                   |
| float          | 76.0 ms                                                             | 73.9 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                               | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                              | 135 ms: 1.01x faster                                                   |
| regex_v8       | 22.0 ms                                                             | 22.2 ms: 1.01x slower                                                  |
| regex_dna      | 196 ms                                                              | 208 ms: 1.06x slower                                                   |
| regex_effbot   | 3.32 ms                                                             | 3.66 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                               | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.57 ms: 1.31x faster                                                  |
| unpickle_pure_python | 228 us                                                              | 202 us: 1.13x faster                                                   |
| xml_etree_parse      | 162 ms                                                              | 149 ms: 1.09x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                              | 99.5 ms: 1.08x faster                                                  |
| json_loads           | 26.2 us                                                             | 24.2 us: 1.08x faster                                                  |
| pickle_pure_python   | 307 us                                                              | 285 us: 1.08x faster                                                   |
| pickle_dict          | 30.9 us                                                             | 31.0 us: 1.00x slower                                                  |
| unpickle_list        | 4.96 us                                                             | 5.01 us: 1.01x slower                                                  |
| xml_etree_process    | 54.1 ms                                                             | 56.0 ms: 1.04x slower                                                  |
| xml_etree_generate   | 76.5 ms                                                             | 80.3 ms: 1.05x slower                                                  |
| pickle_list          | 4.03 us                                                             | 4.27 us: 1.06x slower                                                  |
| pickle               | 9.79 us                                                             | 10.4 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.04x faster                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.79 ms: 1.04x slower                                                  |
| python_startup_no_site | 5.98 ms                                                             | 6.50 ms: 1.09x slower                                                  |
| Geometric mean         | (ref)                                                               | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 51.8 ms                                                             | 47.6 ms: 1.09x faster                                                  |
| genshi_text    | 21.8 ms                                                             | 21.5 ms: 1.02x faster                                                  |
| mako           | 9.82 ms                                                             | 9.89 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| generators              | 73.4 ms                                                             | 29.4 ms: 2.50x faster                                                  |
| asyncio_tcp             | 888 ms                                                              | 503 ms: 1.76x faster                                                   |
| json_dumps              | 12.5 ms                                                             | 9.57 ms: 1.31x faster                                                  |
| mypy2                   | 422 ms                                                              | 333 ms: 1.27x faster                                                   |
| deltablue               | 3.66 ms                                                             | 3.19 ms: 1.15x faster                                                  |
| unpack_sequence         | 49.5 ns                                                             | 43.7 ns: 1.13x faster                                                  |
| unpickle_pure_python    | 228 us                                                              | 202 us: 1.13x faster                                                   |
| nbody                   | 96.7 ms                                                             | 87.8 ms: 1.10x faster                                                  |
| coroutines              | 26.3 ms                                                             | 23.9 ms: 1.10x faster                                                  |
| xml_etree_parse         | 162 ms                                                              | 149 ms: 1.09x faster                                                   |
| genshi_xml              | 51.8 ms                                                             | 47.6 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.13 ms: 1.08x faster                                                  |
| xml_etree_iterparse     | 108 ms                                                              | 99.5 ms: 1.08x faster                                                  |
| json_loads              | 26.2 us                                                             | 24.2 us: 1.08x faster                                                  |
| hexiom                  | 6.48 ms                                                             | 6.01 ms: 1.08x faster                                                  |
| pickle_pure_python      | 307 us                                                              | 285 us: 1.08x faster                                                   |
| logging_simple          | 6.09 us                                                             | 5.68 us: 1.07x faster                                                  |
| deepcopy_memo           | 36.4 us                                                             | 34.1 us: 1.07x faster                                                  |
| scimark_fft             | 328 ms                                                              | 308 ms: 1.06x faster                                                   |
| tornado_http            | 96.7 ms                                                             | 91.1 ms: 1.06x faster                                                  |
| spectral_norm           | 99.5 ms                                                             | 94.0 ms: 1.06x faster                                                  |
| coverage                | 101 ms                                                              | 95.5 ms: 1.06x faster                                                  |
| logging_format          | 6.64 us                                                             | 6.28 us: 1.06x faster                                                  |
| json                    | 4.86 ms                                                             | 4.60 ms: 1.06x faster                                                  |
| richards                | 45.7 ms                                                             | 43.5 ms: 1.05x faster                                                  |
| aiohttp                 | 1.05 ms                                                             | 1.01 ms: 1.05x faster                                                  |
| pidigits                | 197 ms                                                              | 188 ms: 1.05x faster                                                   |
| raytrace                | 292 ms                                                              | 280 ms: 1.04x faster                                                   |
| pprint_pformat          | 1.45 sec                                                            | 1.40 sec: 1.04x faster                                                 |
| nqueens                 | 84.0 ms                                                             | 80.8 ms: 1.04x faster                                                  |
| sqlglot_optimize        | 53.4 ms                                                             | 51.3 ms: 1.04x faster                                                  |
| bench_thread_pool       | 820 us                                                              | 789 us: 1.04x faster                                                   |
| mdp                     | 2.64 sec                                                            | 2.54 sec: 1.04x faster                                                 |
| meteor_contest          | 106 ms                                                              | 102 ms: 1.04x faster                                                   |
| gunicorn                | 1.13 ms                                                             | 1.09 ms: 1.04x faster                                                  |
| deepcopy                | 339 us                                                              | 328 us: 1.03x faster                                                   |
| sympy_expand            | 477 ms                                                              | 463 ms: 1.03x faster                                                   |
| html5lib                | 64.0 ms                                                             | 62.3 ms: 1.03x faster                                                  |
| float                   | 76.0 ms                                                             | 73.9 ms: 1.03x faster                                                  |
| sqlalchemy_imperative   | 18.0 ms                                                             | 17.6 ms: 1.03x faster                                                  |
| pprint_safe_repr        | 701 ms                                                              | 685 ms: 1.02x faster                                                   |
| sympy_integrate         | 21.0 ms                                                             | 20.6 ms: 1.02x faster                                                  |
| logging_silent          | 98.7 ns                                                             | 96.5 ns: 1.02x faster                                                  |
| scimark_sor             | 115 ms                                                              | 112 ms: 1.02x faster                                                   |
| chaos                   | 68.0 ms                                                             | 66.5 ms: 1.02x faster                                                  |
| sympy_str               | 291 ms                                                              | 285 ms: 1.02x faster                                                   |
| genshi_text             | 21.8 ms                                                             | 21.5 ms: 1.02x faster                                                  |
| 2to3                    | 257 ms                                                              | 253 ms: 1.02x faster                                                   |
| pathlib                 | 18.2 ms                                                             | 17.9 ms: 1.02x faster                                                  |
| docutils                | 2.59 sec                                                            | 2.55 sec: 1.02x faster                                                 |
| sqlalchemy_declarative  | 138 ms                                                              | 136 ms: 1.02x faster                                                   |
| regex_compile           | 137 ms                                                              | 135 ms: 1.01x faster                                                   |
| go                      | 138 ms                                                              | 137 ms: 1.01x faster                                                   |
| create_gc_cycles        | 1.48 ms                                                             | 1.46 ms: 1.01x faster                                                  |
| sqlglot_normalize       | 108 ms                                                              | 107 ms: 1.01x faster                                                   |
| fannkuch                | 384 ms                                                              | 380 ms: 1.01x faster                                                   |
| sympy_sum               | 167 ms                                                              | 166 ms: 1.01x faster                                                   |
| dulwich_log             | 63.6 ms                                                             | 63.1 ms: 1.01x faster                                                  |
| pickle_dict             | 30.9 us                                                             | 31.0 us: 1.00x slower                                                  |
| mako                    | 9.82 ms                                                             | 9.89 ms: 1.01x slower                                                  |
| unpickle_list           | 4.96 us                                                             | 5.01 us: 1.01x slower                                                  |
| regex_v8                | 22.0 ms                                                             | 22.2 ms: 1.01x slower                                                  |
| telco                   | 6.59 ms                                                             | 6.67 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed | 736 ms                                                              | 746 ms: 1.01x slower                                                   |
| pyflate                 | 414 ms                                                              | 421 ms: 1.02x slower                                                   |
| thrift                  | 766 us                                                              | 780 us: 1.02x slower                                                   |
| pycparser               | 1.14 sec                                                            | 1.17 sec: 1.02x slower                                                 |
| xml_etree_process       | 54.1 ms                                                             | 56.0 ms: 1.04x slower                                                  |
| python_startup          | 8.49 ms                                                             | 8.79 ms: 1.04x slower                                                  |
| sqlglot_transpile       | 1.65 ms                                                             | 1.72 ms: 1.04x slower                                                  |
| sqlite_synth            | 2.51 us                                                             | 2.62 us: 1.04x slower                                                  |
| sqlglot_parse           | 1.36 ms                                                             | 1.43 ms: 1.05x slower                                                  |
| xml_etree_generate      | 76.5 ms                                                             | 80.3 ms: 1.05x slower                                                  |
| async_tree_memoization  | 621 ms                                                              | 652 ms: 1.05x slower                                                   |
| regex_dna               | 196 ms                                                              | 208 ms: 1.06x slower                                                   |
| pickle_list             | 4.03 us                                                             | 4.27 us: 1.06x slower                                                  |
| pickle                  | 9.79 us                                                             | 10.4 us: 1.06x slower                                                  |
| comprehensions          | 22.2 us                                                             | 23.7 us: 1.07x slower                                                  |
| python_startup_no_site  | 5.98 ms                                                             | 6.50 ms: 1.09x slower                                                  |
| regex_effbot            | 3.32 ms                                                             | 3.66 ms: 1.10x slower                                                  |
| async_generators        | 361 ms                                                              | 408 ms: 1.13x slower                                                   |
| gc_traversal            | 3.63 ms                                                             | 4.31 ms: 1.19x slower                                                  |
| dask                    | 368 ms                                                              | 511 ms: 1.39x slower                                                   |
| Geometric mean          | (ref)                                                               | 1.03x faster                                                           |

Benchmark hidden because not significant (11): deepcopy_reduce, unpickle, bench_mp_pool, scimark_monte_carlo, chameleon, async_tree_none, djangocms, django_template, scimark_lu, crypto_pyaes, async_tree_io
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint
