
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 206f05a
- commit date: 2023-01-14
- overall geometric mean: 1.00x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 183 ms: 1.01x slower                                   |
| chameleon      | 4.61 ms                                                             | 4.59 ms: 1.01x faster                                  |
| docutils       | 1.46 sec                                                            | 1.44 sec: 1.01x faster                                 |
| Geometric mean | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 51.7 ms                                                             | 51.5 ms: 1.00x faster                                  |
| nbody          | 65.2 ms                                                             | 63.4 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 74.6 ms: 1.02x faster                                  |
| regex_dna      | 151 ms                                                              | 154 ms: 1.02x slower                                   |
| regex_effbot   | 2.63 ms                                                             | 2.73 ms: 1.04x slower                                  |
| regex_v8       | 16.5 ms                                                             | 16.8 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                               | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.12 ms: 1.25x faster                                  |
| json_loads           | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| pickle               | 7.21 us                                                             | 7.56 us: 1.05x slower                                  |
| pickle_list          | 2.86 us                                                             | 2.89 us: 1.01x slower                                  |
| pickle_pure_python   | 200 us                                                              | 194 us: 1.03x faster                                   |
| unpickle             | 9.68 us                                                             | 9.84 us: 1.02x slower                                  |
| unpickle_list        | 2.64 us                                                             | 2.71 us: 1.03x slower                                  |
| unpickle_pure_python | 159 us                                                              | 142 us: 1.12x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 93.1 ms: 1.07x faster                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 66.4 ms: 1.01x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 48.0 ms: 1.01x faster                                  |
| xml_etree_process    | 35.1 ms                                                             | 34.8 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                               | 1.03x faster                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.33 ms: 1.01x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.34 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                               | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.7 ms: 1.03x slower                                  |
| genshi_text     | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 28.4 ms: 1.07x faster                                  |
| mako            | 8.40 ms                                                             | 8.10 ms: 1.04x faster                                  |
| Geometric mean  | (ref)                                                               | 1.02x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 183 ms: 1.01x slower                                   |
| async_generators        | 195 ms                                                              | 200 ms: 1.02x slower                                   |
| async_tree_none         | 281 ms                                                              | 285 ms: 1.01x slower                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 540 ms: 1.02x slower                                   |
| async_tree_io           | 696 ms                                                              | 737 ms: 1.06x slower                                   |
| async_tree_memoization  | 317 ms                                                              | 327 ms: 1.03x slower                                   |
| chameleon               | 4.61 ms                                                             | 4.59 ms: 1.01x faster                                  |
| chaos                   | 49.3 ms                                                             | 50.3 ms: 1.02x slower                                  |
| bench_thread_pool       | 457 us                                                              | 447 us: 1.02x faster                                   |
| coroutines              | 17.8 ms                                                             | 18.6 ms: 1.05x slower                                  |
| coverage                | 58.4 ms                                                             | 56.4 ms: 1.03x faster                                  |
| crypto_pyaes            | 51.7 ms                                                             | 52.9 ms: 1.02x slower                                  |
| deepcopy                | 222 us                                                              | 220 us: 1.01x faster                                   |
| deepcopy_memo           | 26.2 us                                                             | 25.9 us: 1.01x faster                                  |
| deltablue               | 2.82 ms                                                             | 2.61 ms: 1.08x faster                                  |
| django_template         | 21.1 ms                                                             | 21.7 ms: 1.03x slower                                  |
| docutils                | 1.46 sec                                                            | 1.44 sec: 1.01x faster                                 |
| dulwich_log             | 29.1 ms                                                             | 28.6 ms: 1.02x faster                                  |
| fannkuch                | 262 ms                                                              | 255 ms: 1.03x faster                                   |
| float                   | 51.7 ms                                                             | 51.5 ms: 1.00x faster                                  |
| generators              | 28.4 ms                                                             | 33.6 ms: 1.18x slower                                  |
| genshi_text             | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                  |
| genshi_xml              | 30.5 ms                                                             | 28.4 ms: 1.07x faster                                  |
| go                      | 109 ms                                                              | 108 ms: 1.01x faster                                   |
| hexiom                  | 4.73 ms                                                             | 4.92 ms: 1.04x slower                                  |
| json_dumps              | 7.67 ms                                                             | 6.12 ms: 1.25x faster                                  |
| json_loads              | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| logging_format          | 3.73 us                                                             | 3.79 us: 1.02x slower                                  |
| logging_silent          | 67.4 ns                                                             | 66.2 ns: 1.02x faster                                  |
| logging_simple          | 3.47 us                                                             | 3.50 us: 1.01x slower                                  |
| mako                    | 8.40 ms                                                             | 8.10 ms: 1.04x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.50 sec: 1.03x faster                                 |
| meteor_contest          | 73.9 ms                                                             | 74.5 ms: 1.01x slower                                  |
| mypy                    | 421 ms                                                              | 414 ms: 1.02x faster                                   |
| nbody                   | 65.2 ms                                                             | 63.4 ms: 1.03x faster                                  |
| nqueens                 | 59.5 ms                                                             | 60.8 ms: 1.02x slower                                  |
| pathlib                 | 20.6 ms                                                             | 20.9 ms: 1.02x slower                                  |
| pickle                  | 7.21 us                                                             | 7.56 us: 1.05x slower                                  |
| pickle_list             | 2.86 us                                                             | 2.89 us: 1.01x slower                                  |
| pickle_pure_python      | 200 us                                                              | 194 us: 1.03x faster                                   |
| pprint_safe_repr        | 467 ms                                                              | 464 ms: 1.01x faster                                   |
| pprint_pformat          | 953 ms                                                              | 939 ms: 1.01x faster                                   |
| pycparser               | 694 ms                                                              | 682 ms: 1.02x faster                                   |
| pyflate                 | 313 ms                                                              | 319 ms: 1.02x slower                                   |
| python_startup          | 9.19 ms                                                             | 9.33 ms: 1.01x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.34 ms: 1.01x slower                                  |
| raytrace                | 207 ms                                                              | 223 ms: 1.08x slower                                   |
| regex_compile           | 76.3 ms                                                             | 74.6 ms: 1.02x faster                                  |
| regex_dna               | 151 ms                                                              | 154 ms: 1.02x slower                                   |
| regex_effbot            | 2.63 ms                                                             | 2.73 ms: 1.04x slower                                  |
| regex_v8                | 16.5 ms                                                             | 16.8 ms: 1.02x slower                                  |
| richards                | 32.7 ms                                                             | 30.4 ms: 1.08x faster                                  |
| scimark_fft             | 201 ms                                                              | 195 ms: 1.03x faster                                   |
| scimark_monte_carlo     | 46.9 ms                                                             | 50.6 ms: 1.08x slower                                  |
| scimark_sor             | 83.3 ms                                                             | 82.0 ms: 1.02x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.79 ms: 1.15x faster                                  |
| spectral_norm           | 72.7 ms                                                             | 73.6 ms: 1.01x slower                                  |
| sqlglot_parse           | 948 us                                                              | 1.02 ms: 1.08x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.18 ms: 1.07x slower                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 31.2 ms: 1.00x faster                                  |
| sqlglot_normalize       | 171 ms                                                              | 171 ms: 1.00x slower                                   |
| sqlite_synth            | 1.29 us                                                             | 1.38 us: 1.07x slower                                  |
| sympy_expand            | 242 ms                                                              | 241 ms: 1.01x faster                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.4 ms: 1.01x faster                                  |
| sympy_sum               | 85.5 ms                                                             | 85.9 ms: 1.00x slower                                  |
| thrift                  | 429 us                                                              | 442 us: 1.03x slower                                   |
| unpack_sequence         | 33.1 ns                                                             | 32.8 ns: 1.01x faster                                  |
| unpickle                | 9.68 us                                                             | 9.84 us: 1.02x slower                                  |
| unpickle_list           | 2.64 us                                                             | 2.71 us: 1.03x slower                                  |
| unpickle_pure_python    | 159 us                                                              | 142 us: 1.12x faster                                   |
| xml_etree_parse         | 99.6 ms                                                             | 93.1 ms: 1.07x faster                                  |
| xml_etree_iterparse     | 65.6 ms                                                             | 66.4 ms: 1.01x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 48.0 ms: 1.01x faster                                  |
| xml_etree_process       | 35.1 ms                                                             | 34.8 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                               | 1.00x faster                                           |

Benchmark hidden because not significant (10): bench_mp_pool, deepcopy_reduce, html5lib, json, pickle_dict, pidigits, scimark_lu, sympy_str, telco, tornado_http
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of public/results/bm-20230114-3.12.0a4+-206f05a/bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
