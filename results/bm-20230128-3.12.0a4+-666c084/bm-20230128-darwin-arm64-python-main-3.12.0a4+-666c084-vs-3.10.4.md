
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 666c084
- commit date: 2023-01-28
- overall geometric mean: 1.23x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 185 ms: 1.20x faster                                   |
| chameleon      | 5.86 ms                                                | 4.58 ms: 1.28x faster                                  |
| docutils       | 1.76 sec                                               | 1.45 sec: 1.21x faster                                 |
| html5lib       | 44.0 ms                                                | 35.2 ms: 1.25x faster                                  |
| tornado_http   | 90.1 ms                                                | 70.3 ms: 1.28x faster                                  |
| Geometric mean | (ref)                                                  | 1.24x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.7 ms: 1.39x faster                                  |
| nbody          | 94.6 ms                                                | 64.2 ms: 1.47x faster                                  |
| pidigits       | 284 ms                                                 | 283 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 73.6 ms: 1.31x faster                                  |
| regex_dna      | 164 ms                                                 | 150 ms: 1.10x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.65 ms: 1.08x slower                                  |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.13 ms: 1.36x faster                                  |
| json_loads           | 17.0 us                                                | 16.4 us: 1.04x faster                                  |
| pickle_dict          | 18.0 us                                                | 17.9 us: 1.00x faster                                  |
| pickle_list          | 2.83 us                                                | 2.86 us: 1.01x slower                                  |
| pickle_pure_python   | 284 us                                                 | 192 us: 1.47x faster                                   |
| unpickle             | 10.0 us                                                | 10.1 us: 1.01x slower                                  |
| unpickle_list        | 2.66 us                                                | 2.73 us: 1.03x slower                                  |
| unpickle_pure_python | 204 us                                                 | 148 us: 1.38x faster                                   |
| xml_etree_parse      | 100 ms                                                 | 93.9 ms: 1.06x faster                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 67.9 ms: 1.02x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 49.4 ms: 1.10x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 35.8 ms: 1.26x faster                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.40 ms: 1.02x faster                                  |
| python_startup_no_site | 7.00 ms                                                | 7.39 ms: 1.06x slower                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.3 ms: 1.28x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.7 ms: 1.24x faster                                  |
| genshi_xml      | 37.7 ms                                                | 29.0 ms: 1.30x faster                                  |
| mako            | 10.6 ms                                                | 7.25 ms: 1.46x faster                                  |
| Geometric mean  | (ref)                                                  | 1.32x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 185 ms: 1.20x faster                                   |
| async_generators        | 231 ms                                                 | 200 ms: 1.16x faster                                   |
| async_tree_none         | 396 ms                                                 | 288 ms: 1.37x faster                                   |
| async_tree_cpu_io_mixed | 665 ms                                                 | 544 ms: 1.22x faster                                   |
| async_tree_io           | 1.01 sec                                               | 740 ms: 1.37x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 323 ms: 1.50x faster                                   |
| chameleon               | 5.86 ms                                                | 4.58 ms: 1.28x faster                                  |
| chaos                   | 66.5 ms                                                | 47.7 ms: 1.39x faster                                  |
| bench_mp_pool           | 40.8 ms                                                | 42.6 ms: 1.04x slower                                  |
| bench_thread_pool       | 531 us                                                 | 450 us: 1.18x faster                                   |
| coroutines              | 20.1 ms                                                | 18.8 ms: 1.07x faster                                  |
| coverage                | 40.8 ms                                                | 57.1 ms: 1.40x slower                                  |
| crypto_pyaes            | 77.9 ms                                                | 51.9 ms: 1.50x faster                                  |
| deepcopy                | 278 us                                                 | 219 us: 1.27x faster                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.88 us: 1.25x faster                                  |
| deepcopy_memo           | 34.4 us                                                | 26.0 us: 1.32x faster                                  |
| deltablue               | 5.37 ms                                                | 2.50 ms: 2.15x faster                                  |
| django_template         | 27.2 ms                                                | 21.3 ms: 1.28x faster                                  |
| docutils                | 1.76 sec                                               | 1.45 sec: 1.21x faster                                 |
| dulwich_log             | 36.4 ms                                                | 28.5 ms: 1.28x faster                                  |
| fannkuch                | 318 ms                                                 | 258 ms: 1.23x faster                                   |
| float                   | 72.1 ms                                                | 51.7 ms: 1.39x faster                                  |
| generators              | 32.5 ms                                                | 34.7 ms: 1.07x slower                                  |
| genshi_text             | 18.2 ms                                                | 14.7 ms: 1.24x faster                                  |
| genshi_xml              | 37.7 ms                                                | 29.0 ms: 1.30x faster                                  |
| go                      | 165 ms                                                 | 111 ms: 1.49x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.70 ms: 1.34x faster                                  |
| html5lib                | 44.0 ms                                                | 35.2 ms: 1.25x faster                                  |
| json                    | 3.13 ms                                                | 2.86 ms: 1.09x faster                                  |
| json_dumps              | 8.34 ms                                                | 6.13 ms: 1.36x faster                                  |
| json_loads              | 17.0 us                                                | 16.4 us: 1.04x faster                                  |
| logging_format          | 4.95 us                                                | 3.79 us: 1.30x faster                                  |
| logging_silent          | 119 ns                                                 | 66.4 ns: 1.80x faster                                  |
| logging_simple          | 4.61 us                                                | 3.51 us: 1.31x faster                                  |
| mako                    | 10.6 ms                                                | 7.25 ms: 1.46x faster                                  |
| mdp                     | 1.66 sec                                               | 1.51 sec: 1.10x faster                                 |
| meteor_contest          | 77.7 ms                                                | 73.8 ms: 1.05x faster                                  |
| mypy                    | 521 ms                                                 | 413 ms: 1.26x faster                                   |
| nbody                   | 94.6 ms                                                | 64.2 ms: 1.47x faster                                  |
| nqueens                 | 68.6 ms                                                | 59.9 ms: 1.14x faster                                  |
| pathlib                 | 22.2 ms                                                | 20.6 ms: 1.08x faster                                  |
| pickle_dict             | 18.0 us                                                | 17.9 us: 1.00x faster                                  |
| pickle_list             | 2.83 us                                                | 2.86 us: 1.01x slower                                  |
| pickle_pure_python      | 284 us                                                 | 192 us: 1.47x faster                                   |
| pidigits                | 284 ms                                                 | 283 ms: 1.00x faster                                   |
| pprint_safe_repr        | 608 ms                                                 | 468 ms: 1.30x faster                                   |
| pprint_pformat          | 1.24 sec                                               | 950 ms: 1.30x faster                                   |
| pycparser               | 915 ms                                                 | 680 ms: 1.34x faster                                   |
| pyflate                 | 454 ms                                                 | 324 ms: 1.40x faster                                   |
| python_startup          | 9.59 ms                                                | 9.40 ms: 1.02x faster                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.39 ms: 1.06x slower                                  |
| raytrace                | 329 ms                                                 | 208 ms: 1.58x faster                                   |
| regex_compile           | 96.2 ms                                                | 73.6 ms: 1.31x faster                                  |
| regex_dna               | 164 ms                                                 | 150 ms: 1.10x faster                                   |
| regex_effbot            | 2.45 ms                                                | 2.65 ms: 1.08x slower                                  |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| richards                | 51.4 ms                                                | 31.0 ms: 1.66x faster                                  |
| scimark_fft             | 231 ms                                                 | 192 ms: 1.20x faster                                   |
| scimark_lu              | 110 ms                                                 | 70.7 ms: 1.55x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 48.9 ms: 1.48x faster                                  |
| scimark_sor             | 126 ms                                                 | 77.8 ms: 1.62x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.79 ms: 1.24x faster                                  |
| spectral_norm           | 95.8 ms                                                | 72.3 ms: 1.33x faster                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.02 ms: 1.31x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.18 ms: 1.31x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.4 ms: 1.21x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 172 ms: 1.15x faster                                   |
| sqlite_synth            | 1.50 us                                                | 1.36 us: 1.10x faster                                  |
| sympy_expand            | 275 ms                                                 | 240 ms: 1.15x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.1 ms: 1.19x faster                                  |
| sympy_sum               | 93.5 ms                                                | 81.9 ms: 1.14x faster                                  |
| sympy_str               | 169 ms                                                 | 145 ms: 1.17x faster                                   |
| telco                   | 3.63 ms                                                | 3.43 ms: 1.06x faster                                  |
| thrift                  | 577 us                                                 | 449 us: 1.29x faster                                   |
| tornado_http            | 90.1 ms                                                | 70.3 ms: 1.28x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 32.8 ns: 1.17x faster                                  |
| unpickle                | 10.0 us                                                | 10.1 us: 1.01x slower                                  |
| unpickle_list           | 2.66 us                                                | 2.73 us: 1.03x slower                                  |
| unpickle_pure_python    | 204 us                                                 | 148 us: 1.38x faster                                   |
| xml_etree_parse         | 100 ms                                                 | 93.9 ms: 1.06x faster                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 67.9 ms: 1.02x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 49.4 ms: 1.10x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 35.8 ms: 1.26x faster                                  |
| Geometric mean          | (ref)                                                  | 1.23x faster                                           |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of public/results/bm-20230128-3.12.0a4+-666c084/bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
