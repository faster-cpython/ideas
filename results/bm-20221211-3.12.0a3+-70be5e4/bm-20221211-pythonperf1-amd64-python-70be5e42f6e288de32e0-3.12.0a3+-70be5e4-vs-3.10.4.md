
# Results vs. 3.10.4

- fork: python
- ref: 70be5e42f6e288de32e0
- machine: windows-amd64
- commit hash: 70be5e4
- commit date: 2022-12-11
- overall geometric mean: 1.17x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 201 ms: 1.14x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.68 ms: 1.23x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 36.2 ms: 1.31x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.21x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 49.7 ms: 1.20x faster                                                       |
| nbody          | 71.5 ms                                                                  | 62.7 ms: 1.14x faster                                                       |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 84.9 ms: 1.22x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.6 ms: 1.11x faster                                                       |
| regex_dna      | 131 ms                                                                   | 120 ms: 1.09x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.54 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.41 ms: 1.67x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 184 us: 1.44x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 130 us: 1.38x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.3 ms: 1.22x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.01 us: 1.11x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.3 us: 1.07x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.2 ms: 1.05x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 91.5 ms: 1.05x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.60 us: 1.04x faster                                                       |
| pickle               | 6.67 us                                                                  | 7.21 us: 1.08x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.83 us: 1.10x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.2 us: 1.15x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 19.0 ms: 1.02x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.18 ms: 1.41x faster                                                       |
| django_template | 29.2 ms                                                                  | 22.2 ms: 1.31x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.4 ms: 1.28x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 32.6 ms: 1.19x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.30x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.17 ms: 1.91x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.41 ms: 1.67x faster                                                       |
| go                      | 143 ms                                                                   | 88.5 ms: 1.62x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 59.5 ns: 1.59x faster                                                       |
| richards                | 41.0 ms                                                                  | 26.3 ms: 1.56x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 66.7 ms: 1.55x faster                                                       |
| mypy2                   | 337 ms                                                                   | 221 ms: 1.53x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 184 us: 1.44x faster                                                        |
| raytrace                | 267 ms                                                                   | 189 ms: 1.42x faster                                                        |
| mako                    | 8.69 ms                                                                  | 6.18 ms: 1.41x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 59.8 ms: 1.40x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 878 us: 1.39x faster                                                        |
| pyflate                 | 388 ms                                                                   | 282 ms: 1.38x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 130 us: 1.38x faster                                                        |
| thrift                  | 632 us                                                                   | 460 us: 1.37x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 41.2 ms: 1.36x faster                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 29.1 ns: 1.35x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.09 ms: 1.35x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.10 ms: 1.33x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 499 ms: 1.33x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 21.5 us: 1.32x faster                                                       |
| django_template         | 29.2 ms                                                                  | 22.2 ms: 1.31x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 36.2 ms: 1.31x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 47.0 ms: 1.31x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 14.4 ms: 1.28x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 45.6 ms: 1.28x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 803 ms: 1.27x faster                                                        |
| pycparser               | 873 ms                                                                   | 689 ms: 1.27x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 972 ms: 1.26x faster                                                        |
| async_tree_memoization  | 485 ms                                                                   | 387 ms: 1.25x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 331 ms: 1.25x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 474 ms: 1.25x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.68 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 494 ms: 1.22x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 35.3 ms: 1.22x faster                                                       |
| regex_compile           | 103 ms                                                                   | 84.9 ms: 1.22x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 61.6 ms: 1.21x faster                                                       |
| async_generators        | 214 ms                                                                   | 179 ms: 1.20x faster                                                        |
| float                   | 59.5 ms                                                                  | 49.7 ms: 1.20x faster                                                       |
| deepcopy                | 256 us                                                                   | 214 us: 1.19x faster                                                        |
| genshi_xml              | 38.8 ms                                                                  | 32.6 ms: 1.19x faster                                                       |
| dask                    | 310 ms                                                                   | 266 ms: 1.17x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 33.1 ms: 1.17x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.88 us: 1.16x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                      |
| json                    | 3.18 ms                                                                  | 2.78 ms: 1.14x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 62.7 ms: 1.14x faster                                                       |
| 2to3                    | 229 ms                                                                   | 201 ms: 1.14x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 846 us: 1.13x faster                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.38 ms: 1.12x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.1 ms: 1.12x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.9 ms: 1.12x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 683 us: 1.12x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 180 ms: 1.12x faster                                                        |
| unpickle                | 8.88 us                                                                  | 8.01 us: 1.11x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 282 ms: 1.11x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.6 ms: 1.11x faster                                                       |
| regex_dna               | 131 ms                                                                   | 120 ms: 1.09x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 60.4 ms: 1.07x faster                                                       |
| sympy_str               | 189 ms                                                                   | 176 ms: 1.07x faster                                                        |
| json_loads              | 14.2 us                                                                  | 13.3 us: 1.07x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.54 ms: 1.07x faster                                                       |
| fannkuch                | 252 ms                                                                   | 237 ms: 1.06x faster                                                        |
| coroutines              | 15.6 ms                                                                  | 14.7 ms: 1.06x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.2 ms: 1.05x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 178 ms: 1.05x faster                                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 91.5 ms: 1.05x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.60 us: 1.04x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.78 us: 1.04x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 99.4 ms: 1.03x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 72.8 ms: 1.02x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 19.0 ms: 1.02x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.7 us: 1.01x faster                                                       |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                        |
| telco                   | 3.77 ms                                                                  | 3.84 ms: 1.02x slower                                                       |
| logging_format          | 6.53 us                                                                  | 6.73 us: 1.03x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.6 ms: 1.08x slower                                                       |
| pickle                  | 6.67 us                                                                  | 7.21 us: 1.08x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.83 us: 1.10x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.51 ms: 1.13x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 19.2 us: 1.15x slower                                                       |
| generators              | 31.4 ms                                                                  | 38.0 ms: 1.21x slower                                                       |
| coverage                | 37.5 ms                                                                  | 54.5 ms: 1.45x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.17x faster                                                                |

Benchmark hidden because not significant (3): logging_simple, pathlib, xml_etree_iterparse
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
