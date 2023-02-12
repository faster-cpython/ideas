
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 3eb12df
- commit date: 2023-02-11
- overall geometric mean: 1.24x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 181 ms: 1.23x faster                                   |
| chameleon      | 5.86 ms                                                | 4.34 ms: 1.35x faster                                  |
| docutils       | 1.76 sec                                               | 1.46 sec: 1.20x faster                                 |
| html5lib       | 44.0 ms                                                | 35.0 ms: 1.26x faster                                  |
| tornado_http   | 90.1 ms                                                | 68.4 ms: 1.32x faster                                  |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 63.1 ms: 1.50x faster                                  |
| float          | 72.1 ms                                                | 49.7 ms: 1.45x faster                                  |
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.30x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 71.0 ms: 1.36x faster                                  |
| regex_v8       | 17.7 ms                                                | 16.0 ms: 1.10x faster                                  |
| regex_dna      | 164 ms                                                 | 150 ms: 1.10x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.60 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 185 us: 1.53x faster                                   |
| unpickle_pure_python | 204 us                                                 | 137 us: 1.49x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.06 ms: 1.38x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 35.2 ms: 1.28x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 49.2 ms: 1.11x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 93.0 ms: 1.08x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 67.1 ms: 1.03x faster                                  |
| unpickle             | 10.0 us                                                | 9.91 us: 1.01x faster                                  |
| unpickle_list        | 2.66 us                                                | 2.67 us: 1.00x slower                                  |
| pickle               | 7.50 us                                                | 7.57 us: 1.01x slower                                  |
| Geometric mean       | (ref)                                                  | 1.13x faster                                           |

Benchmark hidden because not significant (2): pickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.36 ms: 1.02x faster                                  |
| python_startup_no_site | 7.00 ms                                                | 7.38 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.13 ms: 1.49x faster                                  |
| genshi_xml      | 37.7 ms                                                | 27.5 ms: 1.37x faster                                  |
| genshi_text     | 18.2 ms                                                | 13.8 ms: 1.32x faster                                  |
| django_template | 27.2 ms                                                | 20.8 ms: 1.31x faster                                  |
| Geometric mean  | (ref)                                                  | 1.37x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.47 ms: 2.17x faster                                  |
| logging_silent          | 119 ns                                                 | 64.1 ns: 1.86x faster                                  |
| richards                | 51.4 ms                                                | 29.5 ms: 1.74x faster                                  |
| scimark_lu              | 110 ms                                                 | 70.5 ms: 1.56x faster                                  |
| go                      | 165 ms                                                 | 107 ms: 1.54x faster                                   |
| pickle_pure_python      | 284 us                                                 | 185 us: 1.53x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 320 ms: 1.52x faster                                   |
| raytrace                | 329 ms                                                 | 217 ms: 1.52x faster                                   |
| scimark_sor             | 126 ms                                                 | 83.4 ms: 1.51x faster                                  |
| nbody                   | 94.6 ms                                                | 63.1 ms: 1.50x faster                                  |
| hexiom                  | 6.31 ms                                                | 4.21 ms: 1.50x faster                                  |
| mako                    | 10.6 ms                                                | 7.13 ms: 1.49x faster                                  |
| unpickle_pure_python    | 204 us                                                 | 137 us: 1.49x faster                                   |
| chaos                   | 66.5 ms                                                | 45.5 ms: 1.46x faster                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.4 ms: 1.46x faster                                  |
| float                   | 72.1 ms                                                | 49.7 ms: 1.45x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 50.0 ms: 1.44x faster                                  |
| async_tree_none         | 396 ms                                                 | 278 ms: 1.42x faster                                   |
| pyflate                 | 454 ms                                                 | 324 ms: 1.40x faster                                   |
| async_tree_io           | 1.01 sec                                               | 726 ms: 1.39x faster                                   |
| deepcopy_memo           | 34.4 us                                                | 24.7 us: 1.39x faster                                  |
| pycparser               | 915 ms                                                 | 664 ms: 1.38x faster                                   |
| json_dumps              | 8.34 ms                                                | 6.06 ms: 1.38x faster                                  |
| genshi_xml              | 37.7 ms                                                | 27.5 ms: 1.37x faster                                  |
| regex_compile           | 96.2 ms                                                | 71.0 ms: 1.36x faster                                  |
| chameleon               | 5.86 ms                                                | 4.34 ms: 1.35x faster                                  |
| pprint_pformat          | 1.24 sec                                               | 920 ms: 1.35x faster                                   |
| pprint_safe_repr        | 608 ms                                                 | 452 ms: 1.34x faster                                   |
| genshi_text             | 18.2 ms                                                | 13.8 ms: 1.32x faster                                  |
| tornado_http            | 90.1 ms                                                | 68.4 ms: 1.32x faster                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.01 ms: 1.31x faster                                  |
| django_template         | 27.2 ms                                                | 20.8 ms: 1.31x faster                                  |
| logging_simple          | 4.61 us                                                | 3.51 us: 1.31x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.18 ms: 1.31x faster                                  |
| spectral_norm           | 95.8 ms                                                | 73.4 ms: 1.31x faster                                  |
| logging_format          | 4.95 us                                                | 3.80 us: 1.30x faster                                  |
| deepcopy                | 278 us                                                 | 215 us: 1.29x faster                                   |
| thrift                  | 577 us                                                 | 447 us: 1.29x faster                                   |
| dulwich_log             | 36.4 ms                                                | 28.4 ms: 1.28x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 35.2 ms: 1.28x faster                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.86 us: 1.27x faster                                  |
| fannkuch                | 318 ms                                                 | 251 ms: 1.27x faster                                   |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.12 ms: 1.27x faster                                  |
| html5lib                | 44.0 ms                                                | 35.0 ms: 1.26x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.77 ms: 1.25x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 30.6 ns: 1.25x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 534 ms: 1.24x faster                                   |
| 2to3                    | 222 ms                                                 | 181 ms: 1.23x faster                                   |
| sqlglot_optimize        | 38.1 ms                                                | 31.1 ms: 1.22x faster                                  |
| scimark_fft             | 231 ms                                                 | 189 ms: 1.22x faster                                   |
| docutils                | 1.76 sec                                               | 1.46 sec: 1.20x faster                                 |
| bench_thread_pool       | 531 us                                                 | 444 us: 1.19x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.1 ms: 1.19x faster                                  |
| sqlalchemy_declarative  | 74.4 ms                                                | 62.7 ms: 1.19x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 169 ms: 1.17x faster                                   |
| sympy_str               | 169 ms                                                 | 144 ms: 1.17x faster                                   |
| sympy_expand            | 275 ms                                                 | 238 ms: 1.15x faster                                   |
| nqueens                 | 68.6 ms                                                | 59.5 ms: 1.15x faster                                  |
| sympy_sum               | 93.5 ms                                                | 82.1 ms: 1.14x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 49.2 ms: 1.11x faster                                  |
| json                    | 3.13 ms                                                | 2.83 ms: 1.11x faster                                  |
| regex_v8                | 17.7 ms                                                | 16.0 ms: 1.10x faster                                  |
| regex_dna               | 164 ms                                                 | 150 ms: 1.10x faster                                   |
| mdp                     | 1.66 sec                                               | 1.51 sec: 1.10x faster                                 |
| coroutines              | 20.1 ms                                                | 18.4 ms: 1.10x faster                                  |
| sqlite_synth            | 1.50 us                                                | 1.37 us: 1.09x faster                                  |
| xml_etree_parse         | 100 ms                                                 | 93.0 ms: 1.08x faster                                  |
| telco                   | 3.63 ms                                                | 3.38 ms: 1.07x faster                                  |
| meteor_contest          | 77.7 ms                                                | 72.7 ms: 1.07x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 67.1 ms: 1.03x faster                                  |
| python_startup          | 9.59 ms                                                | 9.36 ms: 1.02x faster                                  |
| pathlib                 | 22.2 ms                                                | 21.8 ms: 1.02x faster                                  |
| unpickle                | 10.0 us                                                | 9.91 us: 1.01x faster                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                   |
| unpickle_list           | 2.66 us                                                | 2.67 us: 1.00x slower                                  |
| pickle                  | 7.50 us                                                | 7.57 us: 1.01x slower                                  |
| generators              | 32.5 ms                                                | 32.9 ms: 1.01x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 42.6 ms: 1.04x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.38 ms: 1.05x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.60 ms: 1.06x slower                                  |
| async_generators        | 231 ms                                                 | 255 ms: 1.11x slower                                   |
| coverage                | 40.8 ms                                                | 60.3 ms: 1.48x slower                                  |
| Geometric mean          | (ref)                                                  | 1.24x faster                                           |

Benchmark hidden because not significant (2): pickle_list, pickle_dict
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (4) of public/results/bm-20230211-3.12.0a5+-3eb12df/bm-20230211-darwin-arm64-python-main-3.12.0a5+-3eb12df.json: asyncio_tcp, create_gc_cycles, gc_traversal, mypy2
