Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.59 ms: 1.28x faster                                                 |
| docutils       | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| html5lib       | 44.0 ms                                                | 36.4 ms: 1.21x faster                                                 |
| tornado_http   | 90.1 ms                                                | 70.1 ms: 1.29x faster                                                 |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.3 ms: 1.40x faster                                                 |
| nbody          | 94.6 ms                                                | 64.0 ms: 1.48x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.3 ms: 1.28x faster                                                 |
| regex_dna      | 164 ms                                                 | 151 ms: 1.09x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.72 ms: 1.11x slower                                                 |
| regex_v8       | 17.7 ms                                                | 16.4 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.10 ms: 1.37x faster                                                 |
| json_loads           | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| pickle               | 7.50 us                                                | 7.59 us: 1.01x slower                                                 |
| pickle_list          | 2.83 us                                                | 2.85 us: 1.01x slower                                                 |
| pickle_pure_python   | 284 us                                                 | 198 us: 1.43x faster                                                  |
| unpickle             | 10.0 us                                                | 9.64 us: 1.04x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.58 us: 1.03x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 160 us: 1.27x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 95.9 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 64.5 ms: 1.07x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 47.2 ms: 1.16x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 34.5 ms: 1.31x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                          |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.07 ms: 1.06x faster                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.16 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 20.9 ms: 1.30x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.1 ms: 1.20x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 29.9 ms: 1.26x faster                                                 |
| mako            | 10.6 ms                                                | 7.97 ms: 1.33x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.27x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| async_generators        | 231 ms                                                 | 199 ms: 1.16x faster                                                  |
| async_tree_none         | 396 ms                                                 | 284 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 530 ms: 1.26x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 734 ms: 1.38x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 381 ms: 1.27x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.59 ms: 1.28x faster                                                 |
| chaos                   | 66.5 ms                                                | 49.5 ms: 1.34x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 449 us: 1.18x faster                                                  |
| coroutines              | 20.1 ms                                                | 19.3 ms: 1.04x faster                                                 |
| coverage                | 40.8 ms                                                | 54.3 ms: 1.33x slower                                                 |
| crypto_pyaes            | 77.9 ms                                                | 51.1 ms: 1.52x faster                                                 |
| deepcopy                | 278 us                                                 | 215 us: 1.29x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.85 us: 1.28x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 24.8 us: 1.39x faster                                                 |
| deltablue               | 5.37 ms                                                | 2.84 ms: 1.89x faster                                                 |
| django_template         | 27.2 ms                                                | 20.9 ms: 1.30x faster                                                 |
| docutils                | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| dulwich_log             | 36.4 ms                                                | 29.5 ms: 1.24x faster                                                 |
| fannkuch                | 318 ms                                                 | 268 ms: 1.19x faster                                                  |
| flaskblogging           | 2.59 ms                                                | 2.22 ms: 1.16x faster                                                 |
| float                   | 72.1 ms                                                | 51.3 ms: 1.40x faster                                                 |
| generators              | 32.5 ms                                                | 29.1 ms: 1.12x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.1 ms: 1.20x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 29.9 ms: 1.26x faster                                                 |
| go                      | 165 ms                                                 | 117 ms: 1.41x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.84 ms: 1.30x faster                                                 |
| html5lib                | 44.0 ms                                                | 36.4 ms: 1.21x faster                                                 |
| json                    | 3.13 ms                                                | 2.82 ms: 1.11x faster                                                 |
| json_dumps              | 8.34 ms                                                | 6.10 ms: 1.37x faster                                                 |
| json_loads              | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| logging_format          | 4.95 us                                                | 3.92 us: 1.26x faster                                                 |
| logging_silent          | 119 ns                                                 | 64.5 ns: 1.85x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.63 us: 1.27x faster                                                 |
| mako                    | 10.6 ms                                                | 7.97 ms: 1.33x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.55 sec: 1.07x faster                                                |
| meteor_contest          | 77.7 ms                                                | 77.0 ms: 1.01x faster                                                 |
| mypy                    | 521 ms                                                 | 418 ms: 1.25x faster                                                  |
| nbody                   | 94.6 ms                                                | 64.0 ms: 1.48x faster                                                 |
| nqueens                 | 68.6 ms                                                | 58.7 ms: 1.17x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.8 ms: 1.07x faster                                                 |
| pickle                  | 7.50 us                                                | 7.59 us: 1.01x slower                                                 |
| pickle_list             | 2.83 us                                                | 2.85 us: 1.01x slower                                                 |
| pickle_pure_python      | 284 us                                                 | 198 us: 1.43x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 468 ms: 1.30x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 949 ms: 1.31x faster                                                  |
| pycparser               | 915 ms                                                 | 711 ms: 1.29x faster                                                  |
| pyflate                 | 454 ms                                                 | 345 ms: 1.32x faster                                                  |
| pylint                  | 302 ms                                                 | 264 ms: 1.14x faster                                                  |
| python_startup          | 9.59 ms                                                | 9.07 ms: 1.06x faster                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.16 ms: 1.02x slower                                                 |
| raytrace                | 329 ms                                                 | 211 ms: 1.56x faster                                                  |
| regex_compile           | 96.2 ms                                                | 75.3 ms: 1.28x faster                                                 |
| regex_dna               | 164 ms                                                 | 151 ms: 1.09x faster                                                  |
| regex_effbot            | 2.45 ms                                                | 2.72 ms: 1.11x slower                                                 |
| regex_v8                | 17.7 ms                                                | 16.4 ms: 1.08x faster                                                 |
| richards                | 51.4 ms                                                | 33.4 ms: 1.54x faster                                                 |
| scimark_fft             | 231 ms                                                 | 197 ms: 1.17x faster                                                  |
| scimark_lu              | 110 ms                                                 | 72.7 ms: 1.51x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 53.8 ms: 1.34x faster                                                 |
| scimark_sor             | 126 ms                                                 | 99.0 ms: 1.27x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.80 ms: 1.24x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 71.7 ms: 1.34x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 61.5 ms: 1.21x faster                                                 |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.12 ms: 1.26x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.00 ms: 1.32x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.16 ms: 1.33x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 31.7 ms: 1.20x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 172 ms: 1.16x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.40 us: 1.07x faster                                                 |
| sympy_expand            | 275 ms                                                 | 247 ms: 1.12x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.5 ms: 1.16x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 84.0 ms: 1.11x faster                                                 |
| sympy_str               | 169 ms                                                 | 152 ms: 1.12x faster                                                  |
| telco                   | 3.63 ms                                                | 3.34 ms: 1.09x faster                                                 |
| thrift                  | 577 us                                                 | 441 us: 1.31x faster                                                  |
| tornado_http            | 90.1 ms                                                | 70.1 ms: 1.29x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 33.0 ns: 1.16x faster                                                 |
| unpickle                | 10.0 us                                                | 9.64 us: 1.04x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.58 us: 1.03x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 160 us: 1.27x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 95.9 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 64.5 ms: 1.07x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 47.2 ms: 1.16x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 34.5 ms: 1.31x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (2): bench_mp_pool, pickle_dict
Ignored benchmarks (2) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, gunicorn
