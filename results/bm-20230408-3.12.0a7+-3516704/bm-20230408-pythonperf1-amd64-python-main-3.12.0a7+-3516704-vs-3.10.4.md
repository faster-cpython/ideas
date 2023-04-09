
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 3516704
- commit date: 2023-04-08
- overall geometric mean: 1.20x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 207 ms: 1.11x faster                                        |
| chameleon      | 5.77 ms                                                                  | 4.62 ms: 1.25x faster                                       |
| docutils       | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                      |
| html5lib       | 47.3 ms                                                                  | 36.7 ms: 1.29x faster                                       |
| tornado_http   | 106 ms                                                                   | 89.7 ms: 1.19x faster                                       |
| Geometric mean | (ref)                                                                    | 1.20x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 71.5 ms                                                                  | 56.5 ms: 1.26x faster                                       |
| float          | 59.5 ms                                                                  | 48.1 ms: 1.24x faster                                       |
| pidigits       | 145 ms                                                                   | 148 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 83.5 ms: 1.24x faster                                       |
| regex_v8       | 15.1 ms                                                                  | 13.2 ms: 1.14x faster                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                       |
| regex_dna      | 131 ms                                                                   | 123 ms: 1.07x faster                                        |
| Geometric mean | (ref)                                                                    | 1.13x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.39 ms: 1.67x faster                                       |
| pickle_pure_python   | 264 us                                                                   | 184 us: 1.43x faster                                        |
| unpickle_pure_python | 179 us                                                                   | 127 us: 1.41x faster                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.2 ms: 1.22x faster                                       |
| json_loads           | 14.2 us                                                                  | 13.0 us: 1.09x faster                                       |
| unpickle             | 8.88 us                                                                  | 8.29 us: 1.07x faster                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.9 ms: 1.06x faster                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.7 ms: 1.04x faster                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                       |
| unpickle_list        | 2.71 us                                                                  | 2.74 us: 1.01x slower                                       |
| pickle               | 6.67 us                                                                  | 6.93 us: 1.04x slower                                       |
| pickle_list          | 2.57 us                                                                  | 2.82 us: 1.10x slower                                       |
| pickle_dict          | 16.7 us                                                                  | 19.1 us: 1.14x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.8 ms: 1.03x faster                                       |
| python_startup_no_site | 14.8 ms                                                                  | 16.1 ms: 1.09x slower                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.22 ms: 1.40x faster                                       |
| django_template | 29.2 ms                                                                  | 21.1 ms: 1.38x faster                                       |
| genshi_text     | 18.5 ms                                                                  | 13.8 ms: 1.34x faster                                       |
| genshi_xml      | 38.8 ms                                                                  | 30.5 ms: 1.27x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.35x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.94 ms: 2.14x faster                                       |
| logging_silent          | 94.6 ns                                                                  | 54.4 ns: 1.74x faster                                       |
| go                      | 143 ms                                                                   | 83.8 ms: 1.71x faster                                       |
| json_dumps              | 9.00 ms                                                                  | 5.39 ms: 1.67x faster                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 747 us: 1.63x faster                                        |
| richards                | 41.0 ms                                                                  | 25.2 ms: 1.63x faster                                       |
| scimark_lu              | 83.9 ms                                                                  | 53.8 ms: 1.56x faster                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 947 us: 1.55x faster                                        |
| mypy2                   | 337 ms                                                                   | 219 ms: 1.54x faster                                        |
| raytrace                | 267 ms                                                                   | 176 ms: 1.52x faster                                        |
| generators              | 31.4 ms                                                                  | 20.7 ms: 1.52x faster                                       |
| pickle_pure_python      | 264 us                                                                   | 184 us: 1.43x faster                                        |
| hexiom                  | 5.45 ms                                                                  | 3.87 ms: 1.41x faster                                       |
| unpickle_pure_python    | 179 us                                                                   | 127 us: 1.41x faster                                        |
| scimark_sor             | 104 ms                                                                   | 73.7 ms: 1.40x faster                                       |
| mako                    | 8.69 ms                                                                  | 6.22 ms: 1.40x faster                                       |
| unpack_sequence         | 39.4 ns                                                                  | 28.2 ns: 1.40x faster                                       |
| django_template         | 29.2 ms                                                                  | 21.1 ms: 1.38x faster                                       |
| chaos                   | 58.4 ms                                                                  | 42.6 ms: 1.37x faster                                       |
| asyncio_tcp             | 664 ms                                                                   | 487 ms: 1.36x faster                                        |
| pyflate                 | 388 ms                                                                   | 287 ms: 1.35x faster                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 41.6 ms: 1.35x faster                                       |
| async_tree_io           | 1.02 sec                                                                 | 760 ms: 1.35x faster                                        |
| genshi_text             | 18.5 ms                                                                  | 13.8 ms: 1.34x faster                                       |
| thrift                  | 632 us                                                                   | 473 us: 1.34x faster                                        |
| deepcopy_memo           | 28.4 us                                                                  | 21.3 us: 1.34x faster                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 46.0 ms: 1.33x faster                                       |
| pycparser               | 873 ms                                                                   | 655 ms: 1.33x faster                                        |
| async_tree_none         | 414 ms                                                                   | 314 ms: 1.32x faster                                        |
| async_tree_memoization  | 485 ms                                                                   | 370 ms: 1.31x faster                                        |
| html5lib                | 47.3 ms                                                                  | 36.7 ms: 1.29x faster                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 470 ms: 1.29x faster                                        |
| pprint_pformat          | 1.23 sec                                                                 | 963 ms: 1.27x faster                                        |
| pprint_safe_repr        | 593 ms                                                                   | 467 ms: 1.27x faster                                        |
| genshi_xml              | 38.8 ms                                                                  | 30.5 ms: 1.27x faster                                       |
| nbody                   | 71.5 ms                                                                  | 56.5 ms: 1.26x faster                                       |
| chameleon               | 5.77 ms                                                                  | 4.62 ms: 1.25x faster                                       |
| regex_compile           | 103 ms                                                                   | 83.5 ms: 1.24x faster                                       |
| float                   | 59.5 ms                                                                  | 48.1 ms: 1.24x faster                                       |
| spectral_norm           | 74.3 ms                                                                  | 60.4 ms: 1.23x faster                                       |
| xml_etree_process       | 43.0 ms                                                                  | 35.2 ms: 1.22x faster                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.0 ms: 1.21x faster                                       |
| tornado_http            | 106 ms                                                                   | 89.7 ms: 1.19x faster                                       |
| deepcopy                | 256 us                                                                   | 218 us: 1.18x faster                                        |
| docutils                | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                      |
| json                    | 3.18 ms                                                                  | 2.72 ms: 1.17x faster                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.29 ms: 1.17x faster                                       |
| sqlglot_normalize       | 201 ms                                                                   | 174 ms: 1.16x faster                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.89 us: 1.15x faster                                       |
| coroutines              | 15.6 ms                                                                  | 13.6 ms: 1.15x faster                                       |
| mdp                     | 1.60 sec                                                                 | 1.39 sec: 1.15x faster                                      |
| nqueens                 | 64.8 ms                                                                  | 56.4 ms: 1.15x faster                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.8 ms: 1.15x faster                                       |
| regex_v8                | 15.1 ms                                                                  | 13.2 ms: 1.14x faster                                       |
| scimark_fft             | 187 ms                                                                   | 164 ms: 1.14x faster                                        |
| comprehensions          | 16.0 us                                                                  | 14.2 us: 1.13x faster                                       |
| sympy_expand            | 313 ms                                                                   | 279 ms: 1.12x faster                                        |
| bench_thread_pool       | 953 us                                                                   | 852 us: 1.12x faster                                        |
| 2to3                    | 229 ms                                                                   | 207 ms: 1.11x faster                                        |
| create_gc_cycles        | 764 us                                                                   | 688 us: 1.11x faster                                        |
| dulwich_log             | 47.0 ms                                                                  | 42.3 ms: 1.11x faster                                       |
| json_loads              | 14.2 us                                                                  | 13.0 us: 1.09x faster                                       |
| sympy_str               | 189 ms                                                                   | 174 ms: 1.08x faster                                        |
| unpickle                | 8.88 us                                                                  | 8.29 us: 1.07x faster                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                       |
| regex_dna               | 131 ms                                                                   | 123 ms: 1.07x faster                                        |
| fannkuch                | 252 ms                                                                   | 236 ms: 1.06x faster                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 89.9 ms: 1.06x faster                                       |
| meteor_contest          | 74.3 ms                                                                  | 70.5 ms: 1.05x faster                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.7 ms: 1.04x faster                                       |
| sympy_sum               | 102 ms                                                                   | 98.4 ms: 1.04x faster                                       |
| logging_simple          | 6.12 us                                                                  | 5.94 us: 1.03x faster                                       |
| python_startup          | 19.3 ms                                                                  | 18.8 ms: 1.03x faster                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                       |
| async_generators        | 214 ms                                                                   | 211 ms: 1.02x faster                                        |
| unpickle_list           | 2.71 us                                                                  | 2.74 us: 1.01x slower                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.87 us: 1.01x slower                                       |
| pidigits                | 145 ms                                                                   | 148 ms: 1.02x slower                                        |
| telco                   | 3.77 ms                                                                  | 3.90 ms: 1.04x slower                                       |
| pickle                  | 6.67 us                                                                  | 6.93 us: 1.04x slower                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 16.1 ms: 1.09x slower                                       |
| pickle_list             | 2.57 us                                                                  | 2.82 us: 1.10x slower                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 67.1 ms: 1.13x slower                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.51 ms: 1.14x slower                                       |
| pickle_dict             | 16.7 us                                                                  | 19.1 us: 1.14x slower                                       |
| pathlib                 | 75.2 ms                                                                  | 85.9 ms: 1.14x slower                                       |
| dask                    | 310 ms                                                                   | 360 ms: 1.16x slower                                        |
| coverage                | 37.5 ms                                                                  | 50.8 ms: 1.36x slower                                       |
| Geometric mean          | (ref)                                                                    | 1.20x faster                                                |

Benchmark hidden because not significant (1): logging_format
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
