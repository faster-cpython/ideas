
# Results vs. 3.10.4

- fork: python
- ref: f9774e57d84162ff0cba
- machine: darwin-arm64
- commit hash: f9774e5
- commit date: 2023-03-07
- overall geometric mean: 1.19x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 165 ms: 1.35x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.48 ms: 1.31x faster                                                 |
| docutils       | 1.76 sec                                               | 1.49 sec: 1.18x faster                                                |
| html5lib       | 44.0 ms                                                | 35.4 ms: 1.24x faster                                                 |
| tornado_http   | 90.1 ms                                                | 70.0 ms: 1.29x faster                                                 |
| Geometric mean | (ref)                                                  | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 66.1 ms: 1.43x faster                                                 |
| float          | 72.1 ms                                                | 53.5 ms: 1.35x faster                                                 |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.4 ms: 1.28x faster                                                 |
| regex_v8       | 17.7 ms                                                | 16.2 ms: 1.09x faster                                                 |
| regex_dna      | 164 ms                                                 | 153 ms: 1.07x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.69 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 191 us: 1.49x faster                                                  |
| unpickle_pure_python | 204 us                                                 | 145 us: 1.40x faster                                                  |
| json_dumps           | 8.34 ms                                                | 6.18 ms: 1.35x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 37.0 ms: 1.22x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 51.1 ms: 1.07x faster                                                 |
| json_loads           | 17.0 us                                                | 16.1 us: 1.06x faster                                                 |
| unpickle             | 10.0 us                                                | 9.71 us: 1.03x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 97.9 ms: 1.02x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.65 us: 1.00x faster                                                 |
| pickle               | 7.50 us                                                | 7.47 us: 1.00x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 71.1 ms: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x faster                                                          |

Benchmark hidden because not significant (2): pickle_dict, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.5 ms: 1.30x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 10.4 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.39x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.44 ms: 1.42x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 29.2 ms: 1.29x faster                                                 |
| django_template | 27.2 ms                                                | 21.6 ms: 1.26x faster                                                 |
| genshi_text     | 18.2 ms                                                | 14.7 ms: 1.24x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.30x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.59 ms: 2.08x faster                                                 |
| logging_silent          | 119 ns                                                 | 69.3 ns: 1.72x faster                                                 |
| richards                | 51.4 ms                                                | 30.5 ms: 1.68x faster                                                 |
| go                      | 165 ms                                                 | 111 ms: 1.49x faster                                                  |
| pickle_pure_python      | 284 us                                                 | 191 us: 1.49x faster                                                  |
| scimark_lu              | 110 ms                                                 | 74.2 ms: 1.48x faster                                                 |
| crypto_pyaes            | 77.9 ms                                                | 53.5 ms: 1.46x faster                                                 |
| async_tree_memoization  | 485 ms                                                 | 336 ms: 1.44x faster                                                  |
| raytrace                | 329 ms                                                 | 229 ms: 1.44x faster                                                  |
| scimark_sor             | 126 ms                                                 | 87.7 ms: 1.44x faster                                                 |
| nbody                   | 94.6 ms                                                | 66.1 ms: 1.43x faster                                                 |
| mako                    | 10.6 ms                                                | 7.44 ms: 1.42x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 51.0 ms: 1.42x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.46 ms: 1.42x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 145 us: 1.40x faster                                                  |
| chaos                   | 66.5 ms                                                | 47.8 ms: 1.39x faster                                                 |
| pyflate                 | 454 ms                                                 | 331 ms: 1.37x faster                                                  |
| async_tree_none         | 396 ms                                                 | 289 ms: 1.37x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 744 ms: 1.36x faster                                                  |
| pycparser               | 915 ms                                                 | 674 ms: 1.36x faster                                                  |
| 2to3                    | 222 ms                                                 | 165 ms: 1.35x faster                                                  |
| json_dumps              | 8.34 ms                                                | 6.18 ms: 1.35x faster                                                 |
| float                   | 72.1 ms                                                | 53.5 ms: 1.35x faster                                                 |
| chameleon               | 5.86 ms                                                | 4.48 ms: 1.31x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 26.4 us: 1.30x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 29.2 ms: 1.29x faster                                                 |
| tornado_http            | 90.1 ms                                                | 70.0 ms: 1.29x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 74.9 ms: 1.28x faster                                                 |
| pprint_pformat          | 1.24 sec                                               | 970 ms: 1.28x faster                                                  |
| regex_compile           | 96.2 ms                                                | 75.4 ms: 1.28x faster                                                 |
| thrift                  | 577 us                                                 | 453 us: 1.28x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 477 ms: 1.27x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.05 ms: 1.27x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.22 ms: 1.26x faster                                                 |
| django_template         | 27.2 ms                                                | 21.6 ms: 1.26x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.66 us: 1.26x faster                                                 |
| logging_format          | 4.95 us                                                | 3.95 us: 1.25x faster                                                 |
| deepcopy                | 278 us                                                 | 222 us: 1.25x faster                                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.21 ms: 1.25x faster                                                 |
| html5lib                | 44.0 ms                                                | 35.4 ms: 1.24x faster                                                 |
| genshi_text             | 18.2 ms                                                | 14.7 ms: 1.24x faster                                                 |
| dulwich_log             | 36.4 ms                                                | 29.6 ms: 1.23x faster                                                 |
| fannkuch                | 318 ms                                                 | 258 ms: 1.23x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 37.0 ms: 1.22x faster                                                 |
| async_tree_cpu_io_mixed | 665 ms                                                 | 547 ms: 1.22x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.95 us: 1.21x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 32.1 ms: 1.18x faster                                                 |
| docutils                | 1.76 sec                                               | 1.49 sec: 1.18x faster                                                |
| scimark_fft             | 231 ms                                                 | 196 ms: 1.18x faster                                                  |
| generators              | 32.5 ms                                                | 27.9 ms: 1.17x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 63.8 ms: 1.17x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 32.9 ns: 1.16x faster                                                 |
| sympy_integrate         | 13.3 ms                                                | 11.7 ms: 1.14x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 175 ms: 1.14x faster                                                  |
| bench_thread_pool       | 531 us                                                 | 472 us: 1.12x faster                                                  |
| json                    | 3.13 ms                                                | 2.79 ms: 1.12x faster                                                 |
| coroutines              | 20.1 ms                                                | 18.1 ms: 1.11x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.50 sec: 1.11x faster                                                |
| sympy_expand            | 275 ms                                                 | 248 ms: 1.11x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.37 us: 1.10x faster                                                 |
| regex_v8                | 17.7 ms                                                | 16.2 ms: 1.09x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.17 ms: 1.09x faster                                                 |
| sympy_str               | 169 ms                                                 | 155 ms: 1.09x faster                                                  |
| nqueens                 | 68.6 ms                                                | 63.1 ms: 1.09x faster                                                 |
| regex_dna               | 164 ms                                                 | 153 ms: 1.07x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 51.1 ms: 1.07x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 72.9 ms: 1.07x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 88.2 ms: 1.06x faster                                                 |
| json_loads              | 17.0 us                                                | 16.1 us: 1.06x faster                                                 |
| telco                   | 3.63 ms                                                | 3.49 ms: 1.04x faster                                                 |
| unpickle                | 10.0 us                                                | 9.71 us: 1.03x faster                                                 |
| xml_etree_parse         | 100 ms                                                 | 97.9 ms: 1.02x faster                                                 |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| unpickle_list           | 2.66 us                                                | 2.65 us: 1.00x faster                                                 |
| pickle                  | 7.50 us                                                | 7.47 us: 1.00x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 71.1 ms: 1.03x slower                                                 |
| regex_effbot            | 2.45 ms                                                | 2.69 ms: 1.10x slower                                                 |
| bench_mp_pool           | 40.8 ms                                                | 46.5 ms: 1.14x slower                                                 |
| async_generators        | 231 ms                                                 | 272 ms: 1.18x slower                                                  |
| pathlib                 | 22.2 ms                                                | 27.5 ms: 1.24x slower                                                 |
| python_startup          | 9.59 ms                                                | 12.5 ms: 1.30x slower                                                 |
| coverage                | 40.8 ms                                                | 59.6 ms: 1.46x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 10.4 ms: 1.48x slower                                                 |
| Geometric mean          | (ref)                                                  | 1.19x faster                                                          |

Benchmark hidden because not significant (2): pickle_dict, pickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230307-3.12.0a6-f9774e5/bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
