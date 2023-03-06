
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: d3ca042
- commit date: 2023-03-06
- overall geometric mean: 1.02x slower \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-darwin-arm64-python-main-3.12.0a5+-d3ca042 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 164 ms: 1.10x faster                                   |
| chameleon      | 4.61 ms                                                             | 4.42 ms: 1.04x faster                                  |
| docutils       | 1.46 sec                                                            | 1.49 sec: 1.02x slower                                 |
| html5lib       | 34.7 ms                                                             | 35.6 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-darwin-arm64-python-main-3.12.0a5+-d3ca042 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 64.1 ms: 1.02x faster                                  |
| float          | 51.7 ms                                                             | 53.6 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                               | 1.01x slower                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-darwin-arm64-python-main-3.12.0a5+-d3ca042 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 75.4 ms: 1.01x faster                                  |
| regex_v8       | 16.5 ms                                                             | 16.5 ms: 1.00x slower                                  |
| regex_effbot   | 2.63 ms                                                             | 2.85 ms: 1.09x slower                                  |
| regex_dna      | 151 ms                                                              | 166 ms: 1.10x slower                                   |
| Geometric mean | (ref)                                                               | 1.04x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-darwin-arm64-python-main-3.12.0a5+-d3ca042 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.17 ms: 1.24x faster                                  |
| unpickle_pure_python | 159 us                                                              | 145 us: 1.10x faster                                   |
| pickle_pure_python   | 200 us                                                              | 190 us: 1.05x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 97.7 ms: 1.02x faster                                  |
| pickle_list          | 2.86 us                                                             | 2.83 us: 1.01x faster                                  |
| json_loads           | 16.1 us                                                             | 16.1 us: 1.00x faster                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| unpickle_list        | 2.64 us                                                             | 2.65 us: 1.01x slower                                  |
| pickle               | 7.21 us                                                             | 7.50 us: 1.04x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 36.7 ms: 1.04x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 51.3 ms: 1.06x slower                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 71.0 ms: 1.08x slower                                  |
| Geometric mean       | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-darwin-arm64-python-main-3.12.0a5+-d3ca042 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 10.8 ms: 1.18x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 8.74 ms: 1.21x slower                                  |
| Geometric mean         | (ref)                                                               | 1.19x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-darwin-arm64-python-main-3.12.0a5+-d3ca042 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 8.40 ms                                                             | 7.46 ms: 1.13x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 29.2 ms: 1.05x faster                                  |
| genshi_text     | 15.3 ms                                                             | 14.8 ms: 1.04x faster                                  |
| django_template | 21.1 ms                                                             | 21.6 ms: 1.03x slower                                  |
| Geometric mean  | (ref)                                                               | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-darwin-arm64-python-main-3.12.0a5+-d3ca042 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps              | 7.67 ms                                                             | 6.17 ms: 1.24x faster                                  |
| mako                    | 8.40 ms                                                             | 7.46 ms: 1.13x faster                                  |
| 2to3                    | 181 ms                                                              | 164 ms: 1.10x faster                                   |
| unpickle_pure_python    | 159 us                                                              | 145 us: 1.10x faster                                   |
| deltablue               | 2.82 ms                                                             | 2.59 ms: 1.09x faster                                  |
| richards                | 32.7 ms                                                             | 30.5 ms: 1.07x faster                                  |
| hexiom                  | 4.73 ms                                                             | 4.46 ms: 1.06x faster                                  |
| pickle_pure_python      | 200 us                                                              | 190 us: 1.05x faster                                   |
| genshi_xml              | 30.5 ms                                                             | 29.2 ms: 1.05x faster                                  |
| chameleon               | 4.61 ms                                                             | 4.42 ms: 1.04x faster                                  |
| genshi_text             | 15.3 ms                                                             | 14.8 ms: 1.04x faster                                  |
| chaos                   | 49.3 ms                                                             | 47.8 ms: 1.03x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.50 sec: 1.03x faster                                 |
| scimark_fft             | 201 ms                                                              | 196 ms: 1.03x faster                                   |
| pycparser               | 694 ms                                                              | 679 ms: 1.02x faster                                   |
| xml_etree_parse         | 99.6 ms                                                             | 97.7 ms: 1.02x faster                                  |
| json                    | 2.83 ms                                                             | 2.77 ms: 1.02x faster                                  |
| nbody                   | 65.2 ms                                                             | 64.1 ms: 1.02x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.16 ms: 1.01x faster                                  |
| fannkuch                | 262 ms                                                              | 259 ms: 1.01x faster                                   |
| regex_compile           | 76.3 ms                                                             | 75.4 ms: 1.01x faster                                  |
| unpack_sequence         | 33.1 ns                                                             | 32.7 ns: 1.01x faster                                  |
| pickle_list             | 2.86 us                                                             | 2.83 us: 1.01x faster                                  |
| meteor_contest          | 73.9 ms                                                             | 73.4 ms: 1.01x faster                                  |
| json_loads              | 16.1 us                                                             | 16.1 us: 1.00x faster                                  |
| regex_v8                | 16.5 ms                                                             | 16.5 ms: 1.00x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| generators              | 28.4 ms                                                             | 28.5 ms: 1.00x slower                                  |
| unpickle_list           | 2.64 us                                                             | 2.65 us: 1.01x slower                                  |
| deepcopy_memo           | 26.2 us                                                             | 26.4 us: 1.01x slower                                  |
| logging_silent          | 67.4 ns                                                             | 68.1 ns: 1.01x slower                                  |
| go                      | 109 ms                                                              | 111 ms: 1.01x slower                                   |
| deepcopy                | 222 us                                                              | 225 us: 1.01x slower                                   |
| telco                   | 3.39 ms                                                             | 3.43 ms: 1.01x slower                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.7 ms: 1.02x slower                                  |
| sqlalchemy_declarative  | 62.4 ms                                                             | 63.4 ms: 1.02x slower                                  |
| dulwich_log             | 29.1 ms                                                             | 29.5 ms: 1.02x slower                                  |
| sympy_expand            | 242 ms                                                              | 246 ms: 1.02x slower                                   |
| docutils                | 1.46 sec                                                            | 1.49 sec: 1.02x slower                                 |
| async_tree_none         | 281 ms                                                              | 287 ms: 1.02x slower                                   |
| pprint_pformat          | 953 ms                                                              | 972 ms: 1.02x slower                                   |
| coverage                | 58.4 ms                                                             | 59.5 ms: 1.02x slower                                  |
| coroutines              | 17.8 ms                                                             | 18.1 ms: 1.02x slower                                  |
| pprint_safe_repr        | 467 ms                                                              | 477 ms: 1.02x slower                                   |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.37 ms: 1.02x slower                                  |
| sqlglot_normalize       | 171 ms                                                              | 175 ms: 1.02x slower                                   |
| sympy_sum               | 85.5 ms                                                             | 87.8 ms: 1.03x slower                                  |
| django_template         | 21.1 ms                                                             | 21.6 ms: 1.03x slower                                  |
| html5lib                | 34.7 ms                                                             | 35.6 ms: 1.03x slower                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 32.1 ms: 1.03x slower                                  |
| sympy_str               | 151 ms                                                              | 155 ms: 1.03x slower                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 544 ms: 1.03x slower                                   |
| spectral_norm           | 72.7 ms                                                             | 74.9 ms: 1.03x slower                                  |
| crypto_pyaes            | 51.7 ms                                                             | 53.3 ms: 1.03x slower                                  |
| scimark_lu              | 72.2 ms                                                             | 74.5 ms: 1.03x slower                                  |
| bench_thread_pool       | 457 us                                                              | 473 us: 1.03x slower                                   |
| deepcopy_reduce         | 1.90 us                                                             | 1.97 us: 1.04x slower                                  |
| float                   | 51.7 ms                                                             | 53.6 ms: 1.04x slower                                  |
| pickle                  | 7.21 us                                                             | 7.50 us: 1.04x slower                                  |
| xml_etree_process       | 35.1 ms                                                             | 36.7 ms: 1.04x slower                                  |
| async_tree_memoization  | 317 ms                                                              | 332 ms: 1.05x slower                                   |
| logging_simple          | 3.47 us                                                             | 3.64 us: 1.05x slower                                  |
| logging_format          | 3.73 us                                                             | 3.94 us: 1.06x slower                                  |
| async_tree_io           | 696 ms                                                              | 736 ms: 1.06x slower                                   |
| scimark_sor             | 83.3 ms                                                             | 88.1 ms: 1.06x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 51.3 ms: 1.06x slower                                  |
| nqueens                 | 59.5 ms                                                             | 63.1 ms: 1.06x slower                                  |
| pyflate                 | 313 ms                                                              | 332 ms: 1.06x slower                                   |
| bench_mp_pool           | 41.4 ms                                                             | 44.1 ms: 1.07x slower                                  |
| thrift                  | 429 us                                                              | 458 us: 1.07x slower                                   |
| sqlite_synth            | 1.29 us                                                             | 1.38 us: 1.07x slower                                  |
| xml_etree_iterparse     | 65.6 ms                                                             | 71.0 ms: 1.08x slower                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 50.9 ms: 1.08x slower                                  |
| regex_effbot            | 2.63 ms                                                             | 2.85 ms: 1.09x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.22 ms: 1.10x slower                                  |
| regex_dna               | 151 ms                                                              | 166 ms: 1.10x slower                                   |
| raytrace                | 207 ms                                                              | 228 ms: 1.10x slower                                   |
| sqlglot_parse           | 948 us                                                              | 1.05 ms: 1.11x slower                                  |
| python_startup          | 9.19 ms                                                             | 10.8 ms: 1.18x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 8.74 ms: 1.21x slower                                  |
| pathlib                 | 20.6 ms                                                             | 27.2 ms: 1.32x slower                                  |
| async_generators        | 195 ms                                                              | 270 ms: 1.39x slower                                   |
| Geometric mean          | (ref)                                                               | 1.02x slower                                           |

Benchmark hidden because not significant (3): tornado_http, pidigits, unpickle
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230306-3.12.0a5+-d3ca042/bm-20230306-darwin-arm64-python-main-3.12.0a5+-d3ca042.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
