Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 181 ms: 1.23x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.70 ms: 1.25x faster                                                 |
| docutils       | 1.76 sec                                               | 1.45 sec: 1.21x faster                                                |
| html5lib       | 44.0 ms                                                | 34.0 ms: 1.29x faster                                                 |
| tornado_http   | 90.1 ms                                                | 70.4 ms: 1.28x faster                                                 |
| Geometric mean | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.6 ms: 1.40x faster                                                 |
| nbody          | 94.6 ms                                                | 65.6 ms: 1.44x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                  | 1.27x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.6 ms: 1.27x faster                                                 |
| regex_dna      | 164 ms                                                 | 169 ms: 1.03x slower                                                  |
| regex_effbot   | 2.45 ms                                                | 2.20 ms: 1.12x faster                                                 |
| regex_v8       | 17.7 ms                                                | 20.5 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 7.58 ms: 1.10x faster                                                 |
| json_loads           | 17.0 us                                                | 16.3 us: 1.05x faster                                                 |
| pickle               | 7.50 us                                                | 7.18 us: 1.05x faster                                                 |
| pickle_dict          | 18.0 us                                                | 19.2 us: 1.07x slower                                                 |
| pickle_list          | 2.83 us                                                | 2.80 us: 1.01x faster                                                 |
| pickle_pure_python   | 284 us                                                 | 200 us: 1.42x faster                                                  |
| unpickle             | 10.0 us                                                | 9.82 us: 1.02x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.62 us: 1.02x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 157 us: 1.30x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 95.7 ms: 1.05x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 64.4 ms: 1.07x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 47.9 ms: 1.14x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 35.1 ms: 1.29x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.13 ms: 1.05x faster                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.18 ms: 1.03x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.1 ms: 1.29x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.2 ms: 1.20x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 31.4 ms: 1.20x faster                                                 |
| mako            | 10.6 ms                                                | 8.21 ms: 1.29x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.24x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 181 ms: 1.23x faster                                                  |
| aiohttp                 | 1.19 ms                                                | 1.06 ms: 1.13x faster                                                 |
| async_generators        | 231 ms                                                 | 191 ms: 1.21x faster                                                  |
| async_tree_none         | 396 ms                                                 | 280 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 534 ms: 1.25x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 693 ms: 1.46x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 316 ms: 1.53x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.70 ms: 1.25x faster                                                 |
| chaos                   | 66.5 ms                                                | 49.7 ms: 1.34x faster                                                 |
| bench_mp_pool           | 40.8 ms                                                | 37.1 ms: 1.10x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 476 us: 1.12x faster                                                  |
| coroutines              | 20.1 ms                                                | 17.3 ms: 1.16x faster                                                 |
| crypto_pyaes            | 77.9 ms                                                | 56.5 ms: 1.38x faster                                                 |
| deepcopy                | 278 us                                                 | 220 us: 1.26x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.91 us: 1.24x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 25.4 us: 1.35x faster                                                 |
| deltablue               | 5.37 ms                                                | 2.67 ms: 2.01x faster                                                 |
| django_template         | 27.2 ms                                                | 21.1 ms: 1.29x faster                                                 |
| docutils                | 1.76 sec                                               | 1.45 sec: 1.21x faster                                                |
| dulwich_log             | 36.4 ms                                                | 29.4 ms: 1.24x faster                                                 |
| fannkuch                | 318 ms                                                 | 262 ms: 1.22x faster                                                  |
| flaskblogging           | 2.59 ms                                                | 2.30 ms: 1.12x faster                                                 |
| float                   | 72.1 ms                                                | 51.6 ms: 1.40x faster                                                 |
| generators              | 32.5 ms                                                | 27.9 ms: 1.16x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.2 ms: 1.20x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 31.4 ms: 1.20x faster                                                 |
| go                      | 165 ms                                                 | 107 ms: 1.54x faster                                                  |
| gunicorn                | 1.28 ms                                                | 1.13 ms: 1.14x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.87 ms: 1.30x faster                                                 |
| html5lib                | 44.0 ms                                                | 34.0 ms: 1.29x faster                                                 |
| json                    | 3.13 ms                                                | 2.92 ms: 1.07x faster                                                 |
| json_dumps              | 8.34 ms                                                | 7.58 ms: 1.10x faster                                                 |
| json_loads              | 17.0 us                                                | 16.3 us: 1.05x faster                                                 |
| logging_format          | 4.95 us                                                | 3.65 us: 1.36x faster                                                 |
| logging_silent          | 119 ns                                                 | 69.4 ns: 1.72x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.38 us: 1.36x faster                                                 |
| mako                    | 10.6 ms                                                | 8.21 ms: 1.29x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 75.2 ms: 1.03x faster                                                 |
| mypy                    | 521 ms                                                 | 422 ms: 1.23x faster                                                  |
| nbody                   | 94.6 ms                                                | 65.6 ms: 1.44x faster                                                 |
| nqueens                 | 68.6 ms                                                | 60.6 ms: 1.13x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.9 ms: 1.06x faster                                                 |
| pickle                  | 7.50 us                                                | 7.18 us: 1.05x faster                                                 |
| pickle_dict             | 18.0 us                                                | 19.2 us: 1.07x slower                                                 |
| pickle_list             | 2.83 us                                                | 2.80 us: 1.01x faster                                                 |
| pickle_pure_python      | 284 us                                                 | 200 us: 1.42x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 460 ms: 1.32x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 940 ms: 1.32x faster                                                  |
| pycparser               | 915 ms                                                 | 721 ms: 1.27x faster                                                  |
| pyflate                 | 454 ms                                                 | 317 ms: 1.43x faster                                                  |
| pylint                  | 302 ms                                                 | 271 ms: 1.11x faster                                                  |
| python_startup          | 9.59 ms                                                | 9.13 ms: 1.05x faster                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.18 ms: 1.03x slower                                                 |
| raytrace                | 329 ms                                                 | 209 ms: 1.57x faster                                                  |
| regex_compile           | 96.2 ms                                                | 75.6 ms: 1.27x faster                                                 |
| regex_dna               | 164 ms                                                 | 169 ms: 1.03x slower                                                  |
| regex_effbot            | 2.45 ms                                                | 2.20 ms: 1.12x faster                                                 |
| regex_v8                | 17.7 ms                                                | 20.5 ms: 1.16x slower                                                 |
| richards                | 51.4 ms                                                | 32.1 ms: 1.60x faster                                                 |
| scimark_fft             | 231 ms                                                 | 201 ms: 1.15x faster                                                  |
| scimark_lu              | 110 ms                                                 | 72.6 ms: 1.51x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 46.9 ms: 1.54x faster                                                 |
| scimark_sor             | 126 ms                                                 | 84.7 ms: 1.49x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.22 ms: 1.08x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 73.6 ms: 1.30x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 63.2 ms: 1.18x faster                                                 |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.37 ms: 1.22x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.17 ms: 1.14x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.33 ms: 1.15x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 31.9 ms: 1.19x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 172 ms: 1.15x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.29 us: 1.16x faster                                                 |
| sympy_expand            | 275 ms                                                 | 241 ms: 1.14x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.2 ms: 1.18x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 81.7 ms: 1.14x faster                                                 |
| sympy_str               | 169 ms                                                 | 147 ms: 1.15x faster                                                  |
| telco                   | 3.63 ms                                                | 3.39 ms: 1.07x faster                                                 |
| thrift                  | 577 us                                                 | 439 us: 1.32x faster                                                  |
| tornado_http            | 90.1 ms                                                | 70.4 ms: 1.28x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 31.9 ns: 1.20x faster                                                 |
| unpickle                | 10.0 us                                                | 9.82 us: 1.02x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.62 us: 1.02x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 157 us: 1.30x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 95.7 ms: 1.05x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 64.4 ms: 1.07x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 47.9 ms: 1.14x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 35.1 ms: 1.29x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.22x faster                                                          |

Benchmark hidden because not significant (1): mdp
Ignored benchmarks (1) of public/results/bm-20220323-python-v3.10.4-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: coverage
