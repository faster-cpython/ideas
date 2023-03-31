
# Results vs. 3.10.4

- fork: python
- ref: 044bcc1771fe7e2f8eba
- machine: windows-amd64
- commit hash: 044bcc1
- commit date: 2022-11-04
- overall geometric mean: 1.11x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 207 ms: 1.11x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 5.21 ms: 1.11x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.62 sec: 1.13x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 36.7 ms: 1.29x faster                                                       |
| tornado_http   | 106 ms                                                                   | 92.6 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.16x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.5 ms                                                                  | 65.2 ms: 1.10x faster                                                       |
| float          | 59.5 ms                                                                  | 55.8 ms: 1.07x faster                                                       |
| pidigits       | 145 ms                                                                   | 149 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 86.9 ms: 1.19x faster                                                       |
| regex_dna      | 131 ms                                                                   | 123 ms: 1.07x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 14.2 ms: 1.06x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.62 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.56 ms: 1.62x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 205 us: 1.29x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 143 us: 1.26x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 37.4 ms: 1.15x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.3 us: 1.07x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.9 ms: 1.06x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.63 us: 1.03x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 52.4 ms: 1.03x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.92 us: 1.04x slower                                                       |
| unpickle             | 8.88 us                                                                  | 9.31 us: 1.05x slower                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 66.0 ms: 1.06x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.89 us: 1.13x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.6 ms: 1.04x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 22.9 ms: 1.28x faster                                                       |
| mako            | 8.69 ms                                                                  | 7.05 ms: 1.23x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 17.5 ms: 1.06x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 37.7 ms: 1.03x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.14x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 9.00 ms                                                                  | 5.56 ms: 1.62x faster                                                       |
| deltablue               | 4.15 ms                                                                  | 2.57 ms: 1.62x faster                                                       |
| mypy2                   | 337 ms                                                                   | 225 ms: 1.50x faster                                                        |
| go                      | 143 ms                                                                   | 95.5 ms: 1.50x faster                                                       |
| richards                | 41.0 ms                                                                  | 29.8 ms: 1.38x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 76.2 ms: 1.36x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 62.9 ms: 1.33x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 71.3 ns: 1.33x faster                                                       |
| raytrace                | 267 ms                                                                   | 204 ms: 1.31x faster                                                        |
| pyflate                 | 388 ms                                                                   | 298 ms: 1.30x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 43.0 ms: 1.30x faster                                                       |
| thrift                  | 632 us                                                                   | 487 us: 1.30x faster                                                        |
| html5lib                | 47.3 ms                                                                  | 36.7 ms: 1.29x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 205 us: 1.29x faster                                                        |
| django_template         | 29.2 ms                                                                  | 22.9 ms: 1.28x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 803 ms: 1.27x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 961 us: 1.27x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.17 ms: 1.26x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 143 us: 1.26x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 49.7 ms: 1.24x faster                                                       |
| mako                    | 8.69 ms                                                                  | 7.05 ms: 1.23x faster                                                       |
| pycparser               | 873 ms                                                                   | 709 ms: 1.23x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 336 ms: 1.23x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 4.44 ms: 1.23x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 403 ms: 1.20x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 48.8 ms: 1.20x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 1.03 sec: 1.19x faster                                                      |
| regex_compile           | 103 ms                                                                   | 86.9 ms: 1.19x faster                                                       |
| pylint                  | 337 ms                                                                   | 286 ms: 1.18x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 514 ms: 1.18x faster                                                        |
| async_generators        | 214 ms                                                                   | 183 ms: 1.17x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 509 ms: 1.17x faster                                                        |
| dask                    | 310 ms                                                                   | 269 ms: 1.15x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 37.4 ms: 1.15x faster                                                       |
| tornado_http            | 106 ms                                                                   | 92.6 ms: 1.15x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.62 sec: 1.13x faster                                                      |
| create_gc_cycles        | 764 us                                                                   | 683 us: 1.12x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 25.4 us: 1.12x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.39 ms: 1.12x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 5.21 ms: 1.11x faster                                                       |
| 2to3                    | 229 ms                                                                   | 207 ms: 1.11x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 35.0 ms: 1.10x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 65.2 ms: 1.10x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 42.9 ms: 1.09x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 875 us: 1.09x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.94 ms: 1.08x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.7 ms: 1.07x faster                                                       |
| json_loads              | 14.2 us                                                                  | 13.3 us: 1.07x faster                                                       |
| regex_dna               | 131 ms                                                                   | 123 ms: 1.07x faster                                                        |
| float                   | 59.5 ms                                                                  | 55.8 ms: 1.07x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 89.9 ms: 1.06x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 14.2 ms: 1.06x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 190 ms: 1.06x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 17.5 ms: 1.06x faster                                                       |
| deepcopy                | 256 us                                                                   | 242 us: 1.06x faster                                                        |
| sympy_expand            | 313 ms                                                                   | 299 ms: 1.05x faster                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 2.09 us: 1.05x faster                                                       |
| sympy_str               | 189 ms                                                                   | 180 ms: 1.05x faster                                                        |
| python_startup          | 19.3 ms                                                                  | 18.6 ms: 1.04x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.63 us: 1.03x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.79 us: 1.03x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 37.7 ms: 1.03x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 15.2 ms: 1.03x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 52.4 ms: 1.03x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 72.7 ms: 1.02x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 100 ms: 1.02x faster                                                        |
| fannkuch                | 252 ms                                                                   | 248 ms: 1.01x faster                                                        |
| regex_effbot            | 1.64 ms                                                                  | 1.62 ms: 1.01x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.59 sec: 1.01x faster                                                      |
| meteor_contest          | 74.3 ms                                                                  | 75.9 ms: 1.02x slower                                                       |
| pidigits                | 145 ms                                                                   | 149 ms: 1.03x slower                                                        |
| pickle                  | 6.67 us                                                                  | 6.92 us: 1.04x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.94 ms: 1.04x slower                                                       |
| unpickle                | 8.88 us                                                                  | 9.31 us: 1.05x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 66.0 ms: 1.06x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.7 ms: 1.08x slower                                                       |
| comprehensions          | 16.0 us                                                                  | 17.2 us: 1.08x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.63 us: 1.08x slower                                                       |
| asyncio_tcp             | 664 ms                                                                   | 732 ms: 1.10x slower                                                        |
| logging_format          | 6.53 us                                                                  | 7.21 us: 1.10x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.89 us: 1.13x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.50 ms: 1.13x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| generators              | 31.4 ms                                                                  | 36.1 ms: 1.15x slower                                                       |
| coverage                | 37.5 ms                                                                  | 54.4 ms: 1.45x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (4): unpack_sequence, pathlib, nqueens, scimark_fft
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
