Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 222 ms: 1.23x slower                                   |
| chameleon      | 4.61 ms                                                             | 5.86 ms: 1.27x slower                                  |
| docutils       | 1.46 sec                                                            | 1.76 sec: 1.21x slower                                 |
| html5lib       | 34.7 ms                                                             | 44.0 ms: 1.27x slower                                  |
| tornado_http   | 70.6 ms                                                             | 90.1 ms: 1.28x slower                                  |
| Geometric mean | (ref)                                                               | 1.25x slower                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 51.7 ms                                                             | 72.1 ms: 1.39x slower                                  |
| nbody          | 65.2 ms                                                             | 94.6 ms: 1.45x slower                                  |
| pidigits       | 282 ms                                                              | 284 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                               | 1.27x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 96.2 ms: 1.26x slower                                  |
| regex_dna      | 151 ms                                                              | 164 ms: 1.09x slower                                   |
| regex_effbot   | 2.63 ms                                                             | 2.45 ms: 1.07x faster                                  |
| regex_v8       | 16.5 ms                                                             | 17.7 ms: 1.08x slower                                  |
| Geometric mean | (ref)                                                               | 1.08x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 8.34 ms: 1.09x slower                                  |
| json_loads           | 16.1 us                                                             | 17.0 us: 1.05x slower                                  |
| pickle               | 7.21 us                                                             | 7.50 us: 1.04x slower                                  |
| pickle_list          | 2.86 us                                                             | 2.83 us: 1.01x faster                                  |
| pickle_pure_python   | 200 us                                                              | 284 us: 1.42x slower                                   |
| unpickle             | 9.68 us                                                             | 10.0 us: 1.04x slower                                  |
| unpickle_list        | 2.64 us                                                             | 2.66 us: 1.01x slower                                  |
| unpickle_pure_python | 159 us                                                              | 204 us: 1.28x slower                                   |
| xml_etree_parse      | 99.6 ms                                                             | 100 ms: 1.00x slower                                   |
| xml_etree_iterparse  | 65.6 ms                                                             | 69.0 ms: 1.05x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 54.5 ms: 1.13x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 45.1 ms: 1.28x slower                                  |
| Geometric mean       | (ref)                                                               | 1.10x slower                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.59 ms: 1.04x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.00 ms: 1.03x faster                                  |
| Geometric mean         | (ref)                                                               | 1.00x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 27.2 ms: 1.29x slower                                  |
| genshi_text     | 15.3 ms                                                             | 18.2 ms: 1.19x slower                                  |
| genshi_xml      | 30.5 ms                                                             | 37.7 ms: 1.24x slower                                  |
| mako            | 8.40 ms                                                             | 10.6 ms: 1.26x slower                                  |
| Geometric mean  | (ref)                                                               | 1.24x slower                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 222 ms: 1.23x slower                                   |
| aiohttp                 | 1.06 ms                                                             | 1.19 ms: 1.12x slower                                  |
| async_generators        | 195 ms                                                              | 231 ms: 1.18x slower                                   |
| async_tree_none         | 281 ms                                                              | 396 ms: 1.41x slower                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 665 ms: 1.26x slower                                   |
| async_tree_io           | 696 ms                                                              | 1.01 sec: 1.45x slower                                 |
| async_tree_memoization  | 317 ms                                                              | 485 ms: 1.53x slower                                   |
| chameleon               | 4.61 ms                                                             | 5.86 ms: 1.27x slower                                  |
| chaos                   | 49.3 ms                                                             | 66.5 ms: 1.35x slower                                  |
| bench_thread_pool       | 457 us                                                              | 531 us: 1.16x slower                                   |
| coroutines              | 17.8 ms                                                             | 20.1 ms: 1.13x slower                                  |
| coverage                | 58.4 ms                                                             | 40.8 ms: 1.43x faster                                  |
| crypto_pyaes            | 51.7 ms                                                             | 77.9 ms: 1.51x slower                                  |
| deepcopy                | 222 us                                                              | 278 us: 1.25x slower                                   |
| deepcopy_reduce         | 1.90 us                                                             | 2.36 us: 1.25x slower                                  |
| deepcopy_memo           | 26.2 us                                                             | 34.4 us: 1.31x slower                                  |
| deltablue               | 2.82 ms                                                             | 5.37 ms: 1.90x slower                                  |
| django_template         | 21.1 ms                                                             | 27.2 ms: 1.29x slower                                  |
| docutils                | 1.46 sec                                                            | 1.76 sec: 1.21x slower                                 |
| dulwich_log             | 29.1 ms                                                             | 36.4 ms: 1.25x slower                                  |
| fannkuch                | 262 ms                                                              | 318 ms: 1.21x slower                                   |
| flaskblogging           | 2.29 ms                                                             | 2.59 ms: 1.13x slower                                  |
| float                   | 51.7 ms                                                             | 72.1 ms: 1.39x slower                                  |
| generators              | 28.4 ms                                                             | 32.5 ms: 1.14x slower                                  |
| genshi_text             | 15.3 ms                                                             | 18.2 ms: 1.19x slower                                  |
| genshi_xml              | 30.5 ms                                                             | 37.7 ms: 1.24x slower                                  |
| go                      | 109 ms                                                              | 165 ms: 1.51x slower                                   |
| gunicorn                | 1.12 ms                                                             | 1.28 ms: 1.14x slower                                  |
| hexiom                  | 4.73 ms                                                             | 6.31 ms: 1.33x slower                                  |
| html5lib                | 34.7 ms                                                             | 44.0 ms: 1.27x slower                                  |
| json                    | 2.83 ms                                                             | 3.13 ms: 1.11x slower                                  |
| json_dumps              | 7.67 ms                                                             | 8.34 ms: 1.09x slower                                  |
| json_loads              | 16.1 us                                                             | 17.0 us: 1.05x slower                                  |
| logging_format          | 3.73 us                                                             | 4.95 us: 1.33x slower                                  |
| logging_silent          | 67.4 ns                                                             | 119 ns: 1.77x slower                                   |
| logging_simple          | 3.47 us                                                             | 4.61 us: 1.33x slower                                  |
| mako                    | 8.40 ms                                                             | 10.6 ms: 1.26x slower                                  |
| mdp                     | 1.54 sec                                                            | 1.66 sec: 1.08x slower                                 |
| meteor_contest          | 73.9 ms                                                             | 77.7 ms: 1.05x slower                                  |
| mypy                    | 421 ms                                                              | 521 ms: 1.24x slower                                   |
| nbody                   | 65.2 ms                                                             | 94.6 ms: 1.45x slower                                  |
| nqueens                 | 59.5 ms                                                             | 68.6 ms: 1.15x slower                                  |
| pathlib                 | 20.6 ms                                                             | 22.2 ms: 1.08x slower                                  |
| pickle                  | 7.21 us                                                             | 7.50 us: 1.04x slower                                  |
| pickle_list             | 2.86 us                                                             | 2.83 us: 1.01x faster                                  |
| pickle_pure_python      | 200 us                                                              | 284 us: 1.42x slower                                   |
| pidigits                | 282 ms                                                              | 284 ms: 1.01x slower                                   |
| pprint_safe_repr        | 467 ms                                                              | 608 ms: 1.30x slower                                   |
| pprint_pformat          | 953 ms                                                              | 1.24 sec: 1.30x slower                                 |
| pycparser               | 694 ms                                                              | 915 ms: 1.32x slower                                   |
| pyflate                 | 313 ms                                                              | 454 ms: 1.45x slower                                   |
| pylint                  | 265 ms                                                              | 302 ms: 1.14x slower                                   |
| python_startup          | 9.19 ms                                                             | 9.59 ms: 1.04x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.00 ms: 1.03x faster                                  |
| raytrace                | 207 ms                                                              | 329 ms: 1.59x slower                                   |
| regex_compile           | 76.3 ms                                                             | 96.2 ms: 1.26x slower                                  |
| regex_dna               | 151 ms                                                              | 164 ms: 1.09x slower                                   |
| regex_effbot            | 2.63 ms                                                             | 2.45 ms: 1.07x faster                                  |
| regex_v8                | 16.5 ms                                                             | 17.7 ms: 1.08x slower                                  |
| richards                | 32.7 ms                                                             | 51.4 ms: 1.57x slower                                  |
| scimark_fft             | 201 ms                                                              | 231 ms: 1.15x slower                                   |
| scimark_lu              | 72.2 ms                                                             | 110 ms: 1.52x slower                                   |
| scimark_monte_carlo     | 46.9 ms                                                             | 72.3 ms: 1.54x slower                                  |
| scimark_sor             | 83.3 ms                                                             | 126 ms: 1.51x slower                                   |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.47 ms: 1.08x slower                                  |
| spectral_norm           | 72.7 ms                                                             | 95.8 ms: 1.32x slower                                  |
| sqlalchemy_declarative  | 62.4 ms                                                             | 74.4 ms: 1.19x slower                                  |
| sqlalchemy_imperative   | 7.22 ms                                                             | 9.01 ms: 1.25x slower                                  |
| sqlglot_parse           | 948 us                                                              | 1.33 ms: 1.40x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.54 ms: 1.39x slower                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 38.1 ms: 1.22x slower                                  |
| sqlglot_normalize       | 171 ms                                                              | 198 ms: 1.16x slower                                   |
| sqlite_synth            | 1.29 us                                                             | 1.50 us: 1.16x slower                                  |
| sympy_expand            | 242 ms                                                              | 275 ms: 1.14x slower                                   |
| sympy_integrate         | 11.5 ms                                                             | 13.3 ms: 1.15x slower                                  |
| sympy_sum               | 85.5 ms                                                             | 93.5 ms: 1.09x slower                                  |
| sympy_str               | 151 ms                                                              | 169 ms: 1.12x slower                                   |
| telco                   | 3.39 ms                                                             | 3.63 ms: 1.07x slower                                  |
| thrift                  | 429 us                                                              | 577 us: 1.34x slower                                   |
| tornado_http            | 70.6 ms                                                             | 90.1 ms: 1.28x slower                                  |
| unpack_sequence         | 33.1 ns                                                             | 38.2 ns: 1.15x slower                                  |
| unpickle                | 9.68 us                                                             | 10.0 us: 1.04x slower                                  |
| unpickle_list           | 2.64 us                                                             | 2.66 us: 1.01x slower                                  |
| unpickle_pure_python    | 159 us                                                              | 204 us: 1.28x slower                                   |
| xml_etree_parse         | 99.6 ms                                                             | 100 ms: 1.00x slower                                   |
| xml_etree_iterparse     | 65.6 ms                                                             | 69.0 ms: 1.05x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 54.5 ms: 1.13x slower                                  |
| xml_etree_process       | 35.1 ms                                                             | 45.1 ms: 1.28x slower                                  |
| Geometric mean          | (ref)                                                               | 1.22x slower                                           |

Benchmark hidden because not significant (2): bench_mp_pool, pickle_dict
