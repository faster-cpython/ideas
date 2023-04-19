
# Results vs. 3.10.4

- fork: faster-cpython
- ref: nogil_latest
- machine: linux-x86_64
- commit hash: 1d39009
- commit date: 2023-04-16
- overall geometric mean: 1.19x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 290 ms: 1.16x faster                                                    |
| chameleon      | 9.13 ms                                                             | 7.81 ms: 1.17x faster                                                   |
| docutils       | 3.19 sec                                                            | 3.15 sec: 1.02x faster                                                  |
| html5lib       | 86.4 ms                                                             | 69.2 ms: 1.25x faster                                                   |
| Geometric mean | (ref)                                                               | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 110 ms                                                              | 65.9 ms: 1.67x faster                                                   |
| nbody          | 146 ms                                                              | 107 ms: 1.36x faster                                                    |
| pidigits       | 190 ms                                                              | 186 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                               | 1.32x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 24.9 ms                                                             | 21.1 ms: 1.18x faster                                                   |
| regex_compile  | 177 ms                                                              | 152 ms: 1.17x faster                                                    |
| regex_dna      | 213 ms                                                              | 205 ms: 1.04x faster                                                    |
| regex_effbot   | 3.22 ms                                                             | 3.46 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                               | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 321 us: 1.42x faster                                                    |
| json_dumps           | 13.7 ms                                                             | 10.4 ms: 1.32x faster                                                   |
| unpickle_pure_python | 300 us                                                              | 229 us: 1.31x faster                                                    |
| xml_etree_process    | 74.8 ms                                                             | 61.3 ms: 1.22x faster                                                   |
| xml_etree_parse      | 164 ms                                                              | 137 ms: 1.19x faster                                                    |
| xml_etree_generate   | 94.9 ms                                                             | 83.7 ms: 1.13x faster                                                   |
| pickle_list          | 4.73 us                                                             | 4.33 us: 1.09x faster                                                   |
| json_loads           | 29.3 us                                                             | 28.0 us: 1.04x faster                                                   |
| pickle               | 10.2 us                                                             | 10.3 us: 1.00x slower                                                   |
| xml_etree_iterparse  | 111 ms                                                              | 114 ms: 1.02x slower                                                    |
| unpickle             | 15.0 us                                                             | 15.5 us: 1.03x slower                                                   |
| unpickle_list        | 4.94 us                                                             | 5.20 us: 1.05x slower                                                   |
| pickle_dict          | 27.8 us                                                             | 30.0 us: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                               | 1.11x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 9.18 ms: 1.54x faster                                                   |
| python_startup_no_site | 5.80 ms                                                             | 6.59 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                               | 1.16x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 30.4 ms                                                             | 24.4 ms: 1.25x faster                                                   |
| genshi_xml      | 64.3 ms                                                             | 52.0 ms: 1.24x faster                                                   |
| django_template | 45.8 ms                                                             | 37.4 ms: 1.23x faster                                                   |
| mako            | 14.7 ms                                                             | 13.2 ms: 1.11x faster                                                   |
| Geometric mean  | (ref)                                                               | 1.20x faster                                                            |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io           | 1.78 sec                                                            | 616 ms: 2.89x faster                                                    |
| async_tree_none         | 713 ms                                                              | 311 ms: 2.29x faster                                                    |
| async_tree_memoization  | 853 ms                                                              | 381 ms: 2.24x faster                                                    |
| deltablue               | 7.30 ms                                                             | 3.91 ms: 1.86x faster                                                   |
| async_tree_cpu_io_mixed | 944 ms                                                              | 534 ms: 1.77x faster                                                    |
| asyncio_tcp             | 922 ms                                                              | 525 ms: 1.76x faster                                                    |
| float                   | 110 ms                                                              | 65.9 ms: 1.67x faster                                                   |
| logging_silent          | 169 ns                                                              | 104 ns: 1.63x faster                                                    |
| scimark_sor             | 198 ms                                                              | 123 ms: 1.61x faster                                                    |
| go                      | 226 ms                                                              | 146 ms: 1.54x faster                                                    |
| python_startup          | 14.1 ms                                                             | 9.18 ms: 1.54x faster                                                   |
| richards                | 74.2 ms                                                             | 48.4 ms: 1.53x faster                                                   |
| pyflate                 | 671 ms                                                              | 470 ms: 1.43x faster                                                    |
| crypto_pyaes            | 117 ms                                                              | 81.8 ms: 1.43x faster                                                   |
| pickle_pure_python      | 457 us                                                              | 321 us: 1.42x faster                                                    |
| scimark_monte_carlo     | 109 ms                                                              | 76.4 ms: 1.42x faster                                                   |
| chaos                   | 106 ms                                                              | 74.6 ms: 1.42x faster                                                   |
| hexiom                  | 9.50 ms                                                             | 6.89 ms: 1.38x faster                                                   |
| nbody                   | 146 ms                                                              | 107 ms: 1.36x faster                                                    |
| raytrace                | 470 ms                                                              | 346 ms: 1.36x faster                                                    |
| spectral_norm           | 150 ms                                                              | 112 ms: 1.34x faster                                                    |
| pycparser               | 1.53 sec                                                            | 1.15 sec: 1.33x faster                                                  |
| json_dumps              | 13.7 ms                                                             | 10.4 ms: 1.32x faster                                                   |
| unpickle_pure_python    | 300 us                                                              | 229 us: 1.31x faster                                                    |
| deepcopy_memo           | 51.8 us                                                             | 40.1 us: 1.29x faster                                                   |
| scimark_lu              | 160 ms                                                              | 128 ms: 1.25x faster                                                    |
| pprint_pformat          | 1.98 sec                                                            | 1.58 sec: 1.25x faster                                                  |
| genshi_text             | 30.4 ms                                                             | 24.4 ms: 1.25x faster                                                   |
| html5lib                | 86.4 ms                                                             | 69.2 ms: 1.25x faster                                                   |
| pprint_safe_repr        | 953 ms                                                              | 765 ms: 1.25x faster                                                    |
| genshi_xml              | 64.3 ms                                                             | 52.0 ms: 1.24x faster                                                   |
| django_template         | 45.8 ms                                                             | 37.4 ms: 1.23x faster                                                   |
| xml_etree_process       | 74.8 ms                                                             | 61.3 ms: 1.22x faster                                                   |
| thrift                  | 1.04 ms                                                             | 851 us: 1.22x faster                                                    |
| xml_etree_parse         | 164 ms                                                              | 137 ms: 1.19x faster                                                    |
| coroutines              | 31.8 ms                                                             | 26.8 ms: 1.19x faster                                                   |
| regex_v8                | 24.9 ms                                                             | 21.1 ms: 1.18x faster                                                   |
| logging_format          | 9.07 us                                                             | 7.66 us: 1.18x faster                                                   |
| sqlglot_normalize       | 135 ms                                                              | 115 ms: 1.17x faster                                                    |
| logging_simple          | 8.21 us                                                             | 7.00 us: 1.17x faster                                                   |
| sqlglot_transpile       | 2.45 ms                                                             | 2.10 ms: 1.17x faster                                                   |
| chameleon               | 9.13 ms                                                             | 7.81 ms: 1.17x faster                                                   |
| deepcopy                | 438 us                                                              | 375 us: 1.17x faster                                                    |
| regex_compile           | 177 ms                                                              | 152 ms: 1.17x faster                                                    |
| 2to3                    | 336 ms                                                              | 290 ms: 1.16x faster                                                    |
| sqlglot_parse           | 2.07 ms                                                             | 1.79 ms: 1.16x faster                                                   |
| nqueens                 | 98.8 ms                                                             | 85.8 ms: 1.15x faster                                                   |
| sqlglot_optimize        | 65.3 ms                                                             | 57.1 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.94 ms: 1.14x faster                                                   |
| sqlite_synth            | 2.97 us                                                             | 2.62 us: 1.13x faster                                                   |
| xml_etree_generate      | 94.9 ms                                                             | 83.7 ms: 1.13x faster                                                   |
| unpack_sequence         | 65.6 ns                                                             | 58.1 ns: 1.13x faster                                                   |
| dulwich_log             | 76.3 ms                                                             | 68.1 ms: 1.12x faster                                                   |
| async_generators        | 420 ms                                                              | 377 ms: 1.11x faster                                                    |
| fannkuch                | 485 ms                                                              | 436 ms: 1.11x faster                                                    |
| mako                    | 14.7 ms                                                             | 13.2 ms: 1.11x faster                                                   |
| scimark_fft             | 425 ms                                                              | 383 ms: 1.11x faster                                                    |
| deepcopy_reduce         | 3.80 us                                                             | 3.42 us: 1.11x faster                                                   |
| pickle_list             | 4.73 us                                                             | 4.33 us: 1.09x faster                                                   |
| pathlib                 | 19.8 ms                                                             | 18.2 ms: 1.08x faster                                                   |
| json                    | 5.41 ms                                                             | 5.06 ms: 1.07x faster                                                   |
| sympy_integrate         | 24.3 ms                                                             | 22.8 ms: 1.06x faster                                                   |
| json_loads              | 29.3 us                                                             | 28.0 us: 1.04x faster                                                   |
| regex_dna               | 213 ms                                                              | 205 ms: 1.04x faster                                                    |
| comprehensions          | 27.3 us                                                             | 26.3 us: 1.03x faster                                                   |
| create_gc_cycles        | 1.64 ms                                                             | 1.59 ms: 1.03x faster                                                   |
| pidigits                | 190 ms                                                              | 186 ms: 1.02x faster                                                    |
| docutils                | 3.19 sec                                                            | 3.15 sec: 1.02x faster                                                  |
| bench_mp_pool           | 24.0 ms                                                             | 23.8 ms: 1.01x faster                                                   |
| pickle                  | 10.2 us                                                             | 10.3 us: 1.00x slower                                                   |
| mdp                     | 2.75 sec                                                            | 2.79 sec: 1.01x slower                                                  |
| xml_etree_iterparse     | 111 ms                                                              | 114 ms: 1.02x slower                                                    |
| unpickle                | 15.0 us                                                             | 15.5 us: 1.03x slower                                                   |
| telco                   | 6.67 ms                                                             | 6.92 ms: 1.04x slower                                                   |
| gc_traversal            | 3.53 ms                                                             | 3.67 ms: 1.04x slower                                                   |
| sympy_sum               | 185 ms                                                              | 192 ms: 1.04x slower                                                    |
| generators              | 75.7 ms                                                             | 78.8 ms: 1.04x slower                                                   |
| djangocms               | 36.3 us                                                             | 37.9 us: 1.04x slower                                                   |
| unpickle_list           | 4.94 us                                                             | 5.20 us: 1.05x slower                                                   |
| mypy2                   | 432 ms                                                              | 457 ms: 1.06x slower                                                    |
| regex_effbot            | 3.22 ms                                                             | 3.46 ms: 1.07x slower                                                   |
| pickle_dict             | 27.8 us                                                             | 30.0 us: 1.08x slower                                                   |
| meteor_contest          | 115 ms                                                              | 124 ms: 1.09x slower                                                    |
| python_startup_no_site  | 5.80 ms                                                             | 6.59 ms: 1.14x slower                                                   |
| coverage                | 70.6 ms                                                             | 109 ms: 1.54x slower                                                    |
| bench_thread_pool       | 954 us                                                              | 1.64 ms: 1.72x slower                                                   |
| Geometric mean          | (ref)                                                               | 1.19x faster                                                            |

Benchmark hidden because not significant (2): sympy_expand, sympy_str
Ignored benchmarks (8) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, dask, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
