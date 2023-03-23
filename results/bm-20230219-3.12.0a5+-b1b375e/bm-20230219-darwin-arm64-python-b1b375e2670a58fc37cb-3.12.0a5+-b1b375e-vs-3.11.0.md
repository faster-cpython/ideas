
# Results vs. 3.11.0

- fork: python
- ref: b1b375e2670a58fc37cb
- machine: darwin-arm64
- commit hash: b1b375e
- commit date: 2023-02-19
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 162 ms: 1.00x slower                                                   |
| chameleon      | 4.55 ms                                                             | 4.44 ms: 1.03x faster                                                  |
| docutils       | 1.47 sec                                                            | 1.49 sec: 1.01x slower                                                 |
| html5lib       | 34.8 ms                                                             | 35.8 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                               | 1.00x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 65.5 ms                                                             | 64.1 ms: 1.02x faster                                                  |
| float          | 53.0 ms                                                             | 52.4 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                               | 1.01x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 76.6 ms                                                             | 73.0 ms: 1.05x faster                                                  |
| regex_v8       | 16.1 ms                                                             | 15.8 ms: 1.02x faster                                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                   |
| regex_effbot   | 2.63 ms                                                             | 2.63 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.15 ms: 1.23x faster                                                  |
| unpickle_pure_python | 158 us                                                              | 143 us: 1.11x faster                                                   |
| xml_etree_parse      | 106 ms                                                              | 97.6 ms: 1.08x faster                                                  |
| unpickle_list        | 2.63 us                                                             | 2.57 us: 1.03x faster                                                  |
| pickle_pure_python   | 198 us                                                              | 195 us: 1.02x faster                                                   |
| json_loads           | 16.0 us                                                             | 16.1 us: 1.00x slower                                                  |
| pickle_list          | 2.83 us                                                             | 2.84 us: 1.01x slower                                                  |
| pickle_dict          | 17.9 us                                                             | 18.1 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 69.2 ms                                                             | 70.9 ms: 1.02x slower                                                  |
| xml_etree_process    | 35.0 ms                                                             | 36.0 ms: 1.03x slower                                                  |
| xml_etree_generate   | 48.2 ms                                                             | 50.3 ms: 1.04x slower                                                  |
| pickle               | 7.17 us                                                             | 7.56 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 12.4 ms: 1.01x slower                                                  |
| python_startup_no_site | 10.1 ms                                                             | 10.4 ms: 1.03x slower                                                  |
| Geometric mean         | (ref)                                                               | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 8.42 ms                                                             | 7.36 ms: 1.14x faster                                                  |
| genshi_text     | 15.3 ms                                                             | 14.3 ms: 1.07x faster                                                  |
| genshi_xml      | 29.9 ms                                                             | 28.3 ms: 1.06x faster                                                  |
| django_template | 21.1 ms                                                             | 21.3 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                               | 1.06x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp             | 651 ms                                                              | 441 ms: 1.48x faster                                                   |
| json_dumps              | 7.59 ms                                                             | 6.15 ms: 1.23x faster                                                  |
| mako                    | 8.42 ms                                                             | 7.36 ms: 1.14x faster                                                  |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.82 ms: 1.13x faster                                                  |
| generators              | 28.6 ms                                                             | 25.5 ms: 1.12x faster                                                  |
| unpickle_pure_python    | 158 us                                                              | 143 us: 1.11x faster                                                   |
| hexiom                  | 4.73 ms                                                             | 4.31 ms: 1.10x faster                                                  |
| deltablue               | 2.81 ms                                                             | 2.57 ms: 1.09x faster                                                  |
| xml_etree_parse         | 106 ms                                                              | 97.6 ms: 1.08x faster                                                  |
| richards                | 32.2 ms                                                             | 30.0 ms: 1.07x faster                                                  |
| genshi_text             | 15.3 ms                                                             | 14.3 ms: 1.07x faster                                                  |
| comprehensions          | 16.1 us                                                             | 15.1 us: 1.07x faster                                                  |
| chaos                   | 49.4 ms                                                             | 46.6 ms: 1.06x faster                                                  |
| genshi_xml              | 29.9 ms                                                             | 28.3 ms: 1.06x faster                                                  |
| regex_compile           | 76.6 ms                                                             | 73.0 ms: 1.05x faster                                                  |
| pathlib                 | 28.3 ms                                                             | 27.0 ms: 1.05x faster                                                  |
| pycparser               | 695 ms                                                              | 669 ms: 1.04x faster                                                   |
| logging_silent          | 68.0 ns                                                             | 65.8 ns: 1.03x faster                                                  |
| deepcopy_memo           | 26.3 us                                                             | 25.5 us: 1.03x faster                                                  |
| scimark_fft             | 200 ms                                                              | 194 ms: 1.03x faster                                                   |
| sympy_str               | 151 ms                                                              | 147 ms: 1.03x faster                                                   |
| create_gc_cycles        | 722 us                                                              | 703 us: 1.03x faster                                                   |
| async_tree_memoization  | 338 ms                                                              | 329 ms: 1.03x faster                                                   |
| sympy_sum               | 86.0 ms                                                             | 83.8 ms: 1.03x faster                                                  |
| unpickle_list           | 2.63 us                                                             | 2.57 us: 1.03x faster                                                  |
| unpack_sequence         | 33.5 ns                                                             | 32.7 ns: 1.03x faster                                                  |
| chameleon               | 4.55 ms                                                             | 4.44 ms: 1.03x faster                                                  |
| nbody                   | 65.5 ms                                                             | 64.1 ms: 1.02x faster                                                  |
| regex_v8                | 16.1 ms                                                             | 15.8 ms: 1.02x faster                                                  |
| pickle_pure_python      | 198 us                                                              | 195 us: 1.02x faster                                                   |
| bench_thread_pool       | 474 us                                                              | 466 us: 1.02x faster                                                   |
| fannkuch                | 260 ms                                                              | 257 ms: 1.01x faster                                                   |
| deepcopy                | 224 us                                                              | 221 us: 1.01x faster                                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.3 ms: 1.01x faster                                                  |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                   |
| float                   | 53.0 ms                                                             | 52.4 ms: 1.01x faster                                                  |
| dulwich_log             | 29.7 ms                                                             | 29.5 ms: 1.01x faster                                                  |
| sqlalchemy_imperative   | 7.26 ms                                                             | 7.23 ms: 1.00x faster                                                  |
| mdp                     | 1.54 sec                                                            | 1.54 sec: 1.00x faster                                                 |
| regex_effbot            | 2.63 ms                                                             | 2.63 ms: 1.00x slower                                                  |
| 2to3                    | 161 ms                                                              | 162 ms: 1.00x slower                                                   |
| json_loads              | 16.0 us                                                             | 16.1 us: 1.00x slower                                                  |
| pickle_list             | 2.83 us                                                             | 2.84 us: 1.01x slower                                                  |
| gc_traversal            | 2.41 ms                                                             | 2.42 ms: 1.01x slower                                                  |
| coroutines              | 17.7 ms                                                             | 17.8 ms: 1.01x slower                                                  |
| async_tree_none         | 285 ms                                                              | 286 ms: 1.01x slower                                                   |
| python_startup          | 12.3 ms                                                             | 12.4 ms: 1.01x slower                                                  |
| pprint_pformat          | 946 ms                                                              | 954 ms: 1.01x slower                                                   |
| pprint_safe_repr        | 463 ms                                                              | 468 ms: 1.01x slower                                                   |
| pickle_dict             | 17.9 us                                                             | 18.1 us: 1.01x slower                                                  |
| django_template         | 21.1 ms                                                             | 21.3 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed | 534 ms                                                              | 542 ms: 1.01x slower                                                   |
| docutils                | 1.47 sec                                                            | 1.49 sec: 1.01x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 174 ms: 1.01x slower                                                   |
| scimark_lu              | 72.2 ms                                                             | 73.3 ms: 1.02x slower                                                  |
| sqlalchemy_declarative  | 62.6 ms                                                             | 63.9 ms: 1.02x slower                                                  |
| sqlglot_optimize        | 31.2 ms                                                             | 31.9 ms: 1.02x slower                                                  |
| xml_etree_iterparse     | 69.2 ms                                                             | 70.9 ms: 1.02x slower                                                  |
| telco                   | 3.40 ms                                                             | 3.48 ms: 1.03x slower                                                  |
| html5lib                | 34.8 ms                                                             | 35.8 ms: 1.03x slower                                                  |
| xml_etree_process       | 35.0 ms                                                             | 36.0 ms: 1.03x slower                                                  |
| crypto_pyaes            | 51.8 ms                                                             | 53.5 ms: 1.03x slower                                                  |
| python_startup_no_site  | 10.1 ms                                                             | 10.4 ms: 1.03x slower                                                  |
| logging_format          | 3.77 us                                                             | 3.91 us: 1.04x slower                                                  |
| spectral_norm           | 72.5 ms                                                             | 75.2 ms: 1.04x slower                                                  |
| meteor_contest          | 73.3 ms                                                             | 76.3 ms: 1.04x slower                                                  |
| logging_simple          | 3.49 us                                                             | 3.64 us: 1.04x slower                                                  |
| coverage                | 58.4 ms                                                             | 60.9 ms: 1.04x slower                                                  |
| scimark_sor             | 82.9 ms                                                             | 86.5 ms: 1.04x slower                                                  |
| xml_etree_generate      | 48.2 ms                                                             | 50.3 ms: 1.04x slower                                                  |
| sqlite_synth            | 1.28 us                                                             | 1.35 us: 1.05x slower                                                  |
| async_tree_io           | 707 ms                                                              | 745 ms: 1.05x slower                                                   |
| bench_mp_pool           | 43.8 ms                                                             | 46.2 ms: 1.05x slower                                                  |
| pickle                  | 7.17 us                                                             | 7.56 us: 1.05x slower                                                  |
| pyflate                 | 309 ms                                                              | 328 ms: 1.06x slower                                                   |
| thrift                  | 431 us                                                              | 461 us: 1.07x slower                                                   |
| raytrace                | 207 ms                                                              | 223 ms: 1.08x slower                                                   |
| sqlglot_transpile       | 1.12 ms                                                             | 1.22 ms: 1.09x slower                                                  |
| sqlglot_parse           | 956 us                                                              | 1.05 ms: 1.10x slower                                                  |
| scimark_monte_carlo     | 46.5 ms                                                             | 52.7 ms: 1.13x slower                                                  |
| async_generators        | 195 ms                                                              | 264 ms: 1.35x slower                                                   |
| dask                    | 226 ms                                                              | 321 ms: 1.42x slower                                                   |
| Geometric mean          | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (9): nqueens, tornado_http, json, unpickle, go, pidigits, sympy_expand, deepcopy_reduce, mypy2
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint
