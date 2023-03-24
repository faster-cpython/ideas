
# Results vs. 3.10.4

- fork: python
- ref: 7c12e4835ebe52287acd
- machine: linux-x86_64
- commit hash: 7c12e48
- commit date: 2021-10-05
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 329 ms: 1.02x faster                                                        |
| chameleon      | 9.13 ms                                                             | 8.97 ms: 1.02x faster                                                       |
| docutils       | 3.19 sec                                                            | 3.22 sec: 1.01x slower                                                      |
| html5lib       | 86.4 ms                                                             | 83.0 ms: 1.04x faster                                                       |
| tornado_http   | 129 ms                                                              | 136 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                               | 1.00x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 110 ms                                                              | 86.6 ms: 1.27x faster                                                       |
| nbody          | 146 ms                                                              | 132 ms: 1.10x faster                                                        |
| pidigits       | 190 ms                                                              | 266 ms: 1.40x slower                                                        |
| Geometric mean | (ref)                                                               | 1.00x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.22 ms                                                             | 3.05 ms: 1.05x faster                                                       |
| regex_compile  | 177 ms                                                              | 169 ms: 1.05x faster                                                        |
| regex_v8       | 24.9 ms                                                             | 25.6 ms: 1.03x slower                                                       |
| regex_dna      | 213 ms                                                              | 262 ms: 1.23x slower                                                        |
| Geometric mean | (ref)                                                               | 1.03x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_process    | 74.8 ms                                                             | 64.1 ms: 1.17x faster                                                       |
| pickle_pure_python   | 457 us                                                              | 394 us: 1.16x faster                                                        |
| pickle_list          | 4.73 us                                                             | 4.14 us: 1.14x faster                                                       |
| xml_etree_generate   | 94.9 ms                                                             | 86.0 ms: 1.10x faster                                                       |
| unpickle             | 15.0 us                                                             | 13.7 us: 1.10x faster                                                       |
| unpickle_list        | 4.94 us                                                             | 4.54 us: 1.09x faster                                                       |
| json_loads           | 29.3 us                                                             | 27.0 us: 1.09x faster                                                       |
| xml_etree_parse      | 164 ms                                                              | 158 ms: 1.03x faster                                                        |
| unpickle_pure_python | 300 us                                                              | 293 us: 1.02x faster                                                        |
| pickle               | 10.2 us                                                             | 10.4 us: 1.02x slower                                                       |
| pickle_dict          | 27.8 us                                                             | 31.5 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                               | 1.06x faster                                                                |

Benchmark hidden because not significant (2): json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 11.8 ms: 1.20x faster                                                       |
| python_startup_no_site | 5.80 ms                                                             | 7.57 ms: 1.31x slower                                                       |
| Geometric mean         | (ref)                                                               | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 13.1 ms: 1.13x faster                                                       |
| genshi_text     | 30.4 ms                                                             | 28.3 ms: 1.08x faster                                                       |
| genshi_xml      | 64.3 ms                                                             | 59.9 ms: 1.07x faster                                                       |
| django_template | 45.8 ms                                                             | 47.5 ms: 1.04x slower                                                       |
| Geometric mean  | (ref)                                                               | 1.06x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| bench_mp_pool           | 24.0 ms                                                             | 5.14 ms: 4.67x faster                                                       |
| flaskblogging           | 8.48 ms                                                             | 4.88 ms: 1.74x faster                                                       |
| gunicorn                | 1.43 ms                                                             | 988 us: 1.45x faster                                                        |
| generators              | 75.7 ms                                                             | 52.5 ms: 1.44x faster                                                       |
| async_tree_io           | 1.78 sec                                                            | 1.24 sec: 1.43x faster                                                      |
| unpack_sequence         | 65.6 ns                                                             | 46.5 ns: 1.41x faster                                                       |
| async_tree_none         | 713 ms                                                              | 515 ms: 1.38x faster                                                        |
| scimark_sor             | 198 ms                                                              | 147 ms: 1.35x faster                                                        |
| async_tree_memoization  | 853 ms                                                              | 660 ms: 1.29x faster                                                        |
| scimark_fft             | 425 ms                                                              | 333 ms: 1.28x faster                                                        |
| deltablue               | 7.30 ms                                                             | 5.73 ms: 1.27x faster                                                       |
| float                   | 110 ms                                                              | 86.6 ms: 1.27x faster                                                       |
| raytrace                | 470 ms                                                              | 371 ms: 1.27x faster                                                        |
| logging_silent          | 169 ns                                                              | 134 ns: 1.26x faster                                                        |
| spectral_norm           | 150 ms                                                              | 120 ms: 1.25x faster                                                        |
| logging_format          | 9.07 us                                                             | 7.28 us: 1.25x faster                                                       |
| scimark_monte_carlo     | 109 ms                                                              | 87.3 ms: 1.24x faster                                                       |
| logging_simple          | 8.21 us                                                             | 6.69 us: 1.23x faster                                                       |
| chaos                   | 106 ms                                                              | 87.5 ms: 1.21x faster                                                       |
| python_startup          | 14.1 ms                                                             | 11.8 ms: 1.20x faster                                                       |
| async_tree_cpu_io_mixed | 944 ms                                                              | 796 ms: 1.19x faster                                                        |
| async_generators        | 420 ms                                                              | 356 ms: 1.18x faster                                                        |
| xml_etree_process       | 74.8 ms                                                             | 64.1 ms: 1.17x faster                                                       |
| hexiom                  | 9.50 ms                                                             | 8.15 ms: 1.17x faster                                                       |
| pickle_pure_python      | 457 us                                                              | 394 us: 1.16x faster                                                        |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.84 ms: 1.16x faster                                                       |
| deepcopy_memo           | 51.8 us                                                             | 44.7 us: 1.16x faster                                                       |
| crypto_pyaes            | 117 ms                                                              | 102 ms: 1.14x faster                                                        |
| pickle_list             | 4.73 us                                                             | 4.14 us: 1.14x faster                                                       |
| richards                | 74.2 ms                                                             | 64.9 ms: 1.14x faster                                                       |
| mako                    | 14.7 ms                                                             | 13.1 ms: 1.13x faster                                                       |
| coroutines              | 31.8 ms                                                             | 28.5 ms: 1.12x faster                                                       |
| nbody                   | 146 ms                                                              | 132 ms: 1.10x faster                                                        |
| scimark_lu              | 160 ms                                                              | 145 ms: 1.10x faster                                                        |
| xml_etree_generate      | 94.9 ms                                                             | 86.0 ms: 1.10x faster                                                       |
| unpickle                | 15.0 us                                                             | 13.7 us: 1.10x faster                                                       |
| pyflate                 | 671 ms                                                              | 615 ms: 1.09x faster                                                        |
| unpickle_list           | 4.94 us                                                             | 4.54 us: 1.09x faster                                                       |
| json_loads              | 29.3 us                                                             | 27.0 us: 1.09x faster                                                       |
| pprint_safe_repr        | 953 ms                                                              | 879 ms: 1.08x faster                                                        |
| pycparser               | 1.53 sec                                                            | 1.41 sec: 1.08x faster                                                      |
| pprint_pformat          | 1.98 sec                                                            | 1.83 sec: 1.08x faster                                                      |
| sqlite_synth            | 2.97 us                                                             | 2.76 us: 1.08x faster                                                       |
| genshi_text             | 30.4 ms                                                             | 28.3 ms: 1.08x faster                                                       |
| genshi_xml              | 64.3 ms                                                             | 59.9 ms: 1.07x faster                                                       |
| go                      | 226 ms                                                              | 211 ms: 1.07x faster                                                        |
| regex_effbot            | 3.22 ms                                                             | 3.05 ms: 1.05x faster                                                       |
| regex_compile           | 177 ms                                                              | 169 ms: 1.05x faster                                                        |
| html5lib                | 86.4 ms                                                             | 83.0 ms: 1.04x faster                                                       |
| xml_etree_parse         | 164 ms                                                              | 158 ms: 1.03x faster                                                        |
| dulwich_log             | 76.3 ms                                                             | 74.2 ms: 1.03x faster                                                       |
| fannkuch                | 485 ms                                                              | 472 ms: 1.03x faster                                                        |
| deepcopy_reduce         | 3.80 us                                                             | 3.70 us: 1.03x faster                                                       |
| deepcopy                | 438 us                                                              | 427 us: 1.03x faster                                                        |
| unpickle_pure_python    | 300 us                                                              | 293 us: 1.02x faster                                                        |
| 2to3                    | 336 ms                                                              | 329 ms: 1.02x faster                                                        |
| thrift                  | 1.04 ms                                                             | 1.02 ms: 1.02x faster                                                       |
| chameleon               | 9.13 ms                                                             | 8.97 ms: 1.02x faster                                                       |
| dask                    | 437 ms                                                              | 433 ms: 1.01x faster                                                        |
| sympy_sum               | 185 ms                                                              | 184 ms: 1.00x faster                                                        |
| sqlglot_normalize       | 135 ms                                                              | 135 ms: 1.00x slower                                                        |
| docutils                | 3.19 sec                                                            | 3.22 sec: 1.01x slower                                                      |
| pickle                  | 10.2 us                                                             | 10.4 us: 1.02x slower                                                       |
| sqlglot_optimize        | 65.3 ms                                                             | 66.6 ms: 1.02x slower                                                       |
| coverage                | 70.6 ms                                                             | 72.0 ms: 1.02x slower                                                       |
| regex_v8                | 24.9 ms                                                             | 25.6 ms: 1.03x slower                                                       |
| mdp                     | 2.75 sec                                                            | 2.84 sec: 1.03x slower                                                      |
| django_template         | 45.8 ms                                                             | 47.5 ms: 1.04x slower                                                       |
| nqueens                 | 98.8 ms                                                             | 103 ms: 1.04x slower                                                        |
| sympy_str               | 328 ms                                                              | 343 ms: 1.05x slower                                                        |
| tornado_http            | 129 ms                                                              | 136 ms: 1.06x slower                                                        |
| pathlib                 | 19.8 ms                                                             | 20.9 ms: 1.06x slower                                                       |
| sympy_expand            | 540 ms                                                              | 573 ms: 1.06x slower                                                        |
| comprehensions          | 27.3 us                                                             | 29.5 us: 1.08x slower                                                       |
| sympy_integrate         | 24.3 ms                                                             | 26.8 ms: 1.10x slower                                                       |
| bench_thread_pool       | 954 us                                                              | 1.07 ms: 1.12x slower                                                       |
| sqlglot_transpile       | 2.45 ms                                                             | 2.76 ms: 1.12x slower                                                       |
| pickle_dict             | 27.8 us                                                             | 31.5 us: 1.13x slower                                                       |
| sqlglot_parse           | 2.07 ms                                                             | 2.37 ms: 1.15x slower                                                       |
| meteor_contest          | 115 ms                                                              | 133 ms: 1.16x slower                                                        |
| create_gc_cycles        | 1.64 ms                                                             | 1.90 ms: 1.16x slower                                                       |
| regex_dna               | 213 ms                                                              | 262 ms: 1.23x slower                                                        |
| python_startup_no_site  | 5.80 ms                                                             | 7.57 ms: 1.31x slower                                                       |
| pidigits                | 190 ms                                                              | 266 ms: 1.40x slower                                                        |
| Geometric mean          | (ref)                                                               | 1.09x faster                                                                |

Benchmark hidden because not significant (5): json_dumps, json, xml_etree_iterparse, telco, gc_traversal
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, asyncio_tcp, djangocms, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
