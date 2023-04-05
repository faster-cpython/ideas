
# Results vs. 3.10.4

- fork: python
- ref: edfbf56f4ca6588dfd20
- machine: windows-amd64
- commit hash: edfbf56
- commit date: 2023-01-01
- overall geometric mean: 1.17x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 205 ms: 1.12x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.59 ms: 1.26x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 36.5 ms: 1.30x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.21x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 50.3 ms: 1.18x faster                                                       |
| nbody          | 71.5 ms                                                                  | 66.2 ms: 1.08x faster                                                       |
| pidigits       | 145 ms                                                                   | 152 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 86.2 ms: 1.20x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.4 ms: 1.13x faster                                                       |
| regex_dna      | 131 ms                                                                   | 117 ms: 1.11x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.21 ms: 1.73x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 181 us: 1.46x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 129 us: 1.39x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.3 ms: 1.22x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.94 us: 1.12x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.5 ms: 1.07x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 50.5 ms: 1.07x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.71 us: 1.01x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.5 us: 1.11x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.88 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.13x faster                                                                |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.34 ms: 1.37x faster                                                       |
| django_template | 29.2 ms                                                                  | 22.7 ms: 1.29x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.6 ms: 1.27x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 34.4 ms: 1.13x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.26x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.21 ms: 1.87x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.21 ms: 1.73x faster                                                       |
| go                      | 143 ms                                                                   | 87.9 ms: 1.63x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 59.0 ns: 1.60x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 66.9 ms: 1.55x faster                                                       |
| mypy2                   | 337 ms                                                                   | 224 ms: 1.51x faster                                                        |
| raytrace                | 267 ms                                                                   | 181 ms: 1.48x faster                                                        |
| richards                | 41.0 ms                                                                  | 28.1 ms: 1.46x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 181 us: 1.46x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 58.8 ms: 1.43x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.4 ms: 1.42x faster                                                       |
| pyflate                 | 388 ms                                                                   | 278 ms: 1.40x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 129 us: 1.39x faster                                                        |
| mako                    | 8.69 ms                                                                  | 6.34 ms: 1.37x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 497 ms: 1.34x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 923 us: 1.32x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 29.8 ns: 1.32x faster                                                       |
| pycparser               | 873 ms                                                                   | 662 ms: 1.32x faster                                                        |
| thrift                  | 632 us                                                                   | 479 us: 1.32x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.12 ms: 1.32x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 44.5 ms: 1.31x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 21.8 us: 1.31x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 47.1 ms: 1.31x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 318 ms: 1.30x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 789 ms: 1.30x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 4.21 ms: 1.30x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 36.5 ms: 1.30x faster                                                       |
| django_template         | 29.2 ms                                                                  | 22.7 ms: 1.29x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 14.6 ms: 1.27x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.59 ms: 1.26x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 388 ms: 1.25x faster                                                        |
| async_generators        | 214 ms                                                                   | 173 ms: 1.24x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 990 ms: 1.24x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 35.3 ms: 1.22x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 490 ms: 1.21x faster                                                        |
| regex_compile           | 103 ms                                                                   | 86.2 ms: 1.20x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 504 ms: 1.20x faster                                                        |
| dask                    | 310 ms                                                                   | 260 ms: 1.19x faster                                                        |
| float                   | 59.5 ms                                                                  | 50.3 ms: 1.18x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                                      |
| spectral_norm           | 74.3 ms                                                                  | 63.3 ms: 1.17x faster                                                       |
| deepcopy                | 256 us                                                                   | 220 us: 1.17x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.73 ms: 1.17x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.88 us: 1.16x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 33.4 ms: 1.16x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.32 ms: 1.15x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 34.4 ms: 1.13x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 13.4 ms: 1.13x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.7 ms: 1.13x faster                                                       |
| unpickle                | 8.88 us                                                                  | 7.94 us: 1.12x faster                                                       |
| 2to3                    | 229 ms                                                                   | 205 ms: 1.12x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 853 us: 1.12x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 180 ms: 1.12x faster                                                        |
| regex_dna               | 131 ms                                                                   | 117 ms: 1.11x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 690 us: 1.11x faster                                                        |
| json_loads              | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 285 ms: 1.10x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 13.4 ms: 1.09x faster                                                       |
| fannkuch                | 252 ms                                                                   | 232 ms: 1.09x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 66.2 ms: 1.08x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.5 ms: 1.08x faster                                                       |
| sympy_str               | 189 ms                                                                   | 176 ms: 1.07x faster                                                        |
| regex_effbot            | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 60.6 ms: 1.07x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 89.5 ms: 1.07x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 50.5 ms: 1.07x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 177 ms: 1.06x faster                                                        |
| sqlite_synth            | 1.85 us                                                                  | 1.76 us: 1.05x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 71.5 ms: 1.04x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 99.5 ms: 1.03x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.71 us: 1.01x slower                                                       |
| comprehensions          | 16.0 us                                                                  | 16.3 us: 1.02x slower                                                       |
| logging_format          | 6.53 us                                                                  | 6.83 us: 1.05x slower                                                       |
| pidigits                | 145 ms                                                                   | 152 ms: 1.05x slower                                                        |
| logging_simple          | 6.12 us                                                                  | 6.47 us: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 62.6 ms: 1.06x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.45 ms: 1.09x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.5 us: 1.11x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.88 us: 1.12x slower                                                       |
| generators              | 31.4 ms                                                                  | 36.8 ms: 1.17x slower                                                       |
| coverage                | 37.5 ms                                                                  | 54.2 ms: 1.45x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.17x faster                                                                |

Benchmark hidden because not significant (4): xml_etree_iterparse, pathlib, unpickle_list, telco
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
