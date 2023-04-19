
# Results vs. 3.11.0

- fork: faster-cpython
- ref: nogil_latest
- machine: linux-x86_64
- commit hash: 1d39009
- commit date: 2023-04-16
- overall geometric mean: 1.05x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 290 ms: 1.13x slower                                                    |
| chameleon      | 6.52 ms                                                             | 7.81 ms: 1.20x slower                                                   |
| docutils       | 2.59 sec                                                            | 3.15 sec: 1.21x slower                                                  |
| html5lib       | 64.0 ms                                                             | 69.2 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                               | 1.15x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 76.0 ms                                                             | 65.9 ms: 1.15x faster                                                   |
| pidigits       | 197 ms                                                              | 186 ms: 1.06x faster                                                    |
| nbody          | 96.7 ms                                                             | 107 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                               | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                             | 21.1 ms: 1.04x faster                                                   |
| regex_effbot   | 3.32 ms                                                             | 3.46 ms: 1.04x slower                                                   |
| regex_dna      | 196 ms                                                              | 205 ms: 1.04x slower                                                    |
| regex_compile  | 137 ms                                                              | 152 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                               | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 10.4 ms: 1.21x faster                                                   |
| xml_etree_parse      | 162 ms                                                              | 137 ms: 1.18x faster                                                    |
| pickle_dict          | 30.9 us                                                             | 30.0 us: 1.03x faster                                                   |
| unpickle_pure_python | 228 us                                                              | 229 us: 1.00x slower                                                    |
| pickle_pure_python   | 307 us                                                              | 321 us: 1.04x slower                                                    |
| unpickle_list        | 4.96 us                                                             | 5.20 us: 1.05x slower                                                   |
| pickle               | 9.79 us                                                             | 10.3 us: 1.05x slower                                                   |
| xml_etree_iterparse  | 108 ms                                                              | 114 ms: 1.05x slower                                                    |
| json_loads           | 26.2 us                                                             | 28.0 us: 1.07x slower                                                   |
| pickle_list          | 4.03 us                                                             | 4.33 us: 1.07x slower                                                   |
| xml_etree_generate   | 76.5 ms                                                             | 83.7 ms: 1.09x slower                                                   |
| xml_etree_process    | 54.1 ms                                                             | 61.3 ms: 1.13x slower                                                   |
| unpickle             | 13.2 us                                                             | 15.5 us: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                               | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 9.18 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.98 ms                                                             | 6.59 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                               | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 21.8 ms                                                             | 24.4 ms: 1.11x slower                                                   |
| django_template | 32.9 ms                                                             | 37.4 ms: 1.14x slower                                                   |
| mako            | 9.82 ms                                                             | 13.2 ms: 1.35x slower                                                   |
| Geometric mean  | (ref)                                                               | 1.14x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io           | 1.28 sec                                                            | 616 ms: 2.08x faster                                                    |
| asyncio_tcp             | 888 ms                                                              | 525 ms: 1.69x faster                                                    |
| async_tree_none         | 525 ms                                                              | 311 ms: 1.69x faster                                                    |
| async_tree_memoization  | 621 ms                                                              | 381 ms: 1.63x faster                                                    |
| async_tree_cpu_io_mixed | 736 ms                                                              | 534 ms: 1.38x faster                                                    |
| json_dumps              | 12.5 ms                                                             | 10.4 ms: 1.21x faster                                                   |
| xml_etree_parse         | 162 ms                                                              | 137 ms: 1.18x faster                                                    |
| float                   | 76.0 ms                                                             | 65.9 ms: 1.15x faster                                                   |
| pidigits                | 197 ms                                                              | 186 ms: 1.06x faster                                                    |
| regex_v8                | 22.0 ms                                                             | 21.1 ms: 1.04x faster                                                   |
| pickle_dict             | 30.9 us                                                             | 30.0 us: 1.03x faster                                                   |
| bench_mp_pool           | 24.0 ms                                                             | 23.8 ms: 1.01x faster                                                   |
| unpickle_pure_python    | 228 us                                                              | 229 us: 1.00x slower                                                    |
| gc_traversal            | 3.63 ms                                                             | 3.67 ms: 1.01x slower                                                   |
| coroutines              | 26.3 ms                                                             | 26.8 ms: 1.02x slower                                                   |
| nqueens                 | 84.0 ms                                                             | 85.8 ms: 1.02x slower                                                   |
| regex_effbot            | 3.32 ms                                                             | 3.46 ms: 1.04x slower                                                   |
| json                    | 4.86 ms                                                             | 5.06 ms: 1.04x slower                                                   |
| sqlite_synth            | 2.51 us                                                             | 2.62 us: 1.04x slower                                                   |
| regex_dna               | 196 ms                                                              | 205 ms: 1.04x slower                                                    |
| async_generators        | 361 ms                                                              | 377 ms: 1.04x slower                                                    |
| pickle_pure_python      | 307 us                                                              | 321 us: 1.04x slower                                                    |
| unpickle_list           | 4.96 us                                                             | 5.20 us: 1.05x slower                                                   |
| pickle                  | 9.79 us                                                             | 10.3 us: 1.05x slower                                                   |
| logging_silent          | 98.7 ns                                                             | 104 ns: 1.05x slower                                                    |
| telco                   | 6.59 ms                                                             | 6.92 ms: 1.05x slower                                                   |
| xml_etree_iterparse     | 108 ms                                                              | 114 ms: 1.05x slower                                                    |
| mdp                     | 2.64 sec                                                            | 2.79 sec: 1.06x slower                                                  |
| sqlglot_normalize       | 108 ms                                                              | 115 ms: 1.06x slower                                                    |
| go                      | 138 ms                                                              | 146 ms: 1.06x slower                                                    |
| richards                | 45.7 ms                                                             | 48.4 ms: 1.06x slower                                                   |
| hexiom                  | 6.48 ms                                                             | 6.89 ms: 1.06x slower                                                   |
| scimark_sor             | 115 ms                                                              | 123 ms: 1.07x slower                                                    |
| deltablue               | 3.66 ms                                                             | 3.91 ms: 1.07x slower                                                   |
| dulwich_log             | 63.6 ms                                                             | 68.1 ms: 1.07x slower                                                   |
| sqlglot_optimize        | 53.4 ms                                                             | 57.1 ms: 1.07x slower                                                   |
| json_loads              | 26.2 us                                                             | 28.0 us: 1.07x slower                                                   |
| generators              | 73.4 ms                                                             | 78.8 ms: 1.07x slower                                                   |
| pickle_list             | 4.03 us                                                             | 4.33 us: 1.07x slower                                                   |
| create_gc_cycles        | 1.48 ms                                                             | 1.59 ms: 1.08x slower                                                   |
| coverage                | 101 ms                                                              | 109 ms: 1.08x slower                                                    |
| python_startup          | 8.49 ms                                                             | 9.18 ms: 1.08x slower                                                   |
| html5lib                | 64.0 ms                                                             | 69.2 ms: 1.08x slower                                                   |
| mypy2                   | 422 ms                                                              | 457 ms: 1.08x slower                                                    |
| sympy_integrate         | 21.0 ms                                                             | 22.8 ms: 1.08x slower                                                   |
| pprint_pformat          | 1.45 sec                                                            | 1.58 sec: 1.09x slower                                                  |
| pprint_safe_repr        | 701 ms                                                              | 765 ms: 1.09x slower                                                    |
| xml_etree_generate      | 76.5 ms                                                             | 83.7 ms: 1.09x slower                                                   |
| chaos                   | 68.0 ms                                                             | 74.6 ms: 1.10x slower                                                   |
| deepcopy_memo           | 36.4 us                                                             | 40.1 us: 1.10x slower                                                   |
| python_startup_no_site  | 5.98 ms                                                             | 6.59 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.94 ms: 1.11x slower                                                   |
| nbody                   | 96.7 ms                                                             | 107 ms: 1.11x slower                                                    |
| deepcopy                | 339 us                                                              | 375 us: 1.11x slower                                                    |
| crypto_pyaes            | 73.8 ms                                                             | 81.8 ms: 1.11x slower                                                   |
| thrift                  | 766 us                                                              | 851 us: 1.11x slower                                                    |
| regex_compile           | 137 ms                                                              | 152 ms: 1.11x slower                                                    |
| genshi_text             | 21.8 ms                                                             | 24.4 ms: 1.11x slower                                                   |
| scimark_monte_carlo     | 67.8 ms                                                             | 76.4 ms: 1.13x slower                                                   |
| sympy_expand            | 477 ms                                                              | 537 ms: 1.13x slower                                                    |
| spectral_norm           | 99.5 ms                                                             | 112 ms: 1.13x slower                                                    |
| sympy_str               | 291 ms                                                              | 329 ms: 1.13x slower                                                    |
| 2to3                    | 257 ms                                                              | 290 ms: 1.13x slower                                                    |
| xml_etree_process       | 54.1 ms                                                             | 61.3 ms: 1.13x slower                                                   |
| pyflate                 | 414 ms                                                              | 470 ms: 1.14x slower                                                    |
| django_template         | 32.9 ms                                                             | 37.4 ms: 1.14x slower                                                   |
| fannkuch                | 384 ms                                                              | 436 ms: 1.14x slower                                                    |
| sympy_sum               | 167 ms                                                              | 192 ms: 1.15x slower                                                    |
| logging_simple          | 6.09 us                                                             | 7.00 us: 1.15x slower                                                   |
| logging_format          | 6.64 us                                                             | 7.66 us: 1.15x slower                                                   |
| deepcopy_reduce         | 2.96 us                                                             | 3.42 us: 1.16x slower                                                   |
| scimark_fft             | 328 ms                                                              | 383 ms: 1.17x slower                                                    |
| unpickle                | 13.2 us                                                             | 15.5 us: 1.17x slower                                                   |
| meteor_contest          | 106 ms                                                              | 124 ms: 1.17x slower                                                    |
| djangocms               | 32.3 us                                                             | 37.9 us: 1.17x slower                                                   |
| unpack_sequence         | 49.5 ns                                                             | 58.1 ns: 1.17x slower                                                   |
| scimark_lu              | 108 ms                                                              | 128 ms: 1.18x slower                                                    |
| raytrace                | 292 ms                                                              | 346 ms: 1.18x slower                                                    |
| comprehensions          | 22.2 us                                                             | 26.3 us: 1.18x slower                                                   |
| chameleon               | 6.52 ms                                                             | 7.81 ms: 1.20x slower                                                   |
| docutils                | 2.59 sec                                                            | 3.15 sec: 1.21x slower                                                  |
| sqlglot_transpile       | 1.65 ms                                                             | 2.10 ms: 1.27x slower                                                   |
| sqlglot_parse           | 1.36 ms                                                             | 1.79 ms: 1.31x slower                                                   |
| mako                    | 9.82 ms                                                             | 13.2 ms: 1.35x slower                                                   |
| bench_thread_pool       | 820 us                                                              | 1.64 ms: 2.01x slower                                                   |
| Geometric mean          | (ref)                                                               | 1.05x slower                                                            |

Benchmark hidden because not significant (3): pathlib, genshi_xml, pycparser
Ignored benchmarks (8) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, dask, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
