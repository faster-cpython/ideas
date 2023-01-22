
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: c1c5882
- commit date: 2023-01-21
- overall geometric mean: 1.00x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 183 ms: 1.01x slower                                   |
| docutils       | 1.46 sec                                                            | 1.44 sec: 1.01x faster                                 |
| Geometric mean | (ref)                                                               | 1.00x faster                                           |

Benchmark hidden because not significant (3): chameleon, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 51.7 ms                                                             | 51.4 ms: 1.00x faster                                  |
| nbody          | 65.2 ms                                                             | 63.5 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 73.4 ms: 1.04x faster                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                   |
| regex_effbot   | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                  |
| regex_v8       | 16.5 ms                                                             | 16.2 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.05 ms: 1.27x faster                                  |
| json_loads           | 16.1 us                                                             | 16.2 us: 1.00x slower                                  |
| pickle               | 7.21 us                                                             | 7.52 us: 1.04x slower                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| pickle_list          | 2.86 us                                                             | 2.82 us: 1.02x faster                                  |
| pickle_pure_python   | 200 us                                                              | 192 us: 1.04x faster                                   |
| unpickle_list        | 2.64 us                                                             | 2.71 us: 1.03x slower                                  |
| unpickle_pure_python | 159 us                                                              | 144 us: 1.11x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 101 ms: 1.01x slower                                   |
| xml_etree_iterparse  | 65.6 ms                                                             | 69.8 ms: 1.06x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 49.2 ms: 1.02x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 35.4 ms: 1.01x slower                                  |
| Geometric mean       | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.37 ms: 1.02x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.36 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                               | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.8 ms: 1.03x slower                                  |
| genshi_text     | 15.3 ms                                                             | 15.5 ms: 1.01x slower                                  |
| genshi_xml      | 30.5 ms                                                             | 28.7 ms: 1.06x faster                                  |
| mako            | 8.40 ms                                                             | 8.14 ms: 1.03x faster                                  |
| Geometric mean  | (ref)                                                               | 1.01x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 183 ms: 1.01x slower                                   |
| async_generators        | 195 ms                                                              | 197 ms: 1.01x slower                                   |
| async_tree_none         | 281 ms                                                              | 286 ms: 1.02x slower                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 538 ms: 1.02x slower                                   |
| async_tree_io           | 696 ms                                                              | 732 ms: 1.05x slower                                   |
| async_tree_memoization  | 317 ms                                                              | 328 ms: 1.03x slower                                   |
| chaos                   | 49.3 ms                                                             | 47.9 ms: 1.03x faster                                  |
| bench_mp_pool           | 41.4 ms                                                             | 42.6 ms: 1.03x slower                                  |
| bench_thread_pool       | 457 us                                                              | 447 us: 1.02x faster                                   |
| coroutines              | 17.8 ms                                                             | 18.9 ms: 1.07x slower                                  |
| coverage                | 58.4 ms                                                             | 55.5 ms: 1.05x faster                                  |
| crypto_pyaes            | 51.7 ms                                                             | 52.2 ms: 1.01x slower                                  |
| deepcopy_reduce         | 1.90 us                                                             | 1.92 us: 1.01x slower                                  |
| deepcopy_memo           | 26.2 us                                                             | 26.1 us: 1.00x faster                                  |
| deltablue               | 2.82 ms                                                             | 2.61 ms: 1.08x faster                                  |
| django_template         | 21.1 ms                                                             | 21.8 ms: 1.03x slower                                  |
| docutils                | 1.46 sec                                                            | 1.44 sec: 1.01x faster                                 |
| dulwich_log             | 29.1 ms                                                             | 28.6 ms: 1.02x faster                                  |
| fannkuch                | 262 ms                                                              | 254 ms: 1.03x faster                                   |
| float                   | 51.7 ms                                                             | 51.4 ms: 1.00x faster                                  |
| generators              | 28.4 ms                                                             | 34.1 ms: 1.20x slower                                  |
| genshi_text             | 15.3 ms                                                             | 15.5 ms: 1.01x slower                                  |
| genshi_xml              | 30.5 ms                                                             | 28.7 ms: 1.06x faster                                  |
| go                      | 109 ms                                                              | 108 ms: 1.01x faster                                   |
| json_dumps              | 7.67 ms                                                             | 6.05 ms: 1.27x faster                                  |
| json_loads              | 16.1 us                                                             | 16.2 us: 1.00x slower                                  |
| logging_format          | 3.73 us                                                             | 3.84 us: 1.03x slower                                  |
| logging_silent          | 67.4 ns                                                             | 66.4 ns: 1.02x faster                                  |
| logging_simple          | 3.47 us                                                             | 3.55 us: 1.02x slower                                  |
| mako                    | 8.40 ms                                                             | 8.14 ms: 1.03x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.51 sec: 1.02x faster                                 |
| meteor_contest          | 73.9 ms                                                             | 75.5 ms: 1.02x slower                                  |
| mypy                    | 421 ms                                                              | 413 ms: 1.02x faster                                   |
| nbody                   | 65.2 ms                                                             | 63.5 ms: 1.03x faster                                  |
| nqueens                 | 59.5 ms                                                             | 60.0 ms: 1.01x slower                                  |
| pathlib                 | 20.6 ms                                                             | 20.8 ms: 1.01x slower                                  |
| pickle                  | 7.21 us                                                             | 7.52 us: 1.04x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| pickle_list             | 2.86 us                                                             | 2.82 us: 1.02x faster                                  |
| pickle_pure_python      | 200 us                                                              | 192 us: 1.04x faster                                   |
| pprint_safe_repr        | 467 ms                                                              | 460 ms: 1.02x faster                                   |
| pprint_pformat          | 953 ms                                                              | 936 ms: 1.02x faster                                   |
| pycparser               | 694 ms                                                              | 679 ms: 1.02x faster                                   |
| pyflate                 | 313 ms                                                              | 322 ms: 1.03x slower                                   |
| python_startup          | 9.19 ms                                                             | 9.37 ms: 1.02x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.36 ms: 1.02x slower                                  |
| raytrace                | 207 ms                                                              | 217 ms: 1.05x slower                                   |
| regex_compile           | 76.3 ms                                                             | 73.4 ms: 1.04x faster                                  |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                   |
| regex_effbot            | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                  |
| regex_v8                | 16.5 ms                                                             | 16.2 ms: 1.02x faster                                  |
| richards                | 32.7 ms                                                             | 30.5 ms: 1.07x faster                                  |
| scimark_fft             | 201 ms                                                              | 192 ms: 1.05x faster                                   |
| scimark_monte_carlo     | 46.9 ms                                                             | 48.3 ms: 1.03x slower                                  |
| scimark_sor             | 83.3 ms                                                             | 81.8 ms: 1.02x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.79 ms: 1.15x faster                                  |
| spectral_norm           | 72.7 ms                                                             | 74.0 ms: 1.02x slower                                  |
| sqlglot_parse           | 948 us                                                              | 1.04 ms: 1.09x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.20 ms: 1.08x slower                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 31.4 ms: 1.00x slower                                  |
| sqlglot_normalize       | 171 ms                                                              | 172 ms: 1.01x slower                                   |
| sqlite_synth            | 1.29 us                                                             | 1.38 us: 1.07x slower                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.4 ms: 1.01x faster                                  |
| sympy_str               | 151 ms                                                              | 152 ms: 1.00x slower                                   |
| telco                   | 3.39 ms                                                             | 3.47 ms: 1.02x slower                                  |
| thrift                  | 429 us                                                              | 441 us: 1.03x slower                                   |
| unpack_sequence         | 33.1 ns                                                             | 32.9 ns: 1.01x faster                                  |
| unpickle_list           | 2.64 us                                                             | 2.71 us: 1.03x slower                                  |
| unpickle_pure_python    | 159 us                                                              | 144 us: 1.11x faster                                   |
| xml_etree_parse         | 99.6 ms                                                             | 101 ms: 1.01x slower                                   |
| xml_etree_iterparse     | 65.6 ms                                                             | 69.8 ms: 1.06x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 49.2 ms: 1.02x slower                                  |
| xml_etree_process       | 35.1 ms                                                             | 35.4 ms: 1.01x slower                                  |
| Geometric mean          | (ref)                                                               | 1.00x faster                                           |

Benchmark hidden because not significant (11): chameleon, deepcopy, hexiom, html5lib, json, pidigits, scimark_lu, sympy_expand, sympy_sum, tornado_http, unpickle
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of public/results/bm-20230121-3.12.0a4+-c1c5882/bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
