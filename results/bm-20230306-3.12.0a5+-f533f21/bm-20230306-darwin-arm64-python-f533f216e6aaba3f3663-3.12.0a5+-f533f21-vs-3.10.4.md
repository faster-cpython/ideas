
# Results vs. 3.10.4

- fork: python
- ref: f533f216e6aaba3f3663
- machine: darwin-arm64
- commit hash: f533f21
- commit date: 2023-03-06
- overall geometric mean: 1.19x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 165 ms: 1.35x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.57 ms: 1.28x faster                                                  |
| docutils       | 1.76 sec                                               | 1.49 sec: 1.18x faster                                                 |
| html5lib       | 44.0 ms                                                | 35.5 ms: 1.24x faster                                                  |
| tornado_http   | 90.1 ms                                                | 71.1 ms: 1.27x faster                                                  |
| Geometric mean | (ref)                                                  | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 63.7 ms: 1.48x faster                                                  |
| float          | 72.1 ms                                                | 53.8 ms: 1.34x faster                                                  |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.26x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.6 ms: 1.27x faster                                                  |
| regex_v8       | 17.7 ms                                                | 16.5 ms: 1.08x faster                                                  |
| regex_dna      | 164 ms                                                 | 159 ms: 1.03x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.74 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 191 us: 1.48x faster                                                   |
| unpickle_pure_python | 204 us                                                 | 145 us: 1.41x faster                                                   |
| json_dumps           | 8.34 ms                                                | 6.19 ms: 1.35x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 36.8 ms: 1.23x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 50.7 ms: 1.07x faster                                                  |
| json_loads           | 17.0 us                                                | 16.1 us: 1.06x faster                                                  |
| unpickle             | 10.0 us                                                | 9.64 us: 1.04x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 97.7 ms: 1.02x faster                                                  |
| pickle_list          | 2.83 us                                                | 2.79 us: 1.01x faster                                                  |
| pickle_dict          | 18.0 us                                                | 18.0 us: 1.00x slower                                                  |
| pickle               | 7.50 us                                                | 7.54 us: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.4 ms: 1.29x slower                                                  |
| python_startup_no_site | 7.00 ms                                                | 10.4 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.46 ms: 1.42x faster                                                  |
| genshi_xml      | 37.7 ms                                                | 29.0 ms: 1.30x faster                                                  |
| django_template | 27.2 ms                                                | 21.6 ms: 1.26x faster                                                  |
| genshi_text     | 18.2 ms                                                | 14.7 ms: 1.24x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.30x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.58 ms: 2.08x faster                                                  |
| logging_silent          | 119 ns                                                 | 68.1 ns: 1.75x faster                                                  |
| richards                | 51.4 ms                                                | 30.6 ms: 1.68x faster                                                  |
| go                      | 165 ms                                                 | 110 ms: 1.49x faster                                                   |
| pickle_pure_python      | 284 us                                                 | 191 us: 1.48x faster                                                   |
| nbody                   | 94.6 ms                                                | 63.7 ms: 1.48x faster                                                  |
| scimark_lu              | 110 ms                                                 | 74.4 ms: 1.48x faster                                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.2 ms: 1.46x faster                                                  |
| raytrace                | 329 ms                                                 | 228 ms: 1.44x faster                                                   |
| async_tree_memoization  | 485 ms                                                 | 338 ms: 1.44x faster                                                   |
| scimark_sor             | 126 ms                                                 | 88.0 ms: 1.43x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 50.7 ms: 1.43x faster                                                  |
| mako                    | 10.6 ms                                                | 7.46 ms: 1.42x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.45 ms: 1.42x faster                                                  |
| unpickle_pure_python    | 204 us                                                 | 145 us: 1.41x faster                                                   |
| chaos                   | 66.5 ms                                                | 47.7 ms: 1.40x faster                                                  |
| pyflate                 | 454 ms                                                 | 331 ms: 1.37x faster                                                   |
| async_tree_none         | 396 ms                                                 | 290 ms: 1.36x faster                                                   |
| async_tree_io           | 1.01 sec                                               | 744 ms: 1.36x faster                                                   |
| 2to3                    | 222 ms                                                 | 165 ms: 1.35x faster                                                   |
| pycparser               | 915 ms                                                 | 678 ms: 1.35x faster                                                   |
| json_dumps              | 8.34 ms                                                | 6.19 ms: 1.35x faster                                                  |
| float                   | 72.1 ms                                                | 53.8 ms: 1.34x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 29.0 ms: 1.30x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 26.5 us: 1.30x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.57 ms: 1.28x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 75.0 ms: 1.28x faster                                                  |
| regex_compile           | 96.2 ms                                                | 75.6 ms: 1.27x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 978 ms: 1.27x faster                                                   |
| tornado_http            | 90.1 ms                                                | 71.1 ms: 1.27x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 480 ms: 1.27x faster                                                   |
| sqlglot_parse           | 1.33 ms                                                | 1.05 ms: 1.26x faster                                                  |
| django_template         | 27.2 ms                                                | 21.6 ms: 1.26x faster                                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.22 ms: 1.26x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.66 us: 1.26x faster                                                  |
| logging_format          | 4.95 us                                                | 3.94 us: 1.25x faster                                                  |
| thrift                  | 577 us                                                 | 461 us: 1.25x faster                                                   |
| html5lib                | 44.0 ms                                                | 35.5 ms: 1.24x faster                                                  |
| genshi_text             | 18.2 ms                                                | 14.7 ms: 1.24x faster                                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.29 ms: 1.24x faster                                                  |
| deepcopy                | 278 us                                                 | 225 us: 1.23x faster                                                   |
| fannkuch                | 318 ms                                                 | 258 ms: 1.23x faster                                                   |
| dulwich_log             | 36.4 ms                                                | 29.6 ms: 1.23x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 36.8 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 549 ms: 1.21x faster                                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.98 us: 1.19x faster                                                  |
| sqlglot_optimize        | 38.1 ms                                                | 32.2 ms: 1.18x faster                                                  |
| scimark_fft             | 231 ms                                                 | 196 ms: 1.18x faster                                                   |
| docutils                | 1.76 sec                                               | 1.49 sec: 1.18x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 32.8 ns: 1.17x faster                                                  |
| sqlalchemy_declarative  | 74.4 ms                                                | 64.0 ms: 1.16x faster                                                  |
| generators              | 32.5 ms                                                | 28.1 ms: 1.15x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.7 ms: 1.14x faster                                                  |
| sqlglot_normalize       | 198 ms                                                 | 175 ms: 1.14x faster                                                   |
| bench_thread_pool       | 531 us                                                 | 470 us: 1.13x faster                                                   |
| json                    | 3.13 ms                                                | 2.79 ms: 1.12x faster                                                  |
| coroutines              | 20.1 ms                                                | 18.0 ms: 1.11x faster                                                  |
| sympy_expand            | 275 ms                                                 | 247 ms: 1.11x faster                                                   |
| mdp                     | 1.66 sec                                               | 1.49 sec: 1.11x faster                                                 |
| sympy_str               | 169 ms                                                 | 154 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.16 ms: 1.10x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.38 us: 1.09x faster                                                  |
| nqueens                 | 68.6 ms                                                | 63.3 ms: 1.08x faster                                                  |
| regex_v8                | 17.7 ms                                                | 16.5 ms: 1.08x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 50.7 ms: 1.07x faster                                                  |
| sympy_sum               | 93.5 ms                                                | 87.8 ms: 1.07x faster                                                  |
| meteor_contest          | 77.7 ms                                                | 73.1 ms: 1.06x faster                                                  |
| json_loads              | 17.0 us                                                | 16.1 us: 1.06x faster                                                  |
| telco                   | 3.63 ms                                                | 3.44 ms: 1.05x faster                                                  |
| unpickle                | 10.0 us                                                | 9.64 us: 1.04x faster                                                  |
| regex_dna               | 164 ms                                                 | 159 ms: 1.03x faster                                                   |
| xml_etree_parse         | 100 ms                                                 | 97.7 ms: 1.02x faster                                                  |
| pickle_list             | 2.83 us                                                | 2.79 us: 1.01x faster                                                  |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| pickle_dict             | 18.0 us                                                | 18.0 us: 1.00x slower                                                  |
| pickle                  | 7.50 us                                                | 7.54 us: 1.01x slower                                                  |
| regex_effbot            | 2.45 ms                                                | 2.74 ms: 1.12x slower                                                  |
| bench_mp_pool           | 40.8 ms                                                | 46.1 ms: 1.13x slower                                                  |
| async_generators        | 231 ms                                                 | 270 ms: 1.17x slower                                                   |
| pathlib                 | 22.2 ms                                                | 27.7 ms: 1.25x slower                                                  |
| python_startup          | 9.59 ms                                                | 12.4 ms: 1.29x slower                                                  |
| coverage                | 40.8 ms                                                | 60.0 ms: 1.47x slower                                                  |
| python_startup_no_site  | 7.00 ms                                                | 10.4 ms: 1.48x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.19x faster                                                           |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_iterparse
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230306-3.12.0a5+-f533f21/bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
