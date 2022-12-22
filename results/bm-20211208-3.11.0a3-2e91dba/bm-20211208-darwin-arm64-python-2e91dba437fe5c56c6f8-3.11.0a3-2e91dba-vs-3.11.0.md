Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.61 ms                                                             | 5.14 ms: 1.12x slower                                                 |
| docutils       | 1.46 sec                                                            | 1.56 sec: 1.06x slower                                                |
| html5lib       | 34.7 ms                                                             | 36.9 ms: 1.07x slower                                                 |
| tornado_http   | 70.6 ms                                                             | 79.7 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                               | 1.08x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 51.7 ms                                                             | 56.5 ms: 1.09x slower                                                 |
| nbody          | 65.2 ms                                                             | 65.2 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                               | 1.03x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 78.4 ms: 1.03x slower                                                 |
| regex_dna      | 151 ms                                                              | 163 ms: 1.07x slower                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.50 ms: 1.05x faster                                                 |
| regex_v8       | 16.5 ms                                                             | 18.0 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                               | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 7.91 ms: 1.03x slower                                                 |
| json_loads           | 16.1 us                                                             | 16.8 us: 1.04x slower                                                 |
| pickle               | 7.21 us                                                             | 7.42 us: 1.03x slower                                                 |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                                 |
| pickle_pure_python   | 200 us                                                              | 224 us: 1.12x slower                                                  |
| unpickle             | 9.68 us                                                             | 10.1 us: 1.05x slower                                                 |
| unpickle_list        | 2.64 us                                                             | 2.50 us: 1.05x faster                                                 |
| unpickle_pure_python | 159 us                                                              | 177 us: 1.11x slower                                                  |
| xml_etree_parse      | 99.6 ms                                                             | 96.5 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 65.6 ms                                                             | 67.2 ms: 1.03x slower                                                 |
| xml_etree_generate   | 48.4 ms                                                             | 49.9 ms: 1.03x slower                                                 |
| xml_etree_process    | 35.1 ms                                                             | 37.5 ms: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.03x slower                                                          |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 12.7 ms: 1.38x slower                                                 |
| python_startup_no_site | 7.24 ms                                                             | 6.93 ms: 1.04x faster                                                 |
| Geometric mean         | (ref)                                                               | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 23.1 ms: 1.10x slower                                                 |
| genshi_text     | 15.3 ms                                                             | 16.1 ms: 1.05x slower                                                 |
| genshi_xml      | 30.5 ms                                                             | 32.4 ms: 1.06x slower                                                 |
| mako            | 8.40 ms                                                             | 8.53 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 185 ms: 1.02x slower                                                  |
| async_generators        | 195 ms                                                              | 197 ms: 1.01x slower                                                  |
| async_tree_none         | 281 ms                                                              | 301 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 580 ms: 1.10x slower                                                  |
| async_tree_io           | 696 ms                                                              | 833 ms: 1.20x slower                                                  |
| async_tree_memoization  | 317 ms                                                              | 391 ms: 1.23x slower                                                  |
| chameleon               | 4.61 ms                                                             | 5.14 ms: 1.12x slower                                                 |
| chaos                   | 49.3 ms                                                             | 49.8 ms: 1.01x slower                                                 |
| bench_thread_pool       | 457 us                                                              | 501 us: 1.10x slower                                                  |
| coroutines              | 17.8 ms                                                             | 18.5 ms: 1.04x slower                                                 |
| coverage                | 58.4 ms                                                             | 45.2 ms: 1.29x faster                                                 |
| crypto_pyaes            | 51.7 ms                                                             | 59.6 ms: 1.15x slower                                                 |
| deepcopy                | 222 us                                                              | 240 us: 1.08x slower                                                  |
| deepcopy_reduce         | 1.90 us                                                             | 2.06 us: 1.09x slower                                                 |
| deepcopy_memo           | 26.2 us                                                             | 27.9 us: 1.07x slower                                                 |
| deltablue               | 2.82 ms                                                             | 3.12 ms: 1.11x slower                                                 |
| django_template         | 21.1 ms                                                             | 23.1 ms: 1.10x slower                                                 |
| docutils                | 1.46 sec                                                            | 1.56 sec: 1.06x slower                                                |
| dulwich_log             | 29.1 ms                                                             | 30.8 ms: 1.06x slower                                                 |
| fannkuch                | 262 ms                                                              | 269 ms: 1.03x slower                                                  |
| flaskblogging           | 2.29 ms                                                             | 2.79 ms: 1.22x slower                                                 |
| float                   | 51.7 ms                                                             | 56.5 ms: 1.09x slower                                                 |
| generators              | 28.4 ms                                                             | 27.3 ms: 1.04x faster                                                 |
| genshi_text             | 15.3 ms                                                             | 16.1 ms: 1.05x slower                                                 |
| genshi_xml              | 30.5 ms                                                             | 32.4 ms: 1.06x slower                                                 |
| go                      | 109 ms                                                              | 119 ms: 1.08x slower                                                  |
| hexiom                  | 4.73 ms                                                             | 4.74 ms: 1.00x slower                                                 |
| html5lib                | 34.7 ms                                                             | 36.9 ms: 1.07x slower                                                 |
| json                    | 2.83 ms                                                             | 3.04 ms: 1.07x slower                                                 |
| json_dumps              | 7.67 ms                                                             | 7.91 ms: 1.03x slower                                                 |
| json_loads              | 16.1 us                                                             | 16.8 us: 1.04x slower                                                 |
| logging_format          | 3.73 us                                                             | 3.83 us: 1.03x slower                                                 |
| logging_silent          | 67.4 ns                                                             | 81.8 ns: 1.21x slower                                                 |
| logging_simple          | 3.47 us                                                             | 3.51 us: 1.01x slower                                                 |
| mako                    | 8.40 ms                                                             | 8.53 ms: 1.02x slower                                                 |
| mdp                     | 1.54 sec                                                            | 1.58 sec: 1.02x slower                                                |
| meteor_contest          | 73.9 ms                                                             | 73.8 ms: 1.00x faster                                                 |
| nbody                   | 65.2 ms                                                             | 65.2 ms: 1.00x faster                                                 |
| nqueens                 | 59.5 ms                                                             | 60.7 ms: 1.02x slower                                                 |
| pathlib                 | 20.6 ms                                                             | 21.1 ms: 1.02x slower                                                 |
| pickle                  | 7.21 us                                                             | 7.42 us: 1.03x slower                                                 |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                                 |
| pickle_pure_python      | 200 us                                                              | 224 us: 1.12x slower                                                  |
| pprint_safe_repr        | 467 ms                                                              | 503 ms: 1.08x slower                                                  |
| pprint_pformat          | 953 ms                                                              | 1.03 sec: 1.08x slower                                                |
| pycparser               | 694 ms                                                              | 762 ms: 1.10x slower                                                  |
| pyflate                 | 313 ms                                                              | 347 ms: 1.11x slower                                                  |
| pylint                  | 265 ms                                                              | 280 ms: 1.06x slower                                                  |
| python_startup          | 9.19 ms                                                             | 12.7 ms: 1.38x slower                                                 |
| python_startup_no_site  | 7.24 ms                                                             | 6.93 ms: 1.04x faster                                                 |
| raytrace                | 207 ms                                                              | 228 ms: 1.10x slower                                                  |
| regex_compile           | 76.3 ms                                                             | 78.4 ms: 1.03x slower                                                 |
| regex_dna               | 151 ms                                                              | 163 ms: 1.07x slower                                                  |
| regex_effbot            | 2.63 ms                                                             | 2.50 ms: 1.05x faster                                                 |
| regex_v8                | 16.5 ms                                                             | 18.0 ms: 1.09x slower                                                 |
| richards                | 32.7 ms                                                             | 36.4 ms: 1.11x slower                                                 |
| scimark_fft             | 201 ms                                                              | 202 ms: 1.01x slower                                                  |
| scimark_lu              | 72.2 ms                                                             | 78.9 ms: 1.09x slower                                                 |
| scimark_monte_carlo     | 46.9 ms                                                             | 51.6 ms: 1.10x slower                                                 |
| scimark_sor             | 83.3 ms                                                             | 86.7 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.25 ms: 1.01x slower                                                 |
| spectral_norm           | 72.7 ms                                                             | 76.7 ms: 1.05x slower                                                 |
| sqlglot_parse           | 948 us                                                              | 1.30 ms: 1.38x slower                                                 |
| sqlglot_transpile       | 1.11 ms                                                             | 1.48 ms: 1.33x slower                                                 |
| sqlglot_optimize        | 31.3 ms                                                             | 34.5 ms: 1.10x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 180 ms: 1.05x slower                                                  |
| sqlite_synth            | 1.29 us                                                             | 1.39 us: 1.08x slower                                                 |
| sympy_expand            | 242 ms                                                              | 262 ms: 1.08x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 12.1 ms: 1.05x slower                                                 |
| sympy_sum               | 85.5 ms                                                             | 88.7 ms: 1.04x slower                                                 |
| sympy_str               | 151 ms                                                              | 161 ms: 1.07x slower                                                  |
| telco                   | 3.39 ms                                                             | 3.56 ms: 1.05x slower                                                 |
| thrift                  | 429 us                                                              | 474 us: 1.10x slower                                                  |
| tornado_http            | 70.6 ms                                                             | 79.7 ms: 1.13x slower                                                 |
| unpack_sequence         | 33.1 ns                                                             | 32.2 ns: 1.03x faster                                                 |
| unpickle                | 9.68 us                                                             | 10.1 us: 1.05x slower                                                 |
| unpickle_list           | 2.64 us                                                             | 2.50 us: 1.05x faster                                                 |
| unpickle_pure_python    | 159 us                                                              | 177 us: 1.11x slower                                                  |
| xml_etree_parse         | 99.6 ms                                                             | 96.5 ms: 1.03x faster                                                 |
| xml_etree_iterparse     | 65.6 ms                                                             | 67.2 ms: 1.03x slower                                                 |
| xml_etree_generate      | 48.4 ms                                                             | 49.9 ms: 1.03x slower                                                 |
| xml_etree_process       | 35.1 ms                                                             | 37.5 ms: 1.07x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.06x slower                                                          |

Benchmark hidden because not significant (3): bench_mp_pool, pickle_list, pidigits
Ignored benchmarks (5) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy, sqlalchemy_declarative, sqlalchemy_imperative
