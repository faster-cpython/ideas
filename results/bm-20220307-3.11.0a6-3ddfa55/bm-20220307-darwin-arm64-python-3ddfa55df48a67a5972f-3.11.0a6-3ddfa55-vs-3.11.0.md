Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.61 ms                                                             | 4.64 ms: 1.01x slower                                                 |
| docutils       | 1.46 sec                                                            | 1.48 sec: 1.01x slower                                                |
| html5lib       | 34.7 ms                                                             | 33.3 ms: 1.04x faster                                                 |
| tornado_http   | 70.6 ms                                                             | 73.9 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                               | 1.01x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 51.7 ms                                                             | 53.8 ms: 1.04x slower                                                 |
| nbody          | 65.2 ms                                                             | 66.0 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                               | 1.02x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 76.1 ms: 1.00x faster                                                 |
| regex_dna      | 151 ms                                                              | 162 ms: 1.07x slower                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.45 ms: 1.07x faster                                                 |
| regex_v8       | 16.5 ms                                                             | 18.2 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                               | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle               | 7.21 us                                                             | 7.24 us: 1.00x slower                                                 |
| pickle_dict          | 17.9 us                                                             | 18.2 us: 1.01x slower                                                 |
| pickle_list          | 2.86 us                                                             | 2.83 us: 1.01x faster                                                 |
| pickle_pure_python   | 200 us                                                              | 205 us: 1.03x slower                                                  |
| unpickle             | 9.68 us                                                             | 9.95 us: 1.03x slower                                                 |
| unpickle_pure_python | 159 us                                                              | 169 us: 1.06x slower                                                  |
| xml_etree_parse      | 99.6 ms                                                             | 95.4 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 65.6 ms                                                             | 64.8 ms: 1.01x faster                                                 |
| xml_etree_generate   | 48.4 ms                                                             | 48.0 ms: 1.01x faster                                                 |
| xml_etree_process    | 35.1 ms                                                             | 35.7 ms: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (3): json_dumps, json_loads, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 12.9 ms: 1.40x slower                                                 |
| python_startup_no_site | 7.24 ms                                                             | 7.12 ms: 1.02x faster                                                 |
| Geometric mean         | (ref)                                                               | 1.18x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 22.2 ms: 1.05x slower                                                 |
| genshi_text     | 15.3 ms                                                             | 15.0 ms: 1.02x faster                                                 |
| genshi_xml      | 30.5 ms                                                             | 31.6 ms: 1.04x slower                                                 |
| mako            | 8.40 ms                                                             | 7.66 ms: 1.10x faster                                                 |
| Geometric mean  | (ref)                                                               | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 185 ms: 1.02x slower                                                  |
| aiohttp                 | 1.06 ms                                                             | 1.01 ms: 1.05x faster                                                 |
| async_tree_none         | 281 ms                                                              | 284 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 538 ms: 1.02x slower                                                  |
| async_tree_io           | 696 ms                                                              | 701 ms: 1.01x slower                                                  |
| async_tree_memoization  | 317 ms                                                              | 376 ms: 1.19x slower                                                  |
| chameleon               | 4.61 ms                                                             | 4.64 ms: 1.01x slower                                                 |
| chaos                   | 49.3 ms                                                             | 48.2 ms: 1.02x faster                                                 |
| bench_mp_pool           | 41.4 ms                                                             | 44.8 ms: 1.08x slower                                                 |
| bench_thread_pool       | 457 us                                                              | 495 us: 1.08x slower                                                  |
| coroutines              | 17.8 ms                                                             | 18.7 ms: 1.05x slower                                                 |
| coverage                | 58.4 ms                                                             | 50.4 ms: 1.16x faster                                                 |
| crypto_pyaes            | 51.7 ms                                                             | 57.2 ms: 1.11x slower                                                 |
| deepcopy                | 222 us                                                              | 232 us: 1.05x slower                                                  |
| deepcopy_reduce         | 1.90 us                                                             | 2.01 us: 1.06x slower                                                 |
| deepcopy_memo           | 26.2 us                                                             | 27.4 us: 1.05x slower                                                 |
| deltablue               | 2.82 ms                                                             | 2.97 ms: 1.05x slower                                                 |
| django_template         | 21.1 ms                                                             | 22.2 ms: 1.05x slower                                                 |
| docutils                | 1.46 sec                                                            | 1.48 sec: 1.01x slower                                                |
| dulwich_log             | 29.1 ms                                                             | 30.0 ms: 1.03x slower                                                 |
| fannkuch                | 262 ms                                                              | 266 ms: 1.01x slower                                                  |
| flaskblogging           | 2.29 ms                                                             | 2.31 ms: 1.01x slower                                                 |
| float                   | 51.7 ms                                                             | 53.8 ms: 1.04x slower                                                 |
| generators              | 28.4 ms                                                             | 29.0 ms: 1.02x slower                                                 |
| genshi_text             | 15.3 ms                                                             | 15.0 ms: 1.02x faster                                                 |
| genshi_xml              | 30.5 ms                                                             | 31.6 ms: 1.04x slower                                                 |
| go                      | 109 ms                                                              | 109 ms: 1.01x faster                                                  |
| hexiom                  | 4.73 ms                                                             | 4.66 ms: 1.01x faster                                                 |
| html5lib                | 34.7 ms                                                             | 33.3 ms: 1.04x faster                                                 |
| logging_format          | 3.73 us                                                             | 3.31 us: 1.13x faster                                                 |
| logging_silent          | 67.4 ns                                                             | 73.9 ns: 1.10x slower                                                 |
| logging_simple          | 3.47 us                                                             | 3.03 us: 1.14x faster                                                 |
| mako                    | 8.40 ms                                                             | 7.66 ms: 1.10x faster                                                 |
| mdp                     | 1.54 sec                                                            | 1.58 sec: 1.02x slower                                                |
| meteor_contest          | 73.9 ms                                                             | 74.3 ms: 1.00x slower                                                 |
| nbody                   | 65.2 ms                                                             | 66.0 ms: 1.01x slower                                                 |
| nqueens                 | 59.5 ms                                                             | 61.2 ms: 1.03x slower                                                 |
| pickle                  | 7.21 us                                                             | 7.24 us: 1.00x slower                                                 |
| pickle_dict             | 17.9 us                                                             | 18.2 us: 1.01x slower                                                 |
| pickle_list             | 2.86 us                                                             | 2.83 us: 1.01x faster                                                 |
| pickle_pure_python      | 200 us                                                              | 205 us: 1.03x slower                                                  |
| pprint_safe_repr        | 467 ms                                                              | 490 ms: 1.05x slower                                                  |
| pprint_pformat          | 953 ms                                                              | 998 ms: 1.05x slower                                                  |
| pycparser               | 694 ms                                                              | 739 ms: 1.06x slower                                                  |
| pyflate                 | 313 ms                                                              | 325 ms: 1.04x slower                                                  |
| pylint                  | 265 ms                                                              | 276 ms: 1.04x slower                                                  |
| python_startup          | 9.19 ms                                                             | 12.9 ms: 1.40x slower                                                 |
| python_startup_no_site  | 7.24 ms                                                             | 7.12 ms: 1.02x faster                                                 |
| raytrace                | 207 ms                                                              | 216 ms: 1.04x slower                                                  |
| regex_compile           | 76.3 ms                                                             | 76.1 ms: 1.00x faster                                                 |
| regex_dna               | 151 ms                                                              | 162 ms: 1.07x slower                                                  |
| regex_effbot            | 2.63 ms                                                             | 2.45 ms: 1.07x faster                                                 |
| regex_v8                | 16.5 ms                                                             | 18.2 ms: 1.10x slower                                                 |
| richards                | 32.7 ms                                                             | 33.4 ms: 1.02x slower                                                 |
| scimark_fft             | 201 ms                                                              | 203 ms: 1.01x slower                                                  |
| scimark_lu              | 72.2 ms                                                             | 74.7 ms: 1.03x slower                                                 |
| scimark_monte_carlo     | 46.9 ms                                                             | 51.3 ms: 1.09x slower                                                 |
| scimark_sor             | 83.3 ms                                                             | 80.0 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.25 ms: 1.01x slower                                                 |
| spectral_norm           | 72.7 ms                                                             | 76.6 ms: 1.05x slower                                                 |
| sqlalchemy_declarative  | 62.4 ms                                                             | 64.4 ms: 1.03x slower                                                 |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.49 ms: 1.04x slower                                                 |
| sqlglot_parse           | 948 us                                                              | 1.18 ms: 1.24x slower                                                 |
| sqlglot_transpile       | 1.11 ms                                                             | 1.35 ms: 1.22x slower                                                 |
| sqlglot_optimize        | 31.3 ms                                                             | 32.9 ms: 1.05x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 175 ms: 1.03x slower                                                  |
| sqlite_synth            | 1.29 us                                                             | 1.30 us: 1.01x slower                                                 |
| sympy_expand            | 242 ms                                                              | 250 ms: 1.03x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.5 ms: 1.00x slower                                                 |
| sympy_sum               | 85.5 ms                                                             | 84.9 ms: 1.01x faster                                                 |
| sympy_str               | 151 ms                                                              | 152 ms: 1.01x slower                                                  |
| telco                   | 3.39 ms                                                             | 3.51 ms: 1.04x slower                                                 |
| thrift                  | 429 us                                                              | 446 us: 1.04x slower                                                  |
| tornado_http            | 70.6 ms                                                             | 73.9 ms: 1.05x slower                                                 |
| unpack_sequence         | 33.1 ns                                                             | 90.4 ns: 2.73x slower                                                 |
| unpickle                | 9.68 us                                                             | 9.95 us: 1.03x slower                                                 |
| unpickle_pure_python    | 159 us                                                              | 169 us: 1.06x slower                                                  |
| xml_etree_parse         | 99.6 ms                                                             | 95.4 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 65.6 ms                                                             | 64.8 ms: 1.01x faster                                                 |
| xml_etree_generate      | 48.4 ms                                                             | 48.0 ms: 1.01x faster                                                 |
| xml_etree_process       | 35.1 ms                                                             | 35.7 ms: 1.02x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.04x slower                                                          |

Benchmark hidden because not significant (8): async_generators, gunicorn, json, json_dumps, json_loads, pathlib, pidigits, unpickle_list
Ignored benchmarks (1) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: mypy
