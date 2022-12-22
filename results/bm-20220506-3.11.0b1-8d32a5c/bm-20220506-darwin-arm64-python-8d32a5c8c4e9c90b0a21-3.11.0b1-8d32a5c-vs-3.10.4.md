Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 184 ms: 1.21x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.75 ms: 1.23x faster                                                 |
| docutils       | 1.76 sec                                               | 1.45 sec: 1.21x faster                                                |
| html5lib       | 44.0 ms                                                | 33.2 ms: 1.32x faster                                                 |
| tornado_http   | 90.1 ms                                                | 70.4 ms: 1.28x faster                                                 |
| Geometric mean | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.4 ms: 1.40x faster                                                 |
| nbody          | 94.6 ms                                                | 64.0 ms: 1.48x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 78.4 ms: 1.23x faster                                                 |
| regex_dna      | 164 ms                                                 | 140 ms: 1.17x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.03 ms: 1.21x faster                                                 |
| regex_v8       | 17.7 ms                                                | 15.8 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                  | 1.18x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 7.77 ms: 1.07x faster                                                 |
| json_loads           | 17.0 us                                                | 16.4 us: 1.04x faster                                                 |
| pickle               | 7.50 us                                                | 7.17 us: 1.05x faster                                                 |
| pickle_dict          | 18.0 us                                                | 17.1 us: 1.05x faster                                                 |
| pickle_list          | 2.83 us                                                | 2.71 us: 1.04x faster                                                 |
| pickle_pure_python   | 284 us                                                 | 212 us: 1.34x faster                                                  |
| unpickle             | 10.0 us                                                | 9.91 us: 1.01x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.61 us: 1.02x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 181 us: 1.13x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 99.3 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 65.5 ms: 1.05x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 49.0 ms: 1.11x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 35.9 ms: 1.26x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.22 ms: 1.04x faster                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.24 ms: 1.03x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.5 ms: 1.27x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.4 ms: 1.18x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 31.6 ms: 1.19x faster                                                 |
| mako            | 10.6 ms                                                | 8.40 ms: 1.26x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.23x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 184 ms: 1.21x faster                                                  |
| aiohttp                 | 1.19 ms                                                | 1.03 ms: 1.15x faster                                                 |
| async_generators        | 231 ms                                                 | 200 ms: 1.15x faster                                                  |
| async_tree_none         | 396 ms                                                 | 286 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 534 ms: 1.25x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 705 ms: 1.43x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 356 ms: 1.36x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.75 ms: 1.23x faster                                                 |
| chaos                   | 66.5 ms                                                | 50.6 ms: 1.32x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 482 us: 1.10x faster                                                  |
| coroutines              | 20.1 ms                                                | 18.8 ms: 1.07x faster                                                 |
| crypto_pyaes            | 77.9 ms                                                | 52.1 ms: 1.50x faster                                                 |
| deepcopy                | 278 us                                                 | 222 us: 1.25x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.90 us: 1.24x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 26.2 us: 1.31x faster                                                 |
| deltablue               | 5.37 ms                                                | 2.74 ms: 1.96x faster                                                 |
| django_template         | 27.2 ms                                                | 21.5 ms: 1.27x faster                                                 |
| docutils                | 1.76 sec                                               | 1.45 sec: 1.21x faster                                                |
| dulwich_log             | 36.4 ms                                                | 29.5 ms: 1.23x faster                                                 |
| fannkuch                | 318 ms                                                 | 261 ms: 1.22x faster                                                  |
| flaskblogging           | 2.59 ms                                                | 2.29 ms: 1.13x faster                                                 |
| float                   | 72.1 ms                                                | 51.4 ms: 1.40x faster                                                 |
| generators              | 32.5 ms                                                | 28.6 ms: 1.14x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.4 ms: 1.18x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 31.6 ms: 1.19x faster                                                 |
| go                      | 165 ms                                                 | 110 ms: 1.50x faster                                                  |
| gunicorn                | 1.28 ms                                                | 1.14 ms: 1.12x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.92 ms: 1.28x faster                                                 |
| html5lib                | 44.0 ms                                                | 33.2 ms: 1.32x faster                                                 |
| json                    | 3.13 ms                                                | 2.92 ms: 1.07x faster                                                 |
| json_dumps              | 8.34 ms                                                | 7.77 ms: 1.07x faster                                                 |
| json_loads              | 17.0 us                                                | 16.4 us: 1.04x faster                                                 |
| logging_format          | 4.95 us                                                | 3.90 us: 1.27x faster                                                 |
| logging_silent          | 119 ns                                                 | 67.5 ns: 1.77x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.60 us: 1.28x faster                                                 |
| mako                    | 10.6 ms                                                | 8.40 ms: 1.26x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.56 sec: 1.06x faster                                                |
| meteor_contest          | 77.7 ms                                                | 76.8 ms: 1.01x faster                                                 |
| mypy                    | 521 ms                                                 | 421 ms: 1.24x faster                                                  |
| nbody                   | 94.6 ms                                                | 64.0 ms: 1.48x faster                                                 |
| nqueens                 | 68.6 ms                                                | 60.4 ms: 1.13x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.7 ms: 1.07x faster                                                 |
| pickle                  | 7.50 us                                                | 7.17 us: 1.05x faster                                                 |
| pickle_dict             | 18.0 us                                                | 17.1 us: 1.05x faster                                                 |
| pickle_list             | 2.83 us                                                | 2.71 us: 1.04x faster                                                 |
| pickle_pure_python      | 284 us                                                 | 212 us: 1.34x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 470 ms: 1.29x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 966 ms: 1.28x faster                                                  |
| pycparser               | 915 ms                                                 | 709 ms: 1.29x faster                                                  |
| pyflate                 | 454 ms                                                 | 322 ms: 1.41x faster                                                  |
| pylint                  | 302 ms                                                 | 268 ms: 1.12x faster                                                  |
| python_startup          | 9.59 ms                                                | 9.22 ms: 1.04x faster                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.24 ms: 1.03x slower                                                 |
| raytrace                | 329 ms                                                 | 207 ms: 1.60x faster                                                  |
| regex_compile           | 96.2 ms                                                | 78.4 ms: 1.23x faster                                                 |
| regex_dna               | 164 ms                                                 | 140 ms: 1.17x faster                                                  |
| regex_effbot            | 2.45 ms                                                | 2.03 ms: 1.21x faster                                                 |
| regex_v8                | 17.7 ms                                                | 15.8 ms: 1.12x faster                                                 |
| richards                | 51.4 ms                                                | 33.8 ms: 1.52x faster                                                 |
| scimark_fft             | 231 ms                                                 | 201 ms: 1.15x faster                                                  |
| scimark_lu              | 110 ms                                                 | 73.7 ms: 1.49x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 48.9 ms: 1.48x faster                                                 |
| scimark_sor             | 126 ms                                                 | 79.2 ms: 1.59x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.23 ms: 1.07x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 71.7 ms: 1.34x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 62.8 ms: 1.18x faster                                                 |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.44 ms: 1.21x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.21 ms: 1.10x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.38 ms: 1.12x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 33.0 ms: 1.15x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 179 ms: 1.11x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.32 us: 1.13x faster                                                 |
| sympy_expand            | 275 ms                                                 | 249 ms: 1.11x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.7 ms: 1.13x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 83.6 ms: 1.12x faster                                                 |
| sympy_str               | 169 ms                                                 | 153 ms: 1.11x faster                                                  |
| telco                   | 3.63 ms                                                | 3.41 ms: 1.06x faster                                                 |
| thrift                  | 577 us                                                 | 443 us: 1.30x faster                                                  |
| tornado_http            | 90.1 ms                                                | 70.4 ms: 1.28x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 32.3 ns: 1.18x faster                                                 |
| unpickle                | 10.0 us                                                | 9.91 us: 1.01x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.61 us: 1.02x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 181 us: 1.13x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 99.3 ms: 1.01x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 65.5 ms: 1.05x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 49.0 ms: 1.11x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 35.9 ms: 1.26x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (1) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: coverage
