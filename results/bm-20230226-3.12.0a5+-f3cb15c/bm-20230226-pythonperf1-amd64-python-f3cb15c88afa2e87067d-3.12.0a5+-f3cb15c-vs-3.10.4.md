
# Results vs. 3.10.4

- fork: python
- ref: f3cb15c88afa2e87067d
- machine: windows-amd64
- commit hash: f3cb15c
- commit date: 2023-02-26
- overall geometric mean: 1.21x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 200 ms: 1.15x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.45 ms: 1.30x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.1 ms: 1.35x faster                                                       |
| tornado_http   | 106 ms                                                                   | 89.4 ms: 1.19x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 48.0 ms: 1.24x faster                                                       |
| nbody          | 71.5 ms                                                                  | 58.7 ms: 1.22x faster                                                       |
| pidigits       | 145 ms                                                                   | 149 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 81.3 ms: 1.27x faster                                                       |
| regex_dna      | 131 ms                                                                   | 118 ms: 1.11x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.52 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.38 ms: 1.67x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 167 us: 1.58x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 118 us: 1.52x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 34.6 ms: 1.24x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.86 us: 1.13x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 92.2 ms: 1.04x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 52.9 ms: 1.02x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.9 ms: 1.02x slower                                                       |
| pickle               | 6.67 us                                                                  | 6.89 us: 1.03x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.78 us: 1.08x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.13x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.8 ms: 1.02x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.9 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 20.8 ms: 1.41x faster                                                       |
| mako            | 8.69 ms                                                                  | 6.22 ms: 1.40x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.7 ms: 1.36x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 30.8 ms: 1.26x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.35x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.94 ms: 2.14x faster                                                       |
| richards                | 41.0 ms                                                                  | 23.2 ms: 1.77x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 54.5 ns: 1.74x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 61.6 ms: 1.68x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.38 ms: 1.67x faster                                                       |
| go                      | 143 ms                                                                   | 87.5 ms: 1.64x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 167 us: 1.58x faster                                                        |
| mypy2                   | 337 ms                                                                   | 215 ms: 1.57x faster                                                        |
| raytrace                | 267 ms                                                                   | 173 ms: 1.54x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 118 us: 1.52x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 26.2 ns: 1.50x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 831 us: 1.47x faster                                                        |
| generators              | 31.4 ms                                                                  | 21.5 ms: 1.46x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 57.4 ms: 1.46x faster                                                       |
| pyflate                 | 388 ms                                                                   | 270 ms: 1.44x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 20.0 us: 1.42x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.84 ms: 1.42x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 41.3 ms: 1.41x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.04 ms: 1.41x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.8 ms: 1.41x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.22 ms: 1.40x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 44.4 ms: 1.38x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 41.0 ms: 1.37x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 486 ms: 1.37x faster                                                        |
| async_tree_memoization  | 485 ms                                                                   | 356 ms: 1.36x faster                                                        |
| thrift                  | 632 us                                                                   | 464 us: 1.36x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 13.7 ms: 1.36x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.1 ms: 1.35x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 308 ms: 1.34x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 764 ms: 1.34x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 938 ms: 1.31x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.45 ms: 1.30x faster                                                       |
| pycparser               | 873 ms                                                                   | 677 ms: 1.29x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 464 ms: 1.28x faster                                                        |
| regex_compile           | 103 ms                                                                   | 81.3 ms: 1.27x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 58.4 ms: 1.27x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 30.8 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 484 ms: 1.25x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 34.6 ms: 1.24x faster                                                       |
| float                   | 59.5 ms                                                                  | 48.0 ms: 1.24x faster                                                       |
| deepcopy                | 256 us                                                                   | 208 us: 1.23x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.5 ms: 1.23x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 58.7 ms: 1.22x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.81 us: 1.21x faster                                                       |
| tornado_http            | 106 ms                                                                   | 89.4 ms: 1.19x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| sqlglot_normalize       | 201 ms                                                                   | 171 ms: 1.17x faster                                                        |
| fannkuch                | 252 ms                                                                   | 216 ms: 1.16x faster                                                        |
| sympy_expand            | 313 ms                                                                   | 269 ms: 1.16x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 162 ms: 1.15x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 12.8 ms: 1.15x faster                                                       |
| 2to3                    | 229 ms                                                                   | 200 ms: 1.15x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.79 ms: 1.14x faster                                                       |
| unpickle                | 8.88 us                                                                  | 7.86 us: 1.13x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.38 ms: 1.12x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 13.9 ms: 1.12x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.9 ms: 1.12x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 852 us: 1.12x faster                                                        |
| regex_dna               | 131 ms                                                                   | 118 ms: 1.11x faster                                                        |
| json_loads              | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 58.6 ms: 1.11x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 696 us: 1.10x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.47 sec: 1.09x faster                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.52 ms: 1.08x faster                                                       |
| sympy_str               | 189 ms                                                                   | 176 ms: 1.07x faster                                                        |
| sympy_sum               | 102 ms                                                                   | 96.9 ms: 1.06x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.2 us: 1.05x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 70.6 ms: 1.05x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 92.2 ms: 1.04x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.37 us: 1.03x faster                                                       |
| pathlib                 | 75.2 ms                                                                  | 73.4 ms: 1.02x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.8 ms: 1.02x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 52.9 ms: 1.02x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.86 us: 1.01x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.85 ms: 1.02x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.9 ms: 1.02x slower                                                       |
| async_generators        | 214 ms                                                                   | 220 ms: 1.02x slower                                                        |
| pidigits                | 145 ms                                                                   | 149 ms: 1.03x slower                                                        |
| pickle                  | 6.67 us                                                                  | 6.89 us: 1.03x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.9 ms: 1.07x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.78 us: 1.08x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 65.8 ms: 1.11x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| dask                    | 310 ms                                                                   | 353 ms: 1.14x slower                                                        |
| gc_traversal            | 1.33 ms                                                                  | 1.53 ms: 1.15x slower                                                       |
| coverage                | 37.5 ms                                                                  | 51.0 ms: 1.36x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.21x faster                                                                |

Benchmark hidden because not significant (2): logging_simple, unpickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
