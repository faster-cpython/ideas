
# Results vs. 3.10.4

- fork: python
- ref: 2cdc5189a6bc3157fddd
- machine: linux-x86_64
- commit hash: 2cdc518
- commit date: 2023-03-26
- overall geometric mean: 1.30x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 253 ms: 1.33x faster                                                   |
| chameleon      | 9.13 ms                                                             | 6.52 ms: 1.40x faster                                                  |
| docutils       | 3.19 sec                                                            | 2.55 sec: 1.25x faster                                                 |
| html5lib       | 86.4 ms                                                             | 62.3 ms: 1.39x faster                                                  |
| tornado_http   | 129 ms                                                              | 91.1 ms: 1.42x faster                                                  |
| Geometric mean | (ref)                                                               | 1.36x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 87.8 ms: 1.66x faster                                                  |
| float          | 110 ms                                                              | 73.9 ms: 1.49x faster                                                  |
| pidigits       | 190 ms                                                              | 188 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                               | 1.35x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 135 ms: 1.32x faster                                                   |
| regex_v8       | 24.9 ms                                                             | 22.2 ms: 1.12x faster                                                  |
| regex_dna      | 213 ms                                                              | 208 ms: 1.03x faster                                                   |
| regex_effbot   | 3.22 ms                                                             | 3.66 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                               | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 285 us: 1.60x faster                                                   |
| unpickle_pure_python | 300 us                                                              | 202 us: 1.49x faster                                                   |
| json_dumps           | 13.7 ms                                                             | 9.57 ms: 1.43x faster                                                  |
| xml_etree_process    | 74.8 ms                                                             | 56.0 ms: 1.34x faster                                                  |
| json_loads           | 29.3 us                                                             | 24.2 us: 1.21x faster                                                  |
| xml_etree_generate   | 94.9 ms                                                             | 80.3 ms: 1.18x faster                                                  |
| unpickle             | 15.0 us                                                             | 13.2 us: 1.13x faster                                                  |
| xml_etree_iterparse  | 111 ms                                                              | 99.5 ms: 1.12x faster                                                  |
| pickle_list          | 4.73 us                                                             | 4.27 us: 1.11x faster                                                  |
| xml_etree_parse      | 164 ms                                                              | 149 ms: 1.10x faster                                                   |
| unpickle_list        | 4.94 us                                                             | 5.01 us: 1.01x slower                                                  |
| pickle               | 10.2 us                                                             | 10.4 us: 1.02x slower                                                  |
| pickle_dict          | 27.8 us                                                             | 31.0 us: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.18x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.79 ms: 1.61x faster                                                  |
| python_startup_no_site | 5.80 ms                                                             | 6.50 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                               | 1.20x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|-----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.89 ms: 1.49x faster                                                  |
| genshi_text     | 30.4 ms                                                             | 21.5 ms: 1.42x faster                                                  |
| django_template | 45.8 ms                                                             | 33.0 ms: 1.39x faster                                                  |
| genshi_xml      | 64.3 ms                                                             | 47.6 ms: 1.35x faster                                                  |
| Geometric mean  | (ref)                                                               | 1.41x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| generators              | 75.7 ms                                                             | 29.4 ms: 2.58x faster                                                  |
| deltablue               | 7.30 ms                                                             | 3.19 ms: 2.29x faster                                                  |
| asyncio_tcp             | 922 ms                                                              | 503 ms: 1.83x faster                                                   |
| scimark_sor             | 198 ms                                                              | 112 ms: 1.76x faster                                                   |
| logging_silent          | 169 ns                                                              | 96.5 ns: 1.75x faster                                                  |
| richards                | 74.2 ms                                                             | 43.5 ms: 1.70x faster                                                  |
| raytrace                | 470 ms                                                              | 280 ms: 1.68x faster                                                   |
| nbody                   | 146 ms                                                              | 87.8 ms: 1.66x faster                                                  |
| go                      | 226 ms                                                              | 137 ms: 1.65x faster                                                   |
| python_startup          | 14.1 ms                                                             | 8.79 ms: 1.61x faster                                                  |
| pickle_pure_python      | 457 us                                                              | 285 us: 1.60x faster                                                   |
| scimark_monte_carlo     | 109 ms                                                              | 67.8 ms: 1.60x faster                                                  |
| spectral_norm           | 150 ms                                                              | 94.0 ms: 1.60x faster                                                  |
| pyflate                 | 671 ms                                                              | 421 ms: 1.59x faster                                                   |
| chaos                   | 106 ms                                                              | 66.5 ms: 1.59x faster                                                  |
| hexiom                  | 9.50 ms                                                             | 6.01 ms: 1.58x faster                                                  |
| crypto_pyaes            | 117 ms                                                              | 74.0 ms: 1.58x faster                                                  |
| deepcopy_memo           | 51.8 us                                                             | 34.1 us: 1.52x faster                                                  |
| unpack_sequence         | 65.6 ns                                                             | 43.7 ns: 1.50x faster                                                  |
| mako                    | 14.7 ms                                                             | 9.89 ms: 1.49x faster                                                  |
| float                   | 110 ms                                                              | 73.9 ms: 1.49x faster                                                  |
| unpickle_pure_python    | 300 us                                                              | 202 us: 1.49x faster                                                   |
| scimark_lu              | 160 ms                                                              | 109 ms: 1.47x faster                                                   |
| sqlglot_parse           | 2.07 ms                                                             | 1.43 ms: 1.45x faster                                                  |
| logging_format          | 9.07 us                                                             | 6.28 us: 1.45x faster                                                  |
| logging_simple          | 8.21 us                                                             | 5.68 us: 1.44x faster                                                  |
| json_dumps              | 13.7 ms                                                             | 9.57 ms: 1.43x faster                                                  |
| sqlglot_transpile       | 2.45 ms                                                             | 1.72 ms: 1.43x faster                                                  |
| pprint_pformat          | 1.98 sec                                                            | 1.40 sec: 1.42x faster                                                 |
| genshi_text             | 30.4 ms                                                             | 21.5 ms: 1.42x faster                                                  |
| tornado_http            | 129 ms                                                              | 91.1 ms: 1.42x faster                                                  |
| chameleon               | 9.13 ms                                                             | 6.52 ms: 1.40x faster                                                  |
| pprint_safe_repr        | 953 ms                                                              | 685 ms: 1.39x faster                                                   |
| django_template         | 45.8 ms                                                             | 33.0 ms: 1.39x faster                                                  |
| html5lib                | 86.4 ms                                                             | 62.3 ms: 1.39x faster                                                  |
| async_tree_io           | 1.78 sec                                                            | 1.29 sec: 1.38x faster                                                 |
| scimark_fft             | 425 ms                                                              | 308 ms: 1.38x faster                                                   |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.13 ms: 1.36x faster                                                  |
| async_tree_none         | 713 ms                                                              | 526 ms: 1.36x faster                                                   |
| genshi_xml              | 64.3 ms                                                             | 47.6 ms: 1.35x faster                                                  |
| aiohttp                 | 1.35 ms                                                             | 1.01 ms: 1.34x faster                                                  |
| xml_etree_process       | 74.8 ms                                                             | 56.0 ms: 1.34x faster                                                  |
| deepcopy                | 438 us                                                              | 328 us: 1.33x faster                                                   |
| 2to3                    | 336 ms                                                              | 253 ms: 1.33x faster                                                   |
| thrift                  | 1.04 ms                                                             | 780 us: 1.33x faster                                                   |
| coroutines              | 31.8 ms                                                             | 23.9 ms: 1.33x faster                                                  |
| gunicorn                | 1.43 ms                                                             | 1.09 ms: 1.32x faster                                                  |
| regex_compile           | 177 ms                                                              | 135 ms: 1.32x faster                                                   |
| async_tree_memoization  | 853 ms                                                              | 652 ms: 1.31x faster                                                   |
| pycparser               | 1.53 sec                                                            | 1.17 sec: 1.31x faster                                                 |
| mypy2                   | 432 ms                                                              | 333 ms: 1.30x faster                                                   |
| deepcopy_reduce         | 3.80 us                                                             | 2.95 us: 1.29x faster                                                  |
| fannkuch                | 485 ms                                                              | 380 ms: 1.27x faster                                                   |
| sqlglot_optimize        | 65.3 ms                                                             | 51.3 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed | 944 ms                                                              | 746 ms: 1.27x faster                                                   |
| docutils                | 3.19 sec                                                            | 2.55 sec: 1.25x faster                                                 |
| sqlglot_normalize       | 135 ms                                                              | 107 ms: 1.25x faster                                                   |
| nqueens                 | 98.8 ms                                                             | 80.8 ms: 1.22x faster                                                  |
| sqlalchemy_declarative  | 166 ms                                                              | 136 ms: 1.22x faster                                                   |
| json_loads              | 29.3 us                                                             | 24.2 us: 1.21x faster                                                  |
| bench_thread_pool       | 954 us                                                              | 789 us: 1.21x faster                                                   |
| dulwich_log             | 76.3 ms                                                             | 63.1 ms: 1.21x faster                                                  |
| sqlalchemy_imperative   | 21.2 ms                                                             | 17.6 ms: 1.21x faster                                                  |
| xml_etree_generate      | 94.9 ms                                                             | 80.3 ms: 1.18x faster                                                  |
| sympy_integrate         | 24.3 ms                                                             | 20.6 ms: 1.18x faster                                                  |
| json                    | 5.41 ms                                                             | 4.60 ms: 1.18x faster                                                  |
| sympy_expand            | 540 ms                                                              | 463 ms: 1.17x faster                                                   |
| comprehensions          | 27.3 us                                                             | 23.7 us: 1.15x faster                                                  |
| sympy_str               | 328 ms                                                              | 285 ms: 1.15x faster                                                   |
| sqlite_synth            | 2.97 us                                                             | 2.62 us: 1.14x faster                                                  |
| unpickle                | 15.0 us                                                             | 13.2 us: 1.13x faster                                                  |
| djangocms               | 36.3 us                                                             | 32.3 us: 1.12x faster                                                  |
| regex_v8                | 24.9 ms                                                             | 22.2 ms: 1.12x faster                                                  |
| meteor_contest          | 115 ms                                                              | 102 ms: 1.12x faster                                                   |
| create_gc_cycles        | 1.64 ms                                                             | 1.46 ms: 1.12x faster                                                  |
| xml_etree_iterparse     | 111 ms                                                              | 99.5 ms: 1.12x faster                                                  |
| sympy_sum               | 185 ms                                                              | 166 ms: 1.11x faster                                                   |
| pickle_list             | 4.73 us                                                             | 4.27 us: 1.11x faster                                                  |
| pathlib                 | 19.8 ms                                                             | 17.9 ms: 1.10x faster                                                  |
| xml_etree_parse         | 164 ms                                                              | 149 ms: 1.10x faster                                                   |
| mdp                     | 2.75 sec                                                            | 2.54 sec: 1.08x faster                                                 |
| async_generators        | 420 ms                                                              | 408 ms: 1.03x faster                                                   |
| regex_dna               | 213 ms                                                              | 208 ms: 1.03x faster                                                   |
| pidigits                | 190 ms                                                              | 188 ms: 1.01x faster                                                   |
| unpickle_list           | 4.94 us                                                             | 5.01 us: 1.01x slower                                                  |
| pickle                  | 10.2 us                                                             | 10.4 us: 1.02x slower                                                  |
| pickle_dict             | 27.8 us                                                             | 31.0 us: 1.12x slower                                                  |
| python_startup_no_site  | 5.80 ms                                                             | 6.50 ms: 1.12x slower                                                  |
| regex_effbot            | 3.22 ms                                                             | 3.66 ms: 1.14x slower                                                  |
| dask                    | 437 ms                                                              | 511 ms: 1.17x slower                                                   |
| gc_traversal            | 3.53 ms                                                             | 4.31 ms: 1.22x slower                                                  |
| coverage                | 70.6 ms                                                             | 95.5 ms: 1.35x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.30x faster                                                           |

Benchmark hidden because not significant (2): telco, bench_mp_pool
Ignored benchmarks (2) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging, pylint
