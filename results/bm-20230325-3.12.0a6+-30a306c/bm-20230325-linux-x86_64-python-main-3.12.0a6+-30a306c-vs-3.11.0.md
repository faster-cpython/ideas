
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 30a306c
- commit date: 2023-03-25
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 254 ms: 1.01x faster                                   |
| docutils       | 2.59 sec                                                            | 2.56 sec: 1.01x faster                                 |
| html5lib       | 64.0 ms                                                             | 62.0 ms: 1.03x faster                                  |
| tornado_http   | 96.7 ms                                                             | 91.2 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 96.7 ms                                                             | 89.5 ms: 1.08x faster                                  |
| pidigits       | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| float          | 76.0 ms                                                             | 73.8 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                               | 1.05x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 137 ms                                                              | 134 ms: 1.02x faster                                   |
| regex_v8       | 22.0 ms                                                             | 22.4 ms: 1.02x slower                                  |
| regex_dna      | 196 ms                                                              | 204 ms: 1.04x slower                                   |
| regex_effbot   | 3.32 ms                                                             | 3.45 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                               | 1.02x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.58 ms: 1.31x faster                                  |
| unpickle_pure_python | 228 us                                                              | 200 us: 1.14x faster                                   |
| xml_etree_parse      | 162 ms                                                              | 148 ms: 1.09x faster                                   |
| json_loads           | 26.2 us                                                             | 24.0 us: 1.09x faster                                  |
| xml_etree_iterparse  | 108 ms                                                              | 101 ms: 1.07x faster                                   |
| pickle_pure_python   | 307 us                                                              | 287 us: 1.07x faster                                   |
| xml_etree_process    | 54.1 ms                                                             | 56.0 ms: 1.03x slower                                  |
| pickle_dict          | 30.9 us                                                             | 32.3 us: 1.04x slower                                  |
| pickle               | 9.79 us                                                             | 10.4 us: 1.07x slower                                  |
| xml_etree_generate   | 76.5 ms                                                             | 81.7 ms: 1.07x slower                                  |
| pickle_list          | 4.03 us                                                             | 4.35 us: 1.08x slower                                  |
| Geometric mean       | (ref)                                                               | 1.03x faster                                           |

Benchmark hidden because not significant (2): unpickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.86 ms: 1.04x slower                                  |
| python_startup_no_site | 5.98 ms                                                             | 6.54 ms: 1.09x slower                                  |
| Geometric mean         | (ref)                                                               | 1.07x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 48.3 ms: 1.07x faster                                  |
| genshi_text     | 21.8 ms                                                             | 21.3 ms: 1.03x faster                                  |
| django_template | 32.9 ms                                                             | 33.5 ms: 1.02x slower                                  |
| Geometric mean  | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 73.4 ms                                                             | 29.6 ms: 2.48x faster                                  |
| asyncio_tcp             | 888 ms                                                              | 504 ms: 1.76x faster                                   |
| json_dumps              | 12.5 ms                                                             | 9.58 ms: 1.31x faster                                  |
| mypy2                   | 422 ms                                                              | 333 ms: 1.27x faster                                   |
| unpack_sequence         | 49.5 ns                                                             | 42.1 ns: 1.17x faster                                  |
| unpickle_pure_python    | 228 us                                                              | 200 us: 1.14x faster                                   |
| coroutines              | 26.3 ms                                                             | 23.0 ms: 1.14x faster                                  |
| deltablue               | 3.66 ms                                                             | 3.21 ms: 1.14x faster                                  |
| xml_etree_parse         | 162 ms                                                              | 148 ms: 1.09x faster                                   |
| spectral_norm           | 99.5 ms                                                             | 90.9 ms: 1.09x faster                                  |
| json_loads              | 26.2 us                                                             | 24.0 us: 1.09x faster                                  |
| hexiom                  | 6.48 ms                                                             | 5.99 ms: 1.08x faster                                  |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.14 ms: 1.08x faster                                  |
| nbody                   | 96.7 ms                                                             | 89.5 ms: 1.08x faster                                  |
| scimark_fft             | 328 ms                                                              | 305 ms: 1.07x faster                                   |
| genshi_xml              | 51.8 ms                                                             | 48.3 ms: 1.07x faster                                  |
| deepcopy_memo           | 36.4 us                                                             | 34.1 us: 1.07x faster                                  |
| xml_etree_iterparse     | 108 ms                                                              | 101 ms: 1.07x faster                                   |
| pickle_pure_python      | 307 us                                                              | 287 us: 1.07x faster                                   |
| logging_simple          | 6.09 us                                                             | 5.74 us: 1.06x faster                                  |
| tornado_http            | 96.7 ms                                                             | 91.2 ms: 1.06x faster                                  |
| json                    | 4.86 ms                                                             | 4.59 ms: 1.06x faster                                  |
| logging_format          | 6.64 us                                                             | 6.32 us: 1.05x faster                                  |
| pidigits                | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| aiohttp                 | 1.05 ms                                                             | 1.01 ms: 1.05x faster                                  |
| sqlglot_optimize        | 53.4 ms                                                             | 51.3 ms: 1.04x faster                                  |
| gunicorn                | 1.13 ms                                                             | 1.09 ms: 1.04x faster                                  |
| richards                | 45.7 ms                                                             | 44.0 ms: 1.04x faster                                  |
| bench_thread_pool       | 820 us                                                              | 790 us: 1.04x faster                                   |
| coverage                | 101 ms                                                              | 97.6 ms: 1.04x faster                                  |
| mdp                     | 2.64 sec                                                            | 2.55 sec: 1.04x faster                                 |
| raytrace                | 292 ms                                                              | 282 ms: 1.03x faster                                   |
| chaos                   | 68.0 ms                                                             | 65.8 ms: 1.03x faster                                  |
| html5lib                | 64.0 ms                                                             | 62.0 ms: 1.03x faster                                  |
| deepcopy                | 339 us                                                              | 328 us: 1.03x faster                                   |
| meteor_contest          | 106 ms                                                              | 103 ms: 1.03x faster                                   |
| float                   | 76.0 ms                                                             | 73.8 ms: 1.03x faster                                  |
| sympy_expand            | 477 ms                                                              | 463 ms: 1.03x faster                                   |
| scimark_monte_carlo     | 67.8 ms                                                             | 65.9 ms: 1.03x faster                                  |
| genshi_text             | 21.8 ms                                                             | 21.3 ms: 1.03x faster                                  |
| sympy_integrate         | 21.0 ms                                                             | 20.5 ms: 1.03x faster                                  |
| scimark_sor             | 115 ms                                                              | 112 ms: 1.02x faster                                   |
| telco                   | 6.59 ms                                                             | 6.44 ms: 1.02x faster                                  |
| sqlglot_normalize       | 108 ms                                                              | 106 ms: 1.02x faster                                   |
| fannkuch                | 384 ms                                                              | 375 ms: 1.02x faster                                   |
| sympy_str               | 291 ms                                                              | 285 ms: 1.02x faster                                   |
| pprint_pformat          | 1.45 sec                                                            | 1.42 sec: 1.02x faster                                 |
| nqueens                 | 84.0 ms                                                             | 82.5 ms: 1.02x faster                                  |
| regex_compile           | 137 ms                                                              | 134 ms: 1.02x faster                                   |
| pathlib                 | 18.2 ms                                                             | 17.9 ms: 1.02x faster                                  |
| go                      | 138 ms                                                              | 137 ms: 1.01x faster                                   |
| pprint_safe_repr        | 701 ms                                                              | 692 ms: 1.01x faster                                   |
| logging_silent          | 98.7 ns                                                             | 97.6 ns: 1.01x faster                                  |
| 2to3                    | 257 ms                                                              | 254 ms: 1.01x faster                                   |
| async_tree_none         | 525 ms                                                              | 520 ms: 1.01x faster                                   |
| docutils                | 2.59 sec                                                            | 2.56 sec: 1.01x faster                                 |
| pyflate                 | 414 ms                                                              | 410 ms: 1.01x faster                                   |
| crypto_pyaes            | 73.8 ms                                                             | 73.2 ms: 1.01x faster                                  |
| sympy_sum               | 167 ms                                                              | 166 ms: 1.01x faster                                   |
| create_gc_cycles        | 1.48 ms                                                             | 1.48 ms: 1.00x slower                                  |
| scimark_lu              | 108 ms                                                              | 109 ms: 1.01x slower                                   |
| async_tree_io           | 1.28 sec                                                            | 1.30 sec: 1.01x slower                                 |
| deepcopy_reduce         | 2.96 us                                                             | 3.00 us: 1.01x slower                                  |
| django_template         | 32.9 ms                                                             | 33.5 ms: 1.02x slower                                  |
| regex_v8                | 22.0 ms                                                             | 22.4 ms: 1.02x slower                                  |
| pycparser               | 1.14 sec                                                            | 1.18 sec: 1.03x slower                                 |
| xml_etree_process       | 54.1 ms                                                             | 56.0 ms: 1.03x slower                                  |
| async_tree_memoization  | 621 ms                                                              | 643 ms: 1.03x slower                                   |
| regex_dna               | 196 ms                                                              | 204 ms: 1.04x slower                                   |
| regex_effbot            | 3.32 ms                                                             | 3.45 ms: 1.04x slower                                  |
| sqlglot_transpile       | 1.65 ms                                                             | 1.72 ms: 1.04x slower                                  |
| thrift                  | 766 us                                                              | 795 us: 1.04x slower                                   |
| python_startup          | 8.49 ms                                                             | 8.86 ms: 1.04x slower                                  |
| pickle_dict             | 30.9 us                                                             | 32.3 us: 1.04x slower                                  |
| sqlglot_parse           | 1.36 ms                                                             | 1.42 ms: 1.05x slower                                  |
| sqlite_synth            | 2.51 us                                                             | 2.65 us: 1.05x slower                                  |
| comprehensions          | 22.2 us                                                             | 23.5 us: 1.06x slower                                  |
| pickle                  | 9.79 us                                                             | 10.4 us: 1.07x slower                                  |
| xml_etree_generate      | 76.5 ms                                                             | 81.7 ms: 1.07x slower                                  |
| pickle_list             | 4.03 us                                                             | 4.35 us: 1.08x slower                                  |
| gc_traversal            | 3.63 ms                                                             | 3.93 ms: 1.08x slower                                  |
| python_startup_no_site  | 5.98 ms                                                             | 6.54 ms: 1.09x slower                                  |
| async_generators        | 361 ms                                                              | 409 ms: 1.13x slower                                   |
| dask                    | 368 ms                                                              | 514 ms: 1.40x slower                                   |
| Geometric mean          | (ref)                                                               | 1.03x faster                                           |

Benchmark hidden because not significant (10): djangocms, sqlalchemy_declarative, async_tree_cpu_io_mixed, sqlalchemy_imperative, bench_mp_pool, mako, unpickle_list, unpickle, dulwich_log, chameleon
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint
