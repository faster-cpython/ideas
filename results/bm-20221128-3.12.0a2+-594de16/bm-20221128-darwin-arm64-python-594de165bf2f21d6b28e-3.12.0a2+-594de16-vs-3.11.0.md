Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 186 ms: 1.02x slower                                                   |
| chameleon      | 4.61 ms                                                             | 4.64 ms: 1.01x slower                                                  |
| html5lib       | 34.7 ms                                                             | 36.1 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                               | 1.01x slower                                                           |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 51.7 ms                                                             | 56.4 ms: 1.09x slower                                                  |
| nbody          | 65.2 ms                                                             | 65.0 ms: 1.00x faster                                                  |
| pidigits       | 282 ms                                                              | 283 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                               | 1.03x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 75.9 ms: 1.01x faster                                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                   |
| regex_effbot   | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                                  |
| regex_v8       | 16.5 ms                                                             | 16.0 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                               | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.07 ms: 1.26x faster                                                  |
| json_loads           | 16.1 us                                                             | 16.4 us: 1.01x slower                                                  |
| pickle               | 7.21 us                                                             | 7.54 us: 1.05x slower                                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                                  |
| pickle_list          | 2.86 us                                                             | 2.85 us: 1.00x faster                                                  |
| pickle_pure_python   | 200 us                                                              | 210 us: 1.05x slower                                                   |
| unpickle             | 9.68 us                                                             | 9.84 us: 1.02x slower                                                  |
| unpickle_list        | 2.64 us                                                             | 2.59 us: 1.02x faster                                                  |
| unpickle_pure_python | 159 us                                                              | 161 us: 1.01x slower                                                   |
| xml_etree_parse      | 99.6 ms                                                             | 93.2 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 66.4 ms: 1.01x slower                                                  |
| xml_etree_generate   | 48.4 ms                                                             | 48.7 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.01x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.29 ms: 1.01x slower                                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.33 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.6 ms: 1.03x slower                                                  |
| genshi_text     | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                                  |
| genshi_xml      | 30.5 ms                                                             | 29.6 ms: 1.03x faster                                                  |
| mako            | 8.40 ms                                                             | 8.24 ms: 1.02x faster                                                  |
| Geometric mean  | (ref)                                                               | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 186 ms: 1.02x slower                                                   |
| async_generators        | 195 ms                                                              | 204 ms: 1.05x slower                                                   |
| async_tree_none         | 281 ms                                                              | 286 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 539 ms: 1.02x slower                                                   |
| async_tree_io           | 696 ms                                                              | 733 ms: 1.05x slower                                                   |
| async_tree_memoization  | 317 ms                                                              | 323 ms: 1.02x slower                                                   |
| chameleon               | 4.61 ms                                                             | 4.64 ms: 1.01x slower                                                  |
| chaos                   | 49.3 ms                                                             | 51.1 ms: 1.04x slower                                                  |
| bench_thread_pool       | 457 us                                                              | 456 us: 1.00x faster                                                   |
| coroutines              | 17.8 ms                                                             | 20.0 ms: 1.13x slower                                                  |
| crypto_pyaes            | 51.7 ms                                                             | 53.4 ms: 1.03x slower                                                  |
| deepcopy                | 222 us                                                              | 240 us: 1.08x slower                                                   |
| deepcopy_reduce         | 1.90 us                                                             | 2.04 us: 1.07x slower                                                  |
| deepcopy_memo           | 26.2 us                                                             | 29.5 us: 1.13x slower                                                  |
| deltablue               | 2.82 ms                                                             | 2.81 ms: 1.01x faster                                                  |
| django_template         | 21.1 ms                                                             | 21.6 ms: 1.03x slower                                                  |
| dulwich_log             | 29.1 ms                                                             | 29.3 ms: 1.01x slower                                                  |
| fannkuch                | 262 ms                                                              | 276 ms: 1.05x slower                                                   |
| float                   | 51.7 ms                                                             | 56.4 ms: 1.09x slower                                                  |
| generators              | 28.4 ms                                                             | 34.1 ms: 1.20x slower                                                  |
| genshi_text             | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                                  |
| genshi_xml              | 30.5 ms                                                             | 29.6 ms: 1.03x faster                                                  |
| go                      | 109 ms                                                              | 118 ms: 1.08x slower                                                   |
| hexiom                  | 4.73 ms                                                             | 4.93 ms: 1.04x slower                                                  |
| html5lib                | 34.7 ms                                                             | 36.1 ms: 1.04x slower                                                  |
| json                    | 2.83 ms                                                             | 2.86 ms: 1.01x slower                                                  |
| json_dumps              | 7.67 ms                                                             | 6.07 ms: 1.26x faster                                                  |
| json_loads              | 16.1 us                                                             | 16.4 us: 1.01x slower                                                  |
| logging_format          | 3.73 us                                                             | 3.91 us: 1.05x slower                                                  |
| logging_silent          | 67.4 ns                                                             | 64.4 ns: 1.05x faster                                                  |
| logging_simple          | 3.47 us                                                             | 3.62 us: 1.05x slower                                                  |
| mako                    | 8.40 ms                                                             | 8.24 ms: 1.02x faster                                                  |
| meteor_contest          | 73.9 ms                                                             | 77.2 ms: 1.04x slower                                                  |
| nbody                   | 65.2 ms                                                             | 65.0 ms: 1.00x faster                                                  |
| nqueens                 | 59.5 ms                                                             | 61.9 ms: 1.04x slower                                                  |
| pickle                  | 7.21 us                                                             | 7.54 us: 1.05x slower                                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                                  |
| pickle_list             | 2.86 us                                                             | 2.85 us: 1.00x faster                                                  |
| pickle_pure_python      | 200 us                                                              | 210 us: 1.05x slower                                                   |
| pidigits                | 282 ms                                                              | 283 ms: 1.00x slower                                                   |
| pprint_safe_repr        | 467 ms                                                              | 491 ms: 1.05x slower                                                   |
| pprint_pformat          | 953 ms                                                              | 1.00 sec: 1.05x slower                                                 |
| pycparser               | 694 ms                                                              | 702 ms: 1.01x slower                                                   |
| pyflate                 | 313 ms                                                              | 356 ms: 1.14x slower                                                   |
| python_startup          | 9.19 ms                                                             | 9.29 ms: 1.01x slower                                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.33 ms: 1.01x slower                                                  |
| raytrace                | 207 ms                                                              | 220 ms: 1.06x slower                                                   |
| regex_compile           | 76.3 ms                                                             | 75.9 ms: 1.01x faster                                                  |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                   |
| regex_effbot            | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                                  |
| regex_v8                | 16.5 ms                                                             | 16.0 ms: 1.03x faster                                                  |
| richards                | 32.7 ms                                                             | 31.3 ms: 1.05x faster                                                  |
| scimark_fft             | 201 ms                                                              | 198 ms: 1.01x faster                                                   |
| scimark_lu              | 72.2 ms                                                             | 71.0 ms: 1.02x faster                                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 56.3 ms: 1.20x slower                                                  |
| scimark_sor             | 83.3 ms                                                             | 99.3 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.83 ms: 1.13x faster                                                  |
| spectral_norm           | 72.7 ms                                                             | 73.7 ms: 1.01x slower                                                  |
| sqlglot_parse           | 948 us                                                              | 996 us: 1.05x slower                                                   |
| sqlglot_transpile       | 1.11 ms                                                             | 1.17 ms: 1.05x slower                                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 31.6 ms: 1.01x slower                                                  |
| sqlglot_normalize       | 171 ms                                                              | 173 ms: 1.01x slower                                                   |
| sqlite_synth            | 1.29 us                                                             | 1.43 us: 1.11x slower                                                  |
| sympy_expand            | 242 ms                                                              | 247 ms: 1.02x slower                                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.8 ms: 1.02x slower                                                  |
| sympy_sum               | 85.5 ms                                                             | 86.6 ms: 1.01x slower                                                  |
| sympy_str               | 151 ms                                                              | 155 ms: 1.02x slower                                                   |
| telco                   | 3.39 ms                                                             | 3.43 ms: 1.01x slower                                                  |
| thrift                  | 429 us                                                              | 438 us: 1.02x slower                                                   |
| unpack_sequence         | 33.1 ns                                                             | 62.7 ns: 1.89x slower                                                  |
| unpickle                | 9.68 us                                                             | 9.84 us: 1.02x slower                                                  |
| unpickle_list           | 2.64 us                                                             | 2.59 us: 1.02x faster                                                  |
| unpickle_pure_python    | 159 us                                                              | 161 us: 1.01x slower                                                   |
| xml_etree_parse         | 99.6 ms                                                             | 93.2 ms: 1.07x faster                                                  |
| xml_etree_iterparse     | 65.6 ms                                                             | 66.4 ms: 1.01x slower                                                  |
| xml_etree_generate      | 48.4 ms                                                             | 48.7 ms: 1.01x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.03x slower                                                           |

Benchmark hidden because not significant (8): bench_mp_pool, coverage, docutils, mdp, mypy, pathlib, tornado_http, xml_etree_process
Ignored benchmarks (6) of public/results/bm-20221024-python-deaf509e8fc6e0363bd6-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
