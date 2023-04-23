
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 0fd3891
- commit date: 2023-04-22
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-darwin-arm64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 161 ms: 1.00x faster                                   |
| chameleon      | 4.55 ms                                                             | 4.42 ms: 1.03x faster                                  |
| docutils       | 1.47 sec                                                            | 1.46 sec: 1.01x faster                                 |
| Geometric mean | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-darwin-arm64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.5 ms                                                             | 61.3 ms: 1.07x faster                                  |
| pidigits       | 281 ms                                                              | 280 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-darwin-arm64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.6 ms                                                             | 70.8 ms: 1.08x faster                                  |
| regex_v8       | 16.1 ms                                                             | 15.9 ms: 1.01x faster                                  |
| regex_dna      | 151 ms                                                              | 151 ms: 1.00x faster                                   |
| regex_effbot   | 2.63 ms                                                             | 2.65 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-darwin-arm64-python-main-3.12.0a7+-0fd3891 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.08 ms: 1.25x faster                                  |
| unpickle_pure_python | 158 us                                                              | 144 us: 1.10x faster                                   |
| pickle_pure_python   | 198 us                                                              | 184 us: 1.08x faster                                   |
| xml_etree_parse      | 106 ms                                                              | 98.4 ms: 1.08x faster                                  |
| unpickle             | 9.66 us                                                             | 9.29 us: 1.04x faster                                  |
| json_loads           | 16.0 us                                                             | 16.3 us: 1.01x slower                                  |
| xml_etree_process    | 35.0 ms                                                             | 35.7 ms: 1.02x slower                                  |
| pickle_list          | 2.83 us                                                             | 2.89 us: 1.02x slower                                  |
| pickle_dict          | 17.9 us                                                             | 18.4 us: 1.03x slower                                  |
| pickle               | 7.17 us                                                             | 7.55 us: 1.05x slower                                  |
| xml_etree_generate   | 48.2 ms                                                             | 51.0 ms: 1.06x slower                                  |
| Geometric mean       | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-darwin-arm64-python-main-3.12.0a7+-0fd3891 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 11.8 ms: 1.05x faster                                  |
| python_startup_no_site | 10.1 ms                                                             | 9.72 ms: 1.04x faster                                  |
| Geometric mean         | (ref)                                                               | 1.04x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-darwin-arm64-python-main-3.12.0a7+-0fd3891 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 8.42 ms                                                             | 7.53 ms: 1.12x faster                                  |
| genshi_text     | 15.3 ms                                                             | 13.8 ms: 1.11x faster                                  |
| genshi_xml      | 29.9 ms                                                             | 28.3 ms: 1.06x faster                                  |
| django_template | 21.1 ms                                                             | 19.9 ms: 1.06x faster                                  |
| Geometric mean  | (ref)                                                               | 1.09x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-darwin-arm64-python-main-3.12.0a7+-0fd3891 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| asyncio_tcp             | 651 ms                                                              | 458 ms: 1.42x faster                                   |
| json_dumps              | 7.59 ms                                                             | 6.08 ms: 1.25x faster                                  |
| unpack_sequence         | 33.5 ns                                                             | 27.9 ns: 1.20x faster                                  |
| generators              | 28.6 ms                                                             | 24.6 ms: 1.16x faster                                  |
| deltablue               | 2.81 ms                                                             | 2.44 ms: 1.15x faster                                  |
| hexiom                  | 4.73 ms                                                             | 4.13 ms: 1.15x faster                                  |
| sqlglot_parse           | 956 us                                                              | 838 us: 1.14x faster                                   |
| coverage                | 58.4 ms                                                             | 51.7 ms: 1.13x faster                                  |
| chaos                   | 49.4 ms                                                             | 44.1 ms: 1.12x faster                                  |
| sqlglot_transpile       | 1.12 ms                                                             | 998 us: 1.12x faster                                   |
| mako                    | 8.42 ms                                                             | 7.53 ms: 1.12x faster                                  |
| genshi_text             | 15.3 ms                                                             | 13.8 ms: 1.11x faster                                  |
| nqueens                 | 62.4 ms                                                             | 56.4 ms: 1.11x faster                                  |
| unpickle_pure_python    | 158 us                                                              | 144 us: 1.10x faster                                   |
| fannkuch                | 260 ms                                                              | 238 ms: 1.09x faster                                   |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.94 ms: 1.09x faster                                  |
| regex_compile           | 76.6 ms                                                             | 70.8 ms: 1.08x faster                                  |
| pickle_pure_python      | 198 us                                                              | 184 us: 1.08x faster                                   |
| xml_etree_parse         | 106 ms                                                              | 98.4 ms: 1.08x faster                                  |
| nbody                   | 65.5 ms                                                             | 61.3 ms: 1.07x faster                                  |
| pycparser               | 695 ms                                                              | 654 ms: 1.06x faster                                   |
| async_tree_memoization  | 338 ms                                                              | 318 ms: 1.06x faster                                   |
| scimark_fft             | 200 ms                                                              | 188 ms: 1.06x faster                                   |
| pathlib                 | 28.3 ms                                                             | 26.7 ms: 1.06x faster                                  |
| genshi_xml              | 29.9 ms                                                             | 28.3 ms: 1.06x faster                                  |
| django_template         | 21.1 ms                                                             | 19.9 ms: 1.06x faster                                  |
| sqlalchemy_imperative   | 7.26 ms                                                             | 6.88 ms: 1.06x faster                                  |
| richards                | 32.2 ms                                                             | 30.7 ms: 1.05x faster                                  |
| create_gc_cycles        | 722 us                                                              | 688 us: 1.05x faster                                   |
| scimark_sor             | 82.9 ms                                                             | 79.2 ms: 1.05x faster                                  |
| pylint                  | 271 ms                                                              | 259 ms: 1.05x faster                                   |
| python_startup          | 12.3 ms                                                             | 11.8 ms: 1.05x faster                                  |
| dulwich_log             | 29.7 ms                                                             | 28.6 ms: 1.04x faster                                  |
| unpickle                | 9.66 us                                                             | 9.29 us: 1.04x faster                                  |
| deepcopy                | 224 us                                                              | 215 us: 1.04x faster                                   |
| python_startup_no_site  | 10.1 ms                                                             | 9.72 ms: 1.04x faster                                  |
| pprint_pformat          | 946 ms                                                              | 914 ms: 1.03x faster                                   |
| bench_thread_pool       | 474 us                                                              | 459 us: 1.03x faster                                   |
| async_tree_none         | 285 ms                                                              | 276 ms: 1.03x faster                                   |
| pprint_safe_repr        | 463 ms                                                              | 449 ms: 1.03x faster                                   |
| chameleon               | 4.55 ms                                                             | 4.42 ms: 1.03x faster                                  |
| sympy_str               | 151 ms                                                              | 147 ms: 1.03x faster                                   |
| go                      | 109 ms                                                              | 106 ms: 1.03x faster                                   |
| deepcopy_memo           | 26.3 us                                                             | 25.6 us: 1.03x faster                                  |
| logging_simple          | 3.49 us                                                             | 3.40 us: 1.03x faster                                  |
| logging_format          | 3.77 us                                                             | 3.67 us: 1.03x faster                                  |
| sympy_expand            | 243 ms                                                              | 237 ms: 1.03x faster                                   |
| coroutines              | 17.7 ms                                                             | 17.3 ms: 1.02x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.51 sec: 1.02x faster                                 |
| spectral_norm           | 72.5 ms                                                             | 71.4 ms: 1.02x faster                                  |
| deepcopy_reduce         | 1.91 us                                                             | 1.88 us: 1.01x faster                                  |
| sympy_sum               | 86.0 ms                                                             | 84.9 ms: 1.01x faster                                  |
| regex_v8                | 16.1 ms                                                             | 15.9 ms: 1.01x faster                                  |
| sqlalchemy_declarative  | 62.6 ms                                                             | 62.0 ms: 1.01x faster                                  |
| docutils                | 1.47 sec                                                            | 1.46 sec: 1.01x faster                                 |
| sqlglot_normalize       | 171 ms                                                              | 170 ms: 1.01x faster                                   |
| logging_silent          | 68.0 ns                                                             | 67.4 ns: 1.01x faster                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.4 ms: 1.01x faster                                  |
| async_tree_cpu_io_mixed | 534 ms                                                              | 531 ms: 1.01x faster                                   |
| regex_dna               | 151 ms                                                              | 151 ms: 1.00x faster                                   |
| comprehensions          | 16.1 us                                                             | 16.1 us: 1.00x faster                                  |
| 2to3                    | 161 ms                                                              | 161 ms: 1.00x faster                                   |
| pidigits                | 281 ms                                                              | 280 ms: 1.00x faster                                   |
| gc_traversal            | 2.41 ms                                                             | 2.42 ms: 1.00x slower                                  |
| sqlglot_optimize        | 31.2 ms                                                             | 31.3 ms: 1.00x slower                                  |
| async_tree_io           | 707 ms                                                              | 710 ms: 1.00x slower                                   |
| scimark_lu              | 72.2 ms                                                             | 72.5 ms: 1.01x slower                                  |
| regex_effbot            | 2.63 ms                                                             | 2.65 ms: 1.01x slower                                  |
| telco                   | 3.40 ms                                                             | 3.42 ms: 1.01x slower                                  |
| json_loads              | 16.0 us                                                             | 16.3 us: 1.01x slower                                  |
| json                    | 2.77 ms                                                             | 2.82 ms: 1.02x slower                                  |
| meteor_contest          | 73.3 ms                                                             | 74.6 ms: 1.02x slower                                  |
| xml_etree_process       | 35.0 ms                                                             | 35.7 ms: 1.02x slower                                  |
| pickle_list             | 2.83 us                                                             | 2.89 us: 1.02x slower                                  |
| crypto_pyaes            | 51.8 ms                                                             | 53.0 ms: 1.02x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.4 us: 1.03x slower                                  |
| thrift                  | 431 us                                                              | 450 us: 1.04x slower                                   |
| pickle                  | 7.17 us                                                             | 7.55 us: 1.05x slower                                  |
| pyflate                 | 309 ms                                                              | 326 ms: 1.05x slower                                   |
| xml_etree_generate      | 48.2 ms                                                             | 51.0 ms: 1.06x slower                                  |
| sqlite_synth            | 1.28 us                                                             | 1.36 us: 1.06x slower                                  |
| scimark_monte_carlo     | 46.5 ms                                                             | 49.5 ms: 1.07x slower                                  |
| raytrace                | 207 ms                                                              | 220 ms: 1.07x slower                                   |
| bench_mp_pool           | 43.8 ms                                                             | 46.8 ms: 1.07x slower                                  |
| async_generators        | 195 ms                                                              | 265 ms: 1.36x slower                                   |
| dask                    | 226 ms                                                              | 310 ms: 1.37x slower                                   |
| Geometric mean          | (ref)                                                               | 1.03x faster                                           |

Benchmark hidden because not significant (6): tornado_http, xml_etree_iterparse, float, unpickle_list, html5lib, mypy2
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn
