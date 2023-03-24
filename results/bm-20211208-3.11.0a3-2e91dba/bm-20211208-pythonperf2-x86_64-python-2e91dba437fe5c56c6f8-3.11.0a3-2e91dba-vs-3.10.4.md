
# Results vs. 3.10.4

- fork: python
- ref: 2e91dba437fe5c56c6f8
- machine: linux-x86_64
- commit hash: 2e91dba
- commit date: 2021-12-08
- overall geometric mean: 1.14x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 293 ms: 1.15x faster                                                        |
| chameleon      | 9.13 ms                                                             | 8.85 ms: 1.03x faster                                                       |
| docutils       | 3.19 sec                                                            | 3.02 sec: 1.06x faster                                                      |
| html5lib       | 86.4 ms                                                             | 75.1 ms: 1.15x faster                                                       |
| tornado_http   | 129 ms                                                              | 135 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                               | 1.07x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 110 ms                                                              | 80.9 ms: 1.36x faster                                                       |
| nbody          | 146 ms                                                              | 109 ms: 1.34x faster                                                        |
| pidigits       | 190 ms                                                              | 253 ms: 1.33x slower                                                        |
| Geometric mean | (ref)                                                               | 1.11x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 153 ms: 1.16x faster                                                        |
| regex_effbot   | 3.22 ms                                                             | 3.10 ms: 1.04x faster                                                       |
| regex_v8       | 24.9 ms                                                             | 25.7 ms: 1.03x slower                                                       |
| regex_dna      | 213 ms                                                              | 261 ms: 1.22x slower                                                        |
| Geometric mean | (ref)                                                               | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 366 us: 1.25x faster                                                        |
| xml_etree_process    | 74.8 ms                                                             | 60.9 ms: 1.23x faster                                                       |
| json_loads           | 29.3 us                                                             | 25.3 us: 1.16x faster                                                       |
| xml_etree_generate   | 94.9 ms                                                             | 82.8 ms: 1.15x faster                                                       |
| unpickle             | 15.0 us                                                             | 13.2 us: 1.13x faster                                                       |
| unpickle_pure_python | 300 us                                                              | 265 us: 1.13x faster                                                        |
| pickle_list          | 4.73 us                                                             | 4.32 us: 1.10x faster                                                       |
| unpickle_list        | 4.94 us                                                             | 4.53 us: 1.09x faster                                                       |
| xml_etree_parse      | 164 ms                                                              | 155 ms: 1.05x faster                                                        |
| xml_etree_iterparse  | 111 ms                                                              | 110 ms: 1.01x faster                                                        |
| json_dumps           | 13.7 ms                                                             | 14.1 ms: 1.03x slower                                                       |
| pickle_dict          | 27.8 us                                                             | 33.0 us: 1.19x slower                                                       |
| Geometric mean       | (ref)                                                               | 1.08x faster                                                                |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 10.1 ms: 1.40x faster                                                       |
| python_startup_no_site | 5.80 ms                                                             | 7.14 ms: 1.23x slower                                                       |
| Geometric mean         | (ref)                                                               | 1.07x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 12.9 ms: 1.15x faster                                                       |
| genshi_xml      | 64.3 ms                                                             | 59.7 ms: 1.08x faster                                                       |
| genshi_text     | 30.4 ms                                                             | 28.2 ms: 1.08x faster                                                       |
| django_template | 45.8 ms                                                             | 44.9 ms: 1.02x faster                                                       |
| Geometric mean  | (ref)                                                               | 1.08x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211208-pythonperf2-x86_64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| bench_mp_pool           | 24.0 ms                                                             | 4.90 ms: 4.89x faster                                                       |
| scimark_sor             | 198 ms                                                              | 115 ms: 1.71x faster                                                        |
| flaskblogging           | 8.48 ms                                                             | 4.95 ms: 1.71x faster                                                       |
| deltablue               | 7.30 ms                                                             | 4.78 ms: 1.53x faster                                                       |
| generators              | 75.7 ms                                                             | 50.1 ms: 1.51x faster                                                       |
| spectral_norm           | 150 ms                                                              | 99.9 ms: 1.50x faster                                                       |
| scimark_lu              | 160 ms                                                              | 110 ms: 1.46x faster                                                        |
| logging_silent          | 169 ns                                                              | 116 ns: 1.46x faster                                                        |
| gunicorn                | 1.43 ms                                                             | 1.00 ms: 1.43x faster                                                       |
| unpack_sequence         | 65.6 ns                                                             | 46.3 ns: 1.42x faster                                                       |
| scimark_monte_carlo     | 109 ms                                                              | 76.7 ms: 1.42x faster                                                       |
| python_startup          | 14.1 ms                                                             | 10.1 ms: 1.40x faster                                                       |
| float                   | 110 ms                                                              | 80.9 ms: 1.36x faster                                                       |
| scimark_fft             | 425 ms                                                              | 314 ms: 1.36x faster                                                        |
| raytrace                | 470 ms                                                              | 347 ms: 1.35x faster                                                        |
| chaos                   | 106 ms                                                              | 78.3 ms: 1.35x faster                                                       |
| async_tree_io           | 1.78 sec                                                            | 1.32 sec: 1.35x faster                                                      |
| nbody                   | 146 ms                                                              | 109 ms: 1.34x faster                                                        |
| async_generators        | 420 ms                                                              | 319 ms: 1.32x faster                                                        |
| go                      | 226 ms                                                              | 173 ms: 1.31x faster                                                        |
| richards                | 74.2 ms                                                             | 56.7 ms: 1.31x faster                                                       |
| async_tree_none         | 713 ms                                                              | 545 ms: 1.31x faster                                                        |
| hexiom                  | 9.50 ms                                                             | 7.41 ms: 1.28x faster                                                       |
| pyflate                 | 671 ms                                                              | 525 ms: 1.28x faster                                                        |
| deepcopy_memo           | 51.8 us                                                             | 41.5 us: 1.25x faster                                                       |
| pickle_pure_python      | 457 us                                                              | 366 us: 1.25x faster                                                        |
| async_tree_memoization  | 853 ms                                                              | 686 ms: 1.24x faster                                                        |
| crypto_pyaes            | 117 ms                                                              | 94.7 ms: 1.23x faster                                                       |
| xml_etree_process       | 74.8 ms                                                             | 60.9 ms: 1.23x faster                                                       |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.58 ms: 1.23x faster                                                       |
| coroutines              | 31.8 ms                                                             | 27.0 ms: 1.18x faster                                                       |
| logging_format          | 9.07 us                                                             | 7.70 us: 1.18x faster                                                       |
| logging_simple          | 8.21 us                                                             | 7.04 us: 1.17x faster                                                       |
| async_tree_cpu_io_mixed | 944 ms                                                              | 811 ms: 1.16x faster                                                        |
| regex_compile           | 177 ms                                                              | 153 ms: 1.16x faster                                                        |
| json_loads              | 29.3 us                                                             | 25.3 us: 1.16x faster                                                       |
| html5lib                | 86.4 ms                                                             | 75.1 ms: 1.15x faster                                                       |
| pprint_safe_repr        | 953 ms                                                              | 832 ms: 1.15x faster                                                        |
| xml_etree_generate      | 94.9 ms                                                             | 82.8 ms: 1.15x faster                                                       |
| mako                    | 14.7 ms                                                             | 12.9 ms: 1.15x faster                                                       |
| 2to3                    | 336 ms                                                              | 293 ms: 1.15x faster                                                        |
| pprint_pformat          | 1.98 sec                                                            | 1.74 sec: 1.14x faster                                                      |
| pycparser               | 1.53 sec                                                            | 1.35 sec: 1.14x faster                                                      |
| unpickle                | 15.0 us                                                             | 13.2 us: 1.13x faster                                                       |
| fannkuch                | 485 ms                                                              | 428 ms: 1.13x faster                                                        |
| unpickle_pure_python    | 300 us                                                              | 265 us: 1.13x faster                                                        |
| sqlite_synth            | 2.97 us                                                             | 2.70 us: 1.10x faster                                                       |
| pickle_list             | 4.73 us                                                             | 4.32 us: 1.10x faster                                                       |
| unpickle_list           | 4.94 us                                                             | 4.53 us: 1.09x faster                                                       |
| genshi_xml              | 64.3 ms                                                             | 59.7 ms: 1.08x faster                                                       |
| genshi_text             | 30.4 ms                                                             | 28.2 ms: 1.08x faster                                                       |
| deepcopy_reduce         | 3.80 us                                                             | 3.55 us: 1.07x faster                                                       |
| docutils                | 3.19 sec                                                            | 3.02 sec: 1.06x faster                                                      |
| xml_etree_parse         | 164 ms                                                              | 155 ms: 1.05x faster                                                        |
| deepcopy                | 438 us                                                              | 418 us: 1.05x faster                                                        |
| dulwich_log             | 76.3 ms                                                             | 73.0 ms: 1.05x faster                                                       |
| thrift                  | 1.04 ms                                                             | 995 us: 1.04x faster                                                        |
| regex_effbot            | 3.22 ms                                                             | 3.10 ms: 1.04x faster                                                       |
| json                    | 5.41 ms                                                             | 5.24 ms: 1.03x faster                                                       |
| chameleon               | 9.13 ms                                                             | 8.85 ms: 1.03x faster                                                       |
| django_template         | 45.8 ms                                                             | 44.9 ms: 1.02x faster                                                       |
| sqlglot_normalize       | 135 ms                                                              | 133 ms: 1.01x faster                                                        |
| xml_etree_iterparse     | 111 ms                                                              | 110 ms: 1.01x faster                                                        |
| sqlglot_optimize        | 65.3 ms                                                             | 64.7 ms: 1.01x faster                                                       |
| mdp                     | 2.75 sec                                                            | 2.76 sec: 1.00x slower                                                      |
| pathlib                 | 19.8 ms                                                             | 19.9 ms: 1.01x slower                                                       |
| create_gc_cycles        | 1.64 ms                                                             | 1.66 ms: 1.01x slower                                                       |
| coverage                | 70.6 ms                                                             | 72.1 ms: 1.02x slower                                                       |
| sympy_sum               | 185 ms                                                              | 189 ms: 1.02x slower                                                        |
| json_dumps              | 13.7 ms                                                             | 14.1 ms: 1.03x slower                                                       |
| regex_v8                | 24.9 ms                                                             | 25.7 ms: 1.03x slower                                                       |
| nqueens                 | 98.8 ms                                                             | 103 ms: 1.04x slower                                                        |
| tornado_http            | 129 ms                                                              | 135 ms: 1.04x slower                                                        |
| sqlglot_transpile       | 2.45 ms                                                             | 2.60 ms: 1.06x slower                                                       |
| telco                   | 6.67 ms                                                             | 7.11 ms: 1.07x slower                                                       |
| sqlglot_parse           | 2.07 ms                                                             | 2.21 ms: 1.07x slower                                                       |
| sympy_str               | 328 ms                                                              | 350 ms: 1.07x slower                                                        |
| sympy_expand            | 540 ms                                                              | 579 ms: 1.07x slower                                                        |
| sympy_integrate         | 24.3 ms                                                             | 26.5 ms: 1.09x slower                                                       |
| gc_traversal            | 3.53 ms                                                             | 3.89 ms: 1.10x slower                                                       |
| bench_thread_pool       | 954 us                                                              | 1.06 ms: 1.11x slower                                                       |
| comprehensions          | 27.3 us                                                             | 30.6 us: 1.12x slower                                                       |
| meteor_contest          | 115 ms                                                              | 129 ms: 1.13x slower                                                        |
| pickle_dict             | 27.8 us                                                             | 33.0 us: 1.19x slower                                                       |
| regex_dna               | 213 ms                                                              | 261 ms: 1.22x slower                                                        |
| python_startup_no_site  | 5.80 ms                                                             | 7.14 ms: 1.23x slower                                                       |
| pidigits                | 190 ms                                                              | 253 ms: 1.33x slower                                                        |
| Geometric mean          | (ref)                                                               | 1.14x faster                                                                |

Benchmark hidden because not significant (2): dask, pickle
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, asyncio_tcp, djangocms, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
