
# Results vs. 3.10.4

- fork: python
- ref: b6bd7ffcbc1ffaa68e34
- machine: linux-x86_64
- commit hash: b6bd7ff
- commit date: 2022-12-06
- overall geometric mean: 1.29x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 246 ms: 1.36x faster                                                  |
| chameleon      | 9.13 ms                                                             | 6.48 ms: 1.41x faster                                                 |
| docutils       | 3.19 sec                                                            | 2.55 sec: 1.25x faster                                                |
| html5lib       | 86.4 ms                                                             | 60.0 ms: 1.44x faster                                                 |
| Geometric mean | (ref)                                                               | 1.36x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 96.4 ms: 1.51x faster                                                 |
| float          | 110 ms                                                              | 73.3 ms: 1.50x faster                                                 |
| pidigits       | 190 ms                                                              | 189 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                               | 1.31x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 130 ms: 1.36x faster                                                  |
| regex_v8       | 24.9 ms                                                             | 21.0 ms: 1.19x faster                                                 |
| regex_dna      | 213 ms                                                              | 201 ms: 1.06x faster                                                  |
| regex_effbot   | 3.22 ms                                                             | 3.44 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                               | 1.12x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 282 us: 1.62x faster                                                  |
| unpickle_pure_python | 300 us                                                              | 199 us: 1.50x faster                                                  |
| json_dumps           | 13.7 ms                                                             | 9.51 ms: 1.44x faster                                                 |
| xml_etree_process    | 74.8 ms                                                             | 53.6 ms: 1.40x faster                                                 |
| xml_etree_generate   | 94.9 ms                                                             | 76.8 ms: 1.23x faster                                                 |
| json_loads           | 29.3 us                                                             | 23.8 us: 1.23x faster                                                 |
| pickle_list          | 4.73 us                                                             | 3.99 us: 1.19x faster                                                 |
| unpickle             | 15.0 us                                                             | 13.1 us: 1.14x faster                                                 |
| xml_etree_parse      | 164 ms                                                              | 149 ms: 1.10x faster                                                  |
| xml_etree_iterparse  | 111 ms                                                              | 105 ms: 1.06x faster                                                  |
| pickle               | 10.2 us                                                             | 10.3 us: 1.01x slower                                                 |
| unpickle_list        | 4.94 us                                                             | 5.02 us: 1.02x slower                                                 |
| pickle_dict          | 27.8 us                                                             | 30.9 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.20x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.55 ms: 1.65x faster                                                 |
| python_startup_no_site | 5.80 ms                                                             | 6.10 ms: 1.05x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.25x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.48 ms: 1.55x faster                                                 |
| genshi_text     | 30.4 ms                                                             | 20.3 ms: 1.49x faster                                                 |
| django_template | 45.8 ms                                                             | 32.5 ms: 1.41x faster                                                 |
| genshi_xml      | 64.3 ms                                                             | 46.5 ms: 1.38x faster                                                 |
| Geometric mean  | (ref)                                                               | 1.46x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 7.30 ms                                                             | 3.22 ms: 2.27x faster                                                 |
| scimark_sor             | 198 ms                                                              | 105 ms: 1.88x faster                                                  |
| logging_silent          | 169 ns                                                              | 93.1 ns: 1.81x faster                                                 |
| richards                | 74.2 ms                                                             | 41.6 ms: 1.78x faster                                                 |
| scimark_monte_carlo     | 109 ms                                                              | 64.3 ms: 1.69x faster                                                 |
| pyflate                 | 671 ms                                                              | 398 ms: 1.68x faster                                                  |
| raytrace                | 470 ms                                                              | 283 ms: 1.66x faster                                                  |
| python_startup          | 14.1 ms                                                             | 8.55 ms: 1.65x faster                                                 |
| go                      | 226 ms                                                              | 137 ms: 1.64x faster                                                  |
| pickle_pure_python      | 457 us                                                              | 282 us: 1.62x faster                                                  |
| chaos                   | 106 ms                                                              | 66.6 ms: 1.59x faster                                                 |
| crypto_pyaes            | 117 ms                                                              | 74.2 ms: 1.57x faster                                                 |
| mako                    | 14.7 ms                                                             | 9.48 ms: 1.55x faster                                                 |
| hexiom                  | 9.50 ms                                                             | 6.12 ms: 1.55x faster                                                 |
| sqlglot_parse           | 2.07 ms                                                             | 1.34 ms: 1.54x faster                                                 |
| spectral_norm           | 150 ms                                                              | 98.1 ms: 1.53x faster                                                 |
| scimark_lu              | 160 ms                                                              | 106 ms: 1.51x faster                                                  |
| nbody                   | 146 ms                                                              | 96.4 ms: 1.51x faster                                                 |
| deepcopy_memo           | 51.8 us                                                             | 34.3 us: 1.51x faster                                                 |
| sqlglot_transpile       | 2.45 ms                                                             | 1.63 ms: 1.51x faster                                                 |
| unpickle_pure_python    | 300 us                                                              | 199 us: 1.50x faster                                                  |
| float                   | 110 ms                                                              | 73.3 ms: 1.50x faster                                                 |
| genshi_text             | 30.4 ms                                                             | 20.3 ms: 1.49x faster                                                 |
| json_dumps              | 13.7 ms                                                             | 9.51 ms: 1.44x faster                                                 |
| html5lib                | 86.4 ms                                                             | 60.0 ms: 1.44x faster                                                 |
| pprint_pformat          | 1.98 sec                                                            | 1.39 sec: 1.43x faster                                                |
| logging_format          | 9.07 us                                                             | 6.37 us: 1.42x faster                                                 |
| pprint_safe_repr        | 953 ms                                                              | 670 ms: 1.42x faster                                                  |
| logging_simple          | 8.21 us                                                             | 5.79 us: 1.42x faster                                                 |
| unpack_sequence         | 65.6 ns                                                             | 46.5 ns: 1.41x faster                                                 |
| chameleon               | 9.13 ms                                                             | 6.48 ms: 1.41x faster                                                 |
| django_template         | 45.8 ms                                                             | 32.5 ms: 1.41x faster                                                 |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.01 ms: 1.40x faster                                                 |
| pycparser               | 1.53 sec                                                            | 1.10 sec: 1.40x faster                                                |
| xml_etree_process       | 74.8 ms                                                             | 53.6 ms: 1.40x faster                                                 |
| thrift                  | 1.04 ms                                                             | 749 us: 1.38x faster                                                  |
| genshi_xml              | 64.3 ms                                                             | 46.5 ms: 1.38x faster                                                 |
| 2to3                    | 336 ms                                                              | 246 ms: 1.36x faster                                                  |
| regex_compile           | 177 ms                                                              | 130 ms: 1.36x faster                                                  |
| scimark_fft             | 425 ms                                                              | 313 ms: 1.36x faster                                                  |
| async_tree_io           | 1.78 sec                                                            | 1.34 sec: 1.33x faster                                                |
| async_tree_none         | 713 ms                                                              | 539 ms: 1.32x faster                                                  |
| deepcopy                | 438 us                                                              | 332 us: 1.32x faster                                                  |
| deepcopy_reduce         | 3.80 us                                                             | 2.89 us: 1.31x faster                                                 |
| mypy2                   | 432 ms                                                              | 329 ms: 1.31x faster                                                  |
| fannkuch                | 485 ms                                                              | 372 ms: 1.30x faster                                                  |
| sqlglot_optimize        | 65.3 ms                                                             | 50.5 ms: 1.29x faster                                                 |
| sqlglot_normalize       | 135 ms                                                              | 104 ms: 1.29x faster                                                  |
| coroutines              | 31.8 ms                                                             | 24.9 ms: 1.28x faster                                                 |
| docutils                | 3.19 sec                                                            | 2.55 sec: 1.25x faster                                                |
| nqueens                 | 98.8 ms                                                             | 79.2 ms: 1.25x faster                                                 |
| async_tree_memoization  | 853 ms                                                              | 684 ms: 1.25x faster                                                  |
| xml_etree_generate      | 94.9 ms                                                             | 76.8 ms: 1.23x faster                                                 |
| json_loads              | 29.3 us                                                             | 23.8 us: 1.23x faster                                                 |
| async_tree_cpu_io_mixed | 944 ms                                                              | 766 ms: 1.23x faster                                                  |
| bench_thread_pool       | 954 us                                                              | 776 us: 1.23x faster                                                  |
| dulwich_log             | 76.3 ms                                                             | 62.3 ms: 1.22x faster                                                 |
| dask                    | 437 ms                                                              | 359 ms: 1.22x faster                                                  |
| async_generators        | 420 ms                                                              | 351 ms: 1.20x faster                                                  |
| sympy_expand            | 540 ms                                                              | 451 ms: 1.20x faster                                                  |
| sympy_integrate         | 24.3 ms                                                             | 20.4 ms: 1.19x faster                                                 |
| regex_v8                | 24.9 ms                                                             | 21.0 ms: 1.19x faster                                                 |
| pickle_list             | 4.73 us                                                             | 3.99 us: 1.19x faster                                                 |
| json                    | 5.41 ms                                                             | 4.64 ms: 1.17x faster                                                 |
| sympy_str               | 328 ms                                                              | 281 ms: 1.17x faster                                                  |
| comprehensions          | 27.3 us                                                             | 23.5 us: 1.16x faster                                                 |
| sqlite_synth            | 2.97 us                                                             | 2.59 us: 1.15x faster                                                 |
| unpickle                | 15.0 us                                                             | 13.1 us: 1.14x faster                                                 |
| sympy_sum               | 185 ms                                                              | 163 ms: 1.14x faster                                                  |
| create_gc_cycles        | 1.64 ms                                                             | 1.45 ms: 1.13x faster                                                 |
| djangocms               | 36.3 us                                                             | 32.3 us: 1.13x faster                                                 |
| pathlib                 | 19.8 ms                                                             | 17.6 ms: 1.12x faster                                                 |
| xml_etree_parse         | 164 ms                                                              | 149 ms: 1.10x faster                                                  |
| meteor_contest          | 115 ms                                                              | 105 ms: 1.10x faster                                                  |
| xml_etree_iterparse     | 111 ms                                                              | 105 ms: 1.06x faster                                                  |
| telco                   | 6.67 ms                                                             | 6.28 ms: 1.06x faster                                                 |
| regex_dna               | 213 ms                                                              | 201 ms: 1.06x faster                                                  |
| asyncio_tcp             | 922 ms                                                              | 890 ms: 1.04x faster                                                  |
| mdp                     | 2.75 sec                                                            | 2.74 sec: 1.01x faster                                                |
| pidigits                | 190 ms                                                              | 189 ms: 1.00x faster                                                  |
| pickle                  | 10.2 us                                                             | 10.3 us: 1.01x slower                                                 |
| unpickle_list           | 4.94 us                                                             | 5.02 us: 1.02x slower                                                 |
| generators              | 75.7 ms                                                             | 77.4 ms: 1.02x slower                                                 |
| python_startup_no_site  | 5.80 ms                                                             | 6.10 ms: 1.05x slower                                                 |
| regex_effbot            | 3.22 ms                                                             | 3.44 ms: 1.07x slower                                                 |
| pickle_dict             | 27.8 us                                                             | 30.9 us: 1.11x slower                                                 |
| gc_traversal            | 3.53 ms                                                             | 4.38 ms: 1.24x slower                                                 |
| coverage                | 70.6 ms                                                             | 101 ms: 1.43x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.29x faster                                                          |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
