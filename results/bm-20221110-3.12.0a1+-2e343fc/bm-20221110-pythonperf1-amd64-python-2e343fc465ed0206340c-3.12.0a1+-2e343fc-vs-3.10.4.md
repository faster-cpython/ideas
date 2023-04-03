
# Results vs. 3.10.4

- fork: python
- ref: 2e343fc465ed0206340c
- machine: windows-amd64
- commit hash: 2e343fc
- commit date: 2022-11-10
- overall geometric mean: 1.15x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 198 ms: 1.16x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.89 ms: 1.18x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.7 ms: 1.33x faster                                                       |
| tornado_http   | 106 ms                                                                   | 93.4 ms: 1.14x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.19x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.5 ms                                                                  | 63.1 ms: 1.13x faster                                                       |
| float          | 59.5 ms                                                                  | 54.1 ms: 1.10x faster                                                       |
| pidigits       | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 84.7 ms: 1.22x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.5 ms: 1.12x faster                                                       |
| regex_dna      | 131 ms                                                                   | 124 ms: 1.05x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.58 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.38 ms: 1.67x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 190 us: 1.39x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 140 us: 1.28x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 36.3 ms: 1.19x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.75 us: 1.15x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.1 us: 1.08x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.56 us: 1.06x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.6 ms: 1.04x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 91.9 ms: 1.04x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 64.5 ms: 1.03x slower                                                       |
| pickle               | 6.67 us                                                                  | 6.96 us: 1.04x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.80 us: 1.09x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.3 us: 1.15x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 16.1 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 21.7 ms: 1.34x faster                                                       |
| mako            | 8.69 ms                                                                  | 6.55 ms: 1.33x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 15.8 ms: 1.17x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 35.3 ms: 1.10x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.23x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.35 ms: 1.76x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.38 ms: 1.67x faster                                                       |
| go                      | 143 ms                                                                   | 91.2 ms: 1.57x faster                                                       |
| richards                | 41.0 ms                                                                  | 27.2 ms: 1.51x faster                                                       |
| mypy2                   | 337 ms                                                                   | 225 ms: 1.50x faster                                                        |
| logging_silent          | 94.6 ns                                                                  | 65.3 ns: 1.45x faster                                                       |
| raytrace                | 267 ms                                                                   | 188 ms: 1.42x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 73.4 ms: 1.41x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 190 us: 1.39x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 885 us: 1.38x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.07 ms: 1.37x faster                                                       |
| django_template         | 29.2 ms                                                                  | 21.7 ms: 1.34x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 62.4 ms: 1.34x faster                                                       |
| pyflate                 | 388 ms                                                                   | 291 ms: 1.33x faster                                                        |
| mako                    | 8.69 ms                                                                  | 6.55 ms: 1.33x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.7 ms: 1.33x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 42.3 ms: 1.32x faster                                                       |
| pycparser               | 873 ms                                                                   | 669 ms: 1.31x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 784 ms: 1.31x faster                                                        |
| thrift                  | 632 us                                                                   | 488 us: 1.29x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 47.5 ms: 1.29x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 45.5 ms: 1.29x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 140 us: 1.28x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 4.28 ms: 1.28x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 330 ms: 1.25x faster                                                        |
| async_tree_memoization  | 485 ms                                                                   | 387 ms: 1.25x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 481 ms: 1.23x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 32.2 ns: 1.22x faster                                                       |
| async_generators        | 214 ms                                                                   | 175 ms: 1.22x faster                                                        |
| regex_compile           | 103 ms                                                                   | 84.7 ms: 1.22x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 1.01 sec: 1.21x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 508 ms: 1.19x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 36.3 ms: 1.19x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.89 ms: 1.18x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.7 ms: 1.18x faster                                                       |
| dask                    | 310 ms                                                                   | 263 ms: 1.18x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 24.1 us: 1.18x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 15.8 ms: 1.17x faster                                                       |
| 2to3                    | 229 ms                                                                   | 198 ms: 1.16x faster                                                        |
| docutils                | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                      |
| json                    | 3.18 ms                                                                  | 2.76 ms: 1.15x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.32 ms: 1.15x faster                                                       |
| unpickle                | 8.88 us                                                                  | 7.75 us: 1.15x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.91 us: 1.14x faster                                                       |
| tornado_http            | 106 ms                                                                   | 93.4 ms: 1.14x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 65.3 ms: 1.14x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 63.1 ms: 1.13x faster                                                       |
| deepcopy                | 256 us                                                                   | 226 us: 1.13x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 676 us: 1.13x faster                                                        |
| coroutines              | 15.6 ms                                                                  | 13.9 ms: 1.13x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 852 us: 1.12x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.5 ms: 1.12x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 280 ms: 1.12x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 182 ms: 1.10x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 13.3 ms: 1.10x faster                                                       |
| float                   | 59.5 ms                                                                  | 54.1 ms: 1.10x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 35.3 ms: 1.10x faster                                                       |
| json_loads              | 14.2 us                                                                  | 13.1 us: 1.08x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 43.9 ms: 1.07x faster                                                       |
| fannkuch                | 252 ms                                                                   | 236 ms: 1.07x faster                                                        |
| sympy_str               | 189 ms                                                                   | 177 ms: 1.06x faster                                                        |
| unpickle_list           | 2.71 us                                                                  | 2.56 us: 1.06x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 70.4 ms: 1.06x faster                                                       |
| regex_dna               | 131 ms                                                                   | 124 ms: 1.05x faster                                                        |
| sympy_sum               | 102 ms                                                                   | 97.3 ms: 1.05x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 179 ms: 1.05x faster                                                        |
| xml_etree_generate      | 53.8 ms                                                                  | 51.6 ms: 1.04x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 91.9 ms: 1.04x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.58 ms: 1.04x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.79 us: 1.03x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 62.8 ms: 1.03x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.6 us: 1.03x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 64.5 ms: 1.03x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.91 ms: 1.04x slower                                                       |
| pidigits                | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| pickle                  | 6.67 us                                                                  | 6.96 us: 1.04x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.2 ms: 1.07x slower                                                       |
| logging_format          | 6.53 us                                                                  | 6.99 us: 1.07x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.58 us: 1.07x slower                                                       |
| generators              | 31.4 ms                                                                  | 33.9 ms: 1.08x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 16.1 ms: 1.08x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.45 ms: 1.09x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.80 us: 1.09x slower                                                       |
| asyncio_tcp             | 664 ms                                                                   | 746 ms: 1.12x slower                                                        |
| pickle_dict             | 16.7 us                                                                  | 19.3 us: 1.15x slower                                                       |
| coverage                | 37.5 ms                                                                  | 53.4 ms: 1.43x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.15x faster                                                                |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
