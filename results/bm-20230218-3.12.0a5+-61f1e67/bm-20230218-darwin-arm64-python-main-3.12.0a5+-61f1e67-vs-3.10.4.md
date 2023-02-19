
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 61f1e67
- commit date: 2023-02-18
- overall geometric mean: 1.21x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 161 ms: 1.38x faster                                   |
| chameleon      | 5.86 ms                                                | 4.45 ms: 1.32x faster                                  |
| docutils       | 1.76 sec                                               | 1.48 sec: 1.19x faster                                 |
| html5lib       | 44.0 ms                                                | 35.5 ms: 1.24x faster                                  |
| tornado_http   | 90.1 ms                                                | 70.2 ms: 1.28x faster                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 64.1 ms: 1.47x faster                                  |
| float          | 72.1 ms                                                | 52.4 ms: 1.38x faster                                  |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 72.9 ms: 1.32x faster                                  |
| regex_v8       | 17.7 ms                                                | 15.7 ms: 1.13x faster                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.60 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 193 us: 1.47x faster                                   |
| unpickle_pure_python | 204 us                                                 | 142 us: 1.43x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.16 ms: 1.35x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 35.9 ms: 1.25x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 50.2 ms: 1.09x faster                                  |
| json_loads           | 17.0 us                                                | 16.1 us: 1.06x faster                                  |
| unpickle_list        | 2.66 us                                                | 2.56 us: 1.04x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 96.6 ms: 1.04x faster                                  |
| unpickle             | 10.0 us                                                | 9.70 us: 1.03x faster                                  |
| pickle_list          | 2.83 us                                                | 2.80 us: 1.01x faster                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 69.8 ms: 1.01x slower                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                           |

Benchmark hidden because not significant (2): pickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 11.4 ms: 1.19x slower                                  |
| python_startup_no_site | 7.00 ms                                                | 9.34 ms: 1.33x slower                                  |
| Geometric mean         | (ref)                                                  | 1.26x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.35 ms: 1.44x faster                                  |
| genshi_xml      | 37.7 ms                                                | 28.2 ms: 1.34x faster                                  |
| django_template | 27.2 ms                                                | 21.3 ms: 1.28x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.3 ms: 1.28x faster                                  |
| Geometric mean  | (ref)                                                  | 1.33x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.56 ms: 2.10x faster                                  |
| logging_silent          | 119 ns                                                 | 66.0 ns: 1.81x faster                                  |
| richards                | 51.4 ms                                                | 29.9 ms: 1.72x faster                                  |
| go                      | 165 ms                                                 | 108 ms: 1.52x faster                                   |
| scimark_lu              | 110 ms                                                 | 72.7 ms: 1.51x faster                                  |
| async_tree_memoization  | 485 ms                                                 | 325 ms: 1.49x faster                                   |
| raytrace                | 329 ms                                                 | 223 ms: 1.48x faster                                   |
| nbody                   | 94.6 ms                                                | 64.1 ms: 1.47x faster                                  |
| pickle_pure_python      | 284 us                                                 | 193 us: 1.47x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.30 ms: 1.47x faster                                  |
| scimark_sor             | 126 ms                                                 | 85.9 ms: 1.47x faster                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.5 ms: 1.46x faster                                  |
| mako                    | 10.6 ms                                                | 7.35 ms: 1.44x faster                                  |
| unpickle_pure_python    | 204 us                                                 | 142 us: 1.43x faster                                   |
| chaos                   | 66.5 ms                                                | 46.5 ms: 1.43x faster                                  |
| pyflate                 | 454 ms                                                 | 325 ms: 1.40x faster                                   |
| async_tree_none         | 396 ms                                                 | 283 ms: 1.40x faster                                   |
| pycparser               | 915 ms                                                 | 662 ms: 1.38x faster                                   |
| scimark_monte_carlo     | 72.3 ms                                                | 52.4 ms: 1.38x faster                                  |
| 2to3                    | 222 ms                                                 | 161 ms: 1.38x faster                                   |
| float                   | 72.1 ms                                                | 52.4 ms: 1.38x faster                                  |
| async_tree_io           | 1.01 sec                                               | 736 ms: 1.37x faster                                   |
| deepcopy_memo           | 34.4 us                                                | 25.3 us: 1.36x faster                                  |
| json_dumps              | 8.34 ms                                                | 6.16 ms: 1.35x faster                                  |
| genshi_xml              | 37.7 ms                                                | 28.2 ms: 1.34x faster                                  |
| regex_compile           | 96.2 ms                                                | 72.9 ms: 1.32x faster                                  |
| chameleon               | 5.86 ms                                                | 4.45 ms: 1.32x faster                                  |
| pprint_pformat          | 1.24 sec                                               | 959 ms: 1.29x faster                                   |
| pprint_safe_repr        | 608 ms                                                 | 470 ms: 1.29x faster                                   |
| tornado_http            | 90.1 ms                                                | 70.2 ms: 1.28x faster                                  |
| django_template         | 27.2 ms                                                | 21.3 ms: 1.28x faster                                  |
| logging_simple          | 4.61 us                                                | 3.61 us: 1.28x faster                                  |
| genshi_text             | 18.2 ms                                                | 14.3 ms: 1.28x faster                                  |
| spectral_norm           | 95.8 ms                                                | 75.2 ms: 1.28x faster                                  |
| logging_format          | 4.95 us                                                | 3.89 us: 1.27x faster                                  |
| generators              | 32.5 ms                                                | 25.5 ms: 1.27x faster                                  |
| deepcopy                | 278 us                                                 | 220 us: 1.27x faster                                   |
| sqlglot_parse           | 1.33 ms                                                | 1.05 ms: 1.26x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.22 ms: 1.26x faster                                  |
| thrift                  | 577 us                                                 | 458 us: 1.26x faster                                   |
| xml_etree_process       | 45.1 ms                                                | 35.9 ms: 1.25x faster                                  |
| fannkuch                | 318 ms                                                 | 255 ms: 1.25x faster                                   |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.24 ms: 1.24x faster                                  |
| html5lib                | 44.0 ms                                                | 35.5 ms: 1.24x faster                                  |
| dulwich_log             | 36.4 ms                                                | 29.5 ms: 1.23x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.81 ms: 1.23x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 541 ms: 1.23x faster                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.93 us: 1.22x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.8 ms: 1.20x faster                                  |
| scimark_fft             | 231 ms                                                 | 193 ms: 1.20x faster                                   |
| docutils                | 1.76 sec                                               | 1.48 sec: 1.19x faster                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 63.4 ms: 1.17x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 32.7 ns: 1.17x faster                                  |
| sympy_integrate         | 13.3 ms                                                | 11.3 ms: 1.17x faster                                  |
| sympy_str               | 169 ms                                                 | 147 ms: 1.15x faster                                   |
| bench_thread_pool       | 531 us                                                 | 463 us: 1.14x faster                                   |
| sqlglot_normalize       | 198 ms                                                 | 173 ms: 1.14x faster                                   |
| coroutines              | 20.1 ms                                                | 17.7 ms: 1.14x faster                                  |
| sympy_expand            | 275 ms                                                 | 243 ms: 1.13x faster                                   |
| regex_v8                | 17.7 ms                                                | 15.7 ms: 1.13x faster                                  |
| json                    | 3.13 ms                                                | 2.77 ms: 1.13x faster                                  |
| nqueens                 | 68.6 ms                                                | 61.1 ms: 1.12x faster                                  |
| sympy_sum               | 93.5 ms                                                | 83.5 ms: 1.12x faster                                  |
| sqlite_synth            | 1.50 us                                                | 1.36 us: 1.10x faster                                  |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                   |
| xml_etree_generate      | 54.5 ms                                                | 50.2 ms: 1.09x faster                                  |
| mdp                     | 1.66 sec                                               | 1.53 sec: 1.08x faster                                 |
| json_loads              | 17.0 us                                                | 16.1 us: 1.06x faster                                  |
| telco                   | 3.63 ms                                                | 3.47 ms: 1.05x faster                                  |
| unpickle_list           | 2.66 us                                                | 2.56 us: 1.04x faster                                  |
| xml_etree_parse         | 100 ms                                                 | 96.6 ms: 1.04x faster                                  |
| unpickle                | 10.0 us                                                | 9.70 us: 1.03x faster                                  |
| meteor_contest          | 77.7 ms                                                | 75.8 ms: 1.03x faster                                  |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                   |
| pickle_list             | 2.83 us                                                | 2.80 us: 1.01x faster                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 69.8 ms: 1.01x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.60 ms: 1.06x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 45.0 ms: 1.10x slower                                  |
| async_generators        | 231 ms                                                 | 263 ms: 1.14x slower                                   |
| python_startup          | 9.59 ms                                                | 11.4 ms: 1.19x slower                                  |
| pathlib                 | 22.2 ms                                                | 27.4 ms: 1.23x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 9.34 ms: 1.33x slower                                  |
| coverage                | 40.8 ms                                                | 61.0 ms: 1.49x slower                                  |
| Geometric mean          | (ref)                                                  | 1.21x faster                                           |

Benchmark hidden because not significant (2): pickle, pickle_dict
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230218-3.12.0a5+-61f1e67/bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal, mypy2
