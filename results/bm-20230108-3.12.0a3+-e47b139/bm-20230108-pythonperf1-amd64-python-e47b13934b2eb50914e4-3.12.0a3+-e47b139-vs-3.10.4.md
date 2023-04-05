
# Results vs. 3.10.4

- fork: python
- ref: e47b13934b2eb50914e4
- machine: windows-amd64
- commit hash: e47b139
- commit date: 2023-01-08
- overall geometric mean: 1.21x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 201 ms: 1.14x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.58 ms: 1.26x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.5 ms: 1.33x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 48.3 ms: 1.23x faster                                                       |
| nbody          | 71.5 ms                                                                  | 60.2 ms: 1.19x faster                                                       |
| pidigits       | 145 ms                                                                   | 152 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 80.3 ms: 1.29x faster                                                       |
| regex_dna      | 131 ms                                                                   | 117 ms: 1.12x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 14.0 ms: 1.08x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.54 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.13 ms: 1.76x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 169 us: 1.56x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 122 us: 1.47x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 34.0 ms: 1.27x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 87.9 ms: 1.09x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.33 us: 1.07x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.2 ms: 1.05x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.98 us: 1.05x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.77 us: 1.08x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.6 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.14x faster                                                                |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.23 ms: 1.39x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.4 ms: 1.39x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.1 ms: 1.38x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 30.6 ms: 1.27x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.36x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.01 ms: 2.07x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.13 ms: 1.76x faster                                                       |
| go                      | 143 ms                                                                   | 82.4 ms: 1.74x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 54.7 ns: 1.73x faster                                                       |
| richards                | 41.0 ms                                                                  | 24.2 ms: 1.69x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 63.1 ms: 1.64x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 169 us: 1.56x faster                                                        |
| mypy2                   | 337 ms                                                                   | 218 ms: 1.55x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 25.9 ns: 1.52x faster                                                       |
| raytrace                | 267 ms                                                                   | 176 ms: 1.52x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 38.0 ms: 1.47x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 122 us: 1.47x faster                                                        |
| pyflate                 | 388 ms                                                                   | 267 ms: 1.45x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 58.1 ms: 1.44x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.82 ms: 1.43x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 20.0 us: 1.42x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 860 us: 1.42x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 41.8 ms: 1.40x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.23 ms: 1.39x faster                                                       |
| thrift                  | 632 us                                                                   | 454 us: 1.39x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 13.4 ms: 1.39x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.06 ms: 1.39x faster                                                       |
| django_template         | 29.2 ms                                                                  | 21.1 ms: 1.38x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 305 ms: 1.36x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 761 ms: 1.34x faster                                                        |
| pycparser               | 873 ms                                                                   | 651 ms: 1.34x faster                                                        |
| asyncio_tcp             | 664 ms                                                                   | 498 ms: 1.33x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 46.1 ms: 1.33x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.5 ms: 1.33x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 367 ms: 1.32x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 940 ms: 1.31x faster                                                        |
| spectral_norm           | 74.3 ms                                                                  | 57.5 ms: 1.29x faster                                                       |
| regex_compile           | 103 ms                                                                   | 80.3 ms: 1.29x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 30.6 ms: 1.27x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 34.0 ms: 1.27x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.58 ms: 1.26x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 475 ms: 1.25x faster                                                        |
| deepcopy                | 256 us                                                                   | 207 us: 1.24x faster                                                        |
| float                   | 59.5 ms                                                                  | 48.3 ms: 1.23x faster                                                       |
| async_generators        | 214 ms                                                                   | 175 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 497 ms: 1.22x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.9 ms: 1.21x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.22 ms: 1.21x faster                                                       |
| dask                    | 310 ms                                                                   | 259 ms: 1.20x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 60.2 ms: 1.19x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.88 us: 1.16x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.76 ms: 1.15x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 272 ms: 1.15x faster                                                        |
| fannkuch                | 252 ms                                                                   | 219 ms: 1.15x faster                                                        |
| 2to3                    | 229 ms                                                                   | 201 ms: 1.14x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 177 ms: 1.14x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 57.1 ms: 1.13x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.1 ms: 1.12x faster                                                       |
| regex_dna               | 131 ms                                                                   | 117 ms: 1.12x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 168 ms: 1.11x faster                                                        |
| json_loads              | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 857 us: 1.11x faster                                                        |
| dulwich_log             | 47.0 ms                                                                  | 42.5 ms: 1.11x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 692 us: 1.11x faster                                                        |
| sympy_str               | 189 ms                                                                   | 171 ms: 1.10x faster                                                        |
| comprehensions          | 16.0 us                                                                  | 14.5 us: 1.10x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.3 ms: 1.09x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 87.9 ms: 1.09x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 14.0 ms: 1.08x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 95.2 ms: 1.07x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 69.5 ms: 1.07x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.33 us: 1.07x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.54 ms: 1.07x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.76 us: 1.05x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.2 ms: 1.05x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.35 us: 1.03x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.98 us: 1.05x slower                                                       |
| pidigits                | 145 ms                                                                   | 152 ms: 1.05x slower                                                        |
| generators              | 31.4 ms                                                                  | 33.1 ms: 1.05x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 62.9 ms: 1.06x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.77 us: 1.08x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.45 ms: 1.09x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.6 us: 1.11x slower                                                       |
| coverage                | 37.5 ms                                                                  | 53.2 ms: 1.42x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.21x faster                                                                |

Benchmark hidden because not significant (6): unpickle_list, xml_etree_iterparse, mdp, logging_simple, pathlib, telco
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
