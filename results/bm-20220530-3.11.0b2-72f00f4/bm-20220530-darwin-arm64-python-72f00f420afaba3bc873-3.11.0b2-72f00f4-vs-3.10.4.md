Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 182 ms: 1.22x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.71 ms: 1.24x faster                                                 |
| docutils       | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                |
| html5lib       | 44.0 ms                                                | 35.9 ms: 1.23x faster                                                 |
| tornado_http   | 90.1 ms                                                | 69.6 ms: 1.30x faster                                                 |
| Geometric mean | (ref)                                                  | 1.24x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 55.0 ms: 1.31x faster                                                 |
| nbody          | 94.6 ms                                                | 63.9 ms: 1.48x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 77.4 ms: 1.24x faster                                                 |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.39 ms: 1.02x faster                                                 |
| regex_v8       | 17.7 ms                                                | 16.6 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                  | 1.11x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 7.63 ms: 1.09x faster                                                 |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                                 |
| pickle               | 7.50 us                                                | 7.12 us: 1.05x faster                                                 |
| pickle_dict          | 18.0 us                                                | 17.2 us: 1.04x faster                                                 |
| pickle_list          | 2.83 us                                                | 2.71 us: 1.04x faster                                                 |
| pickle_pure_python   | 284 us                                                 | 223 us: 1.27x faster                                                  |
| unpickle_list        | 2.66 us                                                | 2.71 us: 1.02x slower                                                 |
| unpickle_pure_python | 204 us                                                 | 175 us: 1.16x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 99.3 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 65.3 ms: 1.06x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 48.2 ms: 1.13x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 34.7 ms: 1.30x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.15 ms: 1.05x faster                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.20 ms: 1.03x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.0 ms: 1.30x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.4 ms: 1.18x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 31.3 ms: 1.20x faster                                                 |
| mako            | 10.6 ms                                                | 8.38 ms: 1.26x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.24x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 182 ms: 1.22x faster                                                  |
| aiohttp                 | 1.19 ms                                                | 1.05 ms: 1.13x faster                                                 |
| async_generators        | 231 ms                                                 | 198 ms: 1.17x faster                                                  |
| async_tree_none         | 396 ms                                                 | 287 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 534 ms: 1.24x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 702 ms: 1.44x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 344 ms: 1.41x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.71 ms: 1.24x faster                                                 |
| chaos                   | 66.5 ms                                                | 49.4 ms: 1.35x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 462 us: 1.15x faster                                                  |
| coroutines              | 20.1 ms                                                | 17.4 ms: 1.15x faster                                                 |
| crypto_pyaes            | 77.9 ms                                                | 51.6 ms: 1.51x faster                                                 |
| deepcopy                | 278 us                                                 | 239 us: 1.17x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.05 us: 1.15x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 28.5 us: 1.21x faster                                                 |
| deltablue               | 5.37 ms                                                | 2.84 ms: 1.89x faster                                                 |
| django_template         | 27.2 ms                                                | 21.0 ms: 1.30x faster                                                 |
| docutils                | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                |
| dulwich_log             | 36.4 ms                                                | 29.4 ms: 1.24x faster                                                 |
| fannkuch                | 318 ms                                                 | 260 ms: 1.22x faster                                                  |
| float                   | 72.1 ms                                                | 55.0 ms: 1.31x faster                                                 |
| generators              | 32.5 ms                                                | 27.6 ms: 1.18x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.4 ms: 1.18x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 31.3 ms: 1.20x faster                                                 |
| go                      | 165 ms                                                 | 108 ms: 1.53x faster                                                  |
| gunicorn                | 1.28 ms                                                | 1.13 ms: 1.13x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.70 ms: 1.34x faster                                                 |
| html5lib                | 44.0 ms                                                | 35.9 ms: 1.23x faster                                                 |
| json                    | 3.13 ms                                                | 2.92 ms: 1.07x faster                                                 |
| json_dumps              | 8.34 ms                                                | 7.63 ms: 1.09x faster                                                 |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                                 |
| logging_format          | 4.95 us                                                | 3.74 us: 1.32x faster                                                 |
| logging_silent          | 119 ns                                                 | 65.4 ns: 1.82x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.46 us: 1.33x faster                                                 |
| mako                    | 10.6 ms                                                | 8.38 ms: 1.26x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.53 sec: 1.09x faster                                                |
| meteor_contest          | 77.7 ms                                                | 77.4 ms: 1.00x faster                                                 |
| mypy                    | 521 ms                                                 | 416 ms: 1.25x faster                                                  |
| nbody                   | 94.6 ms                                                | 63.9 ms: 1.48x faster                                                 |
| nqueens                 | 68.6 ms                                                | 58.7 ms: 1.17x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.6 ms: 1.08x faster                                                 |
| pickle                  | 7.50 us                                                | 7.12 us: 1.05x faster                                                 |
| pickle_dict             | 18.0 us                                                | 17.2 us: 1.04x faster                                                 |
| pickle_list             | 2.83 us                                                | 2.71 us: 1.04x faster                                                 |
| pickle_pure_python      | 284 us                                                 | 223 us: 1.27x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 490 ms: 1.24x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 1.01 sec: 1.23x faster                                                |
| pycparser               | 915 ms                                                 | 703 ms: 1.30x faster                                                  |
| pyflate                 | 454 ms                                                 | 316 ms: 1.44x faster                                                  |
| pylint                  | 302 ms                                                 | 263 ms: 1.14x faster                                                  |
| python_startup          | 9.59 ms                                                | 9.15 ms: 1.05x faster                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.20 ms: 1.03x slower                                                 |
| raytrace                | 329 ms                                                 | 210 ms: 1.57x faster                                                  |
| regex_compile           | 96.2 ms                                                | 77.4 ms: 1.24x faster                                                 |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| regex_effbot            | 2.45 ms                                                | 2.39 ms: 1.02x faster                                                 |
| regex_v8                | 17.7 ms                                                | 16.6 ms: 1.07x faster                                                 |
| richards                | 51.4 ms                                                | 33.5 ms: 1.53x faster                                                 |
| scimark_fft             | 231 ms                                                 | 200 ms: 1.16x faster                                                  |
| scimark_lu              | 110 ms                                                 | 71.4 ms: 1.54x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 48.7 ms: 1.48x faster                                                 |
| scimark_sor             | 126 ms                                                 | 75.5 ms: 1.67x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.20 ms: 1.08x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 72.2 ms: 1.33x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 61.5 ms: 1.21x faster                                                 |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.26 ms: 1.24x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.19 ms: 1.12x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.35 ms: 1.14x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 31.4 ms: 1.21x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 170 ms: 1.17x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.35 us: 1.11x faster                                                 |
| sympy_expand            | 275 ms                                                 | 243 ms: 1.13x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.5 ms: 1.15x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 82.2 ms: 1.14x faster                                                 |
| sympy_str               | 169 ms                                                 | 150 ms: 1.13x faster                                                  |
| telco                   | 3.63 ms                                                | 3.41 ms: 1.06x faster                                                 |
| thrift                  | 577 us                                                 | 437 us: 1.32x faster                                                  |
| tornado_http            | 90.1 ms                                                | 69.6 ms: 1.30x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 32.2 ns: 1.19x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.71 us: 1.02x slower                                                 |
| unpickle_pure_python    | 204 us                                                 | 175 us: 1.16x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 99.3 ms: 1.01x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 65.3 ms: 1.06x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 48.2 ms: 1.13x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 34.7 ms: 1.30x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (2): bench_mp_pool, unpickle
Ignored benchmarks (2) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: coverage, flaskblogging
