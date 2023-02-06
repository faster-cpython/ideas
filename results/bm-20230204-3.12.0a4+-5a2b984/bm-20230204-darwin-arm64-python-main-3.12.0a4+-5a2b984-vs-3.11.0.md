
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 5a2b984
- commit date: 2023-02-04
- overall geometric mean: 1.01x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 182 ms: 1.00x slower                                   |
| chameleon      | 4.61 ms                                                             | 4.71 ms: 1.02x slower                                  |
| docutils       | 1.46 sec                                                            | 1.45 sec: 1.01x faster                                 |
| Geometric mean | (ref)                                                               | 1.00x slower                                           |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 64.0 ms: 1.02x faster                                  |
| pidigits       | 282 ms                                                              | 283 ms: 1.00x slower                                   |
| float          | 51.7 ms                                                             | 51.9 ms: 1.00x slower                                  |
| Geometric mean | (ref)                                                               | 1.00x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 72.1 ms: 1.06x faster                                  |
| regex_v8       | 16.5 ms                                                             | 16.2 ms: 1.02x faster                                  |
| regex_dna      | 151 ms                                                              | 150 ms: 1.01x faster                                   |
| regex_effbot   | 2.63 ms                                                             | 2.63 ms: 1.00x faster                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.10 ms: 1.26x faster                                  |
| xml_etree_parse      | 99.6 ms                                                             | 93.9 ms: 1.06x faster                                  |
| pickle_pure_python   | 200 us                                                              | 192 us: 1.04x faster                                   |
| xml_etree_process    | 35.1 ms                                                             | 34.4 ms: 1.02x faster                                  |
| unpickle_pure_python | 159 us                                                              | 157 us: 1.02x faster                                   |
| pickle_list          | 2.86 us                                                             | 2.81 us: 1.02x faster                                  |
| xml_etree_generate   | 48.4 ms                                                             | 47.8 ms: 1.01x faster                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| json_loads           | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| unpickle             | 9.68 us                                                             | 9.91 us: 1.02x slower                                  |
| unpickle_list        | 2.64 us                                                             | 2.71 us: 1.03x slower                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 67.8 ms: 1.03x slower                                  |
| pickle               | 7.21 us                                                             | 7.57 us: 1.05x slower                                  |
| Geometric mean       | (ref)                                                               | 1.02x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                             | 7.35 ms: 1.02x slower                                  |
| python_startup         | 9.19 ms                                                             | 9.36 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                               | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 8.40 ms                                                             | 7.16 ms: 1.17x faster                                  |
| genshi_text     | 15.3 ms                                                             | 14.3 ms: 1.08x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 28.4 ms: 1.07x faster                                  |
| django_template | 21.1 ms                                                             | 20.9 ms: 1.01x faster                                  |
| Geometric mean  | (ref)                                                               | 1.08x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps              | 7.67 ms                                                             | 6.10 ms: 1.26x faster                                  |
| mako                    | 8.40 ms                                                             | 7.16 ms: 1.17x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.81 ms: 1.14x faster                                  |
| richards                | 32.7 ms                                                             | 29.7 ms: 1.10x faster                                  |
| deltablue               | 2.82 ms                                                             | 2.57 ms: 1.10x faster                                  |
| hexiom                  | 4.73 ms                                                             | 4.32 ms: 1.10x faster                                  |
| chaos                   | 49.3 ms                                                             | 45.5 ms: 1.08x faster                                  |
| genshi_text             | 15.3 ms                                                             | 14.3 ms: 1.08x faster                                  |
| genshi_xml              | 30.5 ms                                                             | 28.4 ms: 1.07x faster                                  |
| xml_etree_parse         | 99.6 ms                                                             | 93.9 ms: 1.06x faster                                  |
| regex_compile           | 76.3 ms                                                             | 72.1 ms: 1.06x faster                                  |
| sympy_sum               | 85.5 ms                                                             | 81.9 ms: 1.04x faster                                  |
| scimark_fft             | 201 ms                                                              | 192 ms: 1.04x faster                                   |
| pickle_pure_python      | 200 us                                                              | 192 us: 1.04x faster                                   |
| pycparser               | 694 ms                                                              | 669 ms: 1.04x faster                                   |
| sympy_str               | 151 ms                                                              | 145 ms: 1.04x faster                                   |
| logging_silent          | 67.4 ns                                                             | 65.7 ns: 1.03x faster                                  |
| fannkuch                | 262 ms                                                              | 256 ms: 1.03x faster                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.2 ms: 1.03x faster                                  |
| mypy                    | 421 ms                                                              | 411 ms: 1.02x faster                                   |
| bench_thread_pool       | 457 us                                                              | 447 us: 1.02x faster                                   |
| coverage                | 58.4 ms                                                             | 57.1 ms: 1.02x faster                                  |
| scimark_lu              | 72.2 ms                                                             | 70.8 ms: 1.02x faster                                  |
| xml_etree_process       | 35.1 ms                                                             | 34.4 ms: 1.02x faster                                  |
| nbody                   | 65.2 ms                                                             | 64.0 ms: 1.02x faster                                  |
| unpickle_pure_python    | 159 us                                                              | 157 us: 1.02x faster                                   |
| regex_v8                | 16.5 ms                                                             | 16.2 ms: 1.02x faster                                  |
| pickle_list             | 2.86 us                                                             | 2.81 us: 1.02x faster                                  |
| dulwich_log             | 29.1 ms                                                             | 28.6 ms: 1.01x faster                                  |
| xml_etree_generate      | 48.4 ms                                                             | 47.8 ms: 1.01x faster                                  |
| regex_dna               | 151 ms                                                              | 150 ms: 1.01x faster                                   |
| mdp                     | 1.54 sec                                                            | 1.52 sec: 1.01x faster                                 |
| deepcopy                | 222 us                                                              | 220 us: 1.01x faster                                   |
| deepcopy_memo           | 26.2 us                                                             | 25.9 us: 1.01x faster                                  |
| unpack_sequence         | 33.1 ns                                                             | 32.8 ns: 1.01x faster                                  |
| docutils                | 1.46 sec                                                            | 1.45 sec: 1.01x faster                                 |
| django_template         | 21.1 ms                                                             | 20.9 ms: 1.01x faster                                  |
| go                      | 109 ms                                                              | 109 ms: 1.01x faster                                   |
| regex_effbot            | 2.63 ms                                                             | 2.63 ms: 1.00x faster                                  |
| pidigits                | 282 ms                                                              | 283 ms: 1.00x slower                                   |
| pprint_pformat          | 953 ms                                                              | 955 ms: 1.00x slower                                   |
| sqlglot_optimize        | 31.3 ms                                                             | 31.4 ms: 1.00x slower                                  |
| deepcopy_reduce         | 1.90 us                                                             | 1.90 us: 1.00x slower                                  |
| 2to3                    | 181 ms                                                              | 182 ms: 1.00x slower                                   |
| float                   | 51.7 ms                                                             | 51.9 ms: 1.00x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| pprint_safe_repr        | 467 ms                                                              | 470 ms: 1.01x slower                                   |
| json_loads              | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| telco                   | 3.39 ms                                                             | 3.43 ms: 1.01x slower                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 536 ms: 1.01x slower                                   |
| python_startup_no_site  | 7.24 ms                                                             | 7.35 ms: 1.02x slower                                  |
| async_tree_memoization  | 317 ms                                                              | 322 ms: 1.02x slower                                   |
| python_startup          | 9.19 ms                                                             | 9.36 ms: 1.02x slower                                  |
| crypto_pyaes            | 51.7 ms                                                             | 52.7 ms: 1.02x slower                                  |
| chameleon               | 4.61 ms                                                             | 4.71 ms: 1.02x slower                                  |
| async_generators        | 195 ms                                                              | 200 ms: 1.02x slower                                   |
| nqueens                 | 59.5 ms                                                             | 60.8 ms: 1.02x slower                                  |
| unpickle                | 9.68 us                                                             | 9.91 us: 1.02x slower                                  |
| scimark_sor             | 83.3 ms                                                             | 85.3 ms: 1.02x slower                                  |
| meteor_contest          | 73.9 ms                                                             | 75.9 ms: 1.03x slower                                  |
| thrift                  | 429 us                                                              | 442 us: 1.03x slower                                   |
| unpickle_list           | 2.64 us                                                             | 2.71 us: 1.03x slower                                  |
| xml_etree_iterparse     | 65.6 ms                                                             | 67.8 ms: 1.03x slower                                  |
| bench_mp_pool           | 41.4 ms                                                             | 42.9 ms: 1.04x slower                                  |
| logging_simple          | 3.47 us                                                             | 3.64 us: 1.05x slower                                  |
| pickle                  | 7.21 us                                                             | 7.57 us: 1.05x slower                                  |
| async_tree_io           | 696 ms                                                              | 732 ms: 1.05x slower                                   |
| logging_format          | 3.73 us                                                             | 3.93 us: 1.05x slower                                  |
| coroutines              | 17.8 ms                                                             | 18.8 ms: 1.06x slower                                  |
| raytrace                | 207 ms                                                              | 219 ms: 1.06x slower                                   |
| scimark_monte_carlo     | 46.9 ms                                                             | 49.8 ms: 1.06x slower                                  |
| pyflate                 | 313 ms                                                              | 333 ms: 1.07x slower                                   |
| sqlglot_transpile       | 1.11 ms                                                             | 1.19 ms: 1.07x slower                                  |
| sqlite_synth            | 1.29 us                                                             | 1.40 us: 1.08x slower                                  |
| sqlglot_parse           | 948 us                                                              | 1.02 ms: 1.08x slower                                  |
| generators              | 28.4 ms                                                             | 34.1 ms: 1.20x slower                                  |
| Geometric mean          | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (8): tornado_http, async_tree_none, spectral_norm, sqlglot_normalize, sympy_expand, json, html5lib, pathlib
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of public/results/bm-20230204-3.12.0a4+-5a2b984/bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
