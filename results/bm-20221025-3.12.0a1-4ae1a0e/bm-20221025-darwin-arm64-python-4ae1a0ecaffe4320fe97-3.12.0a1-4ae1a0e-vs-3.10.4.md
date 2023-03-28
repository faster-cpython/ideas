
# Results vs. 3.10.4

- fork: python
- ref: 4ae1a0ecaffe4320fe97
- machine: darwin-arm64
- commit hash: 4ae1a0e
- commit date: 2022-10-25
- overall geometric mean: 1.18x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 165 ms: 1.34x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.58 ms: 1.28x faster                                                 |
| docutils       | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| html5lib       | 44.0 ms                                                | 36.5 ms: 1.20x faster                                                 |
| tornado_http   | 90.1 ms                                                | 70.8 ms: 1.27x faster                                                 |
| Geometric mean | (ref)                                                  | 1.26x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 64.7 ms: 1.46x faster                                                 |
| float          | 72.1 ms                                                | 56.4 ms: 1.28x faster                                                 |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.24x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 76.0 ms: 1.27x faster                                                 |
| regex_v8       | 17.7 ms                                                | 16.2 ms: 1.10x faster                                                 |
| regex_dna      | 164 ms                                                 | 153 ms: 1.07x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.68 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 208 us: 1.37x faster                                                  |
| json_dumps           | 8.34 ms                                                | 6.14 ms: 1.36x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 34.9 ms: 1.29x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 162 us: 1.26x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 47.2 ms: 1.15x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 93.9 ms: 1.07x faster                                                 |
| json_loads           | 17.0 us                                                | 16.4 us: 1.04x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.58 us: 1.03x faster                                                 |
| unpickle             | 10.0 us                                                | 9.71 us: 1.03x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 68.2 ms: 1.01x faster                                                 |
| pickle_dict          | 18.0 us                                                | 17.9 us: 1.00x faster                                                 |
| pickle               | 7.50 us                                                | 7.62 us: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x faster                                                          |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.1 ms: 1.26x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 10.0 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 8.16 ms: 1.30x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 29.8 ms: 1.26x faster                                                 |
| django_template | 27.2 ms                                                | 21.9 ms: 1.25x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.5 ms: 1.18x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.25x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.74 ms: 1.96x faster                                                 |
| logging_silent          | 119 ns                                                 | 66.2 ns: 1.80x faster                                                 |
| richards                | 51.4 ms                                                | 33.6 ms: 1.53x faster                                                 |
| scimark_lu              | 110 ms                                                 | 72.2 ms: 1.52x faster                                                 |
| crypto_pyaes            | 77.9 ms                                                | 51.9 ms: 1.50x faster                                                 |
| raytrace                | 329 ms                                                 | 222 ms: 1.48x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 331 ms: 1.47x faster                                                  |
| nbody                   | 94.6 ms                                                | 64.7 ms: 1.46x faster                                                 |
| go                      | 165 ms                                                 | 119 ms: 1.38x faster                                                  |
| pickle_pure_python      | 284 us                                                 | 208 us: 1.37x faster                                                  |
| json_dumps              | 8.34 ms                                                | 6.14 ms: 1.36x faster                                                 |
| async_tree_none         | 396 ms                                                 | 292 ms: 1.36x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 748 ms: 1.35x faster                                                  |
| 2to3                    | 222 ms                                                 | 165 ms: 1.34x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 54.5 ms: 1.33x faster                                                 |
| chaos                   | 66.5 ms                                                | 50.4 ms: 1.32x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 72.9 ms: 1.31x faster                                                 |
| thrift                  | 577 us                                                 | 441 us: 1.31x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.01 ms: 1.31x faster                                                 |
| pycparser               | 915 ms                                                 | 701 ms: 1.30x faster                                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.18 ms: 1.30x faster                                                 |
| mako                    | 10.6 ms                                                | 8.16 ms: 1.30x faster                                                 |
| pyflate                 | 454 ms                                                 | 351 ms: 1.30x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 34.9 ms: 1.29x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.93 ms: 1.28x faster                                                 |
| chameleon               | 5.86 ms                                                | 4.58 ms: 1.28x faster                                                 |
| float                   | 72.1 ms                                                | 56.4 ms: 1.28x faster                                                 |
| tornado_http            | 90.1 ms                                                | 70.8 ms: 1.27x faster                                                 |
| regex_compile           | 96.2 ms                                                | 76.0 ms: 1.27x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 29.8 ms: 1.26x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 162 us: 1.26x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.66 us: 1.26x faster                                                 |
| scimark_sor             | 126 ms                                                 | 100 ms: 1.25x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 486 ms: 1.25x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 992 ms: 1.25x faster                                                  |
| logging_format          | 4.95 us                                                | 3.96 us: 1.25x faster                                                 |
| django_template         | 27.2 ms                                                | 21.9 ms: 1.25x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.78 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed | 665 ms                                                 | 551 ms: 1.21x faster                                                  |
| html5lib                | 44.0 ms                                                | 36.5 ms: 1.20x faster                                                 |
| dulwich_log             | 36.4 ms                                                | 30.4 ms: 1.20x faster                                                 |
| docutils                | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| fannkuch                | 318 ms                                                 | 268 ms: 1.19x faster                                                  |
| sqlglot_optimize        | 38.1 ms                                                | 32.1 ms: 1.19x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 29.1 us: 1.18x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.5 ms: 1.18x faster                                                 |
| scimark_fft             | 231 ms                                                 | 197 ms: 1.18x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.04 us: 1.16x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 47.2 ms: 1.15x faster                                                 |
| deepcopy                | 278 us                                                 | 241 us: 1.15x faster                                                  |
| async_generators        | 231 ms                                                 | 201 ms: 1.15x faster                                                  |
| unpack_sequence         | 38.2 ns                                                | 33.3 ns: 1.15x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 174 ms: 1.14x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.7 ms: 1.14x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 468 us: 1.13x faster                                                  |
| nqueens                 | 68.6 ms                                                | 60.6 ms: 1.13x faster                                                 |
| sympy_expand            | 275 ms                                                 | 247 ms: 1.12x faster                                                  |
| pylint                  | 302 ms                                                 | 270 ms: 1.11x faster                                                  |
| generators              | 32.5 ms                                                | 29.2 ms: 1.11x faster                                                 |
| json                    | 3.13 ms                                                | 2.82 ms: 1.11x faster                                                 |
| sympy_str               | 169 ms                                                 | 153 ms: 1.11x faster                                                  |
| regex_v8                | 17.7 ms                                                | 16.2 ms: 1.10x faster                                                 |
| telco                   | 3.63 ms                                                | 3.32 ms: 1.09x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.52 sec: 1.09x faster                                                |
| sympy_sum               | 93.5 ms                                                | 86.4 ms: 1.08x faster                                                 |
| regex_dna               | 164 ms                                                 | 153 ms: 1.07x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 93.9 ms: 1.07x faster                                                 |
| coroutines              | 20.1 ms                                                | 19.0 ms: 1.06x faster                                                 |
| sqlite_synth            | 1.50 us                                                | 1.42 us: 1.05x faster                                                 |
| json_loads              | 17.0 us                                                | 16.4 us: 1.04x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.58 us: 1.03x faster                                                 |
| unpickle                | 10.0 us                                                | 9.71 us: 1.03x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 68.2 ms: 1.01x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 76.9 ms: 1.01x faster                                                 |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| pickle_dict             | 18.0 us                                                | 17.9 us: 1.00x faster                                                 |
| pickle                  | 7.50 us                                                | 7.62 us: 1.02x slower                                                 |
| bench_mp_pool           | 40.8 ms                                                | 43.7 ms: 1.07x slower                                                 |
| regex_effbot            | 2.45 ms                                                | 2.68 ms: 1.09x slower                                                 |
| pathlib                 | 22.2 ms                                                | 27.7 ms: 1.25x slower                                                 |
| python_startup          | 9.59 ms                                                | 12.1 ms: 1.26x slower                                                 |
| coverage                | 40.8 ms                                                | 53.1 ms: 1.30x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 10.0 ms: 1.43x slower                                                 |
| Geometric mean          | (ref)                                                  | 1.18x faster                                                          |

Benchmark hidden because not significant (1): pickle_list
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of public/results/bm-20221025-3.12.0a1-4ae1a0e/bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
