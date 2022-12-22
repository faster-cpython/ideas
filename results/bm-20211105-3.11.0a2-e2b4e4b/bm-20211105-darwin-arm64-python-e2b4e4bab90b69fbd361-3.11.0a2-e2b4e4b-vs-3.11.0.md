Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 186 ms: 1.03x slower                                                  |
| chameleon      | 4.61 ms                                                             | 5.09 ms: 1.10x slower                                                 |
| docutils       | 1.46 sec                                                            | 1.53 sec: 1.05x slower                                                |
| html5lib       | 34.7 ms                                                             | 36.5 ms: 1.05x slower                                                 |
| tornado_http   | 70.6 ms                                                             | 75.9 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                               | 1.06x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 74.0 ms: 1.13x slower                                                 |
| pidigits       | 282 ms                                                              | 282 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                               | 1.04x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 77.9 ms: 1.02x slower                                                 |
| regex_dna      | 151 ms                                                              | 164 ms: 1.09x slower                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.47 ms: 1.07x faster                                                 |
| regex_v8       | 16.5 ms                                                             | 18.1 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                               | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 7.80 ms: 1.02x slower                                                 |
| json_loads           | 16.1 us                                                             | 16.8 us: 1.04x slower                                                 |
| pickle               | 7.21 us                                                             | 7.28 us: 1.01x slower                                                 |
| pickle_dict          | 17.9 us                                                             | 17.7 us: 1.02x faster                                                 |
| pickle_list          | 2.86 us                                                             | 2.84 us: 1.01x faster                                                 |
| pickle_pure_python   | 200 us                                                              | 227 us: 1.14x slower                                                  |
| unpickle             | 9.68 us                                                             | 10.0 us: 1.03x slower                                                 |
| unpickle_list        | 2.64 us                                                             | 2.52 us: 1.04x faster                                                 |
| unpickle_pure_python | 159 us                                                              | 174 us: 1.09x slower                                                  |
| xml_etree_parse      | 99.6 ms                                                             | 95.7 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 65.6 ms                                                             | 66.5 ms: 1.01x slower                                                 |
| xml_etree_generate   | 48.4 ms                                                             | 48.7 ms: 1.01x slower                                                 |
| xml_etree_process    | 35.1 ms                                                             | 36.8 ms: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.02x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 13.6 ms: 1.48x slower                                                 |
| python_startup_no_site | 7.24 ms                                                             | 7.30 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.22x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 22.7 ms: 1.08x slower                                                 |
| genshi_text     | 15.3 ms                                                             | 15.7 ms: 1.02x slower                                                 |
| genshi_xml      | 30.5 ms                                                             | 31.1 ms: 1.02x slower                                                 |
| mako            | 8.40 ms                                                             | 8.49 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.03x slower                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 186 ms: 1.03x slower                                                  |
| async_generators        | 195 ms                                                              | 197 ms: 1.01x slower                                                  |
| async_tree_none         | 281 ms                                                              | 290 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 579 ms: 1.10x slower                                                  |
| async_tree_io           | 696 ms                                                              | 779 ms: 1.12x slower                                                  |
| async_tree_memoization  | 317 ms                                                              | 360 ms: 1.14x slower                                                  |
| chameleon               | 4.61 ms                                                             | 5.09 ms: 1.10x slower                                                 |
| chaos                   | 49.3 ms                                                             | 49.0 ms: 1.01x faster                                                 |
| bench_mp_pool           | 41.4 ms                                                             | 39.9 ms: 1.04x faster                                                 |
| bench_thread_pool       | 457 us                                                              | 496 us: 1.08x slower                                                  |
| coroutines              | 17.8 ms                                                             | 19.2 ms: 1.08x slower                                                 |
| coverage                | 58.4 ms                                                             | 43.0 ms: 1.36x faster                                                 |
| crypto_pyaes            | 51.7 ms                                                             | 58.1 ms: 1.12x slower                                                 |
| deepcopy                | 222 us                                                              | 237 us: 1.07x slower                                                  |
| deepcopy_reduce         | 1.90 us                                                             | 2.04 us: 1.07x slower                                                 |
| deepcopy_memo           | 26.2 us                                                             | 27.8 us: 1.06x slower                                                 |
| deltablue               | 2.82 ms                                                             | 3.19 ms: 1.13x slower                                                 |
| django_template         | 21.1 ms                                                             | 22.7 ms: 1.08x slower                                                 |
| docutils                | 1.46 sec                                                            | 1.53 sec: 1.05x slower                                                |
| dulwich_log             | 29.1 ms                                                             | 30.0 ms: 1.03x slower                                                 |
| fannkuch                | 262 ms                                                              | 280 ms: 1.07x slower                                                  |
| flaskblogging           | 2.29 ms                                                             | 2.76 ms: 1.20x slower                                                 |
| generators              | 28.4 ms                                                             | 28.2 ms: 1.00x faster                                                 |
| genshi_text             | 15.3 ms                                                             | 15.7 ms: 1.02x slower                                                 |
| genshi_xml              | 30.5 ms                                                             | 31.1 ms: 1.02x slower                                                 |
| go                      | 109 ms                                                              | 119 ms: 1.08x slower                                                  |
| hexiom                  | 4.73 ms                                                             | 4.91 ms: 1.04x slower                                                 |
| html5lib                | 34.7 ms                                                             | 36.5 ms: 1.05x slower                                                 |
| json                    | 2.83 ms                                                             | 3.03 ms: 1.07x slower                                                 |
| json_dumps              | 7.67 ms                                                             | 7.80 ms: 1.02x slower                                                 |
| json_loads              | 16.1 us                                                             | 16.8 us: 1.04x slower                                                 |
| logging_format          | 3.73 us                                                             | 3.72 us: 1.00x faster                                                 |
| logging_silent          | 67.4 ns                                                             | 82.6 ns: 1.23x slower                                                 |
| logging_simple          | 3.47 us                                                             | 3.45 us: 1.01x faster                                                 |
| mako                    | 8.40 ms                                                             | 8.49 ms: 1.01x slower                                                 |
| mdp                     | 1.54 sec                                                            | 1.56 sec: 1.02x slower                                                |
| meteor_contest          | 73.9 ms                                                             | 74.3 ms: 1.01x slower                                                 |
| nbody                   | 65.2 ms                                                             | 74.0 ms: 1.13x slower                                                 |
| nqueens                 | 59.5 ms                                                             | 61.3 ms: 1.03x slower                                                 |
| pickle                  | 7.21 us                                                             | 7.28 us: 1.01x slower                                                 |
| pickle_dict             | 17.9 us                                                             | 17.7 us: 1.02x faster                                                 |
| pickle_list             | 2.86 us                                                             | 2.84 us: 1.01x faster                                                 |
| pickle_pure_python      | 200 us                                                              | 227 us: 1.14x slower                                                  |
| pidigits                | 282 ms                                                              | 282 ms: 1.00x faster                                                  |
| pprint_safe_repr        | 467 ms                                                              | 500 ms: 1.07x slower                                                  |
| pprint_pformat          | 953 ms                                                              | 1.02 sec: 1.07x slower                                                |
| pycparser               | 694 ms                                                              | 766 ms: 1.10x slower                                                  |
| pyflate                 | 313 ms                                                              | 361 ms: 1.16x slower                                                  |
| pylint                  | 265 ms                                                              | 276 ms: 1.04x slower                                                  |
| python_startup          | 9.19 ms                                                             | 13.6 ms: 1.48x slower                                                 |
| python_startup_no_site  | 7.24 ms                                                             | 7.30 ms: 1.01x slower                                                 |
| raytrace                | 207 ms                                                              | 208 ms: 1.01x slower                                                  |
| regex_compile           | 76.3 ms                                                             | 77.9 ms: 1.02x slower                                                 |
| regex_dna               | 151 ms                                                              | 164 ms: 1.09x slower                                                  |
| regex_effbot            | 2.63 ms                                                             | 2.47 ms: 1.07x faster                                                 |
| regex_v8                | 16.5 ms                                                             | 18.1 ms: 1.10x slower                                                 |
| richards                | 32.7 ms                                                             | 37.4 ms: 1.14x slower                                                 |
| scimark_fft             | 201 ms                                                              | 202 ms: 1.01x slower                                                  |
| scimark_lu              | 72.2 ms                                                             | 93.9 ms: 1.30x slower                                                 |
| scimark_monte_carlo     | 46.9 ms                                                             | 48.8 ms: 1.04x slower                                                 |
| scimark_sor             | 83.3 ms                                                             | 98.8 ms: 1.19x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.24 ms: 1.01x slower                                                 |
| spectral_norm           | 72.7 ms                                                             | 75.0 ms: 1.03x slower                                                 |
| sqlglot_parse           | 948 us                                                              | 1.23 ms: 1.29x slower                                                 |
| sqlglot_transpile       | 1.11 ms                                                             | 1.40 ms: 1.26x slower                                                 |
| sqlglot_optimize        | 31.3 ms                                                             | 33.5 ms: 1.07x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 174 ms: 1.02x slower                                                  |
| sqlite_synth            | 1.29 us                                                             | 1.39 us: 1.08x slower                                                 |
| sympy_expand            | 242 ms                                                              | 254 ms: 1.05x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 12.1 ms: 1.06x slower                                                 |
| sympy_sum               | 85.5 ms                                                             | 86.0 ms: 1.01x slower                                                 |
| sympy_str               | 151 ms                                                              | 157 ms: 1.04x slower                                                  |
| telco                   | 3.39 ms                                                             | 3.40 ms: 1.00x slower                                                 |
| thrift                  | 429 us                                                              | 465 us: 1.08x slower                                                  |
| tornado_http            | 70.6 ms                                                             | 75.9 ms: 1.08x slower                                                 |
| unpack_sequence         | 33.1 ns                                                             | 31.2 ns: 1.06x faster                                                 |
| unpickle                | 9.68 us                                                             | 10.0 us: 1.03x slower                                                 |
| unpickle_list           | 2.64 us                                                             | 2.52 us: 1.04x faster                                                 |
| unpickle_pure_python    | 159 us                                                              | 174 us: 1.09x slower                                                  |
| xml_etree_parse         | 99.6 ms                                                             | 95.7 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 65.6 ms                                                             | 66.5 ms: 1.01x slower                                                 |
| xml_etree_generate      | 48.4 ms                                                             | 48.7 ms: 1.01x slower                                                 |
| xml_etree_process       | 35.1 ms                                                             | 36.8 ms: 1.05x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.05x slower                                                          |

Benchmark hidden because not significant (3): float, gunicorn, pathlib
Ignored benchmarks (4) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, mypy, sqlalchemy_declarative, sqlalchemy_imperative
