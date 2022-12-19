Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 223 ms: 1.22x slower                                                |
| chameleon      | 4.73 ms                                                               | 5.83 ms: 1.23x slower                                               |
| docutils       | 1.46 sec                                                              | 1.77 sec: 1.21x slower                                              |
| html5lib       | 35.8 ms                                                               | 46.5 ms: 1.30x slower                                               |
| tornado_http   | 69.7 ms                                                               | 93.5 ms: 1.34x slower                                               |
| Geometric mean | (ref)                                                                 | 1.26x slower                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 72.1 ms: 1.29x slower                                               |
| nbody          | 63.8 ms                                                               | 92.6 ms: 1.45x slower                                               |
| pidigits       | 282 ms                                                                | 284 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                 | 1.24x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 96.5 ms: 1.24x slower                                               |
| regex_dna      | 149 ms                                                                | 180 ms: 1.21x slower                                                |
| regex_effbot   | 2.40 ms                                                               | 2.64 ms: 1.10x slower                                               |
| regex_v8       | 16.8 ms                                                               | 18.3 ms: 1.09x slower                                               |
| Geometric mean | (ref)                                                                 | 1.16x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 8.25 ms: 1.07x slower                                               |
| json_loads           | 16.4 us                                                               | 17.0 us: 1.04x slower                                               |
| pickle               | 7.14 us                                                               | 7.56 us: 1.06x slower                                               |
| pickle_dict          | 17.6 us                                                               | 18.8 us: 1.07x slower                                               |
| pickle_list          | 2.73 us                                                               | 2.96 us: 1.08x slower                                               |
| pickle_pure_python   | 222 us                                                                | 284 us: 1.28x slower                                                |
| unpickle             | 9.97 us                                                               | 9.87 us: 1.01x faster                                               |
| unpickle_list        | 2.77 us                                                               | 2.66 us: 1.04x faster                                               |
| unpickle_pure_python | 175 us                                                                | 203 us: 1.16x slower                                                |
| xml_etree_parse      | 99.1 ms                                                               | 100 ms: 1.01x slower                                                |
| xml_etree_iterparse  | 65.2 ms                                                               | 69.0 ms: 1.06x slower                                               |
| xml_etree_generate   | 48.0 ms                                                               | 54.3 ms: 1.13x slower                                               |
| xml_etree_process    | 34.8 ms                                                               | 44.9 ms: 1.29x slower                                               |
| Geometric mean       | (ref)                                                                 | 1.09x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.57 ms: 1.04x slower                                               |
| python_startup_no_site | 7.30 ms                                                               | 6.95 ms: 1.05x faster                                               |
| Geometric mean         | (ref)                                                                 | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|-----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 27.3 ms: 1.30x slower                                               |
| genshi_text     | 15.5 ms                                                               | 18.2 ms: 1.17x slower                                               |
| genshi_xml      | 31.3 ms                                                               | 37.3 ms: 1.19x slower                                               |
| mako            | 8.44 ms                                                               | 10.7 ms: 1.26x slower                                               |
| Geometric mean  | (ref)                                                                 | 1.23x slower                                                        |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|-------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 223 ms: 1.22x slower                                                |
| aiohttp                 | 1.05 ms                                                               | 1.19 ms: 1.13x slower                                               |
| async_generators        | 197 ms                                                                | 231 ms: 1.17x slower                                                |
| async_tree_none         | 287 ms                                                                | 394 ms: 1.37x slower                                                |
| async_tree_cpu_io_mixed | 533 ms                                                                | 661 ms: 1.24x slower                                                |
| async_tree_io           | 702 ms                                                                | 1.00 sec: 1.43x slower                                              |
| async_tree_memoization  | 346 ms                                                                | 481 ms: 1.39x slower                                                |
| chameleon               | 4.73 ms                                                               | 5.83 ms: 1.23x slower                                               |
| chaos                   | 49.5 ms                                                               | 66.6 ms: 1.35x slower                                               |
| bench_thread_pool       | 462 us                                                                | 518 us: 1.12x slower                                                |
| coroutines              | 17.4 ms                                                               | 20.1 ms: 1.16x slower                                               |
| crypto_pyaes            | 51.7 ms                                                               | 77.9 ms: 1.51x slower                                               |
| deepcopy                | 237 us                                                                | 280 us: 1.18x slower                                                |
| deepcopy_reduce         | 2.04 us                                                               | 2.34 us: 1.15x slower                                               |
| deepcopy_memo           | 28.7 us                                                               | 34.5 us: 1.20x slower                                               |
| deltablue               | 2.83 ms                                                               | 5.15 ms: 1.82x slower                                               |
| django_template         | 21.0 ms                                                               | 27.3 ms: 1.30x slower                                               |
| docutils                | 1.46 sec                                                              | 1.77 sec: 1.21x slower                                              |
| dulwich_log             | 29.4 ms                                                               | 36.7 ms: 1.25x slower                                               |
| fannkuch                | 261 ms                                                                | 318 ms: 1.22x slower                                                |
| flaskblogging           | 2.27 ms                                                               | 2.60 ms: 1.14x slower                                               |
| float                   | 55.7 ms                                                               | 72.1 ms: 1.29x slower                                               |
| generators              | 27.7 ms                                                               | 32.4 ms: 1.17x slower                                               |
| genshi_text             | 15.5 ms                                                               | 18.2 ms: 1.17x slower                                               |
| genshi_xml              | 31.3 ms                                                               | 37.3 ms: 1.19x slower                                               |
| go                      | 106 ms                                                                | 165 ms: 1.55x slower                                                |
| gunicorn                | 1.12 ms                                                               | 1.26 ms: 1.13x slower                                               |
| hexiom                  | 4.71 ms                                                               | 6.30 ms: 1.34x slower                                               |
| html5lib                | 35.8 ms                                                               | 46.5 ms: 1.30x slower                                               |
| json                    | 2.91 ms                                                               | 3.11 ms: 1.07x slower                                               |
| json_dumps              | 7.69 ms                                                               | 8.25 ms: 1.07x slower                                               |
| json_loads              | 16.4 us                                                               | 17.0 us: 1.04x slower                                               |
| logging_format          | 3.74 us                                                               | 4.99 us: 1.33x slower                                               |
| logging_silent          | 65.7 ns                                                               | 118 ns: 1.80x slower                                                |
| logging_simple          | 3.44 us                                                               | 4.63 us: 1.35x slower                                               |
| mako                    | 8.44 ms                                                               | 10.7 ms: 1.26x slower                                               |
| mdp                     | 1.53 sec                                                              | 1.66 sec: 1.09x slower                                              |
| meteor_contest          | 77.8 ms                                                               | 77.4 ms: 1.01x faster                                               |
| mypy                    | 418 ms                                                                | 524 ms: 1.25x slower                                                |
| nbody                   | 63.8 ms                                                               | 92.6 ms: 1.45x slower                                               |
| nqueens                 | 58.7 ms                                                               | 68.1 ms: 1.16x slower                                               |
| pathlib                 | 20.8 ms                                                               | 22.0 ms: 1.05x slower                                               |
| pickle                  | 7.14 us                                                               | 7.56 us: 1.06x slower                                               |
| pickle_dict             | 17.6 us                                                               | 18.8 us: 1.07x slower                                               |
| pickle_list             | 2.73 us                                                               | 2.96 us: 1.08x slower                                               |
| pickle_pure_python      | 222 us                                                                | 284 us: 1.28x slower                                                |
| pidigits                | 282 ms                                                                | 284 ms: 1.01x slower                                                |
| pprint_safe_repr        | 488 ms                                                                | 603 ms: 1.24x slower                                                |
| pprint_pformat          | 1.00 sec                                                              | 1.23 sec: 1.23x slower                                              |
| pycparser               | 704 ms                                                                | 912 ms: 1.30x slower                                                |
| pyflate                 | 318 ms                                                                | 453 ms: 1.43x slower                                                |
| pylint                  | 264 ms                                                                | 300 ms: 1.14x slower                                                |
| python_startup          | 9.25 ms                                                               | 9.57 ms: 1.04x slower                                               |
| python_startup_no_site  | 7.30 ms                                                               | 6.95 ms: 1.05x faster                                               |
| raytrace                | 208 ms                                                                | 327 ms: 1.57x slower                                                |
| regex_compile           | 77.7 ms                                                               | 96.5 ms: 1.24x slower                                               |
| regex_dna               | 149 ms                                                                | 180 ms: 1.21x slower                                                |
| regex_effbot            | 2.40 ms                                                               | 2.64 ms: 1.10x slower                                               |
| regex_v8                | 16.8 ms                                                               | 18.3 ms: 1.09x slower                                               |
| richards                | 33.3 ms                                                               | 51.0 ms: 1.54x slower                                               |
| scimark_fft             | 199 ms                                                                | 230 ms: 1.15x slower                                                |
| scimark_lu              | 71.8 ms                                                               | 110 ms: 1.53x slower                                                |
| scimark_monte_carlo     | 48.9 ms                                                               | 72.0 ms: 1.47x slower                                               |
| scimark_sor             | 77.6 ms                                                               | 126 ms: 1.62x slower                                                |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.46 ms: 1.08x slower                                               |
| spectral_norm           | 72.2 ms                                                               | 96.2 ms: 1.33x slower                                               |
| sqlalchemy_declarative  | 61.8 ms                                                               | 74.5 ms: 1.21x slower                                               |
| sqlalchemy_imperative   | 7.29 ms                                                               | 8.96 ms: 1.23x slower                                               |
| sqlglot_parse           | 1.19 ms                                                               | 1.33 ms: 1.12x slower                                               |
| sqlglot_transpile       | 1.35 ms                                                               | 1.55 ms: 1.15x slower                                               |
| sqlglot_optimize        | 31.4 ms                                                               | 37.9 ms: 1.21x slower                                               |
| sqlglot_normalize       | 169 ms                                                                | 196 ms: 1.16x slower                                                |
| sqlite_synth            | 1.35 us                                                               | 1.49 us: 1.10x slower                                               |
| sympy_expand            | 243 ms                                                                | 276 ms: 1.14x slower                                                |
| sympy_integrate         | 11.6 ms                                                               | 13.4 ms: 1.16x slower                                               |
| sympy_sum               | 82.4 ms                                                               | 95.4 ms: 1.16x slower                                               |
| sympy_str               | 151 ms                                                                | 170 ms: 1.13x slower                                                |
| telco                   | 3.42 ms                                                               | 3.64 ms: 1.06x slower                                               |
| thrift                  | 435 us                                                                | 582 us: 1.34x slower                                                |
| tornado_http            | 69.7 ms                                                               | 93.5 ms: 1.34x slower                                               |
| unpack_sequence         | 32.2 ns                                                               | 37.4 ns: 1.16x slower                                               |
| unpickle                | 9.97 us                                                               | 9.87 us: 1.01x faster                                               |
| unpickle_list           | 2.77 us                                                               | 2.66 us: 1.04x faster                                               |
| unpickle_pure_python    | 175 us                                                                | 203 us: 1.16x slower                                                |
| xml_etree_parse         | 99.1 ms                                                               | 100 ms: 1.01x slower                                                |
| xml_etree_iterparse     | 65.2 ms                                                               | 69.0 ms: 1.06x slower                                               |
| xml_etree_generate      | 48.0 ms                                                               | 54.3 ms: 1.13x slower                                               |
| xml_etree_process       | 34.8 ms                                                               | 44.9 ms: 1.29x slower                                               |
| Geometric mean          | (ref)                                                                 | 1.21x slower                                                        |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (1) of public/results/bm-20221206-python-1dd9be6584413fbfa823-3.10.9-1dd9be6/bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6.json: coverage
