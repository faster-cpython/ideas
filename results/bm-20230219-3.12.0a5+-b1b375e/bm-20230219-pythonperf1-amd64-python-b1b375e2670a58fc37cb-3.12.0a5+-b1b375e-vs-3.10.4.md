
# Results vs. 3.10.4

- fork: python
- ref: b1b375e2670a58fc37cb
- machine: windows-amd64
- commit hash: b1b375e
- commit date: 2023-02-19
- overall geometric mean: 1.21x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 199 ms: 1.15x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.63 ms: 1.25x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.0 ms: 1.35x faster                                                       |
| tornado_http   | 106 ms                                                                   | 91.4 ms: 1.16x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.22x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 48.6 ms: 1.22x faster                                                       |
| nbody          | 71.5 ms                                                                  | 61.9 ms: 1.15x faster                                                       |
| pidigits       | 145 ms                                                                   | 150 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 79.1 ms: 1.31x faster                                                       |
| regex_dna      | 131 ms                                                                   | 120 ms: 1.09x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 14.2 ms: 1.06x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.58 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.37 ms: 1.68x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 173 us: 1.53x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 122 us: 1.47x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.8 ms: 1.20x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.87 us: 1.13x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.1 ms: 1.05x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 92.5 ms: 1.03x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.7 ms: 1.01x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.75 us: 1.01x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.71 us: 1.05x slower                                                       |
| pickle               | 6.67 us                                                                  | 7.13 us: 1.07x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.13x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.19 ms: 1.40x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.3 ms: 1.37x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.0 ms: 1.33x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 32.0 ms: 1.21x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.33x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.96 ms: 2.12x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 54.2 ns: 1.74x faster                                                       |
| richards                | 41.0 ms                                                                  | 23.9 ms: 1.71x faster                                                       |
| go                      | 143 ms                                                                   | 83.6 ms: 1.71x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.37 ms: 1.68x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 63.5 ms: 1.63x faster                                                       |
| mypy2                   | 337 ms                                                                   | 217 ms: 1.55x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 173 us: 1.53x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 25.9 ns: 1.52x faster                                                       |
| raytrace                | 267 ms                                                                   | 176 ms: 1.52x faster                                                        |
| pyflate                 | 388 ms                                                                   | 256 ms: 1.51x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 56.1 ms: 1.49x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 122 us: 1.47x faster                                                        |
| generators              | 31.4 ms                                                                  | 21.6 ms: 1.45x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.84 ms: 1.42x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.7 ms: 1.41x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 41.6 ms: 1.40x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.19 ms: 1.40x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 44.6 ms: 1.38x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 483 ms: 1.37x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 888 us: 1.37x faster                                                        |
| django_template         | 29.2 ms                                                                  | 21.3 ms: 1.37x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.0 ms: 1.35x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.09 ms: 1.35x faster                                                       |
| thrift                  | 632 us                                                                   | 470 us: 1.34x faster                                                        |
| comprehensions          | 16.0 us                                                                  | 11.9 us: 1.34x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 14.0 ms: 1.33x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 366 ms: 1.33x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 775 ms: 1.32x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 316 ms: 1.31x faster                                                        |
| regex_compile           | 103 ms                                                                   | 79.1 ms: 1.31x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 21.8 us: 1.30x faster                                                       |
| pycparser               | 873 ms                                                                   | 672 ms: 1.30x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 961 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 479 ms: 1.26x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 476 ms: 1.25x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.63 ms: 1.25x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.3 ms: 1.23x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.17 ms: 1.23x faster                                                       |
| float                   | 59.5 ms                                                                  | 48.6 ms: 1.22x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 32.0 ms: 1.21x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 61.5 ms: 1.21x faster                                                       |
| deepcopy                | 256 us                                                                   | 213 us: 1.21x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 35.8 ms: 1.20x faster                                                       |
| fannkuch                | 252 ms                                                                   | 212 ms: 1.19x faster                                                        |
| docutils                | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.87 us: 1.17x faster                                                       |
| tornado_http            | 106 ms                                                                   | 91.4 ms: 1.16x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 40.5 ms: 1.16x faster                                                       |
| 2to3                    | 229 ms                                                                   | 199 ms: 1.15x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 174 ms: 1.15x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 61.9 ms: 1.15x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 272 ms: 1.15x faster                                                        |
| sympy_str               | 189 ms                                                                   | 164 ms: 1.15x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 57.1 ms: 1.14x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.9 ms: 1.13x faster                                                       |
| unpickle                | 8.88 us                                                                  | 7.87 us: 1.13x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 846 us: 1.13x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 167 ms: 1.12x faster                                                        |
| json_loads              | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.1 ms: 1.11x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.89 ms: 1.10x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 92.8 ms: 1.10x faster                                                       |
| regex_dna               | 131 ms                                                                   | 120 ms: 1.09x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 708 us: 1.08x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 14.2 ms: 1.06x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.1 ms: 1.05x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.53 sec: 1.05x faster                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.58 ms: 1.04x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 71.8 ms: 1.03x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 92.5 ms: 1.03x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.81 us: 1.02x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.41 us: 1.02x faster                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.7 ms: 1.01x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.72 ms: 1.01x faster                                                       |
| logging_simple          | 6.12 us                                                                  | 6.19 us: 1.01x slower                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.75 us: 1.01x slower                                                       |
| async_generators        | 214 ms                                                                   | 220 ms: 1.03x slower                                                        |
| pidigits                | 145 ms                                                                   | 150 ms: 1.04x slower                                                        |
| pickle_list             | 2.57 us                                                                  | 2.71 us: 1.05x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| pickle                  | 6.67 us                                                                  | 7.13 us: 1.07x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 64.9 ms: 1.10x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.48 ms: 1.12x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                       |
| dask                    | 310 ms                                                                   | 350 ms: 1.13x slower                                                        |
| coverage                | 37.5 ms                                                                  | 50.6 ms: 1.35x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.21x faster                                                                |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
