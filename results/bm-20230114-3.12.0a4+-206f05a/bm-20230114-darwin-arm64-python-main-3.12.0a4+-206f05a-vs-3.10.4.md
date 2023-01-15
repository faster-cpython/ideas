
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 206f05a
- commit date: 2023-01-14
- overall geometric mean: 1.22x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 183 ms: 1.22x faster                                   |
| chameleon      | 5.86 ms                                                | 4.59 ms: 1.28x faster                                  |
| docutils       | 1.76 sec                                               | 1.44 sec: 1.22x faster                                 |
| html5lib       | 44.0 ms                                                | 34.7 ms: 1.27x faster                                  |
| tornado_http   | 90.1 ms                                                | 68.3 ms: 1.32x faster                                  |
| Geometric mean | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.5 ms: 1.40x faster                                  |
| nbody          | 94.6 ms                                                | 63.4 ms: 1.49x faster                                  |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 74.6 ms: 1.29x faster                                  |
| regex_dna      | 164 ms                                                 | 154 ms: 1.07x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.73 ms: 1.11x slower                                  |
| regex_v8       | 17.7 ms                                                | 16.8 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.12 ms: 1.36x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.05x faster                                  |
| pickle               | 7.50 us                                                | 7.56 us: 1.01x slower                                  |
| pickle_list          | 2.83 us                                                | 2.89 us: 1.02x slower                                  |
| pickle_pure_python   | 284 us                                                 | 194 us: 1.46x faster                                   |
| unpickle             | 10.0 us                                                | 9.84 us: 1.02x faster                                  |
| unpickle_list        | 2.66 us                                                | 2.71 us: 1.02x slower                                  |
| unpickle_pure_python | 204 us                                                 | 142 us: 1.43x faster                                   |
| xml_etree_parse      | 100 ms                                                 | 93.1 ms: 1.07x faster                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 66.4 ms: 1.04x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.0 ms: 1.14x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 34.8 ms: 1.30x faster                                  |
| Geometric mean       | (ref)                                                  | 1.13x faster                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.33 ms: 1.03x faster                                  |
| python_startup_no_site | 7.00 ms                                                | 7.34 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.7 ms: 1.26x faster                                  |
| genshi_text     | 18.2 ms                                                | 15.2 ms: 1.19x faster                                  |
| genshi_xml      | 37.7 ms                                                | 28.4 ms: 1.33x faster                                  |
| mako            | 10.6 ms                                                | 8.10 ms: 1.31x faster                                  |
| Geometric mean  | (ref)                                                  | 1.27x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 183 ms: 1.22x faster                                   |
| async_generators        | 231 ms                                                 | 200 ms: 1.15x faster                                   |
| async_tree_none         | 396 ms                                                 | 285 ms: 1.39x faster                                   |
| async_tree_cpu_io_mixed | 665 ms                                                 | 540 ms: 1.23x faster                                   |
| async_tree_io           | 1.01 sec                                               | 737 ms: 1.37x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 327 ms: 1.48x faster                                   |
| chameleon               | 5.86 ms                                                | 4.59 ms: 1.28x faster                                  |
| chaos                   | 66.5 ms                                                | 50.3 ms: 1.32x faster                                  |
| bench_mp_pool           | 40.8 ms                                                | 42.1 ms: 1.03x slower                                  |
| bench_thread_pool       | 531 us                                                 | 447 us: 1.19x faster                                   |
| coroutines              | 20.1 ms                                                | 18.6 ms: 1.08x faster                                  |
| coverage                | 40.8 ms                                                | 56.4 ms: 1.38x slower                                  |
| crypto_pyaes            | 77.9 ms                                                | 52.9 ms: 1.47x faster                                  |
| deepcopy                | 278 us                                                 | 220 us: 1.26x faster                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.90 us: 1.24x faster                                  |
| deepcopy_memo           | 34.4 us                                                | 25.9 us: 1.33x faster                                  |
| deltablue               | 5.37 ms                                                | 2.61 ms: 2.06x faster                                  |
| django_template         | 27.2 ms                                                | 21.7 ms: 1.26x faster                                  |
| docutils                | 1.76 sec                                               | 1.44 sec: 1.22x faster                                 |
| dulwich_log             | 36.4 ms                                                | 28.6 ms: 1.28x faster                                  |
| fannkuch                | 318 ms                                                 | 255 ms: 1.25x faster                                   |
| float                   | 72.1 ms                                                | 51.5 ms: 1.40x faster                                  |
| generators              | 32.5 ms                                                | 33.6 ms: 1.03x slower                                  |
| genshi_text             | 18.2 ms                                                | 15.2 ms: 1.19x faster                                  |
| genshi_xml              | 37.7 ms                                                | 28.4 ms: 1.33x faster                                  |
| go                      | 165 ms                                                 | 108 ms: 1.52x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.92 ms: 1.28x faster                                  |
| html5lib                | 44.0 ms                                                | 34.7 ms: 1.27x faster                                  |
| json                    | 3.13 ms                                                | 2.82 ms: 1.11x faster                                  |
| json_dumps              | 8.34 ms                                                | 6.12 ms: 1.36x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.05x faster                                  |
| logging_format          | 4.95 us                                                | 3.79 us: 1.30x faster                                  |
| logging_silent          | 119 ns                                                 | 66.2 ns: 1.80x faster                                  |
| logging_simple          | 4.61 us                                                | 3.50 us: 1.31x faster                                  |
| mako                    | 10.6 ms                                                | 8.10 ms: 1.31x faster                                  |
| mdp                     | 1.66 sec                                               | 1.50 sec: 1.11x faster                                 |
| meteor_contest          | 77.7 ms                                                | 74.5 ms: 1.04x faster                                  |
| mypy                    | 521 ms                                                 | 414 ms: 1.26x faster                                   |
| nbody                   | 94.6 ms                                                | 63.4 ms: 1.49x faster                                  |
| nqueens                 | 68.6 ms                                                | 60.8 ms: 1.13x faster                                  |
| pathlib                 | 22.2 ms                                                | 20.9 ms: 1.06x faster                                  |
| pickle                  | 7.50 us                                                | 7.56 us: 1.01x slower                                  |
| pickle_list             | 2.83 us                                                | 2.89 us: 1.02x slower                                  |
| pickle_pure_python      | 284 us                                                 | 194 us: 1.46x faster                                   |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                   |
| pprint_safe_repr        | 608 ms                                                 | 464 ms: 1.31x faster                                   |
| pprint_pformat          | 1.24 sec                                               | 939 ms: 1.32x faster                                   |
| pycparser               | 915 ms                                                 | 682 ms: 1.34x faster                                   |
| pyflate                 | 454 ms                                                 | 319 ms: 1.42x faster                                   |
| python_startup          | 9.59 ms                                                | 9.33 ms: 1.03x faster                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.34 ms: 1.05x slower                                  |
| raytrace                | 329 ms                                                 | 223 ms: 1.47x faster                                   |
| regex_compile           | 96.2 ms                                                | 74.6 ms: 1.29x faster                                  |
| regex_dna               | 164 ms                                                 | 154 ms: 1.07x faster                                   |
| regex_effbot            | 2.45 ms                                                | 2.73 ms: 1.11x slower                                  |
| regex_v8                | 17.7 ms                                                | 16.8 ms: 1.05x faster                                  |
| richards                | 51.4 ms                                                | 30.4 ms: 1.69x faster                                  |
| scimark_fft             | 231 ms                                                 | 195 ms: 1.19x faster                                   |
| scimark_lu              | 110 ms                                                 | 72.3 ms: 1.52x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 50.6 ms: 1.43x faster                                  |
| scimark_sor             | 126 ms                                                 | 82.0 ms: 1.54x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.79 ms: 1.24x faster                                  |
| spectral_norm           | 95.8 ms                                                | 73.6 ms: 1.30x faster                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.02 ms: 1.30x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.18 ms: 1.30x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.2 ms: 1.22x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 171 ms: 1.16x faster                                   |
| sqlite_synth            | 1.50 us                                                | 1.38 us: 1.09x faster                                  |
| sympy_expand            | 275 ms                                                 | 241 ms: 1.14x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.4 ms: 1.16x faster                                  |
| sympy_sum               | 93.5 ms                                                | 85.9 ms: 1.09x faster                                  |
| sympy_str               | 169 ms                                                 | 151 ms: 1.12x faster                                   |
| telco                   | 3.63 ms                                                | 3.39 ms: 1.07x faster                                  |
| thrift                  | 577 us                                                 | 442 us: 1.31x faster                                   |
| tornado_http            | 90.1 ms                                                | 68.3 ms: 1.32x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 32.8 ns: 1.17x faster                                  |
| unpickle                | 10.0 us                                                | 9.84 us: 1.02x faster                                  |
| unpickle_list           | 2.66 us                                                | 2.71 us: 1.02x slower                                  |
| unpickle_pure_python    | 204 us                                                 | 142 us: 1.43x faster                                   |
| xml_etree_parse         | 100 ms                                                 | 93.1 ms: 1.07x faster                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 66.4 ms: 1.04x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 48.0 ms: 1.14x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 34.8 ms: 1.30x faster                                  |
| Geometric mean          | (ref)                                                  | 1.22x faster                                           |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of public/results/bm-20230114-3.12.0a4+-206f05a/bm-20230114-darwin-arm64-python-main-3.12.0a4+-206f05a.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
