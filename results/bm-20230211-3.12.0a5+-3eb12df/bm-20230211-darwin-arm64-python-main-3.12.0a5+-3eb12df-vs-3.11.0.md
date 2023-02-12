
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 3eb12df
- commit date: 2023-02-11
- overall geometric mean: 1.02x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 181 ms: 1.00x faster                                   |
| chameleon      | 4.61 ms                                                             | 4.34 ms: 1.06x faster                                  |
| docutils       | 1.46 sec                                                            | 1.46 sec: 1.00x slower                                 |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 51.7 ms                                                             | 49.7 ms: 1.04x faster                                  |
| nbody          | 65.2 ms                                                             | 63.1 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 71.0 ms: 1.08x faster                                  |
| regex_v8       | 16.5 ms                                                             | 16.0 ms: 1.03x faster                                  |
| regex_dna      | 151 ms                                                              | 150 ms: 1.01x faster                                   |
| regex_effbot   | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                               | 1.03x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.06 ms: 1.27x faster                                  |
| unpickle_pure_python | 159 us                                                              | 137 us: 1.16x faster                                   |
| pickle_pure_python   | 200 us                                                              | 185 us: 1.08x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 93.0 ms: 1.07x faster                                  |
| pickle_list          | 2.86 us                                                             | 2.83 us: 1.01x faster                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 35.2 ms: 1.00x slower                                  |
| json_loads           | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| unpickle_list        | 2.64 us                                                             | 2.67 us: 1.01x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 49.2 ms: 1.02x slower                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 67.1 ms: 1.02x slower                                  |
| unpickle             | 9.68 us                                                             | 9.91 us: 1.02x slower                                  |
| pickle               | 7.21 us                                                             | 7.57 us: 1.05x slower                                  |
| Geometric mean       | (ref)                                                               | 1.03x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.36 ms: 1.02x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.38 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                               | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 8.40 ms                                                             | 7.13 ms: 1.18x faster                                  |
| genshi_text     | 15.3 ms                                                             | 13.8 ms: 1.11x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 27.5 ms: 1.11x faster                                  |
| django_template | 21.1 ms                                                             | 20.8 ms: 1.01x faster                                  |
| Geometric mean  | (ref)                                                               | 1.10x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps              | 7.67 ms                                                             | 6.06 ms: 1.27x faster                                  |
| mako                    | 8.40 ms                                                             | 7.13 ms: 1.18x faster                                  |
| unpickle_pure_python    | 159 us                                                              | 137 us: 1.16x faster                                   |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.77 ms: 1.16x faster                                  |
| deltablue               | 2.82 ms                                                             | 2.47 ms: 1.14x faster                                  |
| hexiom                  | 4.73 ms                                                             | 4.21 ms: 1.12x faster                                  |
| genshi_text             | 15.3 ms                                                             | 13.8 ms: 1.11x faster                                  |
| genshi_xml              | 30.5 ms                                                             | 27.5 ms: 1.11x faster                                  |
| richards                | 32.7 ms                                                             | 29.5 ms: 1.11x faster                                  |
| chaos                   | 49.3 ms                                                             | 45.5 ms: 1.08x faster                                  |
| unpack_sequence         | 33.1 ns                                                             | 30.6 ns: 1.08x faster                                  |
| pickle_pure_python      | 200 us                                                              | 185 us: 1.08x faster                                   |
| regex_compile           | 76.3 ms                                                             | 71.0 ms: 1.08x faster                                  |
| xml_etree_parse         | 99.6 ms                                                             | 93.0 ms: 1.07x faster                                  |
| chameleon               | 4.61 ms                                                             | 4.34 ms: 1.06x faster                                  |
| scimark_fft             | 201 ms                                                              | 189 ms: 1.06x faster                                   |
| deepcopy_memo           | 26.2 us                                                             | 24.7 us: 1.06x faster                                  |
| logging_silent          | 67.4 ns                                                             | 64.1 ns: 1.05x faster                                  |
| sympy_str               | 151 ms                                                              | 144 ms: 1.05x faster                                   |
| pycparser               | 694 ms                                                              | 664 ms: 1.05x faster                                   |
| fannkuch                | 262 ms                                                              | 251 ms: 1.04x faster                                   |
| sympy_sum               | 85.5 ms                                                             | 82.1 ms: 1.04x faster                                  |
| float                   | 51.7 ms                                                             | 49.7 ms: 1.04x faster                                  |
| pprint_pformat          | 953 ms                                                              | 920 ms: 1.04x faster                                   |
| nbody                   | 65.2 ms                                                             | 63.1 ms: 1.03x faster                                  |
| pprint_safe_repr        | 467 ms                                                              | 452 ms: 1.03x faster                                   |
| deepcopy                | 222 us                                                              | 215 us: 1.03x faster                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.1 ms: 1.03x faster                                  |
| bench_thread_pool       | 457 us                                                              | 444 us: 1.03x faster                                   |
| regex_v8                | 16.5 ms                                                             | 16.0 ms: 1.03x faster                                  |
| scimark_lu              | 72.2 ms                                                             | 70.5 ms: 1.03x faster                                  |
| dulwich_log             | 29.1 ms                                                             | 28.4 ms: 1.02x faster                                  |
| go                      | 109 ms                                                              | 107 ms: 1.02x faster                                   |
| deepcopy_reduce         | 1.90 us                                                             | 1.86 us: 1.02x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.51 sec: 1.02x faster                                 |
| meteor_contest          | 73.9 ms                                                             | 72.7 ms: 1.02x faster                                  |
| sympy_expand            | 242 ms                                                              | 238 ms: 1.02x faster                                   |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.12 ms: 1.01x faster                                  |
| django_template         | 21.1 ms                                                             | 20.8 ms: 1.01x faster                                  |
| regex_dna               | 151 ms                                                              | 150 ms: 1.01x faster                                   |
| pickle_list             | 2.86 us                                                             | 2.83 us: 1.01x faster                                  |
| sqlglot_normalize       | 171 ms                                                              | 169 ms: 1.01x faster                                   |
| async_tree_none         | 281 ms                                                              | 278 ms: 1.01x faster                                   |
| regex_effbot            | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 31.1 ms: 1.01x faster                                  |
| 2to3                    | 181 ms                                                              | 181 ms: 1.00x faster                                   |
| scimark_sor             | 83.3 ms                                                             | 83.4 ms: 1.00x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| docutils                | 1.46 sec                                                            | 1.46 sec: 1.00x slower                                 |
| xml_etree_process       | 35.1 ms                                                             | 35.2 ms: 1.00x slower                                  |
| sqlalchemy_declarative  | 62.4 ms                                                             | 62.7 ms: 1.00x slower                                  |
| spectral_norm           | 72.7 ms                                                             | 73.4 ms: 1.01x slower                                  |
| async_tree_memoization  | 317 ms                                                              | 320 ms: 1.01x slower                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 534 ms: 1.01x slower                                   |
| json_loads              | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| logging_simple          | 3.47 us                                                             | 3.51 us: 1.01x slower                                  |
| unpickle_list           | 2.64 us                                                             | 2.67 us: 1.01x slower                                  |
| logging_format          | 3.73 us                                                             | 3.80 us: 1.02x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 49.2 ms: 1.02x slower                                  |
| python_startup          | 9.19 ms                                                             | 9.36 ms: 1.02x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.38 ms: 1.02x slower                                  |
| xml_etree_iterparse     | 65.6 ms                                                             | 67.1 ms: 1.02x slower                                  |
| unpickle                | 9.68 us                                                             | 9.91 us: 1.02x slower                                  |
| bench_mp_pool           | 41.4 ms                                                             | 42.6 ms: 1.03x slower                                  |
| crypto_pyaes            | 51.7 ms                                                             | 53.4 ms: 1.03x slower                                  |
| coverage                | 58.4 ms                                                             | 60.3 ms: 1.03x slower                                  |
| coroutines              | 17.8 ms                                                             | 18.4 ms: 1.03x slower                                  |
| pyflate                 | 313 ms                                                              | 324 ms: 1.04x slower                                   |
| thrift                  | 429 us                                                              | 447 us: 1.04x slower                                   |
| async_tree_io           | 696 ms                                                              | 726 ms: 1.04x slower                                   |
| raytrace                | 207 ms                                                              | 217 ms: 1.05x slower                                   |
| pickle                  | 7.21 us                                                             | 7.57 us: 1.05x slower                                  |
| pathlib                 | 20.6 ms                                                             | 21.8 ms: 1.06x slower                                  |
| sqlite_synth            | 1.29 us                                                             | 1.37 us: 1.06x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.18 ms: 1.06x slower                                  |
| sqlglot_parse           | 948 us                                                              | 1.01 ms: 1.07x slower                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 50.0 ms: 1.07x slower                                  |
| generators              | 28.4 ms                                                             | 32.9 ms: 1.16x slower                                  |
| async_generators        | 195 ms                                                              | 255 ms: 1.31x slower                                   |
| Geometric mean          | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (6): tornado_http, telco, pidigits, nqueens, json, html5lib
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (4) of public/results/bm-20230211-3.12.0a5+-3eb12df/bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df.json: asyncio_tcp, create_gc_cycles, gc_traversal, mypy2
