
# Results vs. 3.10.4

- fork: python
- ref: 7b14c2ef194b6eed7967
- machine: windows-amd64
- commit hash: 7b14c2e
- commit date: 2023-01-16
- overall geometric mean: 1.22x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 200 ms: 1.15x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.49 ms: 1.29x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.53 sec: 1.20x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 33.0 ms: 1.43x faster                                                       |
| tornado_http   | 106 ms                                                                   | 91.4 ms: 1.16x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.24x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 47.9 ms: 1.24x faster                                                       |
| nbody          | 71.5 ms                                                                  | 58.5 ms: 1.22x faster                                                       |
| pidigits       | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 78.3 ms: 1.32x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.8 ms: 1.10x faster                                                       |
| regex_dna      | 131 ms                                                                   | 124 ms: 1.06x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.61 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.24 ms: 1.72x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 173 us: 1.53x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 119 us: 1.51x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 33.9 ms: 1.27x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 50.0 ms: 1.08x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.1 ms: 1.07x faster                                                       |
| json_loads           | 14.2 us                                                                  | 14.0 us: 1.02x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.5 ms: 1.02x slower                                                       |
| pickle               | 6.67 us                                                                  | 6.84 us: 1.03x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.74 us: 1.07x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.0 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.13x faster                                                                |

Benchmark hidden because not significant (2): unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 20.4 ms: 1.43x faster                                                       |
| mako            | 8.69 ms                                                                  | 6.12 ms: 1.42x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.9 ms: 1.34x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 31.0 ms: 1.25x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.36x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.93 ms: 2.15x faster                                                       |
| go                      | 143 ms                                                                   | 81.1 ms: 1.77x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 54.9 ns: 1.72x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.24 ms: 1.72x faster                                                       |
| richards                | 41.0 ms                                                                  | 24.1 ms: 1.71x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 61.1 ms: 1.70x faster                                                       |
| raytrace                | 267 ms                                                                   | 168 ms: 1.59x faster                                                        |
| mypy2                   | 337 ms                                                                   | 216 ms: 1.56x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 173 us: 1.53x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 119 us: 1.51x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 55.8 ms: 1.50x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 37.3 ms: 1.50x faster                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 26.4 ns: 1.49x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.67 ms: 1.49x faster                                                       |
| pyflate                 | 388 ms                                                                   | 265 ms: 1.47x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 19.7 us: 1.44x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.4 ms: 1.43x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 33.0 ms: 1.43x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.12 ms: 1.42x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 858 us: 1.42x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 41.8 ms: 1.40x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 475 ms: 1.40x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.06 ms: 1.39x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 351 ms: 1.38x faster                                                        |
| pycparser               | 873 ms                                                                   | 634 ms: 1.38x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 307 ms: 1.35x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 13.9 ms: 1.34x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 46.0 ms: 1.34x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 768 ms: 1.33x faster                                                        |
| thrift                  | 632 us                                                                   | 474 us: 1.33x faster                                                        |
| regex_compile           | 103 ms                                                                   | 78.3 ms: 1.32x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 450 ms: 1.32x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 933 ms: 1.32x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.49 ms: 1.29x faster                                                       |
| deepcopy                | 256 us                                                                   | 201 us: 1.27x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 474 ms: 1.27x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 33.9 ms: 1.27x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 59.2 ms: 1.25x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 31.0 ms: 1.25x faster                                                       |
| float                   | 59.5 ms                                                                  | 47.9 ms: 1.24x faster                                                       |
| async_generators        | 214 ms                                                                   | 173 ms: 1.24x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.5 ms: 1.23x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 58.5 ms: 1.22x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.80 us: 1.21x faster                                                       |
| dask                    | 310 ms                                                                   | 256 ms: 1.21x faster                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.21 ms: 1.21x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 167 ms: 1.21x faster                                                        |
| docutils                | 1.83 sec                                                                 | 1.53 sec: 1.20x faster                                                      |
| fannkuch                | 252 ms                                                                   | 214 ms: 1.17x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 55.3 ms: 1.17x faster                                                       |
| tornado_http            | 106 ms                                                                   | 91.4 ms: 1.16x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.74 ms: 1.16x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 161 ms: 1.16x faster                                                        |
| 2to3                    | 229 ms                                                                   | 200 ms: 1.15x faster                                                        |
| sympy_expand            | 313 ms                                                                   | 273 ms: 1.15x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 670 us: 1.14x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 839 us: 1.14x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 13.1 ms: 1.12x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.9 ms: 1.12x faster                                                       |
| sympy_str               | 189 ms                                                                   | 172 ms: 1.10x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.8 ms: 1.10x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 50.0 ms: 1.08x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 95.0 ms: 1.08x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 89.1 ms: 1.07x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 69.2 ms: 1.07x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.6 ms: 1.07x faster                                                       |
| regex_dna               | 131 ms                                                                   | 124 ms: 1.06x faster                                                        |
| comprehensions          | 16.0 us                                                                  | 15.1 us: 1.06x faster                                                       |
| logging_simple          | 6.12 us                                                                  | 5.80 us: 1.06x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.76 us: 1.05x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.53 sec: 1.05x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.61 ms: 1.02x faster                                                       |
| json_loads              | 14.2 us                                                                  | 14.0 us: 1.02x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.44 us: 1.01x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.75 ms: 1.01x faster                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.5 ms: 1.02x slower                                                       |
| pickle                  | 6.67 us                                                                  | 6.84 us: 1.03x slower                                                       |
| pidigits                | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.74 us: 1.07x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.1 ms: 1.07x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.43 ms: 1.07x slower                                                       |
| generators              | 31.4 ms                                                                  | 34.2 ms: 1.09x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 19.0 us: 1.14x slower                                                       |
| coverage                | 37.5 ms                                                                  | 53.1 ms: 1.42x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.22x faster                                                                |

Benchmark hidden because not significant (3): unpickle, pathlib, unpickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
