Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 179 ms: 1.24x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.28 ms: 1.37x faster                                                  |
| docutils       | 1.76 sec                                               | 1.44 sec: 1.23x faster                                                 |
| html5lib       | 44.0 ms                                                | 34.3 ms: 1.28x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.9 ms: 1.39x faster                                                  |
| nbody          | 94.6 ms                                                | 62.8 ms: 1.51x faster                                                  |
| pidigits       | 284 ms                                                 | 283 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 72.7 ms: 1.32x faster                                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.60 ms: 1.06x slower                                                  |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.17 ms: 1.35x faster                                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                                  |
| pickle               | 7.50 us                                                | 7.63 us: 1.02x slower                                                  |
| pickle_list          | 2.83 us                                                | 2.86 us: 1.01x slower                                                  |
| pickle_pure_python   | 284 us                                                 | 196 us: 1.45x faster                                                   |
| unpickle             | 10.0 us                                                | 9.68 us: 1.04x faster                                                  |
| unpickle_list        | 2.66 us                                                | 2.58 us: 1.03x faster                                                  |
| unpickle_pure_python | 204 us                                                 | 152 us: 1.34x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 93.1 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 65.6 ms: 1.05x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 47.1 ms: 1.16x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 34.4 ms: 1.31x faster                                                  |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.29 ms: 1.03x faster                                                  |
| python_startup_no_site | 7.00 ms                                                | 7.34 ms: 1.05x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 20.2 ms: 1.35x faster                                                  |
| genshi_text     | 18.2 ms                                                | 14.0 ms: 1.30x faster                                                  |
| genshi_xml      | 37.7 ms                                                | 28.3 ms: 1.33x faster                                                  |
| mako            | 10.6 ms                                                | 6.88 ms: 1.54x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.38x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 179 ms: 1.24x faster                                                   |
| async_generators        | 231 ms                                                 | 198 ms: 1.16x faster                                                   |
| async_tree_none         | 396 ms                                                 | 285 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed | 665 ms                                                 | 541 ms: 1.23x faster                                                   |
| async_tree_io           | 1.01 sec                                               | 726 ms: 1.39x faster                                                   |
| async_tree_memoization  | 485 ms                                                 | 329 ms: 1.47x faster                                                   |
| chameleon               | 5.86 ms                                                | 4.28 ms: 1.37x faster                                                  |
| chaos                   | 66.5 ms                                                | 49.2 ms: 1.35x faster                                                  |
| bench_mp_pool           | 40.8 ms                                                | 42.5 ms: 1.04x slower                                                  |
| bench_thread_pool       | 531 us                                                 | 442 us: 1.20x faster                                                   |
| coroutines              | 20.1 ms                                                | 17.5 ms: 1.15x faster                                                  |
| coverage                | 40.8 ms                                                | 55.2 ms: 1.35x slower                                                  |
| crypto_pyaes            | 77.9 ms                                                | 52.9 ms: 1.47x faster                                                  |
| deepcopy                | 278 us                                                 | 228 us: 1.22x faster                                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.94 us: 1.22x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 27.2 us: 1.26x faster                                                  |
| deltablue               | 5.37 ms                                                | 2.48 ms: 2.17x faster                                                  |
| django_template         | 27.2 ms                                                | 20.2 ms: 1.35x faster                                                  |
| docutils                | 1.76 sec                                               | 1.44 sec: 1.23x faster                                                 |
| dulwich_log             | 36.4 ms                                                | 28.4 ms: 1.28x faster                                                  |
| fannkuch                | 318 ms                                                 | 256 ms: 1.24x faster                                                   |
| float                   | 72.1 ms                                                | 51.9 ms: 1.39x faster                                                  |
| generators              | 32.5 ms                                                | 32.0 ms: 1.01x faster                                                  |
| genshi_text             | 18.2 ms                                                | 14.0 ms: 1.30x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 28.3 ms: 1.33x faster                                                  |
| go                      | 165 ms                                                 | 106 ms: 1.55x faster                                                   |
| hexiom                  | 6.31 ms                                                | 4.59 ms: 1.37x faster                                                  |
| html5lib                | 44.0 ms                                                | 34.3 ms: 1.28x faster                                                  |
| json                    | 3.13 ms                                                | 2.84 ms: 1.10x faster                                                  |
| json_dumps              | 8.34 ms                                                | 6.17 ms: 1.35x faster                                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                                  |
| logging_format          | 4.95 us                                                | 3.71 us: 1.33x faster                                                  |
| logging_silent          | 119 ns                                                 | 62.3 ns: 1.91x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.40 us: 1.35x faster                                                  |
| mako                    | 10.6 ms                                                | 6.88 ms: 1.54x faster                                                  |
| mdp                     | 1.66 sec                                               | 1.50 sec: 1.11x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 76.3 ms: 1.02x faster                                                  |
| mypy                    | 521 ms                                                 | 410 ms: 1.27x faster                                                   |
| nbody                   | 94.6 ms                                                | 62.8 ms: 1.51x faster                                                  |
| nqueens                 | 68.6 ms                                                | 59.0 ms: 1.16x faster                                                  |
| pathlib                 | 22.2 ms                                                | 20.3 ms: 1.09x faster                                                  |
| pickle                  | 7.50 us                                                | 7.63 us: 1.02x slower                                                  |
| pickle_list             | 2.83 us                                                | 2.86 us: 1.01x slower                                                  |
| pickle_pure_python      | 284 us                                                 | 196 us: 1.45x faster                                                   |
| pidigits                | 284 ms                                                 | 283 ms: 1.00x faster                                                   |
| pprint_safe_repr        | 608 ms                                                 | 471 ms: 1.29x faster                                                   |
| pprint_pformat          | 1.24 sec                                               | 960 ms: 1.29x faster                                                   |
| pycparser               | 915 ms                                                 | 670 ms: 1.36x faster                                                   |
| pyflate                 | 454 ms                                                 | 323 ms: 1.40x faster                                                   |
| python_startup          | 9.59 ms                                                | 9.29 ms: 1.03x faster                                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.34 ms: 1.05x slower                                                  |
| raytrace                | 329 ms                                                 | 211 ms: 1.56x faster                                                   |
| regex_compile           | 96.2 ms                                                | 72.7 ms: 1.32x faster                                                  |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| regex_effbot            | 2.45 ms                                                | 2.60 ms: 1.06x slower                                                  |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                                  |
| richards                | 51.4 ms                                                | 28.9 ms: 1.78x faster                                                  |
| scimark_fft             | 231 ms                                                 | 194 ms: 1.19x faster                                                   |
| scimark_lu              | 110 ms                                                 | 69.2 ms: 1.59x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 48.3 ms: 1.50x faster                                                  |
| scimark_sor             | 126 ms                                                 | 77.5 ms: 1.63x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.78 ms: 1.25x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 71.8 ms: 1.34x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 948 us: 1.40x faster                                                   |
| sqlglot_transpile       | 1.54 ms                                                | 1.11 ms: 1.39x faster                                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.0 ms: 1.23x faster                                                  |
| sqlglot_normalize       | 198 ms                                                 | 168 ms: 1.18x faster                                                   |
| sqlite_synth            | 1.50 us                                                | 1.44 us: 1.04x faster                                                  |
| sympy_expand            | 275 ms                                                 | 241 ms: 1.14x faster                                                   |
| sympy_integrate         | 13.3 ms                                                | 11.3 ms: 1.17x faster                                                  |
| sympy_sum               | 93.5 ms                                                | 85.2 ms: 1.10x faster                                                  |
| sympy_str               | 169 ms                                                 | 150 ms: 1.13x faster                                                   |
| telco                   | 3.63 ms                                                | 3.35 ms: 1.09x faster                                                  |
| thrift                  | 577 us                                                 | 429 us: 1.35x faster                                                   |
| unpack_sequence         | 38.2 ns                                                | 30.1 ns: 1.27x faster                                                  |
| unpickle                | 10.0 us                                                | 9.68 us: 1.04x faster                                                  |
| unpickle_list           | 2.66 us                                                | 2.58 us: 1.03x faster                                                  |
| unpickle_pure_python    | 204 us                                                 | 152 us: 1.34x faster                                                   |
| xml_etree_parse         | 100 ms                                                 | 93.1 ms: 1.07x faster                                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 65.6 ms: 1.05x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 47.1 ms: 1.16x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 34.4 ms: 1.31x faster                                                  |
| Geometric mean          | (ref)                                                  | 1.24x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (7) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
