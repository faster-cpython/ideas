Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 222 ms: 1.22x slower                                   |
| chameleon      | 4.73 ms                                                               | 5.86 ms: 1.24x slower                                  |
| docutils       | 1.46 sec                                                              | 1.76 sec: 1.21x slower                                 |
| html5lib       | 35.8 ms                                                               | 44.0 ms: 1.23x slower                                  |
| tornado_http   | 69.7 ms                                                               | 90.1 ms: 1.29x slower                                  |
| Geometric mean | (ref)                                                                 | 1.24x slower                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 55.7 ms                                                               | 72.1 ms: 1.29x slower                                  |
| nbody          | 63.8 ms                                                               | 94.6 ms: 1.48x slower                                  |
| pidigits       | 282 ms                                                                | 284 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                                 | 1.24x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 96.2 ms: 1.24x slower                                  |
| regex_dna      | 149 ms                                                                | 164 ms: 1.10x slower                                   |
| regex_effbot   | 2.40 ms                                                               | 2.45 ms: 1.02x slower                                  |
| regex_v8       | 16.8 ms                                                               | 17.7 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                                 | 1.10x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 8.34 ms: 1.08x slower                                  |
| json_loads           | 16.4 us                                                               | 17.0 us: 1.04x slower                                  |
| pickle               | 7.14 us                                                               | 7.50 us: 1.05x slower                                  |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                  |
| pickle_list          | 2.73 us                                                               | 2.83 us: 1.04x slower                                  |
| pickle_pure_python   | 222 us                                                                | 284 us: 1.28x slower                                   |
| unpickle_list        | 2.77 us                                                               | 2.66 us: 1.04x faster                                  |
| unpickle_pure_python | 175 us                                                                | 204 us: 1.16x slower                                   |
| xml_etree_parse      | 99.1 ms                                                               | 100 ms: 1.01x slower                                   |
| xml_etree_iterparse  | 65.2 ms                                                               | 69.0 ms: 1.06x slower                                  |
| xml_etree_generate   | 48.0 ms                                                               | 54.5 ms: 1.14x slower                                  |
| xml_etree_process    | 34.8 ms                                                               | 45.1 ms: 1.30x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.08x slower                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.59 ms: 1.04x slower                                  |
| python_startup_no_site | 7.30 ms                                                               | 7.00 ms: 1.04x faster                                  |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 27.2 ms: 1.30x slower                                  |
| genshi_text     | 15.5 ms                                                               | 18.2 ms: 1.17x slower                                  |
| genshi_xml      | 31.3 ms                                                               | 37.7 ms: 1.20x slower                                  |
| mako            | 8.44 ms                                                               | 10.6 ms: 1.26x slower                                  |
| Geometric mean  | (ref)                                                                 | 1.23x slower                                           |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 |
|-------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 222 ms: 1.22x slower                                   |
| aiohttp                 | 1.05 ms                                                               | 1.19 ms: 1.13x slower                                  |
| async_generators        | 197 ms                                                                | 231 ms: 1.17x slower                                   |
| async_tree_none         | 287 ms                                                                | 396 ms: 1.38x slower                                   |
| async_tree_cpu_io_mixed | 533 ms                                                                | 665 ms: 1.25x slower                                   |
| async_tree_io           | 702 ms                                                                | 1.01 sec: 1.44x slower                                 |
| async_tree_memoization  | 346 ms                                                                | 485 ms: 1.40x slower                                   |
| chameleon               | 4.73 ms                                                               | 5.86 ms: 1.24x slower                                  |
| chaos                   | 49.5 ms                                                               | 66.5 ms: 1.34x slower                                  |
| bench_thread_pool       | 462 us                                                                | 531 us: 1.15x slower                                   |
| coroutines              | 17.4 ms                                                               | 20.1 ms: 1.16x slower                                  |
| crypto_pyaes            | 51.7 ms                                                               | 77.9 ms: 1.51x slower                                  |
| deepcopy                | 237 us                                                                | 278 us: 1.17x slower                                   |
| deepcopy_reduce         | 2.04 us                                                               | 2.36 us: 1.16x slower                                  |
| deepcopy_memo           | 28.7 us                                                               | 34.4 us: 1.20x slower                                  |
| deltablue               | 2.83 ms                                                               | 5.37 ms: 1.90x slower                                  |
| django_template         | 21.0 ms                                                               | 27.2 ms: 1.30x slower                                  |
| docutils                | 1.46 sec                                                              | 1.76 sec: 1.21x slower                                 |
| dulwich_log             | 29.4 ms                                                               | 36.4 ms: 1.24x slower                                  |
| fannkuch                | 261 ms                                                                | 318 ms: 1.22x slower                                   |
| flaskblogging           | 2.27 ms                                                               | 2.59 ms: 1.14x slower                                  |
| float                   | 55.7 ms                                                               | 72.1 ms: 1.29x slower                                  |
| generators              | 27.7 ms                                                               | 32.5 ms: 1.17x slower                                  |
| genshi_text             | 15.5 ms                                                               | 18.2 ms: 1.17x slower                                  |
| genshi_xml              | 31.3 ms                                                               | 37.7 ms: 1.20x slower                                  |
| go                      | 106 ms                                                                | 165 ms: 1.55x slower                                   |
| gunicorn                | 1.12 ms                                                               | 1.28 ms: 1.15x slower                                  |
| hexiom                  | 4.71 ms                                                               | 6.31 ms: 1.34x slower                                  |
| html5lib                | 35.8 ms                                                               | 44.0 ms: 1.23x slower                                  |
| json                    | 2.91 ms                                                               | 3.13 ms: 1.08x slower                                  |
| json_dumps              | 7.69 ms                                                               | 8.34 ms: 1.08x slower                                  |
| json_loads              | 16.4 us                                                               | 17.0 us: 1.04x slower                                  |
| logging_format          | 3.74 us                                                               | 4.95 us: 1.32x slower                                  |
| logging_silent          | 65.7 ns                                                               | 119 ns: 1.82x slower                                   |
| logging_simple          | 3.44 us                                                               | 4.61 us: 1.34x slower                                  |
| mako                    | 8.44 ms                                                               | 10.6 ms: 1.26x slower                                  |
| mdp                     | 1.53 sec                                                              | 1.66 sec: 1.09x slower                                 |
| mypy                    | 418 ms                                                                | 521 ms: 1.25x slower                                   |
| nbody                   | 63.8 ms                                                               | 94.6 ms: 1.48x slower                                  |
| nqueens                 | 58.7 ms                                                               | 68.6 ms: 1.17x slower                                  |
| pathlib                 | 20.8 ms                                                               | 22.2 ms: 1.07x slower                                  |
| pickle                  | 7.14 us                                                               | 7.50 us: 1.05x slower                                  |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                  |
| pickle_list             | 2.73 us                                                               | 2.83 us: 1.04x slower                                  |
| pickle_pure_python      | 222 us                                                                | 284 us: 1.28x slower                                   |
| pidigits                | 282 ms                                                                | 284 ms: 1.01x slower                                   |
| pprint_safe_repr        | 488 ms                                                                | 608 ms: 1.25x slower                                   |
| pprint_pformat          | 1.00 sec                                                              | 1.24 sec: 1.24x slower                                 |
| pycparser               | 704 ms                                                                | 915 ms: 1.30x slower                                   |
| pyflate                 | 318 ms                                                                | 454 ms: 1.43x slower                                   |
| pylint                  | 264 ms                                                                | 302 ms: 1.14x slower                                   |
| python_startup          | 9.25 ms                                                               | 9.59 ms: 1.04x slower                                  |
| python_startup_no_site  | 7.30 ms                                                               | 7.00 ms: 1.04x faster                                  |
| raytrace                | 208 ms                                                                | 329 ms: 1.59x slower                                   |
| regex_compile           | 77.7 ms                                                               | 96.2 ms: 1.24x slower                                  |
| regex_dna               | 149 ms                                                                | 164 ms: 1.10x slower                                   |
| regex_effbot            | 2.40 ms                                                               | 2.45 ms: 1.02x slower                                  |
| regex_v8                | 16.8 ms                                                               | 17.7 ms: 1.06x slower                                  |
| richards                | 33.3 ms                                                               | 51.4 ms: 1.55x slower                                  |
| scimark_fft             | 199 ms                                                                | 231 ms: 1.16x slower                                   |
| scimark_lu              | 71.8 ms                                                               | 110 ms: 1.53x slower                                   |
| scimark_monte_carlo     | 48.9 ms                                                               | 72.3 ms: 1.48x slower                                  |
| scimark_sor             | 77.6 ms                                                               | 126 ms: 1.62x slower                                   |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.47 ms: 1.08x slower                                  |
| spectral_norm           | 72.2 ms                                                               | 95.8 ms: 1.33x slower                                  |
| sqlalchemy_declarative  | 61.8 ms                                                               | 74.4 ms: 1.20x slower                                  |
| sqlalchemy_imperative   | 7.29 ms                                                               | 9.01 ms: 1.24x slower                                  |
| sqlglot_parse           | 1.19 ms                                                               | 1.33 ms: 1.12x slower                                  |
| sqlglot_transpile       | 1.35 ms                                                               | 1.54 ms: 1.14x slower                                  |
| sqlglot_optimize        | 31.4 ms                                                               | 38.1 ms: 1.21x slower                                  |
| sqlglot_normalize       | 169 ms                                                                | 198 ms: 1.17x slower                                   |
| sqlite_synth            | 1.35 us                                                               | 1.50 us: 1.11x slower                                  |
| sympy_expand            | 243 ms                                                                | 275 ms: 1.13x slower                                   |
| sympy_integrate         | 11.6 ms                                                               | 13.3 ms: 1.15x slower                                  |
| sympy_sum               | 82.4 ms                                                               | 93.5 ms: 1.13x slower                                  |
| sympy_str               | 151 ms                                                                | 169 ms: 1.12x slower                                   |
| telco                   | 3.42 ms                                                               | 3.63 ms: 1.06x slower                                  |
| thrift                  | 435 us                                                                | 577 us: 1.33x slower                                   |
| tornado_http            | 69.7 ms                                                               | 90.1 ms: 1.29x slower                                  |
| unpack_sequence         | 32.2 ns                                                               | 38.2 ns: 1.19x slower                                  |
| unpickle_list           | 2.77 us                                                               | 2.66 us: 1.04x faster                                  |
| unpickle_pure_python    | 175 us                                                                | 204 us: 1.16x slower                                   |
| xml_etree_parse         | 99.1 ms                                                               | 100 ms: 1.01x slower                                   |
| xml_etree_iterparse     | 65.2 ms                                                               | 69.0 ms: 1.06x slower                                  |
| xml_etree_generate      | 48.0 ms                                                               | 54.5 ms: 1.14x slower                                  |
| xml_etree_process       | 34.8 ms                                                               | 45.1 ms: 1.30x slower                                  |
| Geometric mean          | (ref)                                                                 | 1.21x slower                                           |

Benchmark hidden because not significant (3): bench_mp_pool, meteor_contest, unpickle
Ignored benchmarks (1) of public/results/bm-20220323-python-v3.10.4-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: coverage
