Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 186 ms: 1.20x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.61 ms: 1.27x faster                                                 |
| docutils       | 1.76 sec                                               | 1.47 sec: 1.20x faster                                                |
| html5lib       | 44.0 ms                                                | 36.6 ms: 1.20x faster                                                 |
| tornado_http   | 90.1 ms                                                | 69.4 ms: 1.30x faster                                                 |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 56.1 ms: 1.28x faster                                                 |
| nbody          | 94.6 ms                                                | 64.3 ms: 1.47x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                  | 1.24x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 76.5 ms: 1.26x faster                                                 |
| regex_dna      | 164 ms                                                 | 151 ms: 1.09x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.68 ms: 1.09x slower                                                 |
| regex_v8       | 17.7 ms                                                | 16.3 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.17 ms: 1.35x faster                                                 |
| json_loads           | 17.0 us                                                | 16.3 us: 1.05x faster                                                 |
| pickle               | 7.50 us                                                | 7.56 us: 1.01x slower                                                 |
| pickle_dict          | 18.0 us                                                | 18.0 us: 1.00x slower                                                 |
| pickle_list          | 2.83 us                                                | 2.91 us: 1.03x slower                                                 |
| pickle_pure_python   | 284 us                                                 | 208 us: 1.36x faster                                                  |
| unpickle             | 10.0 us                                                | 9.78 us: 1.03x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.54 us: 1.05x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 162 us: 1.26x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 90.0 ms: 1.11x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 64.6 ms: 1.07x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 47.1 ms: 1.16x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 34.9 ms: 1.29x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.38 ms: 1.02x faster                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.41 ms: 1.06x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.7 ms: 1.25x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.3 ms: 1.19x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 30.1 ms: 1.25x faster                                                 |
| mako            | 10.6 ms                                                | 8.11 ms: 1.31x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.25x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 186 ms: 1.20x faster                                                  |
| async_generators        | 231 ms                                                 | 199 ms: 1.16x faster                                                  |
| async_tree_none         | 396 ms                                                 | 287 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 545 ms: 1.22x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 736 ms: 1.37x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 325 ms: 1.49x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.61 ms: 1.27x faster                                                 |
| chaos                   | 66.5 ms                                                | 50.4 ms: 1.32x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 452 us: 1.17x faster                                                  |
| coroutines              | 20.1 ms                                                | 19.0 ms: 1.06x faster                                                 |
| coverage                | 40.8 ms                                                | 53.4 ms: 1.31x slower                                                 |
| crypto_pyaes            | 77.9 ms                                                | 51.8 ms: 1.50x faster                                                 |
| deepcopy                | 278 us                                                 | 239 us: 1.16x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.06 us: 1.15x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 29.2 us: 1.18x faster                                                 |
| deltablue               | 5.37 ms                                                | 2.74 ms: 1.96x faster                                                 |
| django_template         | 27.2 ms                                                | 21.7 ms: 1.25x faster                                                 |
| docutils                | 1.76 sec                                               | 1.47 sec: 1.20x faster                                                |
| dulwich_log             | 36.4 ms                                                | 29.3 ms: 1.24x faster                                                 |
| fannkuch                | 318 ms                                                 | 269 ms: 1.18x faster                                                  |
| float                   | 72.1 ms                                                | 56.1 ms: 1.28x faster                                                 |
| generators              | 32.5 ms                                                | 29.0 ms: 1.12x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.3 ms: 1.19x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 30.1 ms: 1.25x faster                                                 |
| go                      | 165 ms                                                 | 120 ms: 1.38x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.92 ms: 1.28x faster                                                 |
| html5lib                | 44.0 ms                                                | 36.6 ms: 1.20x faster                                                 |
| json                    | 3.13 ms                                                | 2.84 ms: 1.10x faster                                                 |
| json_dumps              | 8.34 ms                                                | 6.17 ms: 1.35x faster                                                 |
| json_loads              | 17.0 us                                                | 16.3 us: 1.05x faster                                                 |
| logging_format          | 4.95 us                                                | 4.00 us: 1.24x faster                                                 |
| logging_silent          | 119 ns                                                 | 65.9 ns: 1.81x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.66 us: 1.26x faster                                                 |
| mako                    | 10.6 ms                                                | 8.11 ms: 1.31x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.52 sec: 1.09x faster                                                |
| meteor_contest          | 77.7 ms                                                | 76.2 ms: 1.02x faster                                                 |
| mypy                    | 521 ms                                                 | 419 ms: 1.24x faster                                                  |
| nbody                   | 94.6 ms                                                | 64.3 ms: 1.47x faster                                                 |
| nqueens                 | 68.6 ms                                                | 60.3 ms: 1.14x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.8 ms: 1.07x faster                                                 |
| pickle                  | 7.50 us                                                | 7.56 us: 1.01x slower                                                 |
| pickle_dict             | 18.0 us                                                | 18.0 us: 1.00x slower                                                 |
| pickle_list             | 2.83 us                                                | 2.91 us: 1.03x slower                                                 |
| pickle_pure_python      | 284 us                                                 | 208 us: 1.36x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 486 ms: 1.25x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 992 ms: 1.25x faster                                                  |
| pycparser               | 915 ms                                                 | 706 ms: 1.30x faster                                                  |
| pyflate                 | 454 ms                                                 | 352 ms: 1.29x faster                                                  |
| pylint                  | 302 ms                                                 | 265 ms: 1.14x faster                                                  |
| python_startup          | 9.59 ms                                                | 9.38 ms: 1.02x faster                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.41 ms: 1.06x slower                                                 |
| raytrace                | 329 ms                                                 | 219 ms: 1.51x faster                                                  |
| regex_compile           | 96.2 ms                                                | 76.5 ms: 1.26x faster                                                 |
| regex_dna               | 164 ms                                                 | 151 ms: 1.09x faster                                                  |
| regex_effbot            | 2.45 ms                                                | 2.68 ms: 1.09x slower                                                 |
| regex_v8                | 17.7 ms                                                | 16.3 ms: 1.09x faster                                                 |
| richards                | 51.4 ms                                                | 33.5 ms: 1.54x faster                                                 |
| scimark_fft             | 231 ms                                                 | 198 ms: 1.17x faster                                                  |
| scimark_lu              | 110 ms                                                 | 73.9 ms: 1.49x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 54.6 ms: 1.32x faster                                                 |
| scimark_sor             | 126 ms                                                 | 101 ms: 1.24x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.78 ms: 1.25x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 72.5 ms: 1.32x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 61.0 ms: 1.22x faster                                                 |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.16 ms: 1.26x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.01 ms: 1.32x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.18 ms: 1.31x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 31.7 ms: 1.20x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 173 ms: 1.15x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.45 us: 1.03x faster                                                 |
| sympy_expand            | 275 ms                                                 | 246 ms: 1.12x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.6 ms: 1.14x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 86.0 ms: 1.09x faster                                                 |
| sympy_str               | 169 ms                                                 | 153 ms: 1.11x faster                                                  |
| telco                   | 3.63 ms                                                | 3.32 ms: 1.09x faster                                                 |
| thrift                  | 577 us                                                 | 438 us: 1.32x faster                                                  |
| tornado_http            | 90.1 ms                                                | 69.4 ms: 1.30x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 33.5 ns: 1.14x faster                                                 |
| unpickle                | 10.0 us                                                | 9.78 us: 1.03x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.54 us: 1.05x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 162 us: 1.26x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 90.0 ms: 1.11x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 64.6 ms: 1.07x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 47.1 ms: 1.16x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 34.9 ms: 1.29x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.20x faster                                                          |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-python-v3.10.4-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn
