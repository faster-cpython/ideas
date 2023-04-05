
# Results vs. 3.10.4

- fork: python
- ref: f533f216e6aaba3f3663
- machine: windows-amd64
- commit hash: f533f21
- commit date: 2023-03-06
- overall geometric mean: 1.17x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 203 ms: 1.13x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.82 ms: 1.20x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 36.7 ms: 1.29x faster                                                       |
| tornado_http   | 106 ms                                                                   | 90.7 ms: 1.17x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.19x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 50.4 ms: 1.18x faster                                                       |
| nbody          | 71.5 ms                                                                  | 64.6 ms: 1.11x faster                                                       |
| pidigits       | 145 ms                                                                   | 150 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 82.1 ms: 1.26x faster                                                       |
| regex_dna      | 131 ms                                                                   | 123 ms: 1.06x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 14.3 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.40 ms: 1.67x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 176 us: 1.50x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 126 us: 1.42x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 37.7 ms: 1.14x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.7 us: 1.11x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.04 us: 1.10x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 92.0 ms: 1.04x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.91 us: 1.04x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.80 us: 1.09x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_generate, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 16.0 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.36 ms: 1.37x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.9 ms: 1.34x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.2 ms: 1.31x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 32.1 ms: 1.21x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.30x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.99 ms: 2.09x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 56.1 ns: 1.69x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.40 ms: 1.67x faster                                                       |
| go                      | 143 ms                                                                   | 87.4 ms: 1.64x faster                                                       |
| richards                | 41.0 ms                                                                  | 25.4 ms: 1.61x faster                                                       |
| mypy2                   | 337 ms                                                                   | 216 ms: 1.56x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 176 us: 1.50x faster                                                        |
| raytrace                | 267 ms                                                                   | 185 ms: 1.45x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 71.7 ms: 1.44x faster                                                       |
| generators              | 31.4 ms                                                                  | 21.8 ms: 1.44x faster                                                       |
| pyflate                 | 388 ms                                                                   | 272 ms: 1.43x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 126 us: 1.42x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 59.5 ms: 1.41x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 476 ms: 1.39x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 28.6 ns: 1.38x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 42.5 ms: 1.38x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.36 ms: 1.37x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.02 ms: 1.36x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 45.3 ms: 1.36x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 306 ms: 1.35x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 908 us: 1.34x faster                                                        |
| django_template         | 29.2 ms                                                                  | 21.9 ms: 1.34x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.10 ms: 1.33x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 42.3 ms: 1.33x faster                                                       |
| thrift                  | 632 us                                                                   | 478 us: 1.32x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 778 ms: 1.32x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 14.2 ms: 1.31x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 372 ms: 1.30x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 951 ms: 1.29x faster                                                        |
| html5lib                | 47.3 ms                                                                  | 36.7 ms: 1.29x faster                                                       |
| pycparser               | 873 ms                                                                   | 686 ms: 1.27x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 22.4 us: 1.27x faster                                                       |
| regex_compile           | 103 ms                                                                   | 82.1 ms: 1.26x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 483 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 493 ms: 1.23x faster                                                        |
| genshi_xml              | 38.8 ms                                                                  | 32.1 ms: 1.21x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.82 ms: 1.20x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.5 ms: 1.19x faster                                                       |
| float                   | 59.5 ms                                                                  | 50.4 ms: 1.18x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                                      |
| deepcopy                | 256 us                                                                   | 218 us: 1.17x faster                                                        |
| tornado_http            | 106 ms                                                                   | 90.7 ms: 1.17x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 173 ms: 1.16x faster                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.91 us: 1.14x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 37.7 ms: 1.14x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.2 ms: 1.14x faster                                                       |
| fannkuch                | 252 ms                                                                   | 221 ms: 1.14x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.80 ms: 1.13x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 277 ms: 1.13x faster                                                        |
| 2to3                    | 229 ms                                                                   | 203 ms: 1.13x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 852 us: 1.12x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 13.1 ms: 1.12x faster                                                       |
| json_loads              | 14.2 us                                                                  | 12.7 us: 1.11x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 58.5 ms: 1.11x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 64.6 ms: 1.11x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.04 us: 1.10x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 67.4 ms: 1.10x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.2 ms: 1.10x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 701 us: 1.09x faster                                                        |
| mdp                     | 1.60 sec                                                                 | 1.49 sec: 1.07x faster                                                      |
| sympy_str               | 189 ms                                                                   | 177 ms: 1.07x faster                                                        |
| regex_dna               | 131 ms                                                                   | 123 ms: 1.06x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 14.3 ms: 1.06x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 92.0 ms: 1.04x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.4 us: 1.04x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 182 ms: 1.03x faster                                                        |
| meteor_contest          | 74.3 ms                                                                  | 72.4 ms: 1.03x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 99.8 ms: 1.02x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.82 us: 1.01x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.64 ms: 1.01x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.81 ms: 1.01x slower                                                       |
| pidigits                | 145 ms                                                                   | 150 ms: 1.03x slower                                                        |
| pickle                  | 6.67 us                                                                  | 6.91 us: 1.04x slower                                                       |
| async_generators        | 214 ms                                                                   | 224 ms: 1.05x slower                                                        |
| python_startup_no_site  | 14.8 ms                                                                  | 16.0 ms: 1.08x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.80 us: 1.09x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 65.7 ms: 1.11x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.51 ms: 1.14x slower                                                       |
| dask                    | 310 ms                                                                   | 356 ms: 1.15x slower                                                        |
| coverage                | 37.5 ms                                                                  | 49.1 ms: 1.31x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.17x faster                                                                |

Benchmark hidden because not significant (7): pathlib, xml_etree_iterparse, logging_simple, xml_etree_generate, regex_effbot, logging_format, unpickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
