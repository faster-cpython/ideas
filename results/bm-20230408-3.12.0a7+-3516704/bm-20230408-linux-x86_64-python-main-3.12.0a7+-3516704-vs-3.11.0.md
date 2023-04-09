
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3516704
- commit date: 2023-04-08
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 251 ms: 1.03x faster                                   |
| docutils       | 2.59 sec                                                            | 2.54 sec: 1.02x faster                                 |
| html5lib       | 64.0 ms                                                             | 61.4 ms: 1.04x faster                                  |
| tornado_http   | 96.7 ms                                                             | 94.0 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 96.7 ms                                                             | 86.6 ms: 1.12x faster                                  |
| pidigits       | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| float          | 76.0 ms                                                             | 73.6 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                               | 1.07x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 137 ms                                                              | 135 ms: 1.01x faster                                   |
| regex_v8       | 22.0 ms                                                             | 22.1 ms: 1.01x slower                                  |
| regex_effbot   | 3.32 ms                                                             | 3.36 ms: 1.01x slower                                  |
| regex_dna      | 196 ms                                                              | 204 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                               | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.54 ms: 1.31x faster                                  |
| unpickle_pure_python | 228 us                                                              | 200 us: 1.14x faster                                   |
| xml_etree_parse      | 162 ms                                                              | 148 ms: 1.10x faster                                   |
| json_loads           | 26.2 us                                                             | 24.3 us: 1.08x faster                                  |
| pickle_pure_python   | 307 us                                                              | 288 us: 1.06x faster                                   |
| xml_etree_iterparse  | 108 ms                                                              | 102 ms: 1.05x faster                                   |
| unpickle_list        | 4.96 us                                                             | 5.07 us: 1.02x slower                                  |
| pickle_dict          | 30.9 us                                                             | 31.9 us: 1.03x slower                                  |
| xml_etree_process    | 54.1 ms                                                             | 55.9 ms: 1.03x slower                                  |
| xml_etree_generate   | 76.5 ms                                                             | 81.2 ms: 1.06x slower                                  |
| unpickle             | 13.2 us                                                             | 14.0 us: 1.06x slower                                  |
| pickle_list          | 4.03 us                                                             | 4.29 us: 1.07x slower                                  |
| pickle               | 9.79 us                                                             | 10.7 us: 1.09x slower                                  |
| Geometric mean       | (ref)                                                               | 1.03x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.82 ms: 1.04x slower                                  |
| python_startup_no_site | 5.98 ms                                                             | 6.51 ms: 1.09x slower                                  |
| Geometric mean         | (ref)                                                               | 1.06x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 47.8 ms: 1.08x faster                                  |
| genshi_text     | 21.8 ms                                                             | 21.3 ms: 1.03x faster                                  |
| django_template | 32.9 ms                                                             | 33.0 ms: 1.00x slower                                  |
| mako            | 9.82 ms                                                             | 9.97 ms: 1.01x slower                                  |
| Geometric mean  | (ref)                                                               | 1.02x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 73.4 ms                                                             | 29.0 ms: 2.54x faster                                  |
| asyncio_tcp             | 888 ms                                                              | 506 ms: 1.75x faster                                   |
| json_dumps              | 12.5 ms                                                             | 9.54 ms: 1.31x faster                                  |
| mypy2                   | 422 ms                                                              | 336 ms: 1.26x faster                                   |
| coroutines              | 26.3 ms                                                             | 22.8 ms: 1.15x faster                                  |
| unpickle_pure_python    | 228 us                                                              | 200 us: 1.14x faster                                   |
| unpack_sequence         | 49.5 ns                                                             | 43.5 ns: 1.14x faster                                  |
| deltablue               | 3.66 ms                                                             | 3.24 ms: 1.13x faster                                  |
| sqlglot_parse           | 1.36 ms                                                             | 1.21 ms: 1.12x faster                                  |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 3.99 ms: 1.12x faster                                  |
| nbody                   | 96.7 ms                                                             | 86.6 ms: 1.12x faster                                  |
| sqlglot_transpile       | 1.65 ms                                                             | 1.49 ms: 1.11x faster                                  |
| scimark_fft             | 328 ms                                                              | 298 ms: 1.10x faster                                   |
| xml_etree_parse         | 162 ms                                                              | 148 ms: 1.10x faster                                   |
| genshi_xml              | 51.8 ms                                                             | 47.8 ms: 1.08x faster                                  |
| hexiom                  | 6.48 ms                                                             | 5.98 ms: 1.08x faster                                  |
| json_loads              | 26.2 us                                                             | 24.3 us: 1.08x faster                                  |
| logging_simple          | 6.09 us                                                             | 5.65 us: 1.08x faster                                  |
| deepcopy_memo           | 36.4 us                                                             | 34.1 us: 1.07x faster                                  |
| pickle_pure_python      | 307 us                                                              | 288 us: 1.06x faster                                   |
| xml_etree_iterparse     | 108 ms                                                              | 102 ms: 1.05x faster                                   |
| spectral_norm           | 99.5 ms                                                             | 94.5 ms: 1.05x faster                                  |
| sqlglot_optimize        | 53.4 ms                                                             | 50.8 ms: 1.05x faster                                  |
| logging_format          | 6.64 us                                                             | 6.32 us: 1.05x faster                                  |
| pidigits                | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| richards                | 45.7 ms                                                             | 43.6 ms: 1.05x faster                                  |
| logging_silent          | 98.7 ns                                                             | 94.3 ns: 1.05x faster                                  |
| deepcopy                | 339 us                                                              | 324 us: 1.04x faster                                   |
| nqueens                 | 84.0 ms                                                             | 80.5 ms: 1.04x faster                                  |
| scimark_lu              | 108 ms                                                              | 104 ms: 1.04x faster                                   |
| bench_thread_pool       | 820 us                                                              | 786 us: 1.04x faster                                   |
| html5lib                | 64.0 ms                                                             | 61.4 ms: 1.04x faster                                  |
| sympy_expand            | 477 ms                                                              | 458 ms: 1.04x faster                                   |
| aiohttp                 | 1.05 ms                                                             | 1.01 ms: 1.04x faster                                  |
| sqlglot_normalize       | 108 ms                                                              | 104 ms: 1.04x faster                                   |
| coverage                | 101 ms                                                              | 97.6 ms: 1.04x faster                                  |
| meteor_contest          | 106 ms                                                              | 102 ms: 1.04x faster                                   |
| sympy_integrate         | 21.0 ms                                                             | 20.3 ms: 1.04x faster                                  |
| chaos                   | 68.0 ms                                                             | 65.7 ms: 1.03x faster                                  |
| raytrace                | 292 ms                                                              | 283 ms: 1.03x faster                                   |
| sympy_str               | 291 ms                                                              | 282 ms: 1.03x faster                                   |
| float                   | 76.0 ms                                                             | 73.6 ms: 1.03x faster                                  |
| json                    | 4.86 ms                                                             | 4.71 ms: 1.03x faster                                  |
| pycparser               | 1.14 sec                                                            | 1.11 sec: 1.03x faster                                 |
| tornado_http            | 96.7 ms                                                             | 94.0 ms: 1.03x faster                                  |
| scimark_sor             | 115 ms                                                              | 112 ms: 1.03x faster                                   |
| 2to3                    | 257 ms                                                              | 251 ms: 1.03x faster                                   |
| genshi_text             | 21.8 ms                                                             | 21.3 ms: 1.03x faster                                  |
| fannkuch                | 384 ms                                                              | 375 ms: 1.02x faster                                   |
| gunicorn                | 1.13 ms                                                             | 1.10 ms: 1.02x faster                                  |
| comprehensions          | 22.2 us                                                             | 21.8 us: 1.02x faster                                  |
| deepcopy_reduce         | 2.96 us                                                             | 2.90 us: 1.02x faster                                  |
| sympy_sum               | 167 ms                                                              | 164 ms: 1.02x faster                                   |
| docutils                | 2.59 sec                                                            | 2.54 sec: 1.02x faster                                 |
| scimark_monte_carlo     | 67.8 ms                                                             | 66.7 ms: 1.02x faster                                  |
| regex_compile           | 137 ms                                                              | 135 ms: 1.01x faster                                   |
| pprint_pformat          | 1.45 sec                                                            | 1.43 sec: 1.01x faster                                 |
| create_gc_cycles        | 1.48 ms                                                             | 1.46 ms: 1.01x faster                                  |
| telco                   | 6.59 ms                                                             | 6.52 ms: 1.01x faster                                  |
| go                      | 138 ms                                                              | 137 ms: 1.01x faster                                   |
| mdp                     | 2.64 sec                                                            | 2.62 sec: 1.01x faster                                 |
| pprint_safe_repr        | 701 ms                                                              | 697 ms: 1.01x faster                                   |
| django_template         | 32.9 ms                                                             | 33.0 ms: 1.00x slower                                  |
| pathlib                 | 18.2 ms                                                             | 18.3 ms: 1.01x slower                                  |
| regex_v8                | 22.0 ms                                                             | 22.1 ms: 1.01x slower                                  |
| gc_traversal            | 3.63 ms                                                             | 3.65 ms: 1.01x slower                                  |
| async_tree_io           | 1.28 sec                                                            | 1.30 sec: 1.01x slower                                 |
| regex_effbot            | 3.32 ms                                                             | 3.36 ms: 1.01x slower                                  |
| mako                    | 9.82 ms                                                             | 9.97 ms: 1.01x slower                                  |
| pyflate                 | 414 ms                                                              | 420 ms: 1.02x slower                                   |
| thrift                  | 766 us                                                              | 779 us: 1.02x slower                                   |
| unpickle_list           | 4.96 us                                                             | 5.07 us: 1.02x slower                                  |
| async_tree_memoization  | 621 ms                                                              | 637 ms: 1.02x slower                                   |
| pickle_dict             | 30.9 us                                                             | 31.9 us: 1.03x slower                                  |
| xml_etree_process       | 54.1 ms                                                             | 55.9 ms: 1.03x slower                                  |
| regex_dna               | 196 ms                                                              | 204 ms: 1.04x slower                                   |
| python_startup          | 8.49 ms                                                             | 8.82 ms: 1.04x slower                                  |
| sqlite_synth            | 2.51 us                                                             | 2.63 us: 1.05x slower                                  |
| xml_etree_generate      | 76.5 ms                                                             | 81.2 ms: 1.06x slower                                  |
| unpickle                | 13.2 us                                                             | 14.0 us: 1.06x slower                                  |
| pickle_list             | 4.03 us                                                             | 4.29 us: 1.07x slower                                  |
| python_startup_no_site  | 5.98 ms                                                             | 6.51 ms: 1.09x slower                                  |
| pickle                  | 9.79 us                                                             | 10.7 us: 1.09x slower                                  |
| async_generators        | 361 ms                                                              | 412 ms: 1.14x slower                                   |
| dask                    | 368 ms                                                              | 502 ms: 1.36x slower                                   |
| Geometric mean          | (ref)                                                               | 1.04x faster                                           |

Benchmark hidden because not significant (9): async_tree_none, chameleon, bench_mp_pool, crypto_pyaes, djangocms, dulwich_log, sqlalchemy_imperative, async_tree_cpu_io_mixed, sqlalchemy_declarative
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint
