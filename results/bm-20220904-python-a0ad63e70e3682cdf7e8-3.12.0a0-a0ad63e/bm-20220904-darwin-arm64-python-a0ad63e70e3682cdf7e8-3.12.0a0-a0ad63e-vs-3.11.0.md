Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.61 ms                                                             | 4.59 ms: 1.00x faster                                                 |
| docutils       | 1.46 sec                                                            | 1.48 sec: 1.01x slower                                                |
| html5lib       | 34.7 ms                                                             | 36.4 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 51.7 ms                                                             | 51.3 ms: 1.01x faster                                                 |
| nbody          | 65.2 ms                                                             | 64.0 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                               | 1.01x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 75.3 ms: 1.01x faster                                                 |
| regex_effbot   | 2.63 ms                                                             | 2.72 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                               | 1.00x slower                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.10 ms: 1.26x faster                                                 |
| json_loads           | 16.1 us                                                             | 16.2 us: 1.00x slower                                                 |
| pickle               | 7.21 us                                                             | 7.59 us: 1.05x slower                                                 |
| pickle_pure_python   | 200 us                                                              | 198 us: 1.01x faster                                                  |
| unpickle_list        | 2.64 us                                                             | 2.58 us: 1.02x faster                                                 |
| unpickle_pure_python | 159 us                                                              | 160 us: 1.00x slower                                                  |
| xml_etree_parse      | 99.6 ms                                                             | 95.9 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 65.6 ms                                                             | 64.5 ms: 1.02x faster                                                 |
| xml_etree_generate   | 48.4 ms                                                             | 47.2 ms: 1.03x faster                                                 |
| xml_etree_process    | 35.1 ms                                                             | 34.5 ms: 1.02x faster                                                 |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                          |

Benchmark hidden because not significant (3): pickle_dict, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.07 ms: 1.01x faster                                                 |
| python_startup_no_site | 7.24 ms                                                             | 7.16 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                               | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 20.9 ms: 1.01x faster                                                 |
| genshi_text     | 15.3 ms                                                             | 15.1 ms: 1.01x faster                                                 |
| genshi_xml      | 30.5 ms                                                             | 29.9 ms: 1.02x faster                                                 |
| mako            | 8.40 ms                                                             | 7.97 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                               | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 185 ms: 1.02x slower                                                  |
| async_generators        | 195 ms                                                              | 199 ms: 1.02x slower                                                  |
| async_tree_none         | 281 ms                                                              | 284 ms: 1.01x slower                                                  |
| async_tree_io           | 696 ms                                                              | 734 ms: 1.05x slower                                                  |
| async_tree_memoization  | 317 ms                                                              | 381 ms: 1.20x slower                                                  |
| chameleon               | 4.61 ms                                                             | 4.59 ms: 1.00x faster                                                 |
| chaos                   | 49.3 ms                                                             | 49.5 ms: 1.00x slower                                                 |
| bench_thread_pool       | 457 us                                                              | 449 us: 1.02x faster                                                  |
| coroutines              | 17.8 ms                                                             | 19.3 ms: 1.09x slower                                                 |
| coverage                | 58.4 ms                                                             | 54.3 ms: 1.07x faster                                                 |
| crypto_pyaes            | 51.7 ms                                                             | 51.1 ms: 1.01x faster                                                 |
| deepcopy                | 222 us                                                              | 215 us: 1.03x faster                                                  |
| deepcopy_reduce         | 1.90 us                                                             | 1.85 us: 1.03x faster                                                 |
| deepcopy_memo           | 26.2 us                                                             | 24.8 us: 1.06x faster                                                 |
| deltablue               | 2.82 ms                                                             | 2.84 ms: 1.01x slower                                                 |
| django_template         | 21.1 ms                                                             | 20.9 ms: 1.01x faster                                                 |
| docutils                | 1.46 sec                                                            | 1.48 sec: 1.01x slower                                                |
| dulwich_log             | 29.1 ms                                                             | 29.5 ms: 1.01x slower                                                 |
| fannkuch                | 262 ms                                                              | 268 ms: 1.02x slower                                                  |
| flaskblogging           | 2.29 ms                                                             | 2.22 ms: 1.03x faster                                                 |
| float                   | 51.7 ms                                                             | 51.3 ms: 1.01x faster                                                 |
| generators              | 28.4 ms                                                             | 29.1 ms: 1.03x slower                                                 |
| genshi_text             | 15.3 ms                                                             | 15.1 ms: 1.01x faster                                                 |
| genshi_xml              | 30.5 ms                                                             | 29.9 ms: 1.02x faster                                                 |
| go                      | 109 ms                                                              | 117 ms: 1.07x slower                                                  |
| hexiom                  | 4.73 ms                                                             | 4.84 ms: 1.02x slower                                                 |
| html5lib                | 34.7 ms                                                             | 36.4 ms: 1.05x slower                                                 |
| json_dumps              | 7.67 ms                                                             | 6.10 ms: 1.26x faster                                                 |
| json_loads              | 16.1 us                                                             | 16.2 us: 1.00x slower                                                 |
| logging_format          | 3.73 us                                                             | 3.92 us: 1.05x slower                                                 |
| logging_silent          | 67.4 ns                                                             | 64.5 ns: 1.05x faster                                                 |
| logging_simple          | 3.47 us                                                             | 3.63 us: 1.05x slower                                                 |
| mako                    | 8.40 ms                                                             | 7.97 ms: 1.05x faster                                                 |
| mdp                     | 1.54 sec                                                            | 1.55 sec: 1.01x slower                                                |
| meteor_contest          | 73.9 ms                                                             | 77.0 ms: 1.04x slower                                                 |
| nbody                   | 65.2 ms                                                             | 64.0 ms: 1.02x faster                                                 |
| nqueens                 | 59.5 ms                                                             | 58.7 ms: 1.01x faster                                                 |
| pickle                  | 7.21 us                                                             | 7.59 us: 1.05x slower                                                 |
| pickle_pure_python      | 200 us                                                              | 198 us: 1.01x faster                                                  |
| pprint_pformat          | 953 ms                                                              | 949 ms: 1.00x faster                                                  |
| pycparser               | 694 ms                                                              | 711 ms: 1.02x slower                                                  |
| pyflate                 | 313 ms                                                              | 345 ms: 1.10x slower                                                  |
| python_startup          | 9.19 ms                                                             | 9.07 ms: 1.01x faster                                                 |
| python_startup_no_site  | 7.24 ms                                                             | 7.16 ms: 1.01x faster                                                 |
| raytrace                | 207 ms                                                              | 211 ms: 1.02x slower                                                  |
| regex_compile           | 76.3 ms                                                             | 75.3 ms: 1.01x faster                                                 |
| regex_effbot            | 2.63 ms                                                             | 2.72 ms: 1.04x slower                                                 |
| richards                | 32.7 ms                                                             | 33.4 ms: 1.02x slower                                                 |
| scimark_fft             | 201 ms                                                              | 197 ms: 1.02x faster                                                  |
| scimark_lu              | 72.2 ms                                                             | 72.7 ms: 1.01x slower                                                 |
| scimark_monte_carlo     | 46.9 ms                                                             | 53.8 ms: 1.15x slower                                                 |
| scimark_sor             | 83.3 ms                                                             | 99.0 ms: 1.19x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.80 ms: 1.14x faster                                                 |
| spectral_norm           | 72.7 ms                                                             | 71.7 ms: 1.01x faster                                                 |
| sqlalchemy_declarative  | 62.4 ms                                                             | 61.5 ms: 1.01x faster                                                 |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.12 ms: 1.01x faster                                                 |
| sqlglot_parse           | 948 us                                                              | 1.00 ms: 1.06x slower                                                 |
| sqlglot_transpile       | 1.11 ms                                                             | 1.16 ms: 1.05x slower                                                 |
| sqlglot_optimize        | 31.3 ms                                                             | 31.7 ms: 1.01x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 172 ms: 1.00x slower                                                  |
| sqlite_synth            | 1.29 us                                                             | 1.40 us: 1.08x slower                                                 |
| sympy_expand            | 242 ms                                                              | 247 ms: 1.02x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.5 ms: 1.00x faster                                                 |
| sympy_sum               | 85.5 ms                                                             | 84.0 ms: 1.02x faster                                                 |
| sympy_str               | 151 ms                                                              | 152 ms: 1.01x slower                                                  |
| telco                   | 3.39 ms                                                             | 3.34 ms: 1.01x faster                                                 |
| thrift                  | 429 us                                                              | 441 us: 1.03x slower                                                  |
| unpack_sequence         | 33.1 ns                                                             | 33.0 ns: 1.00x faster                                                 |
| unpickle_list           | 2.64 us                                                             | 2.58 us: 1.02x faster                                                 |
| unpickle_pure_python    | 159 us                                                              | 160 us: 1.00x slower                                                  |
| xml_etree_parse         | 99.6 ms                                                             | 95.9 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 65.6 ms                                                             | 64.5 ms: 1.02x faster                                                 |
| xml_etree_generate      | 48.4 ms                                                             | 47.2 ms: 1.03x faster                                                 |
| xml_etree_process       | 35.1 ms                                                             | 34.5 ms: 1.02x faster                                                 |
| Geometric mean          | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (14): async_tree_cpu_io_mixed, bench_mp_pool, json, mypy, pathlib, pickle_dict, pickle_list, pidigits, pprint_safe_repr, pylint, regex_dna, regex_v8, tornado_http, unpickle
Ignored benchmarks (2) of public/results/bm-20221024-python-deaf509e8fc6e0363bd6-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn
