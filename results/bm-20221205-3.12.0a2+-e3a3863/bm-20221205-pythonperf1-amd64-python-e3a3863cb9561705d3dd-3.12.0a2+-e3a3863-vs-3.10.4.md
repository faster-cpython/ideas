
# Results vs. 3.10.4

- fork: python
- ref: e3a3863cb9561705d3dd
- machine: windows-amd64
- commit hash: e3a3863
- commit date: 2022-12-05
- overall geometric mean: 1.19x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 199 ms: 1.15x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.68 ms: 1.23x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 34.5 ms: 1.37x faster                                                       |
| tornado_http   | 106 ms                                                                   | 90.7 ms: 1.17x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.22x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 49.8 ms: 1.19x faster                                                       |
| nbody          | 71.5 ms                                                                  | 61.5 ms: 1.16x faster                                                       |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 81.9 ms: 1.26x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                       |
| regex_dna      | 131 ms                                                                   | 121 ms: 1.08x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.16 ms: 1.74x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 172 us: 1.54x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 124 us: 1.45x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 34.3 ms: 1.26x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.98 us: 1.11x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.7 ms: 1.07x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 50.6 ms: 1.06x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.59 us: 1.05x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.3 ms: 1.01x slower                                                       |
| pickle               | 6.67 us                                                                  | 7.11 us: 1.07x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.84 us: 1.11x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.9 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.20 ms: 1.40x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.8 ms: 1.34x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.4 ms: 1.29x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 32.1 ms: 1.21x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.31x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.07 ms: 2.00x faster                                                       |
| go                      | 143 ms                                                                   | 82.2 ms: 1.74x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.16 ms: 1.74x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 55.3 ns: 1.71x faster                                                       |
| richards                | 41.0 ms                                                                  | 25.3 ms: 1.62x faster                                                       |
| mypy2                   | 337 ms                                                                   | 218 ms: 1.55x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 172 us: 1.54x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 67.8 ms: 1.53x faster                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 26.3 ns: 1.50x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 57.2 ms: 1.47x faster                                                       |
| raytrace                | 267 ms                                                                   | 182 ms: 1.47x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 835 us: 1.46x faster                                                        |
| pyflate                 | 388 ms                                                                   | 267 ms: 1.45x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 124 us: 1.45x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.5 ms: 1.42x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.20 ms: 1.40x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.05 ms: 1.40x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 34.5 ms: 1.37x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.98 ms: 1.37x faster                                                       |
| thrift                  | 632 us                                                                   | 465 us: 1.36x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 20.9 us: 1.36x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 45.8 ms: 1.34x faster                                                       |
| django_template         | 29.2 ms                                                                  | 21.8 ms: 1.34x faster                                                       |
| pycparser               | 873 ms                                                                   | 662 ms: 1.32x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 934 ms: 1.31x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 44.8 ms: 1.30x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 792 ms: 1.29x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 14.4 ms: 1.29x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 381 ms: 1.27x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 467 ms: 1.27x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 327 ms: 1.27x faster                                                        |
| regex_compile           | 103 ms                                                                   | 81.9 ms: 1.26x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 34.3 ms: 1.26x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.68 ms: 1.23x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 60.5 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 495 ms: 1.22x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.0 ms: 1.21x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 32.1 ms: 1.21x faster                                                       |
| deepcopy                | 256 us                                                                   | 213 us: 1.20x faster                                                        |
| float                   | 59.5 ms                                                                  | 49.8 ms: 1.19x faster                                                       |
| async_generators        | 214 ms                                                                   | 181 ms: 1.18x faster                                                        |
| docutils                | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.85 us: 1.18x faster                                                       |
| tornado_http            | 106 ms                                                                   | 90.7 ms: 1.17x faster                                                       |
| dask                    | 310 ms                                                                   | 264 ms: 1.17x faster                                                        |
| fannkuch                | 252 ms                                                                   | 215 ms: 1.17x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.72 ms: 1.17x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.29 ms: 1.16x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 61.5 ms: 1.16x faster                                                       |
| 2to3                    | 229 ms                                                                   | 199 ms: 1.15x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 176 ms: 1.14x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 12.9 ms: 1.13x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 278 ms: 1.12x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 848 us: 1.12x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 682 us: 1.12x faster                                                        |
| unpickle                | 8.88 us                                                                  | 7.98 us: 1.11x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 42.4 ms: 1.11x faster                                                       |
| json_loads              | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 171 ms: 1.09x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 59.9 ms: 1.08x faster                                                       |
| regex_dna               | 131 ms                                                                   | 121 ms: 1.08x faster                                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 89.7 ms: 1.07x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 50.6 ms: 1.06x faster                                                       |
| sympy_str               | 189 ms                                                                   | 178 ms: 1.06x faster                                                        |
| meteor_contest          | 74.3 ms                                                                  | 70.4 ms: 1.06x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.59 us: 1.05x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.3 us: 1.05x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 15.0 ms: 1.04x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.78 us: 1.04x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 99.6 ms: 1.03x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.59 sec: 1.01x faster                                                      |
| telco                   | 3.77 ms                                                                  | 3.75 ms: 1.01x faster                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.3 ms: 1.01x slower                                                       |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                        |
| logging_format          | 6.53 us                                                                  | 6.67 us: 1.02x slower                                                       |
| pickle                  | 6.67 us                                                                  | 7.11 us: 1.07x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.9 ms: 1.07x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.8 ms: 1.08x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.84 us: 1.11x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.49 ms: 1.12x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| asyncio_tcp             | 664 ms                                                                   | 758 ms: 1.14x slower                                                        |
| generators              | 31.4 ms                                                                  | 36.3 ms: 1.15x slower                                                       |
| coverage                | 37.5 ms                                                                  | 52.8 ms: 1.41x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.19x faster                                                                |

Benchmark hidden because not significant (2): pathlib, logging_simple
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
