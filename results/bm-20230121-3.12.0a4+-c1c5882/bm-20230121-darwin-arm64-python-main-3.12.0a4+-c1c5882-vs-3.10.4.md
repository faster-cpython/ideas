
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: c1c5882
- commit date: 2023-01-21
- overall geometric mean: 1.22x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 183 ms: 1.21x faster                                   |
| chameleon      | 5.86 ms                                                | 4.60 ms: 1.27x faster                                  |
| docutils       | 1.76 sec                                               | 1.44 sec: 1.22x faster                                 |
| html5lib       | 44.0 ms                                                | 35.0 ms: 1.26x faster                                  |
| tornado_http   | 90.1 ms                                                | 69.1 ms: 1.30x faster                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.4 ms: 1.40x faster                                  |
| nbody          | 94.6 ms                                                | 63.5 ms: 1.49x faster                                  |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 73.4 ms: 1.31x faster                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.61 ms: 1.07x slower                                  |
| regex_v8       | 17.7 ms                                                | 16.2 ms: 1.10x faster                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.05 ms: 1.38x faster                                  |
| json_loads           | 17.0 us                                                | 16.2 us: 1.05x faster                                  |
| pickle_pure_python   | 284 us                                                 | 192 us: 1.48x faster                                   |
| unpickle             | 10.0 us                                                | 9.76 us: 1.03x faster                                  |
| unpickle_list        | 2.66 us                                                | 2.71 us: 1.02x slower                                  |
| unpickle_pure_python | 204 us                                                 | 144 us: 1.41x faster                                   |
| xml_etree_parse      | 100 ms                                                 | 101 ms: 1.01x slower                                   |
| xml_etree_iterparse  | 69.0 ms                                                | 69.8 ms: 1.01x slower                                  |
| xml_etree_generate   | 54.5 ms                                                | 49.2 ms: 1.11x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 35.4 ms: 1.27x faster                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                           |

Benchmark hidden because not significant (3): pickle, pickle_dict, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.37 ms: 1.02x faster                                  |
| python_startup_no_site | 7.00 ms                                                | 7.36 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.8 ms: 1.25x faster                                  |
| genshi_text     | 18.2 ms                                                | 15.5 ms: 1.18x faster                                  |
| genshi_xml      | 37.7 ms                                                | 28.7 ms: 1.31x faster                                  |
| mako            | 10.6 ms                                                | 8.14 ms: 1.30x faster                                  |
| Geometric mean  | (ref)                                                  | 1.26x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 183 ms: 1.21x faster                                   |
| async_generators        | 231 ms                                                 | 197 ms: 1.17x faster                                   |
| async_tree_none         | 396 ms                                                 | 286 ms: 1.38x faster                                   |
| async_tree_cpu_io_mixed | 665 ms                                                 | 538 ms: 1.24x faster                                   |
| async_tree_io           | 1.01 sec                                               | 732 ms: 1.38x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 328 ms: 1.48x faster                                   |
| chameleon               | 5.86 ms                                                | 4.60 ms: 1.27x faster                                  |
| chaos                   | 66.5 ms                                                | 47.9 ms: 1.39x faster                                  |
| bench_mp_pool           | 40.8 ms                                                | 42.6 ms: 1.05x slower                                  |
| bench_thread_pool       | 531 us                                                 | 447 us: 1.19x faster                                   |
| coroutines              | 20.1 ms                                                | 18.9 ms: 1.06x faster                                  |
| coverage                | 40.8 ms                                                | 55.5 ms: 1.36x slower                                  |
| crypto_pyaes            | 77.9 ms                                                | 52.2 ms: 1.49x faster                                  |
| deepcopy                | 278 us                                                 | 222 us: 1.25x faster                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.92 us: 1.23x faster                                  |
| deepcopy_memo           | 34.4 us                                                | 26.1 us: 1.32x faster                                  |
| deltablue               | 5.37 ms                                                | 2.61 ms: 2.06x faster                                  |
| django_template         | 27.2 ms                                                | 21.8 ms: 1.25x faster                                  |
| docutils                | 1.76 sec                                               | 1.44 sec: 1.22x faster                                 |
| dulwich_log             | 36.4 ms                                                | 28.6 ms: 1.28x faster                                  |
| fannkuch                | 318 ms                                                 | 254 ms: 1.25x faster                                   |
| float                   | 72.1 ms                                                | 51.4 ms: 1.40x faster                                  |
| generators              | 32.5 ms                                                | 34.1 ms: 1.05x slower                                  |
| genshi_text             | 18.2 ms                                                | 15.5 ms: 1.18x faster                                  |
| genshi_xml              | 37.7 ms                                                | 28.7 ms: 1.31x faster                                  |
| go                      | 165 ms                                                 | 108 ms: 1.52x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.73 ms: 1.33x faster                                  |
| html5lib                | 44.0 ms                                                | 35.0 ms: 1.26x faster                                  |
| json                    | 3.13 ms                                                | 2.83 ms: 1.11x faster                                  |
| json_dumps              | 8.34 ms                                                | 6.05 ms: 1.38x faster                                  |
| json_loads              | 17.0 us                                                | 16.2 us: 1.05x faster                                  |
| logging_format          | 4.95 us                                                | 3.84 us: 1.29x faster                                  |
| logging_silent          | 119 ns                                                 | 66.4 ns: 1.80x faster                                  |
| logging_simple          | 4.61 us                                                | 3.55 us: 1.30x faster                                  |
| mako                    | 10.6 ms                                                | 8.14 ms: 1.30x faster                                  |
| mdp                     | 1.66 sec                                               | 1.51 sec: 1.10x faster                                 |
| meteor_contest          | 77.7 ms                                                | 75.5 ms: 1.03x faster                                  |
| mypy                    | 521 ms                                                 | 413 ms: 1.26x faster                                   |
| nbody                   | 94.6 ms                                                | 63.5 ms: 1.49x faster                                  |
| nqueens                 | 68.6 ms                                                | 60.0 ms: 1.14x faster                                  |
| pathlib                 | 22.2 ms                                                | 20.8 ms: 1.07x faster                                  |
| pickle_pure_python      | 284 us                                                 | 192 us: 1.48x faster                                   |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                   |
| pprint_safe_repr        | 608 ms                                                 | 460 ms: 1.32x faster                                   |
| pprint_pformat          | 1.24 sec                                               | 936 ms: 1.32x faster                                   |
| pycparser               | 915 ms                                                 | 679 ms: 1.35x faster                                   |
| pyflate                 | 454 ms                                                 | 322 ms: 1.41x faster                                   |
| python_startup          | 9.59 ms                                                | 9.37 ms: 1.02x faster                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.36 ms: 1.05x slower                                  |
| raytrace                | 329 ms                                                 | 217 ms: 1.52x faster                                   |
| regex_compile           | 96.2 ms                                                | 73.4 ms: 1.31x faster                                  |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                   |
| regex_effbot            | 2.45 ms                                                | 2.61 ms: 1.07x slower                                  |
| regex_v8                | 17.7 ms                                                | 16.2 ms: 1.10x faster                                  |
| richards                | 51.4 ms                                                | 30.5 ms: 1.68x faster                                  |
| scimark_fft             | 231 ms                                                 | 192 ms: 1.21x faster                                   |
| scimark_lu              | 110 ms                                                 | 72.3 ms: 1.52x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 48.3 ms: 1.49x faster                                  |
| scimark_sor             | 126 ms                                                 | 81.8 ms: 1.54x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.79 ms: 1.24x faster                                  |
| spectral_norm           | 95.8 ms                                                | 74.0 ms: 1.30x faster                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.04 ms: 1.28x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.20 ms: 1.29x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.4 ms: 1.21x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 172 ms: 1.15x faster                                   |
| sqlite_synth            | 1.50 us                                                | 1.38 us: 1.08x faster                                  |
| sympy_expand            | 275 ms                                                 | 242 ms: 1.14x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.4 ms: 1.16x faster                                  |
| sympy_sum               | 93.5 ms                                                | 85.4 ms: 1.09x faster                                  |
| sympy_str               | 169 ms                                                 | 152 ms: 1.12x faster                                   |
| telco                   | 3.63 ms                                                | 3.47 ms: 1.05x faster                                  |
| thrift                  | 577 us                                                 | 441 us: 1.31x faster                                   |
| tornado_http            | 90.1 ms                                                | 69.1 ms: 1.30x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 32.9 ns: 1.16x faster                                  |
| unpickle                | 10.0 us                                                | 9.76 us: 1.03x faster                                  |
| unpickle_list           | 2.66 us                                                | 2.71 us: 1.02x slower                                  |
| unpickle_pure_python    | 204 us                                                 | 144 us: 1.41x faster                                   |
| xml_etree_parse         | 100 ms                                                 | 101 ms: 1.01x slower                                   |
| xml_etree_iterparse     | 69.0 ms                                                | 69.8 ms: 1.01x slower                                  |
| xml_etree_generate      | 54.5 ms                                                | 49.2 ms: 1.11x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 35.4 ms: 1.27x faster                                  |
| Geometric mean          | (ref)                                                  | 1.22x faster                                           |

Benchmark hidden because not significant (3): pickle, pickle_dict, pickle_list
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of public/results/bm-20230121-3.12.0a4+-c1c5882/bm-20230121-darwin-arm64-python-main-3.12.0a4+-c1c5882.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
