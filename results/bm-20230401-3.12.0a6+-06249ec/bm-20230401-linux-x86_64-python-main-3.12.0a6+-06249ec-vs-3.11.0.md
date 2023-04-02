
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 06249ec
- commit date: 2023-04-01
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 251 ms: 1.02x faster                                   |
| chameleon      | 6.52 ms                                                             | 6.49 ms: 1.00x faster                                  |
| docutils       | 2.59 sec                                                            | 2.56 sec: 1.01x faster                                 |
| html5lib       | 64.0 ms                                                             | 61.4 ms: 1.04x faster                                  |
| tornado_http   | 96.7 ms                                                             | 91.1 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                               | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 96.7 ms                                                             | 87.4 ms: 1.11x faster                                  |
| pidigits       | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| float          | 76.0 ms                                                             | 75.2 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                               | 1.05x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 137 ms                                                              | 134 ms: 1.02x faster                                   |
| regex_dna      | 196 ms                                                              | 207 ms: 1.06x slower                                   |
| regex_effbot   | 3.32 ms                                                             | 3.54 ms: 1.07x slower                                  |
| Geometric mean | (ref)                                                               | 1.02x slower                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.43 ms: 1.33x faster                                  |
| unpickle_pure_python | 228 us                                                              | 202 us: 1.13x faster                                   |
| xml_etree_parse      | 162 ms                                                              | 149 ms: 1.09x faster                                   |
| json_loads           | 26.2 us                                                             | 24.3 us: 1.08x faster                                  |
| pickle_pure_python   | 307 us                                                              | 288 us: 1.07x faster                                   |
| xml_etree_iterparse  | 108 ms                                                              | 102 ms: 1.05x faster                                   |
| pickle_dict          | 30.9 us                                                             | 30.6 us: 1.01x faster                                  |
| unpickle             | 13.2 us                                                             | 13.3 us: 1.01x slower                                  |
| unpickle_list        | 4.96 us                                                             | 5.07 us: 1.02x slower                                  |
| xml_etree_process    | 54.1 ms                                                             | 56.0 ms: 1.04x slower                                  |
| pickle_list          | 4.03 us                                                             | 4.20 us: 1.04x slower                                  |
| xml_etree_generate   | 76.5 ms                                                             | 80.9 ms: 1.06x slower                                  |
| pickle               | 9.79 us                                                             | 10.5 us: 1.07x slower                                  |
| Geometric mean       | (ref)                                                               | 1.04x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.83 ms: 1.04x slower                                  |
| python_startup_no_site | 5.98 ms                                                             | 6.53 ms: 1.09x slower                                  |
| Geometric mean         | (ref)                                                               | 1.07x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 47.8 ms: 1.08x faster                                  |
| genshi_text     | 21.8 ms                                                             | 21.3 ms: 1.02x faster                                  |
| django_template | 32.9 ms                                                             | 33.8 ms: 1.03x slower                                  |
| mako            | 9.82 ms                                                             | 10.1 ms: 1.03x slower                                  |
| Geometric mean  | (ref)                                                               | 1.01x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 73.4 ms                                                             | 29.9 ms: 2.46x faster                                  |
| asyncio_tcp             | 888 ms                                                              | 505 ms: 1.76x faster                                   |
| json_dumps              | 12.5 ms                                                             | 9.43 ms: 1.33x faster                                  |
| mypy2                   | 422 ms                                                              | 333 ms: 1.27x faster                                   |
| coroutines              | 26.3 ms                                                             | 22.9 ms: 1.15x faster                                  |
| unpickle_pure_python    | 228 us                                                              | 202 us: 1.13x faster                                   |
| deltablue               | 3.66 ms                                                             | 3.24 ms: 1.13x faster                                  |
| nbody                   | 96.7 ms                                                             | 87.4 ms: 1.11x faster                                  |
| xml_etree_parse         | 162 ms                                                              | 149 ms: 1.09x faster                                   |
| genshi_xml              | 51.8 ms                                                             | 47.8 ms: 1.08x faster                                  |
| json_loads              | 26.2 us                                                             | 24.3 us: 1.08x faster                                  |
| pickle_pure_python      | 307 us                                                              | 288 us: 1.07x faster                                   |
| unpack_sequence         | 49.5 ns                                                             | 46.4 ns: 1.07x faster                                  |
| logging_simple          | 6.09 us                                                             | 5.72 us: 1.06x faster                                  |
| hexiom                  | 6.48 ms                                                             | 6.10 ms: 1.06x faster                                  |
| tornado_http            | 96.7 ms                                                             | 91.1 ms: 1.06x faster                                  |
| coverage                | 101 ms                                                              | 95.5 ms: 1.06x faster                                  |
| xml_etree_iterparse     | 108 ms                                                              | 102 ms: 1.05x faster                                   |
| json                    | 4.86 ms                                                             | 4.62 ms: 1.05x faster                                  |
| pidigits                | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| aiohttp                 | 1.05 ms                                                             | 1.01 ms: 1.05x faster                                  |
| scimark_fft             | 328 ms                                                              | 314 ms: 1.05x faster                                   |
| mdp                     | 2.64 sec                                                            | 2.53 sec: 1.04x faster                                 |
| bench_thread_pool       | 820 us                                                              | 786 us: 1.04x faster                                   |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.29 ms: 1.04x faster                                  |
| sqlglot_optimize        | 53.4 ms                                                             | 51.2 ms: 1.04x faster                                  |
| html5lib                | 64.0 ms                                                             | 61.4 ms: 1.04x faster                                  |
| gunicorn                | 1.13 ms                                                             | 1.09 ms: 1.04x faster                                  |
| deepcopy_memo           | 36.4 us                                                             | 35.1 us: 1.04x faster                                  |
| logging_format          | 6.64 us                                                             | 6.42 us: 1.03x faster                                  |
| sqlglot_normalize       | 108 ms                                                              | 105 ms: 1.03x faster                                   |
| nqueens                 | 84.0 ms                                                             | 81.3 ms: 1.03x faster                                  |
| richards                | 45.7 ms                                                             | 44.3 ms: 1.03x faster                                  |
| pycparser               | 1.14 sec                                                            | 1.11 sec: 1.03x faster                                 |
| meteor_contest          | 106 ms                                                              | 103 ms: 1.03x faster                                   |
| sympy_integrate         | 21.0 ms                                                             | 20.4 ms: 1.03x faster                                  |
| sympy_expand            | 477 ms                                                              | 462 ms: 1.03x faster                                   |
| spectral_norm           | 99.5 ms                                                             | 96.5 ms: 1.03x faster                                  |
| sympy_str               | 291 ms                                                              | 283 ms: 1.03x faster                                   |
| deepcopy                | 339 us                                                              | 330 us: 1.03x faster                                   |
| chaos                   | 68.0 ms                                                             | 66.2 ms: 1.03x faster                                  |
| sqlalchemy_imperative   | 18.0 ms                                                             | 17.6 ms: 1.02x faster                                  |
| genshi_text             | 21.8 ms                                                             | 21.3 ms: 1.02x faster                                  |
| 2to3                    | 257 ms                                                              | 251 ms: 1.02x faster                                   |
| logging_silent          | 98.7 ns                                                             | 96.6 ns: 1.02x faster                                  |
| raytrace                | 292 ms                                                              | 286 ms: 1.02x faster                                   |
| pprint_pformat          | 1.45 sec                                                            | 1.42 sec: 1.02x faster                                 |
| regex_compile           | 137 ms                                                              | 134 ms: 1.02x faster                                   |
| pathlib                 | 18.2 ms                                                             | 18.0 ms: 1.01x faster                                  |
| sqlalchemy_declarative  | 138 ms                                                              | 137 ms: 1.01x faster                                   |
| telco                   | 6.59 ms                                                             | 6.51 ms: 1.01x faster                                  |
| pickle_dict             | 30.9 us                                                             | 30.6 us: 1.01x faster                                  |
| pprint_safe_repr        | 701 ms                                                              | 694 ms: 1.01x faster                                   |
| float                   | 76.0 ms                                                             | 75.2 ms: 1.01x faster                                  |
| docutils                | 2.59 sec                                                            | 2.56 sec: 1.01x faster                                 |
| gc_traversal            | 3.63 ms                                                             | 3.60 ms: 1.01x faster                                  |
| sympy_sum               | 167 ms                                                              | 167 ms: 1.01x faster                                   |
| dulwich_log             | 63.6 ms                                                             | 63.4 ms: 1.00x faster                                  |
| chameleon               | 6.52 ms                                                             | 6.49 ms: 1.00x faster                                  |
| create_gc_cycles        | 1.48 ms                                                             | 1.49 ms: 1.01x slower                                  |
| scimark_lu              | 108 ms                                                              | 109 ms: 1.01x slower                                   |
| unpickle                | 13.2 us                                                             | 13.3 us: 1.01x slower                                  |
| async_tree_io           | 1.28 sec                                                            | 1.29 sec: 1.01x slower                                 |
| go                      | 138 ms                                                              | 140 ms: 1.01x slower                                   |
| deepcopy_reduce         | 2.96 us                                                             | 3.00 us: 1.02x slower                                  |
| pyflate                 | 414 ms                                                              | 420 ms: 1.02x slower                                   |
| thrift                  | 766 us                                                              | 783 us: 1.02x slower                                   |
| unpickle_list           | 4.96 us                                                             | 5.07 us: 1.02x slower                                  |
| django_template         | 32.9 ms                                                             | 33.8 ms: 1.03x slower                                  |
| mako                    | 9.82 ms                                                             | 10.1 ms: 1.03x slower                                  |
| xml_etree_process       | 54.1 ms                                                             | 56.0 ms: 1.04x slower                                  |
| sqlite_synth            | 2.51 us                                                             | 2.61 us: 1.04x slower                                  |
| sqlglot_transpile       | 1.65 ms                                                             | 1.72 ms: 1.04x slower                                  |
| python_startup          | 8.49 ms                                                             | 8.83 ms: 1.04x slower                                  |
| pickle_list             | 4.03 us                                                             | 4.20 us: 1.04x slower                                  |
| sqlglot_parse           | 1.36 ms                                                             | 1.42 ms: 1.04x slower                                  |
| regex_dna               | 196 ms                                                              | 207 ms: 1.06x slower                                   |
| xml_etree_generate      | 76.5 ms                                                             | 80.9 ms: 1.06x slower                                  |
| async_tree_memoization  | 621 ms                                                              | 657 ms: 1.06x slower                                   |
| regex_effbot            | 3.32 ms                                                             | 3.54 ms: 1.07x slower                                  |
| pickle                  | 9.79 us                                                             | 10.5 us: 1.07x slower                                  |
| comprehensions          | 22.2 us                                                             | 23.9 us: 1.07x slower                                  |
| python_startup_no_site  | 5.98 ms                                                             | 6.53 ms: 1.09x slower                                  |
| async_generators        | 361 ms                                                              | 411 ms: 1.14x slower                                   |
| dask                    | 368 ms                                                              | 512 ms: 1.39x slower                                   |
| Geometric mean          | (ref)                                                               | 1.03x faster                                           |

Benchmark hidden because not significant (9): regex_v8, async_tree_none, scimark_sor, bench_mp_pool, crypto_pyaes, fannkuch, djangocms, scimark_monte_carlo, async_tree_cpu_io_mixed
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint
