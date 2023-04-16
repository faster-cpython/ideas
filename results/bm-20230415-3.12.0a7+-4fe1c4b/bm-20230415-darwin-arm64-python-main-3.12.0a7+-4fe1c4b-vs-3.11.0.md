
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 4fe1c4b
- commit date: 2023-04-15
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 161 ms: 1.00x faster                                   |
| chameleon      | 4.55 ms                                                             | 4.23 ms: 1.08x faster                                  |
| docutils       | 1.47 sec                                                            | 1.45 sec: 1.01x faster                                 |
| Geometric mean | (ref)                                                               | 1.03x faster                                           |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.5 ms                                                             | 56.7 ms: 1.15x faster                                  |
| float          | 53.0 ms                                                             | 50.9 ms: 1.04x faster                                  |
| pidigits       | 281 ms                                                              | 280 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                               | 1.06x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.6 ms                                                             | 72.3 ms: 1.06x faster                                  |
| regex_v8       | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.02x faster                                   |
| regex_effbot   | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                               | 1.03x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.04 ms: 1.26x faster                                  |
| unpickle_pure_python | 158 us                                                              | 137 us: 1.15x faster                                   |
| pickle_pure_python   | 198 us                                                              | 182 us: 1.09x faster                                   |
| xml_etree_parse      | 106 ms                                                              | 97.5 ms: 1.09x faster                                  |
| unpickle             | 9.66 us                                                             | 8.99 us: 1.08x faster                                  |
| xml_etree_process    | 35.0 ms                                                             | 34.5 ms: 1.01x faster                                  |
| xml_etree_iterparse  | 69.2 ms                                                             | 68.4 ms: 1.01x faster                                  |
| unpickle_list        | 2.63 us                                                             | 2.62 us: 1.00x faster                                  |
| json_loads           | 16.0 us                                                             | 16.3 us: 1.02x slower                                  |
| xml_etree_generate   | 48.2 ms                                                             | 49.0 ms: 1.02x slower                                  |
| pickle_list          | 2.83 us                                                             | 2.91 us: 1.03x slower                                  |
| pickle_dict          | 17.9 us                                                             | 18.5 us: 1.04x slower                                  |
| pickle               | 7.17 us                                                             | 7.50 us: 1.05x slower                                  |
| Geometric mean       | (ref)                                                               | 1.04x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 11.5 ms: 1.07x faster                                  |
| python_startup_no_site | 10.1 ms                                                             | 9.51 ms: 1.06x faster                                  |
| Geometric mean         | (ref)                                                               | 1.06x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 8.42 ms                                                             | 7.04 ms: 1.20x faster                                  |
| genshi_text     | 15.3 ms                                                             | 13.4 ms: 1.14x faster                                  |
| genshi_xml      | 29.9 ms                                                             | 26.4 ms: 1.13x faster                                  |
| django_template | 21.1 ms                                                             | 20.2 ms: 1.04x faster                                  |
| Geometric mean  | (ref)                                                               | 1.13x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| asyncio_tcp             | 651 ms                                                              | 429 ms: 1.52x faster                                   |
| generators              | 28.6 ms                                                             | 22.5 ms: 1.27x faster                                  |
| json_dumps              | 7.59 ms                                                             | 6.04 ms: 1.26x faster                                  |
| mako                    | 8.42 ms                                                             | 7.04 ms: 1.20x faster                                  |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.71 ms: 1.18x faster                                  |
| hexiom                  | 4.73 ms                                                             | 4.10 ms: 1.16x faster                                  |
| unpickle_pure_python    | 158 us                                                              | 137 us: 1.15x faster                                   |
| nbody                   | 65.5 ms                                                             | 56.7 ms: 1.15x faster                                  |
| sqlglot_parse           | 956 us                                                              | 831 us: 1.15x faster                                   |
| genshi_text             | 15.3 ms                                                             | 13.4 ms: 1.14x faster                                  |
| unpack_sequence         | 33.5 ns                                                             | 29.5 ns: 1.14x faster                                  |
| genshi_xml              | 29.9 ms                                                             | 26.4 ms: 1.13x faster                                  |
| sqlglot_transpile       | 1.12 ms                                                             | 992 us: 1.13x faster                                   |
| deltablue               | 2.81 ms                                                             | 2.50 ms: 1.13x faster                                  |
| coverage                | 58.4 ms                                                             | 52.1 ms: 1.12x faster                                  |
| scimark_fft             | 200 ms                                                              | 179 ms: 1.12x faster                                   |
| logging_silent          | 68.0 ns                                                             | 62.1 ns: 1.09x faster                                  |
| chaos                   | 49.4 ms                                                             | 45.2 ms: 1.09x faster                                  |
| pickle_pure_python      | 198 us                                                              | 182 us: 1.09x faster                                   |
| xml_etree_parse         | 106 ms                                                              | 97.5 ms: 1.09x faster                                  |
| deepcopy_memo           | 26.3 us                                                             | 24.3 us: 1.08x faster                                  |
| chameleon               | 4.55 ms                                                             | 4.23 ms: 1.08x faster                                  |
| unpickle                | 9.66 us                                                             | 8.99 us: 1.08x faster                                  |
| scimark_lu              | 72.2 ms                                                             | 67.3 ms: 1.07x faster                                  |
| python_startup          | 12.3 ms                                                             | 11.5 ms: 1.07x faster                                  |
| spectral_norm           | 72.5 ms                                                             | 67.8 ms: 1.07x faster                                  |
| regex_compile           | 76.6 ms                                                             | 72.3 ms: 1.06x faster                                  |
| deepcopy                | 224 us                                                              | 211 us: 1.06x faster                                   |
| python_startup_no_site  | 10.1 ms                                                             | 9.51 ms: 1.06x faster                                  |
| async_tree_memoization  | 338 ms                                                              | 320 ms: 1.06x faster                                   |
| pylint                  | 271 ms                                                              | 256 ms: 1.06x faster                                   |
| pycparser               | 695 ms                                                              | 658 ms: 1.06x faster                                   |
| pprint_safe_repr        | 463 ms                                                              | 440 ms: 1.05x faster                                   |
| richards                | 32.2 ms                                                             | 30.7 ms: 1.05x faster                                  |
| pprint_pformat          | 946 ms                                                              | 902 ms: 1.05x faster                                   |
| sqlglot_normalize       | 171 ms                                                              | 164 ms: 1.05x faster                                   |
| sqlglot_optimize        | 31.2 ms                                                             | 29.9 ms: 1.04x faster                                  |
| deepcopy_reduce         | 1.91 us                                                             | 1.83 us: 1.04x faster                                  |
| pathlib                 | 28.3 ms                                                             | 27.2 ms: 1.04x faster                                  |
| django_template         | 21.1 ms                                                             | 20.2 ms: 1.04x faster                                  |
| nqueens                 | 62.4 ms                                                             | 59.9 ms: 1.04x faster                                  |
| float                   | 53.0 ms                                                             | 50.9 ms: 1.04x faster                                  |
| bench_thread_pool       | 474 us                                                              | 455 us: 1.04x faster                                   |
| create_gc_cycles        | 722 us                                                              | 700 us: 1.03x faster                                   |
| coroutines              | 17.7 ms                                                             | 17.2 ms: 1.03x faster                                  |
| meteor_contest          | 73.3 ms                                                             | 71.3 ms: 1.03x faster                                  |
| sqlalchemy_imperative   | 7.26 ms                                                             | 7.07 ms: 1.03x faster                                  |
| regex_v8                | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                  |
| async_tree_none         | 285 ms                                                              | 277 ms: 1.03x faster                                   |
| mdp                     | 1.54 sec                                                            | 1.50 sec: 1.03x faster                                 |
| sympy_expand            | 243 ms                                                              | 237 ms: 1.03x faster                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.2 ms: 1.03x faster                                  |
| sympy_str               | 151 ms                                                              | 148 ms: 1.02x faster                                   |
| comprehensions          | 16.1 us                                                             | 15.8 us: 1.02x faster                                  |
| dulwich_log             | 29.7 ms                                                             | 29.2 ms: 1.02x faster                                  |
| sqlalchemy_declarative  | 62.6 ms                                                             | 61.6 ms: 1.02x faster                                  |
| regex_dna               | 151 ms                                                              | 149 ms: 1.02x faster                                   |
| xml_etree_process       | 35.0 ms                                                             | 34.5 ms: 1.01x faster                                  |
| sympy_sum               | 86.0 ms                                                             | 84.9 ms: 1.01x faster                                  |
| scimark_sor             | 82.9 ms                                                             | 81.8 ms: 1.01x faster                                  |
| docutils                | 1.47 sec                                                            | 1.45 sec: 1.01x faster                                 |
| xml_etree_iterparse     | 69.2 ms                                                             | 68.4 ms: 1.01x faster                                  |
| telco                   | 3.40 ms                                                             | 3.36 ms: 1.01x faster                                  |
| fannkuch                | 260 ms                                                              | 257 ms: 1.01x faster                                   |
| logging_simple          | 3.49 us                                                             | 3.46 us: 1.01x faster                                  |
| regex_effbot            | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                  |
| 2to3                    | 161 ms                                                              | 161 ms: 1.00x faster                                   |
| unpickle_list           | 2.63 us                                                             | 2.62 us: 1.00x faster                                  |
| pidigits                | 281 ms                                                              | 280 ms: 1.00x faster                                   |
| logging_format          | 3.77 us                                                             | 3.79 us: 1.00x slower                                  |
| gc_traversal            | 2.41 ms                                                             | 2.43 ms: 1.01x slower                                  |
| go                      | 109 ms                                                              | 110 ms: 1.01x slower                                   |
| async_tree_io           | 707 ms                                                              | 716 ms: 1.01x slower                                   |
| json_loads              | 16.0 us                                                             | 16.3 us: 1.02x slower                                  |
| xml_etree_generate      | 48.2 ms                                                             | 49.0 ms: 1.02x slower                                  |
| thrift                  | 431 us                                                              | 440 us: 1.02x slower                                   |
| raytrace                | 207 ms                                                              | 212 ms: 1.02x slower                                   |
| pickle_list             | 2.83 us                                                             | 2.91 us: 1.03x slower                                  |
| crypto_pyaes            | 51.8 ms                                                             | 53.4 ms: 1.03x slower                                  |
| bench_mp_pool           | 43.8 ms                                                             | 45.1 ms: 1.03x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.5 us: 1.04x slower                                  |
| pickle                  | 7.17 us                                                             | 7.50 us: 1.05x slower                                  |
| scimark_monte_carlo     | 46.5 ms                                                             | 48.9 ms: 1.05x slower                                  |
| sqlite_synth            | 1.28 us                                                             | 1.35 us: 1.05x slower                                  |
| pyflate                 | 309 ms                                                              | 327 ms: 1.06x slower                                   |
| async_generators        | 195 ms                                                              | 257 ms: 1.32x slower                                   |
| dask                    | 226 ms                                                              | 314 ms: 1.39x slower                                   |
| Geometric mean          | (ref)                                                               | 1.04x faster                                           |

Benchmark hidden because not significant (5): tornado_http, async_tree_cpu_io_mixed, html5lib, json, mypy2
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn
