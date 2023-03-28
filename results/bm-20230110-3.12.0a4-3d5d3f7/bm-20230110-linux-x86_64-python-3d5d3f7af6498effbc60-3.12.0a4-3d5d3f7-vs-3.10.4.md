
# Results vs. 3.10.4

- fork: python
- ref: 3d5d3f7af6498effbc60
- machine: linux-x86_64
- commit hash: 3d5d3f7
- commit date: 2023-01-10
- overall geometric mean: 1.30x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 252 ms: 1.33x faster                                                  |
| chameleon      | 9.13 ms                                                             | 6.33 ms: 1.44x faster                                                 |
| docutils       | 3.19 sec                                                            | 2.48 sec: 1.29x faster                                                |
| html5lib       | 86.4 ms                                                             | 59.3 ms: 1.46x faster                                                 |
| Geometric mean | (ref)                                                               | 1.38x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 94.2 ms: 1.55x faster                                                 |
| float          | 110 ms                                                              | 71.4 ms: 1.54x faster                                                 |
| pidigits       | 190 ms                                                              | 190 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                               | 1.34x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 131 ms: 1.36x faster                                                  |
| regex_v8       | 24.9 ms                                                             | 20.5 ms: 1.22x faster                                                 |
| regex_dna      | 213 ms                                                              | 201 ms: 1.06x faster                                                  |
| regex_effbot   | 3.22 ms                                                             | 3.36 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                               | 1.14x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 284 us: 1.61x faster                                                  |
| unpickle_pure_python | 300 us                                                              | 200 us: 1.50x faster                                                  |
| json_dumps           | 13.7 ms                                                             | 9.53 ms: 1.44x faster                                                 |
| xml_etree_process    | 74.8 ms                                                             | 53.7 ms: 1.39x faster                                                 |
| xml_etree_generate   | 94.9 ms                                                             | 76.6 ms: 1.24x faster                                                 |
| json_loads           | 29.3 us                                                             | 24.1 us: 1.21x faster                                                 |
| unpickle             | 15.0 us                                                             | 13.1 us: 1.14x faster                                                 |
| pickle_list          | 4.73 us                                                             | 4.15 us: 1.14x faster                                                 |
| xml_etree_parse      | 164 ms                                                              | 148 ms: 1.11x faster                                                  |
| xml_etree_iterparse  | 111 ms                                                              | 105 ms: 1.06x faster                                                  |
| unpickle_list        | 4.94 us                                                             | 5.00 us: 1.01x slower                                                 |
| pickle_dict          | 27.8 us                                                             | 31.0 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.19x faster                                                          |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.54 ms: 1.66x faster                                                 |
| python_startup_no_site | 5.80 ms                                                             | 6.08 ms: 1.05x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.26x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.67 ms: 1.52x faster                                                 |
| genshi_text     | 30.4 ms                                                             | 20.6 ms: 1.47x faster                                                 |
| django_template | 45.8 ms                                                             | 31.9 ms: 1.44x faster                                                 |
| genshi_xml      | 64.3 ms                                                             | 46.5 ms: 1.38x faster                                                 |
| Geometric mean  | (ref)                                                               | 1.45x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 7.30 ms                                                             | 3.29 ms: 2.22x faster                                                 |
| scimark_sor             | 198 ms                                                              | 107 ms: 1.84x faster                                                  |
| asyncio_tcp             | 922 ms                                                              | 506 ms: 1.82x faster                                                  |
| logging_silent          | 169 ns                                                              | 93.8 ns: 1.80x faster                                                 |
| richards                | 74.2 ms                                                             | 41.6 ms: 1.78x faster                                                 |
| pyflate                 | 671 ms                                                              | 395 ms: 1.70x faster                                                  |
| scimark_monte_carlo     | 109 ms                                                              | 64.3 ms: 1.69x faster                                                 |
| raytrace                | 470 ms                                                              | 280 ms: 1.68x faster                                                  |
| go                      | 226 ms                                                              | 135 ms: 1.67x faster                                                  |
| python_startup          | 14.1 ms                                                             | 8.54 ms: 1.66x faster                                                 |
| pickle_pure_python      | 457 us                                                              | 284 us: 1.61x faster                                                  |
| spectral_norm           | 150 ms                                                              | 95.6 ms: 1.57x faster                                                 |
| chaos                   | 106 ms                                                              | 67.7 ms: 1.56x faster                                                 |
| crypto_pyaes            | 117 ms                                                              | 75.1 ms: 1.55x faster                                                 |
| hexiom                  | 9.50 ms                                                             | 6.13 ms: 1.55x faster                                                 |
| nbody                   | 146 ms                                                              | 94.2 ms: 1.55x faster                                                 |
| float                   | 110 ms                                                              | 71.4 ms: 1.54x faster                                                 |
| unpack_sequence         | 65.6 ns                                                             | 42.9 ns: 1.53x faster                                                 |
| deepcopy_memo           | 51.8 us                                                             | 34.0 us: 1.53x faster                                                 |
| mako                    | 14.7 ms                                                             | 9.67 ms: 1.52x faster                                                 |
| unpickle_pure_python    | 300 us                                                              | 200 us: 1.50x faster                                                  |
| sqlglot_parse           | 2.07 ms                                                             | 1.40 ms: 1.48x faster                                                 |
| genshi_text             | 30.4 ms                                                             | 20.6 ms: 1.47x faster                                                 |
| scimark_lu              | 160 ms                                                              | 109 ms: 1.47x faster                                                  |
| sqlglot_transpile       | 2.45 ms                                                             | 1.69 ms: 1.46x faster                                                 |
| html5lib                | 86.4 ms                                                             | 59.3 ms: 1.46x faster                                                 |
| chameleon               | 9.13 ms                                                             | 6.33 ms: 1.44x faster                                                 |
| django_template         | 45.8 ms                                                             | 31.9 ms: 1.44x faster                                                 |
| json_dumps              | 13.7 ms                                                             | 9.53 ms: 1.44x faster                                                 |
| logging_simple          | 8.21 us                                                             | 5.74 us: 1.43x faster                                                 |
| logging_format          | 9.07 us                                                             | 6.37 us: 1.42x faster                                                 |
| pycparser               | 1.53 sec                                                            | 1.08 sec: 1.41x faster                                                |
| pprint_pformat          | 1.98 sec                                                            | 1.41 sec: 1.40x faster                                                |
| xml_etree_process       | 74.8 ms                                                             | 53.7 ms: 1.39x faster                                                 |
| thrift                  | 1.04 ms                                                             | 748 us: 1.39x faster                                                  |
| genshi_xml              | 64.3 ms                                                             | 46.5 ms: 1.38x faster                                                 |
| pprint_safe_repr        | 953 ms                                                              | 691 ms: 1.38x faster                                                  |
| regex_compile           | 177 ms                                                              | 131 ms: 1.36x faster                                                  |
| async_tree_memoization  | 853 ms                                                              | 630 ms: 1.35x faster                                                  |
| scimark_fft             | 425 ms                                                              | 315 ms: 1.35x faster                                                  |
| async_tree_none         | 713 ms                                                              | 529 ms: 1.35x faster                                                  |
| async_tree_io           | 1.78 sec                                                            | 1.33 sec: 1.34x faster                                                |
| 2to3                    | 336 ms                                                              | 252 ms: 1.33x faster                                                  |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.22 ms: 1.33x faster                                                 |
| fannkuch                | 485 ms                                                              | 369 ms: 1.31x faster                                                  |
| deepcopy                | 438 us                                                              | 334 us: 1.31x faster                                                  |
| mypy2                   | 432 ms                                                              | 332 ms: 1.30x faster                                                  |
| deepcopy_reduce         | 3.80 us                                                             | 2.92 us: 1.30x faster                                                 |
| sqlglot_normalize       | 135 ms                                                              | 104 ms: 1.29x faster                                                  |
| sqlglot_optimize        | 65.3 ms                                                             | 50.7 ms: 1.29x faster                                                 |
| docutils                | 3.19 sec                                                            | 2.48 sec: 1.29x faster                                                |
| coroutines              | 31.8 ms                                                             | 24.8 ms: 1.28x faster                                                 |
| nqueens                 | 98.8 ms                                                             | 78.6 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed | 944 ms                                                              | 753 ms: 1.25x faster                                                  |
| xml_etree_generate      | 94.9 ms                                                             | 76.6 ms: 1.24x faster                                                 |
| dulwich_log             | 76.3 ms                                                             | 62.5 ms: 1.22x faster                                                 |
| bench_thread_pool       | 954 us                                                              | 783 us: 1.22x faster                                                  |
| regex_v8                | 24.9 ms                                                             | 20.5 ms: 1.22x faster                                                 |
| json_loads              | 29.3 us                                                             | 24.1 us: 1.21x faster                                                 |
| dask                    | 437 ms                                                              | 361 ms: 1.21x faster                                                  |
| sympy_integrate         | 24.3 ms                                                             | 20.3 ms: 1.20x faster                                                 |
| async_generators        | 420 ms                                                              | 353 ms: 1.19x faster                                                  |
| sympy_expand            | 540 ms                                                              | 461 ms: 1.17x faster                                                  |
| sqlite_synth            | 2.97 us                                                             | 2.56 us: 1.16x faster                                                 |
| sympy_str               | 328 ms                                                              | 284 ms: 1.15x faster                                                  |
| comprehensions          | 27.3 us                                                             | 23.6 us: 1.15x faster                                                 |
| create_gc_cycles        | 1.64 ms                                                             | 1.43 ms: 1.14x faster                                                 |
| unpickle                | 15.0 us                                                             | 13.1 us: 1.14x faster                                                 |
| pickle_list             | 4.73 us                                                             | 4.15 us: 1.14x faster                                                 |
| json                    | 5.41 ms                                                             | 4.77 ms: 1.14x faster                                                 |
| sympy_sum               | 185 ms                                                              | 164 ms: 1.13x faster                                                  |
| djangocms               | 36.3 us                                                             | 32.4 us: 1.12x faster                                                 |
| meteor_contest          | 115 ms                                                              | 103 ms: 1.12x faster                                                  |
| pathlib                 | 19.8 ms                                                             | 17.8 ms: 1.11x faster                                                 |
| xml_etree_parse         | 164 ms                                                              | 148 ms: 1.11x faster                                                  |
| telco                   | 6.67 ms                                                             | 6.24 ms: 1.07x faster                                                 |
| xml_etree_iterparse     | 111 ms                                                              | 105 ms: 1.06x faster                                                  |
| regex_dna               | 213 ms                                                              | 201 ms: 1.06x faster                                                  |
| mdp                     | 2.75 sec                                                            | 2.66 sec: 1.03x faster                                                |
| pidigits                | 190 ms                                                              | 190 ms: 1.00x faster                                                  |
| unpickle_list           | 4.94 us                                                             | 5.00 us: 1.01x slower                                                 |
| generators              | 75.7 ms                                                             | 77.0 ms: 1.02x slower                                                 |
| regex_effbot            | 3.22 ms                                                             | 3.36 ms: 1.04x slower                                                 |
| python_startup_no_site  | 5.80 ms                                                             | 6.08 ms: 1.05x slower                                                 |
| pickle_dict             | 27.8 us                                                             | 31.0 us: 1.12x slower                                                 |
| gc_traversal            | 3.53 ms                                                             | 4.15 ms: 1.18x slower                                                 |
| coverage                | 70.6 ms                                                             | 100 ms: 1.42x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.30x faster                                                          |

Benchmark hidden because not significant (2): pickle, bench_mp_pool
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
