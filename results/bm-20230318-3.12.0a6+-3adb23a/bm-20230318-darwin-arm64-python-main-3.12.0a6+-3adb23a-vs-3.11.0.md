
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 3adb23a
- commit date: 2023-03-18
- overall geometric mean: 1.02x slower \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 165 ms: 1.10x faster                                   |
| chameleon      | 4.61 ms                                                             | 4.48 ms: 1.03x faster                                  |
| docutils       | 1.46 sec                                                            | 1.51 sec: 1.03x slower                                 |
| html5lib       | 34.7 ms                                                             | 35.7 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 60.7 ms: 1.07x faster                                  |
| float          | 51.7 ms                                                             | 52.7 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 16.5 ms                                                             | 16.1 ms: 1.02x faster                                  |
| regex_compile  | 76.3 ms                                                             | 75.9 ms: 1.01x faster                                  |
| regex_dna      | 151 ms                                                              | 152 ms: 1.00x slower                                   |
| regex_effbot   | 2.63 ms                                                             | 2.68 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                               | 1.00x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.28 ms: 1.22x faster                                  |
| unpickle_pure_python | 159 us                                                              | 145 us: 1.10x faster                                   |
| pickle_pure_python   | 200 us                                                              | 192 us: 1.04x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 97.4 ms: 1.02x faster                                  |
| pickle_list          | 2.86 us                                                             | 2.83 us: 1.01x faster                                  |
| unpickle_list        | 2.64 us                                                             | 2.64 us: 1.00x slower                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| unpickle             | 9.68 us                                                             | 9.77 us: 1.01x slower                                  |
| json_loads           | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| pickle               | 7.21 us                                                             | 7.41 us: 1.03x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 36.7 ms: 1.05x slower                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 70.3 ms: 1.07x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 51.8 ms: 1.07x slower                                  |
| Geometric mean       | (ref)                                                               | 1.01x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 11.0 ms: 1.19x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 8.99 ms: 1.24x slower                                  |
| Geometric mean         | (ref)                                                               | 1.22x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 8.40 ms                                                             | 7.44 ms: 1.13x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 29.3 ms: 1.04x faster                                  |
| genshi_text     | 15.3 ms                                                             | 14.8 ms: 1.03x faster                                  |
| django_template | 21.1 ms                                                             | 21.9 ms: 1.04x slower                                  |
| Geometric mean  | (ref)                                                               | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps              | 7.67 ms                                                             | 6.28 ms: 1.22x faster                                  |
| mako                    | 8.40 ms                                                             | 7.44 ms: 1.13x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.86 ms: 1.12x faster                                  |
| deltablue               | 2.82 ms                                                             | 2.56 ms: 1.10x faster                                  |
| 2to3                    | 181 ms                                                              | 165 ms: 1.10x faster                                   |
| unpickle_pure_python    | 159 us                                                              | 145 us: 1.10x faster                                   |
| nbody                   | 65.2 ms                                                             | 60.7 ms: 1.07x faster                                  |
| hexiom                  | 4.73 ms                                                             | 4.40 ms: 1.07x faster                                  |
| scimark_fft             | 201 ms                                                              | 187 ms: 1.07x faster                                   |
| richards                | 32.7 ms                                                             | 30.7 ms: 1.07x faster                                  |
| coverage                | 58.4 ms                                                             | 56.0 ms: 1.04x faster                                  |
| pickle_pure_python      | 200 us                                                              | 192 us: 1.04x faster                                   |
| chaos                   | 49.3 ms                                                             | 47.4 ms: 1.04x faster                                  |
| genshi_xml              | 30.5 ms                                                             | 29.3 ms: 1.04x faster                                  |
| genshi_text             | 15.3 ms                                                             | 14.8 ms: 1.03x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.49 sec: 1.03x faster                                 |
| chameleon               | 4.61 ms                                                             | 4.48 ms: 1.03x faster                                  |
| pycparser               | 694 ms                                                              | 676 ms: 1.03x faster                                   |
| regex_v8                | 16.5 ms                                                             | 16.1 ms: 1.02x faster                                  |
| xml_etree_parse         | 99.6 ms                                                             | 97.4 ms: 1.02x faster                                  |
| generators              | 28.4 ms                                                             | 27.8 ms: 1.02x faster                                  |
| scimark_lu              | 72.2 ms                                                             | 71.2 ms: 1.01x faster                                  |
| deepcopy_memo           | 26.2 us                                                             | 25.8 us: 1.01x faster                                  |
| pickle_list             | 2.86 us                                                             | 2.83 us: 1.01x faster                                  |
| json                    | 2.83 ms                                                             | 2.80 ms: 1.01x faster                                  |
| spectral_norm           | 72.7 ms                                                             | 72.1 ms: 1.01x faster                                  |
| logging_silent          | 67.4 ns                                                             | 66.9 ns: 1.01x faster                                  |
| regex_compile           | 76.3 ms                                                             | 75.9 ms: 1.01x faster                                  |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.19 ms: 1.00x faster                                  |
| regex_dna               | 151 ms                                                              | 152 ms: 1.00x slower                                   |
| unpickle_list           | 2.64 us                                                             | 2.64 us: 1.00x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| unpack_sequence         | 33.1 ns                                                             | 33.3 ns: 1.01x slower                                  |
| unpickle                | 9.68 us                                                             | 9.77 us: 1.01x slower                                  |
| json_loads              | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| pprint_pformat          | 953 ms                                                              | 967 ms: 1.01x slower                                   |
| sqlglot_normalize       | 171 ms                                                              | 174 ms: 1.02x slower                                   |
| pprint_safe_repr        | 467 ms                                                              | 475 ms: 1.02x slower                                   |
| go                      | 109 ms                                                              | 111 ms: 1.02x slower                                   |
| regex_effbot            | 2.63 ms                                                             | 2.68 ms: 1.02x slower                                  |
| dulwich_log             | 29.1 ms                                                             | 29.6 ms: 1.02x slower                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.7 ms: 1.02x slower                                  |
| float                   | 51.7 ms                                                             | 52.7 ms: 1.02x slower                                  |
| coroutines              | 17.8 ms                                                             | 18.1 ms: 1.02x slower                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 32.0 ms: 1.02x slower                                  |
| scimark_sor             | 83.3 ms                                                             | 85.2 ms: 1.02x slower                                  |
| sympy_str               | 151 ms                                                              | 154 ms: 1.02x slower                                   |
| async_tree_none         | 281 ms                                                              | 288 ms: 1.02x slower                                   |
| sympy_expand            | 242 ms                                                              | 248 ms: 1.03x slower                                   |
| pickle                  | 7.21 us                                                             | 7.41 us: 1.03x slower                                  |
| telco                   | 3.39 ms                                                             | 3.49 ms: 1.03x slower                                  |
| docutils                | 1.46 sec                                                            | 1.51 sec: 1.03x slower                                 |
| html5lib                | 34.7 ms                                                             | 35.7 ms: 1.03x slower                                  |
| bench_thread_pool       | 457 us                                                              | 472 us: 1.03x slower                                   |
| sympy_sum               | 85.5 ms                                                             | 88.3 ms: 1.03x slower                                  |
| sqlalchemy_declarative  | 62.4 ms                                                             | 64.5 ms: 1.03x slower                                  |
| deepcopy_reduce         | 1.90 us                                                             | 1.96 us: 1.03x slower                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 548 ms: 1.04x slower                                   |
| django_template         | 21.1 ms                                                             | 21.9 ms: 1.04x slower                                  |
| nqueens                 | 59.5 ms                                                             | 62.1 ms: 1.04x slower                                  |
| sqlite_synth            | 1.29 us                                                             | 1.35 us: 1.04x slower                                  |
| xml_etree_process       | 35.1 ms                                                             | 36.7 ms: 1.05x slower                                  |
| async_tree_memoization  | 317 ms                                                              | 333 ms: 1.05x slower                                   |
| crypto_pyaes            | 51.7 ms                                                             | 54.6 ms: 1.06x slower                                  |
| logging_simple          | 3.47 us                                                             | 3.66 us: 1.06x slower                                  |
| logging_format          | 3.73 us                                                             | 3.95 us: 1.06x slower                                  |
| pyflate                 | 313 ms                                                              | 332 ms: 1.06x slower                                   |
| thrift                  | 429 us                                                              | 456 us: 1.06x slower                                   |
| async_tree_io           | 696 ms                                                              | 743 ms: 1.07x slower                                   |
| raytrace                | 207 ms                                                              | 222 ms: 1.07x slower                                   |
| xml_etree_iterparse     | 65.6 ms                                                             | 70.3 ms: 1.07x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 51.8 ms: 1.07x slower                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 50.7 ms: 1.08x slower                                  |
| bench_mp_pool           | 41.4 ms                                                             | 44.8 ms: 1.08x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.23 ms: 1.11x slower                                  |
| sqlglot_parse           | 948 us                                                              | 1.06 ms: 1.12x slower                                  |
| python_startup          | 9.19 ms                                                             | 11.0 ms: 1.19x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 8.99 ms: 1.24x slower                                  |
| pathlib                 | 20.6 ms                                                             | 27.9 ms: 1.35x slower                                  |
| async_generators        | 195 ms                                                              | 266 ms: 1.36x slower                                   |
| Geometric mean          | (ref)                                                               | 1.02x slower                                           |

Benchmark hidden because not significant (5): tornado_http, meteor_contest, pidigits, fannkuch, deepcopy
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230318-3.12.0a6+-3adb23a/bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
