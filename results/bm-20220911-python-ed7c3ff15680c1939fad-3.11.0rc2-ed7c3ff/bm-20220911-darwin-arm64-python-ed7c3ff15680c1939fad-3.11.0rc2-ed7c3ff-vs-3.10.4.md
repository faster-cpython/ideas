Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 181 ms: 1.23x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.63 ms: 1.26x faster                                                  |
| docutils       | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                 |
| html5lib       | 44.0 ms                                                | 34.7 ms: 1.27x faster                                                  |
| tornado_http   | 90.1 ms                                                | 70.0 ms: 1.29x faster                                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 52.9 ms: 1.36x faster                                                  |
| nbody          | 94.6 ms                                                | 65.5 ms: 1.44x faster                                                  |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                  | 1.26x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 76.4 ms: 1.26x faster                                                  |
| regex_dna      | 164 ms                                                 | 152 ms: 1.09x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                  |
| regex_v8       | 17.7 ms                                                | 16.4 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 7.58 ms: 1.10x faster                                                  |
| json_loads           | 17.0 us                                                | 16.2 us: 1.05x faster                                                  |
| pickle               | 7.50 us                                                | 7.22 us: 1.04x faster                                                  |
| pickle_list          | 2.83 us                                                | 2.85 us: 1.01x slower                                                  |
| pickle_pure_python   | 284 us                                                 | 199 us: 1.42x faster                                                   |
| unpickle             | 10.0 us                                                | 9.74 us: 1.03x faster                                                  |
| unpickle_list        | 2.66 us                                                | 2.64 us: 1.01x faster                                                  |
| unpickle_pure_python | 204 us                                                 | 159 us: 1.28x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 99.5 ms: 1.01x faster                                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 65.7 ms: 1.05x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.3 ms: 1.13x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 35.1 ms: 1.28x faster                                                  |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.21 ms: 1.04x faster                                                  |
| python_startup_no_site | 7.00 ms                                                | 7.27 ms: 1.04x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.1 ms: 1.29x faster                                                  |
| genshi_text     | 18.2 ms                                                | 15.2 ms: 1.20x faster                                                  |
| genshi_xml      | 37.7 ms                                                | 30.1 ms: 1.25x faster                                                  |
| mako            | 10.6 ms                                                | 8.39 ms: 1.26x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.25x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 181 ms: 1.23x faster                                                   |
| aiohttp                 | 1.19 ms                                                | 1.04 ms: 1.14x faster                                                  |
| async_generators        | 231 ms                                                 | 195 ms: 1.18x faster                                                   |
| async_tree_none         | 396 ms                                                 | 281 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed | 665 ms                                                 | 529 ms: 1.26x faster                                                   |
| async_tree_io           | 1.01 sec                                               | 698 ms: 1.45x faster                                                   |
| async_tree_memoization  | 485 ms                                                 | 317 ms: 1.53x faster                                                   |
| chameleon               | 5.86 ms                                                | 4.63 ms: 1.26x faster                                                  |
| chaos                   | 66.5 ms                                                | 49.3 ms: 1.35x faster                                                  |
| bench_mp_pool           | 40.8 ms                                                | 41.9 ms: 1.03x slower                                                  |
| bench_thread_pool       | 531 us                                                 | 458 us: 1.16x faster                                                   |
| coroutines              | 20.1 ms                                                | 17.6 ms: 1.14x faster                                                  |
| crypto_pyaes            | 77.9 ms                                                | 51.8 ms: 1.51x faster                                                  |
| deepcopy                | 278 us                                                 | 222 us: 1.25x faster                                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.90 us: 1.24x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 26.3 us: 1.31x faster                                                  |
| deltablue               | 5.37 ms                                                | 2.82 ms: 1.90x faster                                                  |
| django_template         | 27.2 ms                                                | 21.1 ms: 1.29x faster                                                  |
| docutils                | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                 |
| dulwich_log             | 36.4 ms                                                | 29.0 ms: 1.26x faster                                                  |
| fannkuch                | 318 ms                                                 | 263 ms: 1.21x faster                                                   |
| flaskblogging           | 2.59 ms                                                | 2.28 ms: 1.13x faster                                                  |
| float                   | 72.1 ms                                                | 52.9 ms: 1.36x faster                                                  |
| generators              | 32.5 ms                                                | 28.4 ms: 1.14x faster                                                  |
| genshi_text             | 18.2 ms                                                | 15.2 ms: 1.20x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 30.1 ms: 1.25x faster                                                  |
| go                      | 165 ms                                                 | 109 ms: 1.51x faster                                                   |
| gunicorn                | 1.28 ms                                                | 1.10 ms: 1.16x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.72 ms: 1.34x faster                                                  |
| html5lib                | 44.0 ms                                                | 34.7 ms: 1.27x faster                                                  |
| json                    | 3.13 ms                                                | 2.83 ms: 1.10x faster                                                  |
| json_dumps              | 8.34 ms                                                | 7.58 ms: 1.10x faster                                                  |
| json_loads              | 17.0 us                                                | 16.2 us: 1.05x faster                                                  |
| logging_format          | 4.95 us                                                | 3.73 us: 1.33x faster                                                  |
| logging_silent          | 119 ns                                                 | 67.5 ns: 1.77x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.45 us: 1.33x faster                                                  |
| mako                    | 10.6 ms                                                | 8.39 ms: 1.26x faster                                                  |
| mdp                     | 1.66 sec                                               | 1.54 sec: 1.08x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 74.0 ms: 1.05x faster                                                  |
| mypy                    | 521 ms                                                 | 418 ms: 1.25x faster                                                   |
| nbody                   | 94.6 ms                                                | 65.5 ms: 1.44x faster                                                  |
| nqueens                 | 68.6 ms                                                | 59.5 ms: 1.15x faster                                                  |
| pathlib                 | 22.2 ms                                                | 20.8 ms: 1.07x faster                                                  |
| pickle                  | 7.50 us                                                | 7.22 us: 1.04x faster                                                  |
| pickle_list             | 2.83 us                                                | 2.85 us: 1.01x slower                                                  |
| pickle_pure_python      | 284 us                                                 | 199 us: 1.42x faster                                                   |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                                   |
| pprint_safe_repr        | 608 ms                                                 | 467 ms: 1.30x faster                                                   |
| pprint_pformat          | 1.24 sec                                               | 954 ms: 1.30x faster                                                   |
| pycparser               | 915 ms                                                 | 696 ms: 1.31x faster                                                   |
| pyflate                 | 454 ms                                                 | 313 ms: 1.45x faster                                                   |
| pylint                  | 302 ms                                                 | 265 ms: 1.14x faster                                                   |
| python_startup          | 9.59 ms                                                | 9.21 ms: 1.04x faster                                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.27 ms: 1.04x slower                                                  |
| raytrace                | 329 ms                                                 | 207 ms: 1.59x faster                                                   |
| regex_compile           | 96.2 ms                                                | 76.4 ms: 1.26x faster                                                  |
| regex_dna               | 164 ms                                                 | 152 ms: 1.09x faster                                                   |
| regex_effbot            | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                  |
| regex_v8                | 17.7 ms                                                | 16.4 ms: 1.08x faster                                                  |
| richards                | 51.4 ms                                                | 32.8 ms: 1.57x faster                                                  |
| scimark_fft             | 231 ms                                                 | 201 ms: 1.15x faster                                                   |
| scimark_lu              | 110 ms                                                 | 72.3 ms: 1.52x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 46.8 ms: 1.54x faster                                                  |
| scimark_sor             | 126 ms                                                 | 83.0 ms: 1.52x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.24 ms: 1.07x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 72.7 ms: 1.32x faster                                                  |
| sqlalchemy_declarative  | 74.4 ms                                                | 62.4 ms: 1.19x faster                                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.24 ms: 1.25x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 953 us: 1.39x faster                                                   |
| sqlglot_transpile       | 1.54 ms                                                | 1.11 ms: 1.38x faster                                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.2 ms: 1.22x faster                                                  |
| sqlglot_normalize       | 198 ms                                                 | 171 ms: 1.16x faster                                                   |
| sqlite_synth            | 1.50 us                                                | 1.29 us: 1.16x faster                                                  |
| sympy_expand            | 275 ms                                                 | 242 ms: 1.14x faster                                                   |
| sympy_integrate         | 13.3 ms                                                | 11.5 ms: 1.16x faster                                                  |
| sympy_sum               | 93.5 ms                                                | 85.5 ms: 1.09x faster                                                  |
| sympy_str               | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| telco                   | 3.63 ms                                                | 3.40 ms: 1.07x faster                                                  |
| thrift                  | 577 us                                                 | 429 us: 1.35x faster                                                   |
| tornado_http            | 90.1 ms                                                | 70.0 ms: 1.29x faster                                                  |
| unpack_sequence         | 38.2 ns                                                | 33.1 ns: 1.15x faster                                                  |
| unpickle                | 10.0 us                                                | 9.74 us: 1.03x faster                                                  |
| unpickle_list           | 2.66 us                                                | 2.64 us: 1.01x faster                                                  |
| unpickle_pure_python    | 204 us                                                 | 159 us: 1.28x faster                                                   |
| xml_etree_parse         | 100 ms                                                 | 99.5 ms: 1.01x faster                                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 65.7 ms: 1.05x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 48.3 ms: 1.13x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 35.1 ms: 1.28x faster                                                  |
| Geometric mean          | (ref)                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (1) of public/results/bm-20220323-python-v3.10.4-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: coverage
