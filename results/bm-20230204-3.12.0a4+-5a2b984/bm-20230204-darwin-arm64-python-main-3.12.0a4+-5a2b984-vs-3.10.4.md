
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 5a2b984
- commit date: 2023-02-04
- overall geometric mean: 1.23x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 182 ms: 1.22x faster                                   |
| chameleon      | 5.86 ms                                                | 4.71 ms: 1.24x faster                                  |
| docutils       | 1.76 sec                                               | 1.45 sec: 1.21x faster                                 |
| html5lib       | 44.0 ms                                                | 34.8 ms: 1.26x faster                                  |
| tornado_http   | 90.1 ms                                                | 69.9 ms: 1.29x faster                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 64.0 ms: 1.48x faster                                  |
| float          | 72.1 ms                                                | 51.9 ms: 1.39x faster                                  |
| pidigits       | 284 ms                                                 | 283 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 72.1 ms: 1.33x faster                                  |
| regex_dna      | 164 ms                                                 | 150 ms: 1.10x faster                                   |
| regex_v8       | 17.7 ms                                                | 16.2 ms: 1.10x faster                                  |
| regex_effbot   | 2.45 ms                                                | 2.63 ms: 1.07x slower                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 192 us: 1.48x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.10 ms: 1.37x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 34.4 ms: 1.31x faster                                  |
| unpickle_pure_python | 204 us                                                 | 157 us: 1.30x faster                                   |
| xml_etree_generate   | 54.5 ms                                                | 47.8 ms: 1.14x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 93.9 ms: 1.07x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.05x faster                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 67.8 ms: 1.02x faster                                  |
| unpickle             | 10.0 us                                                | 9.91 us: 1.01x faster                                  |
| pickle_dict          | 18.0 us                                                | 18.0 us: 1.00x slower                                  |
| pickle               | 7.50 us                                                | 7.57 us: 1.01x slower                                  |
| unpickle_list        | 2.66 us                                                | 2.71 us: 1.02x slower                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.36 ms: 1.02x faster                                  |
| python_startup_no_site | 7.00 ms                                                | 7.35 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.16 ms: 1.48x faster                                  |
| genshi_xml      | 37.7 ms                                                | 28.4 ms: 1.33x faster                                  |
| django_template | 27.2 ms                                                | 20.9 ms: 1.30x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.3 ms: 1.28x faster                                  |
| Geometric mean  | (ref)                                                  | 1.34x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.57 ms: 2.09x faster                                  |
| logging_silent          | 119 ns                                                 | 65.7 ns: 1.82x faster                                  |
| richards                | 51.4 ms                                                | 29.7 ms: 1.73x faster                                  |
| scimark_lu              | 110 ms                                                 | 70.8 ms: 1.55x faster                                  |
| go                      | 165 ms                                                 | 109 ms: 1.51x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 322 ms: 1.51x faster                                   |
| raytrace                | 329 ms                                                 | 219 ms: 1.50x faster                                   |
| mako                    | 10.6 ms                                                | 7.16 ms: 1.48x faster                                  |
| scimark_sor             | 126 ms                                                 | 85.3 ms: 1.48x faster                                  |
| crypto_pyaes            | 77.9 ms                                                | 52.7 ms: 1.48x faster                                  |
| nbody                   | 94.6 ms                                                | 64.0 ms: 1.48x faster                                  |
| pickle_pure_python      | 284 us                                                 | 192 us: 1.48x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.32 ms: 1.46x faster                                  |
| chaos                   | 66.5 ms                                                | 45.5 ms: 1.46x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 49.8 ms: 1.45x faster                                  |
| async_tree_none         | 396 ms                                                 | 280 ms: 1.41x faster                                   |
| float                   | 72.1 ms                                                | 51.9 ms: 1.39x faster                                  |
| async_tree_io           | 1.01 sec                                               | 732 ms: 1.38x faster                                   |
| json_dumps              | 8.34 ms                                                | 6.10 ms: 1.37x faster                                  |
| pycparser               | 915 ms                                                 | 669 ms: 1.37x faster                                   |
| pyflate                 | 454 ms                                                 | 333 ms: 1.36x faster                                   |
| regex_compile           | 96.2 ms                                                | 72.1 ms: 1.33x faster                                  |
| deepcopy_memo           | 34.4 us                                                | 25.9 us: 1.33x faster                                  |
| genshi_xml              | 37.7 ms                                                | 28.4 ms: 1.33x faster                                  |
| spectral_norm           | 95.8 ms                                                | 72.7 ms: 1.32x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 34.4 ms: 1.31x faster                                  |
| thrift                  | 577 us                                                 | 442 us: 1.31x faster                                   |
| unpickle_pure_python    | 204 us                                                 | 157 us: 1.30x faster                                   |
| django_template         | 27.2 ms                                                | 20.9 ms: 1.30x faster                                  |
| pprint_pformat          | 1.24 sec                                               | 955 ms: 1.30x faster                                   |
| sqlglot_parse           | 1.33 ms                                                | 1.02 ms: 1.30x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.19 ms: 1.29x faster                                  |
| pprint_safe_repr        | 608 ms                                                 | 470 ms: 1.29x faster                                   |
| tornado_http            | 90.1 ms                                                | 69.9 ms: 1.29x faster                                  |
| genshi_text             | 18.2 ms                                                | 14.3 ms: 1.28x faster                                  |
| dulwich_log             | 36.4 ms                                                | 28.6 ms: 1.27x faster                                  |
| mypy                    | 521 ms                                                 | 411 ms: 1.27x faster                                   |
| logging_simple          | 4.61 us                                                | 3.64 us: 1.27x faster                                  |
| deepcopy                | 278 us                                                 | 220 us: 1.27x faster                                   |
| html5lib                | 44.0 ms                                                | 34.8 ms: 1.26x faster                                  |
| logging_format          | 4.95 us                                                | 3.93 us: 1.26x faster                                  |
| fannkuch                | 318 ms                                                 | 256 ms: 1.24x faster                                   |
| chameleon               | 5.86 ms                                                | 4.71 ms: 1.24x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 536 ms: 1.24x faster                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.90 us: 1.24x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.81 ms: 1.23x faster                                  |
| 2to3                    | 222 ms                                                 | 182 ms: 1.22x faster                                   |
| sqlglot_optimize        | 38.1 ms                                                | 31.4 ms: 1.21x faster                                  |
| docutils                | 1.76 sec                                               | 1.45 sec: 1.21x faster                                 |
| scimark_fft             | 231 ms                                                 | 192 ms: 1.20x faster                                   |
| bench_thread_pool       | 531 us                                                 | 447 us: 1.19x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.2 ms: 1.18x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 32.8 ns: 1.17x faster                                  |
| sympy_str               | 169 ms                                                 | 145 ms: 1.16x faster                                   |
| sqlglot_normalize       | 198 ms                                                 | 171 ms: 1.16x faster                                   |
| async_generators        | 231 ms                                                 | 200 ms: 1.16x faster                                   |
| sympy_sum               | 93.5 ms                                                | 81.9 ms: 1.14x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 47.8 ms: 1.14x faster                                  |
| sympy_expand            | 275 ms                                                 | 243 ms: 1.13x faster                                   |
| nqueens                 | 68.6 ms                                                | 60.8 ms: 1.13x faster                                  |
| json                    | 3.13 ms                                                | 2.83 ms: 1.10x faster                                  |
| regex_dna               | 164 ms                                                 | 150 ms: 1.10x faster                                   |
| regex_v8                | 17.7 ms                                                | 16.2 ms: 1.10x faster                                  |
| mdp                     | 1.66 sec                                               | 1.52 sec: 1.09x faster                                 |
| sqlite_synth            | 1.50 us                                                | 1.40 us: 1.07x faster                                  |
| coroutines              | 20.1 ms                                                | 18.8 ms: 1.07x faster                                  |
| pathlib                 | 22.2 ms                                                | 20.8 ms: 1.07x faster                                  |
| xml_etree_parse         | 100 ms                                                 | 93.9 ms: 1.07x faster                                  |
| telco                   | 3.63 ms                                                | 3.43 ms: 1.06x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.05x faster                                  |
| python_startup          | 9.59 ms                                                | 9.36 ms: 1.02x faster                                  |
| meteor_contest          | 77.7 ms                                                | 75.9 ms: 1.02x faster                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 67.8 ms: 1.02x faster                                  |
| unpickle                | 10.0 us                                                | 9.91 us: 1.01x faster                                  |
| pidigits                | 284 ms                                                 | 283 ms: 1.00x faster                                   |
| pickle_dict             | 18.0 us                                                | 18.0 us: 1.00x slower                                  |
| pickle                  | 7.50 us                                                | 7.57 us: 1.01x slower                                  |
| unpickle_list           | 2.66 us                                                | 2.71 us: 1.02x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.35 ms: 1.05x slower                                  |
| generators              | 32.5 ms                                                | 34.1 ms: 1.05x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 42.9 ms: 1.05x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.63 ms: 1.07x slower                                  |
| coverage                | 40.8 ms                                                | 57.1 ms: 1.40x slower                                  |
| Geometric mean          | (ref)                                                  | 1.23x faster                                           |

Benchmark hidden because not significant (1): pickle_list
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of public/results/bm-20230204-3.12.0a4+-5a2b984/bm-20230204-darwin-arm64-python-main-3.12.0a4+-5a2b984.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
