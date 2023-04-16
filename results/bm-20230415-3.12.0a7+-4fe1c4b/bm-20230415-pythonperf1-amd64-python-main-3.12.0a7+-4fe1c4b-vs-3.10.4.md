
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 4fe1c4b
- commit date: 2023-04-15
- overall geometric mean: 1.20x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 198 ms: 1.16x faster                                        |
| chameleon      | 5.77 ms                                                                  | 4.67 ms: 1.24x faster                                       |
| docutils       | 1.83 sec                                                                 | 1.49 sec: 1.23x faster                                      |
| html5lib       | 47.3 ms                                                                  | 35.4 ms: 1.34x faster                                       |
| tornado_http   | 106 ms                                                                   | 85.4 ms: 1.25x faster                                       |
| Geometric mean | (ref)                                                                    | 1.24x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 71.5 ms                                                                  | 57.8 ms: 1.24x faster                                       |
| float          | 59.5 ms                                                                  | 48.3 ms: 1.23x faster                                       |
| pidigits       | 145 ms                                                                   | 146 ms: 1.00x slower                                        |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 80.9 ms: 1.28x faster                                       |
| regex_dna      | 131 ms                                                                   | 119 ms: 1.10x faster                                        |
| regex_v8       | 15.1 ms                                                                  | 14.0 ms: 1.08x faster                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.56 ms: 1.05x faster                                       |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.35 ms: 1.68x faster                                       |
| pickle_pure_python   | 264 us                                                                   | 183 us: 1.44x faster                                        |
| unpickle_pure_python | 179 us                                                                   | 127 us: 1.42x faster                                        |
| xml_etree_process    | 43.0 ms                                                                  | 36.1 ms: 1.19x faster                                       |
| json_loads           | 14.2 us                                                                  | 12.7 us: 1.12x faster                                       |
| unpickle             | 8.88 us                                                                  | 8.08 us: 1.10x faster                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.2 ms: 1.07x faster                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 60.1 ms: 1.04x faster                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 52.7 ms: 1.02x faster                                       |
| pickle_list          | 2.57 us                                                                  | 2.82 us: 1.10x slower                                       |
| pickle_dict          | 16.7 us                                                                  | 18.6 us: 1.11x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.13x faster                                                |

Benchmark hidden because not significant (2): unpickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.1 ms: 1.06x faster                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                       |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 21.7 ms: 1.34x faster                                       |
| mako            | 8.69 ms                                                                  | 6.53 ms: 1.33x faster                                       |
| genshi_text     | 18.5 ms                                                                  | 14.3 ms: 1.30x faster                                       |
| genshi_xml      | 38.8 ms                                                                  | 31.5 ms: 1.23x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.30x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.15 ms: 1.93x faster                                       |
| json_dumps              | 9.00 ms                                                                  | 5.35 ms: 1.68x faster                                       |
| mypy2                   | 337 ms                                                                   | 206 ms: 1.64x faster                                        |
| go                      | 143 ms                                                                   | 88.8 ms: 1.61x faster                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 755 us: 1.61x faster                                        |
| richards                | 41.0 ms                                                                  | 25.9 ms: 1.59x faster                                       |
| logging_silent          | 94.6 ns                                                                  | 59.7 ns: 1.58x faster                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 930 us: 1.58x faster                                        |
| generators              | 31.4 ms                                                                  | 20.0 ms: 1.57x faster                                       |
| raytrace                | 267 ms                                                                   | 173 ms: 1.55x faster                                        |
| scimark_lu              | 83.9 ms                                                                  | 54.8 ms: 1.53x faster                                       |
| pickle_pure_python      | 264 us                                                                   | 183 us: 1.44x faster                                        |
| scimark_sor             | 104 ms                                                                   | 72.5 ms: 1.43x faster                                       |
| unpickle_pure_python    | 179 us                                                                   | 127 us: 1.42x faster                                        |
| asyncio_tcp             | 664 ms                                                                   | 471 ms: 1.41x faster                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 40.1 ms: 1.40x faster                                       |
| hexiom                  | 5.45 ms                                                                  | 3.97 ms: 1.37x faster                                       |
| pycparser               | 873 ms                                                                   | 639 ms: 1.37x faster                                        |
| async_tree_io           | 1.02 sec                                                                 | 749 ms: 1.37x faster                                        |
| async_tree_none         | 414 ms                                                                   | 303 ms: 1.37x faster                                        |
| chaos                   | 58.4 ms                                                                  | 42.8 ms: 1.37x faster                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 45.3 ms: 1.36x faster                                       |
| async_tree_memoization  | 485 ms                                                                   | 360 ms: 1.35x faster                                        |
| django_template         | 29.2 ms                                                                  | 21.7 ms: 1.34x faster                                       |
| pyflate                 | 388 ms                                                                   | 289 ms: 1.34x faster                                        |
| thrift                  | 632 us                                                                   | 471 us: 1.34x faster                                        |
| html5lib                | 47.3 ms                                                                  | 35.4 ms: 1.34x faster                                       |
| mako                    | 8.69 ms                                                                  | 6.53 ms: 1.33x faster                                       |
| genshi_text             | 18.5 ms                                                                  | 14.3 ms: 1.30x faster                                       |
| deepcopy_memo           | 28.4 us                                                                  | 22.0 us: 1.29x faster                                       |
| regex_compile           | 103 ms                                                                   | 80.9 ms: 1.28x faster                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 478 ms: 1.26x faster                                        |
| pylint                  | 337 ms                                                                   | 270 ms: 1.25x faster                                        |
| pprint_pformat          | 1.23 sec                                                                 | 985 ms: 1.25x faster                                        |
| tornado_http            | 106 ms                                                                   | 85.4 ms: 1.25x faster                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.3 ms: 1.24x faster                                       |
| chameleon               | 5.77 ms                                                                  | 4.67 ms: 1.24x faster                                       |
| nbody                   | 71.5 ms                                                                  | 57.8 ms: 1.24x faster                                       |
| pprint_safe_repr        | 593 ms                                                                   | 480 ms: 1.24x faster                                        |
| float                   | 59.5 ms                                                                  | 48.3 ms: 1.23x faster                                       |
| genshi_xml              | 38.8 ms                                                                  | 31.5 ms: 1.23x faster                                       |
| docutils                | 1.83 sec                                                                 | 1.49 sec: 1.23x faster                                      |
| spectral_norm           | 74.3 ms                                                                  | 60.7 ms: 1.22x faster                                       |
| bench_thread_pool       | 953 us                                                                   | 789 us: 1.21x faster                                        |
| unpack_sequence         | 39.4 ns                                                                  | 32.8 ns: 1.20x faster                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.24 ms: 1.19x faster                                       |
| xml_etree_process       | 43.0 ms                                                                  | 36.1 ms: 1.19x faster                                       |
| scimark_fft             | 187 ms                                                                   | 157 ms: 1.19x faster                                        |
| json                    | 3.18 ms                                                                  | 2.68 ms: 1.19x faster                                       |
| mdp                     | 1.60 sec                                                                 | 1.37 sec: 1.17x faster                                      |
| deepcopy                | 256 us                                                                   | 219 us: 1.17x faster                                        |
| sqlglot_normalize       | 201 ms                                                                   | 172 ms: 1.17x faster                                        |
| dulwich_log             | 47.0 ms                                                                  | 40.3 ms: 1.16x faster                                       |
| sympy_expand            | 313 ms                                                                   | 269 ms: 1.16x faster                                        |
| 2to3                    | 229 ms                                                                   | 198 ms: 1.16x faster                                        |
| sympy_integrate         | 14.7 ms                                                                  | 12.7 ms: 1.15x faster                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.91 us: 1.14x faster                                       |
| create_gc_cycles        | 764 us                                                                   | 677 us: 1.13x faster                                        |
| coroutines              | 15.6 ms                                                                  | 13.9 ms: 1.12x faster                                       |
| json_loads              | 14.2 us                                                                  | 12.7 us: 1.12x faster                                       |
| nqueens                 | 64.8 ms                                                                  | 58.4 ms: 1.11x faster                                       |
| sympy_str               | 189 ms                                                                   | 170 ms: 1.11x faster                                        |
| comprehensions          | 16.0 us                                                                  | 14.5 us: 1.10x faster                                       |
| unpickle                | 8.88 us                                                                  | 8.08 us: 1.10x faster                                       |
| regex_dna               | 131 ms                                                                   | 119 ms: 1.10x faster                                        |
| sympy_sum               | 102 ms                                                                   | 93.7 ms: 1.09x faster                                       |
| regex_v8                | 15.1 ms                                                                  | 14.0 ms: 1.08x faster                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 89.2 ms: 1.07x faster                                       |
| python_startup          | 19.3 ms                                                                  | 18.1 ms: 1.06x faster                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.56 ms: 1.05x faster                                       |
| meteor_contest          | 74.3 ms                                                                  | 71.2 ms: 1.04x faster                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 60.1 ms: 1.04x faster                                       |
| fannkuch                | 252 ms                                                                   | 245 ms: 1.03x faster                                        |
| sqlite_synth            | 1.85 us                                                                  | 1.80 us: 1.03x faster                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 52.7 ms: 1.02x faster                                       |
| async_generators        | 214 ms                                                                   | 211 ms: 1.02x faster                                        |
| pidigits                | 145 ms                                                                   | 146 ms: 1.00x slower                                        |
| logging_simple          | 6.12 us                                                                  | 6.27 us: 1.02x slower                                       |
| logging_format          | 6.53 us                                                                  | 6.78 us: 1.04x slower                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 64.4 ms: 1.09x slower                                       |
| pathlib                 | 75.2 ms                                                                  | 82.3 ms: 1.09x slower                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.46 ms: 1.10x slower                                       |
| pickle_list             | 2.57 us                                                                  | 2.82 us: 1.10x slower                                       |
| pickle_dict             | 16.7 us                                                                  | 18.6 us: 1.11x slower                                       |
| dask                    | 310 ms                                                                   | 352 ms: 1.13x slower                                        |
| coverage                | 37.5 ms                                                                  | 52.1 ms: 1.39x slower                                       |
| Geometric mean          | (ref)                                                                    | 1.20x faster                                                |

Benchmark hidden because not significant (3): unpickle_list, telco, pickle
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
