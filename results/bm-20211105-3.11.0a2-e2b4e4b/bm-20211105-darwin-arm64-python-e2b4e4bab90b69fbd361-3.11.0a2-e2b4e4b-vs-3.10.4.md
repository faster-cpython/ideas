Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 186 ms: 1.19x faster                                                  |
| chameleon      | 5.86 ms                                                | 5.09 ms: 1.15x faster                                                 |
| docutils       | 1.76 sec                                               | 1.53 sec: 1.15x faster                                                |
| html5lib       | 44.0 ms                                                | 36.5 ms: 1.20x faster                                                 |
| tornado_http   | 90.1 ms                                                | 75.9 ms: 1.19x faster                                                 |
| Geometric mean | (ref)                                                  | 1.18x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.6 ms: 1.40x faster                                                 |
| nbody          | 94.6 ms                                                | 74.0 ms: 1.28x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.22x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 77.9 ms: 1.23x faster                                                 |
| regex_effbot   | 2.45 ms                                                | 2.47 ms: 1.01x slower                                                 |
| regex_v8       | 17.7 ms                                                | 18.1 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 7.80 ms: 1.07x faster                                                 |
| json_loads           | 17.0 us                                                | 16.8 us: 1.02x faster                                                 |
| pickle               | 7.50 us                                                | 7.28 us: 1.03x faster                                                 |
| pickle_dict          | 18.0 us                                                | 17.7 us: 1.02x faster                                                 |
| pickle_list          | 2.83 us                                                | 2.84 us: 1.01x slower                                                 |
| pickle_pure_python   | 284 us                                                 | 227 us: 1.25x faster                                                  |
| unpickle_list        | 2.66 us                                                | 2.52 us: 1.05x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 174 us: 1.17x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 95.7 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 66.5 ms: 1.04x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 48.7 ms: 1.12x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 36.8 ms: 1.22x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 13.6 ms: 1.42x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.30 ms: 1.04x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 22.7 ms: 1.20x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.7 ms: 1.16x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 31.1 ms: 1.21x faster                                                 |
| mako            | 10.6 ms                                                | 8.49 ms: 1.25x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.20x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 186 ms: 1.19x faster                                                  |
| async_generators        | 231 ms                                                 | 197 ms: 1.17x faster                                                  |
| async_tree_none         | 396 ms                                                 | 290 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 579 ms: 1.15x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 779 ms: 1.30x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 360 ms: 1.35x faster                                                  |
| chameleon               | 5.86 ms                                                | 5.09 ms: 1.15x faster                                                 |
| chaos                   | 66.5 ms                                                | 49.0 ms: 1.36x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 496 us: 1.07x faster                                                  |
| coroutines              | 20.1 ms                                                | 19.2 ms: 1.05x faster                                                 |
| coverage                | 40.8 ms                                                | 43.0 ms: 1.05x slower                                                 |
| crypto_pyaes            | 77.9 ms                                                | 58.1 ms: 1.34x faster                                                 |
| deepcopy                | 278 us                                                 | 237 us: 1.17x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.04 us: 1.16x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 27.8 us: 1.24x faster                                                 |
| deltablue               | 5.37 ms                                                | 3.19 ms: 1.68x faster                                                 |
| django_template         | 27.2 ms                                                | 22.7 ms: 1.20x faster                                                 |
| docutils                | 1.76 sec                                               | 1.53 sec: 1.15x faster                                                |
| dulwich_log             | 36.4 ms                                                | 30.0 ms: 1.21x faster                                                 |
| fannkuch                | 318 ms                                                 | 280 ms: 1.14x faster                                                  |
| flaskblogging           | 2.59 ms                                                | 2.76 ms: 1.07x slower                                                 |
| float                   | 72.1 ms                                                | 51.6 ms: 1.40x faster                                                 |
| generators              | 32.5 ms                                                | 28.2 ms: 1.15x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.7 ms: 1.16x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 31.1 ms: 1.21x faster                                                 |
| go                      | 165 ms                                                 | 119 ms: 1.39x faster                                                  |
| gunicorn                | 1.28 ms                                                | 1.13 ms: 1.13x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.91 ms: 1.29x faster                                                 |
| html5lib                | 44.0 ms                                                | 36.5 ms: 1.20x faster                                                 |
| json                    | 3.13 ms                                                | 3.03 ms: 1.03x faster                                                 |
| json_dumps              | 8.34 ms                                                | 7.80 ms: 1.07x faster                                                 |
| json_loads              | 17.0 us                                                | 16.8 us: 1.02x faster                                                 |
| logging_format          | 4.95 us                                                | 3.72 us: 1.33x faster                                                 |
| logging_silent          | 119 ns                                                 | 82.6 ns: 1.44x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.45 us: 1.34x faster                                                 |
| mako                    | 10.6 ms                                                | 8.49 ms: 1.25x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.56 sec: 1.06x faster                                                |
| meteor_contest          | 77.7 ms                                                | 74.3 ms: 1.05x faster                                                 |
| nbody                   | 94.6 ms                                                | 74.0 ms: 1.28x faster                                                 |
| nqueens                 | 68.6 ms                                                | 61.3 ms: 1.12x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.5 ms: 1.08x faster                                                 |
| pickle                  | 7.50 us                                                | 7.28 us: 1.03x faster                                                 |
| pickle_dict             | 18.0 us                                                | 17.7 us: 1.02x faster                                                 |
| pickle_list             | 2.83 us                                                | 2.84 us: 1.01x slower                                                 |
| pickle_pure_python      | 284 us                                                 | 227 us: 1.25x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 500 ms: 1.21x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 1.02 sec: 1.21x faster                                                |
| pycparser               | 915 ms                                                 | 766 ms: 1.19x faster                                                  |
| pyflate                 | 454 ms                                                 | 361 ms: 1.26x faster                                                  |
| pylint                  | 302 ms                                                 | 276 ms: 1.09x faster                                                  |
| python_startup          | 9.59 ms                                                | 13.6 ms: 1.42x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.30 ms: 1.04x slower                                                 |
| raytrace                | 329 ms                                                 | 208 ms: 1.58x faster                                                  |
| regex_compile           | 96.2 ms                                                | 77.9 ms: 1.23x faster                                                 |
| regex_effbot            | 2.45 ms                                                | 2.47 ms: 1.01x slower                                                 |
| regex_v8                | 17.7 ms                                                | 18.1 ms: 1.02x slower                                                 |
| richards                | 51.4 ms                                                | 37.4 ms: 1.37x faster                                                 |
| scimark_fft             | 231 ms                                                 | 202 ms: 1.15x faster                                                  |
| scimark_lu              | 110 ms                                                 | 93.9 ms: 1.17x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 48.8 ms: 1.48x faster                                                 |
| scimark_sor             | 126 ms                                                 | 98.8 ms: 1.28x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.24 ms: 1.07x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 75.0 ms: 1.28x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.23 ms: 1.08x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.40 ms: 1.10x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 33.5 ms: 1.14x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 174 ms: 1.14x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.39 us: 1.08x faster                                                 |
| sympy_expand            | 275 ms                                                 | 254 ms: 1.08x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 12.1 ms: 1.09x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 86.0 ms: 1.09x faster                                                 |
| sympy_str               | 169 ms                                                 | 157 ms: 1.08x faster                                                  |
| telco                   | 3.63 ms                                                | 3.40 ms: 1.07x faster                                                 |
| thrift                  | 577 us                                                 | 465 us: 1.24x faster                                                  |
| tornado_http            | 90.1 ms                                                | 75.9 ms: 1.19x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 31.2 ns: 1.23x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.52 us: 1.05x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 174 us: 1.17x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 95.7 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 66.5 ms: 1.04x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 48.7 ms: 1.12x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 36.8 ms: 1.22x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.15x faster                                                          |

Benchmark hidden because not significant (3): bench_mp_pool, regex_dna, unpickle
Ignored benchmarks (4) of public/results/bm-20220323-python-v3.10.4-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, mypy, sqlalchemy_declarative, sqlalchemy_imperative
