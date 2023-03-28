
# Results vs. 3.11.0

- fork: python
- ref: 4ae1a0ecaffe4320fe97
- machine: linux-x86_64
- commit hash: 4ae1a0e
- commit date: 2022-10-25
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 249 ms: 1.03x faster                                                  |
| docutils       | 2.59 sec                                                            | 2.52 sec: 1.03x faster                                                |
| html5lib       | 64.0 ms                                                             | 59.9 ms: 1.07x faster                                                 |
| tornado_http   | 96.7 ms                                                             | 93.7 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                               | 1.03x faster                                                          |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.0 ms                                                             | 71.4 ms: 1.06x faster                                                 |
| pidigits       | 197 ms                                                              | 198 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                              | 127 ms: 1.07x faster                                                  |
| regex_v8       | 22.0 ms                                                             | 21.4 ms: 1.03x faster                                                 |
| regex_effbot   | 3.32 ms                                                             | 3.37 ms: 1.02x slower                                                 |
| regex_dna      | 196 ms                                                              | 201 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                               | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.36 ms: 1.34x faster                                                 |
| unpickle_pure_python | 228 us                                                              | 202 us: 1.13x faster                                                  |
| json_loads           | 26.2 us                                                             | 23.5 us: 1.12x faster                                                 |
| xml_etree_parse      | 162 ms                                                              | 145 ms: 1.11x faster                                                  |
| pickle_pure_python   | 307 us                                                              | 285 us: 1.08x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                              | 101 ms: 1.07x faster                                                  |
| xml_etree_process    | 54.1 ms                                                             | 53.4 ms: 1.01x faster                                                 |
| unpickle_list        | 4.96 us                                                             | 4.91 us: 1.01x faster                                                 |
| xml_etree_generate   | 76.5 ms                                                             | 76.0 ms: 1.01x faster                                                 |
| pickle_dict          | 30.9 us                                                             | 31.1 us: 1.01x slower                                                 |
| pickle               | 9.79 us                                                             | 10.1 us: 1.04x slower                                                 |
| pickle_list          | 4.03 us                                                             | 4.19 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.06x faster                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.42 ms: 1.01x faster                                                 |
| python_startup_no_site | 5.98 ms                                                             | 5.93 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                               | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 51.8 ms                                                             | 50.0 ms: 1.04x faster                                                 |
| mako           | 9.82 ms                                                             | 9.64 ms: 1.02x faster                                                 |
| genshi_text    | 21.8 ms                                                             | 21.5 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                               | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps              | 12.5 ms                                                             | 9.36 ms: 1.34x faster                                                 |
| mypy2                   | 422 ms                                                              | 328 ms: 1.28x faster                                                  |
| unpickle_pure_python    | 228 us                                                              | 202 us: 1.13x faster                                                  |
| unpack_sequence         | 49.5 ns                                                             | 44.1 ns: 1.12x faster                                                 |
| json_loads              | 26.2 us                                                             | 23.5 us: 1.12x faster                                                 |
| xml_etree_parse         | 162 ms                                                              | 145 ms: 1.11x faster                                                  |
| deltablue               | 3.66 ms                                                             | 3.30 ms: 1.11x faster                                                 |
| scimark_sor             | 115 ms                                                              | 106 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.13 ms: 1.08x faster                                                 |
| logging_silent          | 98.7 ns                                                             | 91.6 ns: 1.08x faster                                                 |
| pickle_pure_python      | 307 us                                                              | 285 us: 1.08x faster                                                  |
| richards                | 45.7 ms                                                             | 42.4 ms: 1.08x faster                                                 |
| regex_compile           | 137 ms                                                              | 127 ms: 1.07x faster                                                  |
| xml_etree_iterparse     | 108 ms                                                              | 101 ms: 1.07x faster                                                  |
| html5lib                | 64.0 ms                                                             | 59.9 ms: 1.07x faster                                                 |
| json                    | 4.86 ms                                                             | 4.55 ms: 1.07x faster                                                 |
| coroutines              | 26.3 ms                                                             | 24.7 ms: 1.07x faster                                                 |
| float                   | 76.0 ms                                                             | 71.4 ms: 1.06x faster                                                 |
| mdp                     | 2.64 sec                                                            | 2.48 sec: 1.06x faster                                                |
| hexiom                  | 6.48 ms                                                             | 6.11 ms: 1.06x faster                                                 |
| deepcopy_memo           | 36.4 us                                                             | 34.4 us: 1.06x faster                                                 |
| pprint_pformat          | 1.45 sec                                                            | 1.38 sec: 1.05x faster                                                |
| pprint_safe_repr        | 701 ms                                                              | 665 ms: 1.05x faster                                                  |
| gunicorn                | 1.13 ms                                                             | 1.07 ms: 1.05x faster                                                 |
| logging_simple          | 6.09 us                                                             | 5.80 us: 1.05x faster                                                 |
| scimark_fft             | 328 ms                                                              | 312 ms: 1.05x faster                                                  |
| bench_thread_pool       | 820 us                                                              | 780 us: 1.05x faster                                                  |
| aiohttp                 | 1.05 ms                                                             | 1.00 ms: 1.05x faster                                                 |
| sympy_expand            | 477 ms                                                              | 455 ms: 1.05x faster                                                  |
| spectral_norm           | 99.5 ms                                                             | 95.2 ms: 1.04x faster                                                 |
| comprehensions          | 22.2 us                                                             | 21.3 us: 1.04x faster                                                 |
| nqueens                 | 84.0 ms                                                             | 80.7 ms: 1.04x faster                                                 |
| sqlglot_optimize        | 53.4 ms                                                             | 51.2 ms: 1.04x faster                                                 |
| logging_format          | 6.64 us                                                             | 6.38 us: 1.04x faster                                                 |
| pylint                  | 476 ms                                                              | 458 ms: 1.04x faster                                                  |
| sqlglot_normalize       | 108 ms                                                              | 104 ms: 1.04x faster                                                  |
| fannkuch                | 384 ms                                                              | 370 ms: 1.04x faster                                                  |
| genshi_xml              | 51.8 ms                                                             | 50.0 ms: 1.04x faster                                                 |
| async_generators        | 361 ms                                                              | 349 ms: 1.04x faster                                                  |
| raytrace                | 292 ms                                                              | 282 ms: 1.03x faster                                                  |
| tornado_http            | 96.7 ms                                                             | 93.7 ms: 1.03x faster                                                 |
| sympy_str               | 291 ms                                                              | 283 ms: 1.03x faster                                                  |
| 2to3                    | 257 ms                                                              | 249 ms: 1.03x faster                                                  |
| sympy_integrate         | 21.0 ms                                                             | 20.4 ms: 1.03x faster                                                 |
| docutils                | 2.59 sec                                                            | 2.52 sec: 1.03x faster                                                |
| regex_v8                | 22.0 ms                                                             | 21.4 ms: 1.03x faster                                                 |
| thrift                  | 766 us                                                              | 746 us: 1.03x faster                                                  |
| pycparser               | 1.14 sec                                                            | 1.12 sec: 1.02x faster                                                |
| go                      | 138 ms                                                              | 135 ms: 1.02x faster                                                  |
| dask                    | 368 ms                                                              | 360 ms: 1.02x faster                                                  |
| sympy_sum               | 167 ms                                                              | 164 ms: 1.02x faster                                                  |
| gc_traversal            | 3.63 ms                                                             | 3.55 ms: 1.02x faster                                                 |
| meteor_contest          | 106 ms                                                              | 104 ms: 1.02x faster                                                  |
| dulwich_log             | 63.6 ms                                                             | 62.4 ms: 1.02x faster                                                 |
| deepcopy                | 339 us                                                              | 333 us: 1.02x faster                                                  |
| mako                    | 9.82 ms                                                             | 9.64 ms: 1.02x faster                                                 |
| deepcopy_reduce         | 2.96 us                                                             | 2.91 us: 1.02x faster                                                 |
| genshi_text             | 21.8 ms                                                             | 21.5 ms: 1.02x faster                                                 |
| scimark_monte_carlo     | 67.8 ms                                                             | 66.6 ms: 1.02x faster                                                 |
| create_gc_cycles        | 1.48 ms                                                             | 1.46 ms: 1.02x faster                                                 |
| sqlglot_parse           | 1.36 ms                                                             | 1.34 ms: 1.02x faster                                                 |
| pyflate                 | 414 ms                                                              | 407 ms: 1.02x faster                                                  |
| pathlib                 | 18.2 ms                                                             | 17.9 ms: 1.02x faster                                                 |
| xml_etree_process       | 54.1 ms                                                             | 53.4 ms: 1.01x faster                                                 |
| sqlglot_transpile       | 1.65 ms                                                             | 1.63 ms: 1.01x faster                                                 |
| chaos                   | 68.0 ms                                                             | 67.1 ms: 1.01x faster                                                 |
| unpickle_list           | 4.96 us                                                             | 4.91 us: 1.01x faster                                                 |
| python_startup          | 8.49 ms                                                             | 8.42 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed | 736 ms                                                              | 730 ms: 1.01x faster                                                  |
| python_startup_no_site  | 5.98 ms                                                             | 5.93 ms: 1.01x faster                                                 |
| xml_etree_generate      | 76.5 ms                                                             | 76.0 ms: 1.01x faster                                                 |
| pidigits                | 197 ms                                                              | 198 ms: 1.00x slower                                                  |
| pickle_dict             | 30.9 us                                                             | 31.1 us: 1.01x slower                                                 |
| generators              | 73.4 ms                                                             | 74.1 ms: 1.01x slower                                                 |
| crypto_pyaes            | 73.8 ms                                                             | 74.8 ms: 1.01x slower                                                 |
| regex_effbot            | 3.32 ms                                                             | 3.37 ms: 1.02x slower                                                 |
| regex_dna               | 196 ms                                                              | 201 ms: 1.02x slower                                                  |
| async_tree_io           | 1.28 sec                                                            | 1.33 sec: 1.04x slower                                                |
| pickle                  | 9.79 us                                                             | 10.1 us: 1.04x slower                                                 |
| pickle_list             | 4.03 us                                                             | 4.19 us: 1.04x slower                                                 |
| sqlite_synth            | 2.51 us                                                             | 2.62 us: 1.04x slower                                                 |
| async_tree_memoization  | 621 ms                                                              | 656 ms: 1.06x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.03x faster                                                          |

Benchmark hidden because not significant (11): telco, unpickle, nbody, chameleon, bench_mp_pool, scimark_lu, asyncio_tcp, django_template, coverage, async_tree_none, djangocms
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
