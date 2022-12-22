Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.67 ms: 1.25x faster                                                 |
| docutils       | 1.76 sec                                               | 1.47 sec: 1.20x faster                                                |
| html5lib       | 44.0 ms                                                | 35.8 ms: 1.23x faster                                                 |
| tornado_http   | 90.1 ms                                                | 69.4 ms: 1.30x faster                                                 |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 56.5 ms: 1.27x faster                                                 |
| nbody          | 94.6 ms                                                | 64.8 ms: 1.46x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.6 ms: 1.27x faster                                                 |
| regex_dna      | 164 ms                                                 | 152 ms: 1.09x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                 |
| regex_v8       | 17.7 ms                                                | 16.3 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.09 ms: 1.37x faster                                                 |
| json_loads           | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| pickle               | 7.50 us                                                | 7.55 us: 1.01x slower                                                 |
| pickle_list          | 2.83 us                                                | 2.86 us: 1.01x slower                                                 |
| pickle_pure_python   | 284 us                                                 | 205 us: 1.38x faster                                                  |
| unpickle             | 10.0 us                                                | 9.74 us: 1.03x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.54 us: 1.05x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 162 us: 1.26x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 96.6 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 65.2 ms: 1.06x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 47.6 ms: 1.15x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 35.0 ms: 1.29x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.08 ms: 1.06x faster                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.15 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.8 ms: 1.25x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.4 ms: 1.18x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 30.2 ms: 1.25x faster                                                 |
| mako            | 10.6 ms                                                | 8.16 ms: 1.30x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.24x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| async_generators        | 231 ms                                                 | 200 ms: 1.15x faster                                                  |
| async_tree_none         | 396 ms                                                 | 285 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 532 ms: 1.25x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 736 ms: 1.37x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 383 ms: 1.27x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.67 ms: 1.25x faster                                                 |
| chaos                   | 66.5 ms                                                | 50.9 ms: 1.31x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 455 us: 1.17x faster                                                  |
| coroutines              | 20.1 ms                                                | 19.5 ms: 1.03x faster                                                 |
| coverage                | 40.8 ms                                                | 53.7 ms: 1.32x slower                                                 |
| crypto_pyaes            | 77.9 ms                                                | 51.8 ms: 1.50x faster                                                 |
| deepcopy                | 278 us                                                 | 241 us: 1.15x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.08 us: 1.14x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 28.7 us: 1.20x faster                                                 |
| deltablue               | 5.37 ms                                                | 2.83 ms: 1.90x faster                                                 |
| django_template         | 27.2 ms                                                | 21.8 ms: 1.25x faster                                                 |
| docutils                | 1.76 sec                                               | 1.47 sec: 1.20x faster                                                |
| dulwich_log             | 36.4 ms                                                | 29.1 ms: 1.25x faster                                                 |
| fannkuch                | 318 ms                                                 | 270 ms: 1.18x faster                                                  |
| flaskblogging           | 2.59 ms                                                | 2.22 ms: 1.16x faster                                                 |
| float                   | 72.1 ms                                                | 56.5 ms: 1.27x faster                                                 |
| generators              | 32.5 ms                                                | 29.2 ms: 1.11x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.4 ms: 1.18x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 30.2 ms: 1.25x faster                                                 |
| go                      | 165 ms                                                 | 118 ms: 1.40x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.92 ms: 1.28x faster                                                 |
| html5lib                | 44.0 ms                                                | 35.8 ms: 1.23x faster                                                 |
| json                    | 3.13 ms                                                | 2.81 ms: 1.11x faster                                                 |
| json_dumps              | 8.34 ms                                                | 6.09 ms: 1.37x faster                                                 |
| json_loads              | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| logging_format          | 4.95 us                                                | 3.95 us: 1.25x faster                                                 |
| logging_silent          | 119 ns                                                 | 66.2 ns: 1.80x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.67 us: 1.25x faster                                                 |
| mako                    | 10.6 ms                                                | 8.16 ms: 1.30x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.52 sec: 1.09x faster                                                |
| meteor_contest          | 77.7 ms                                                | 78.2 ms: 1.01x slower                                                 |
| mypy                    | 521 ms                                                 | 416 ms: 1.25x faster                                                  |
| nbody                   | 94.6 ms                                                | 64.8 ms: 1.46x faster                                                 |
| nqueens                 | 68.6 ms                                                | 61.2 ms: 1.12x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.6 ms: 1.08x faster                                                 |
| pickle                  | 7.50 us                                                | 7.55 us: 1.01x slower                                                 |
| pickle_list             | 2.83 us                                                | 2.86 us: 1.01x slower                                                 |
| pickle_pure_python      | 284 us                                                 | 205 us: 1.38x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 495 ms: 1.23x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 1.00 sec: 1.23x faster                                                |
| pycparser               | 915 ms                                                 | 713 ms: 1.28x faster                                                  |
| pyflate                 | 454 ms                                                 | 351 ms: 1.29x faster                                                  |
| pylint                  | 302 ms                                                 | 264 ms: 1.14x faster                                                  |
| python_startup          | 9.59 ms                                                | 9.08 ms: 1.06x faster                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.15 ms: 1.02x slower                                                 |
| raytrace                | 329 ms                                                 | 214 ms: 1.54x faster                                                  |
| regex_compile           | 96.2 ms                                                | 75.6 ms: 1.27x faster                                                 |
| regex_dna               | 164 ms                                                 | 152 ms: 1.09x faster                                                  |
| regex_effbot            | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                 |
| regex_v8                | 17.7 ms                                                | 16.3 ms: 1.09x faster                                                 |
| richards                | 51.4 ms                                                | 33.2 ms: 1.55x faster                                                 |
| scimark_fft             | 231 ms                                                 | 199 ms: 1.16x faster                                                  |
| scimark_lu              | 110 ms                                                 | 72.3 ms: 1.52x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 54.3 ms: 1.33x faster                                                 |
| scimark_sor             | 126 ms                                                 | 102 ms: 1.24x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.83 ms: 1.23x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 72.9 ms: 1.31x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 61.3 ms: 1.21x faster                                                 |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.00 ms: 1.29x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1000 us: 1.33x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.17 ms: 1.32x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 31.9 ms: 1.19x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 174 ms: 1.14x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.46 us: 1.03x faster                                                 |
| sympy_expand            | 275 ms                                                 | 248 ms: 1.11x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.6 ms: 1.14x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 85.9 ms: 1.09x faster                                                 |
| sympy_str               | 169 ms                                                 | 153 ms: 1.10x faster                                                  |
| telco                   | 3.63 ms                                                | 3.36 ms: 1.08x faster                                                 |
| thrift                  | 577 us                                                 | 442 us: 1.31x faster                                                  |
| tornado_http            | 90.1 ms                                                | 69.4 ms: 1.30x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 34.1 ns: 1.12x faster                                                 |
| unpickle                | 10.0 us                                                | 9.74 us: 1.03x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.54 us: 1.05x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 162 us: 1.26x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 96.6 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 65.2 ms: 1.06x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 47.6 ms: 1.15x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 35.0 ms: 1.29x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.20x faster                                                          |

Benchmark hidden because not significant (2): bench_mp_pool, pickle_dict
Ignored benchmarks (2) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, gunicorn
