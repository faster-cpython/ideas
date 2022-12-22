Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 186 ms: 1.20x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.64 ms: 1.26x faster                                                  |
| docutils       | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                 |
| html5lib       | 44.0 ms                                                | 36.1 ms: 1.22x faster                                                  |
| tornado_http   | 90.1 ms                                                | 68.3 ms: 1.32x faster                                                  |
| Geometric mean | (ref)                                                  | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 56.4 ms: 1.28x faster                                                  |
| nbody          | 94.6 ms                                                | 65.0 ms: 1.45x faster                                                  |
| pidigits       | 284 ms                                                 | 283 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                  | 1.23x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.9 ms: 1.27x faster                                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.61 ms: 1.06x slower                                                  |
| regex_v8       | 17.7 ms                                                | 16.0 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.07 ms: 1.37x faster                                                  |
| json_loads           | 17.0 us                                                | 16.4 us: 1.04x faster                                                  |
| pickle               | 7.50 us                                                | 7.54 us: 1.00x slower                                                  |
| pickle_list          | 2.83 us                                                | 2.85 us: 1.01x slower                                                  |
| pickle_pure_python   | 284 us                                                 | 210 us: 1.35x faster                                                   |
| unpickle             | 10.0 us                                                | 9.84 us: 1.02x faster                                                  |
| unpickle_list        | 2.66 us                                                | 2.59 us: 1.03x faster                                                  |
| unpickle_pure_python | 204 us                                                 | 161 us: 1.27x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 93.2 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 66.4 ms: 1.04x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.7 ms: 1.12x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 35.2 ms: 1.28x faster                                                  |
| Geometric mean       | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.29 ms: 1.03x faster                                                  |
| python_startup_no_site | 7.00 ms                                                | 7.33 ms: 1.05x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.6 ms: 1.26x faster                                                  |
| genshi_text     | 18.2 ms                                                | 15.2 ms: 1.20x faster                                                  |
| genshi_xml      | 37.7 ms                                                | 29.6 ms: 1.28x faster                                                  |
| mako            | 10.6 ms                                                | 8.24 ms: 1.29x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.25x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 186 ms: 1.20x faster                                                   |
| async_generators        | 231 ms                                                 | 204 ms: 1.13x faster                                                   |
| async_tree_none         | 396 ms                                                 | 286 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed | 665 ms                                                 | 539 ms: 1.23x faster                                                   |
| async_tree_io           | 1.01 sec                                               | 733 ms: 1.38x faster                                                   |
| async_tree_memoization  | 485 ms                                                 | 323 ms: 1.50x faster                                                   |
| chameleon               | 5.86 ms                                                | 4.64 ms: 1.26x faster                                                  |
| chaos                   | 66.5 ms                                                | 51.1 ms: 1.30x faster                                                  |
| bench_mp_pool           | 40.8 ms                                                | 42.1 ms: 1.03x slower                                                  |
| bench_thread_pool       | 531 us                                                 | 456 us: 1.16x faster                                                   |
| coroutines              | 20.1 ms                                                | 20.0 ms: 1.00x faster                                                  |
| coverage                | 40.8 ms                                                | 58.2 ms: 1.43x slower                                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.4 ms: 1.46x faster                                                  |
| deepcopy                | 278 us                                                 | 240 us: 1.16x faster                                                   |
| deepcopy_reduce         | 2.36 us                                                | 2.04 us: 1.16x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 29.5 us: 1.17x faster                                                  |
| deltablue               | 5.37 ms                                                | 2.81 ms: 1.91x faster                                                  |
| django_template         | 27.2 ms                                                | 21.6 ms: 1.26x faster                                                  |
| docutils                | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                 |
| dulwich_log             | 36.4 ms                                                | 29.3 ms: 1.24x faster                                                  |
| fannkuch                | 318 ms                                                 | 276 ms: 1.15x faster                                                   |
| float                   | 72.1 ms                                                | 56.4 ms: 1.28x faster                                                  |
| generators              | 32.5 ms                                                | 34.1 ms: 1.05x slower                                                  |
| genshi_text             | 18.2 ms                                                | 15.2 ms: 1.20x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 29.6 ms: 1.28x faster                                                  |
| go                      | 165 ms                                                 | 118 ms: 1.39x faster                                                   |
| hexiom                  | 6.31 ms                                                | 4.93 ms: 1.28x faster                                                  |
| html5lib                | 44.0 ms                                                | 36.1 ms: 1.22x faster                                                  |
| json                    | 3.13 ms                                                | 2.86 ms: 1.09x faster                                                  |
| json_dumps              | 8.34 ms                                                | 6.07 ms: 1.37x faster                                                  |
| json_loads              | 17.0 us                                                | 16.4 us: 1.04x faster                                                  |
| logging_format          | 4.95 us                                                | 3.91 us: 1.27x faster                                                  |
| logging_silent          | 119 ns                                                 | 64.4 ns: 1.85x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.62 us: 1.27x faster                                                  |
| mako                    | 10.6 ms                                                | 8.24 ms: 1.29x faster                                                  |
| mdp                     | 1.66 sec                                               | 1.54 sec: 1.08x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 77.2 ms: 1.01x faster                                                  |
| mypy                    | 521 ms                                                 | 418 ms: 1.25x faster                                                   |
| nbody                   | 94.6 ms                                                | 65.0 ms: 1.45x faster                                                  |
| nqueens                 | 68.6 ms                                                | 61.9 ms: 1.11x faster                                                  |
| pathlib                 | 22.2 ms                                                | 20.6 ms: 1.08x faster                                                  |
| pickle                  | 7.50 us                                                | 7.54 us: 1.00x slower                                                  |
| pickle_list             | 2.83 us                                                | 2.85 us: 1.01x slower                                                  |
| pickle_pure_python      | 284 us                                                 | 210 us: 1.35x faster                                                   |
| pidigits                | 284 ms                                                 | 283 ms: 1.00x faster                                                   |
| pprint_safe_repr        | 608 ms                                                 | 491 ms: 1.24x faster                                                   |
| pprint_pformat          | 1.24 sec                                               | 1.00 sec: 1.23x faster                                                 |
| pycparser               | 915 ms                                                 | 702 ms: 1.30x faster                                                   |
| pyflate                 | 454 ms                                                 | 356 ms: 1.28x faster                                                   |
| python_startup          | 9.59 ms                                                | 9.29 ms: 1.03x faster                                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.33 ms: 1.05x slower                                                  |
| raytrace                | 329 ms                                                 | 220 ms: 1.50x faster                                                   |
| regex_compile           | 96.2 ms                                                | 75.9 ms: 1.27x faster                                                  |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| regex_effbot            | 2.45 ms                                                | 2.61 ms: 1.06x slower                                                  |
| regex_v8                | 17.7 ms                                                | 16.0 ms: 1.11x faster                                                  |
| richards                | 51.4 ms                                                | 31.3 ms: 1.64x faster                                                  |
| scimark_fft             | 231 ms                                                 | 198 ms: 1.16x faster                                                   |
| scimark_lu              | 110 ms                                                 | 71.0 ms: 1.55x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 56.3 ms: 1.28x faster                                                  |
| scimark_sor             | 126 ms                                                 | 99.3 ms: 1.27x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.83 ms: 1.22x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 73.7 ms: 1.30x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 996 us: 1.33x faster                                                   |
| sqlglot_transpile       | 1.54 ms                                                | 1.17 ms: 1.32x faster                                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.6 ms: 1.20x faster                                                  |
| sqlglot_normalize       | 198 ms                                                 | 173 ms: 1.15x faster                                                   |
| sqlite_synth            | 1.50 us                                                | 1.43 us: 1.05x faster                                                  |
| sympy_expand            | 275 ms                                                 | 247 ms: 1.11x faster                                                   |
| sympy_integrate         | 13.3 ms                                                | 11.8 ms: 1.13x faster                                                  |
| sympy_sum               | 93.5 ms                                                | 86.6 ms: 1.08x faster                                                  |
| sympy_str               | 169 ms                                                 | 155 ms: 1.09x faster                                                   |
| telco                   | 3.63 ms                                                | 3.43 ms: 1.06x faster                                                  |
| thrift                  | 577 us                                                 | 438 us: 1.32x faster                                                   |
| tornado_http            | 90.1 ms                                                | 68.3 ms: 1.32x faster                                                  |
| unpack_sequence         | 38.2 ns                                                | 62.7 ns: 1.64x slower                                                  |
| unpickle                | 10.0 us                                                | 9.84 us: 1.02x faster                                                  |
| unpickle_list           | 2.66 us                                                | 2.59 us: 1.03x faster                                                  |
| unpickle_pure_python    | 204 us                                                 | 161 us: 1.27x faster                                                   |
| xml_etree_parse         | 100 ms                                                 | 93.2 ms: 1.07x faster                                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 66.4 ms: 1.04x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 48.7 ms: 1.12x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 35.2 ms: 1.28x faster                                                  |
| Geometric mean          | (ref)                                                  | 1.19x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (6) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
