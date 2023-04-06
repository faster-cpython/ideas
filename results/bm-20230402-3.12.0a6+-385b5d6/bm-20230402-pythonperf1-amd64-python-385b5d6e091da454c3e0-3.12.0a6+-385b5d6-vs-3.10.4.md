
# Results vs. 3.10.4

- fork: python
- ref: 385b5d6e091da454c3e0
- machine: windows-amd64
- commit hash: 385b5d6
- commit date: 2023-04-02
- overall geometric mean: 1.22x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 202 ms: 1.14x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.50 ms: 1.28x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.7 ms: 1.33x faster                                                       |
| tornado_http   | 106 ms                                                                   | 87.7 ms: 1.21x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.22x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.5 ms                                                                  | 53.3 ms: 1.34x faster                                                       |
| float          | 59.5 ms                                                                  | 47.4 ms: 1.26x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.19x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 79.5 ms: 1.30x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                       |
| regex_dna      | 131 ms                                                                   | 123 ms: 1.07x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.55 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.30 ms: 1.70x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 171 us: 1.55x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 121 us: 1.48x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 34.7 ms: 1.24x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.73 us: 1.15x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.7 ms: 1.07x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 50.7 ms: 1.06x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.5 us: 1.05x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 60.4 ms: 1.04x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.76 us: 1.02x slower                                                       |
| pickle               | 6.67 us                                                                  | 7.09 us: 1.06x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.75 us: 1.07x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 19.0 ms: 1.01x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 16.2 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 20.7 ms: 1.41x faster                                                       |
| mako            | 8.69 ms                                                                  | 6.17 ms: 1.41x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.2 ms: 1.40x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 29.6 ms: 1.31x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.38x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.95 ms: 2.12x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 53.8 ns: 1.76x faster                                                       |
| go                      | 143 ms                                                                   | 82.4 ms: 1.74x faster                                                       |
| richards                | 41.0 ms                                                                  | 24.0 ms: 1.71x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.30 ms: 1.70x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 50.6 ms: 1.66x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 65.1 ms: 1.59x faster                                                       |
| raytrace                | 267 ms                                                                   | 169 ms: 1.58x faster                                                        |
| generators              | 31.4 ms                                                                  | 20.2 ms: 1.56x faster                                                       |
| mypy2                   | 337 ms                                                                   | 217 ms: 1.56x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 171 us: 1.55x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 121 us: 1.48x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 38.0 ms: 1.48x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 832 us: 1.46x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.02 ms: 1.44x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.78 ms: 1.44x faster                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 27.4 ns: 1.43x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 40.9 ms: 1.43x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 20.1 us: 1.42x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 43.4 ms: 1.42x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.7 ms: 1.41x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.17 ms: 1.41x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 13.2 ms: 1.40x faster                                                       |
| pyflate                 | 388 ms                                                                   | 278 ms: 1.40x faster                                                        |
| asyncio_tcp             | 664 ms                                                                   | 481 ms: 1.38x faster                                                        |
| thrift                  | 632 us                                                                   | 460 us: 1.37x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 906 ms: 1.36x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 306 ms: 1.35x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 757 ms: 1.35x faster                                                        |
| spectral_norm           | 74.3 ms                                                                  | 55.4 ms: 1.34x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 362 ms: 1.34x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 53.3 ms: 1.34x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.7 ms: 1.33x faster                                                       |
| pycparser               | 873 ms                                                                   | 665 ms: 1.31x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 453 ms: 1.31x faster                                                        |
| genshi_xml              | 38.8 ms                                                                  | 29.6 ms: 1.31x faster                                                       |
| regex_compile           | 103 ms                                                                   | 79.5 ms: 1.30x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.50 ms: 1.28x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.09 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 476 ms: 1.27x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 30.7 ms: 1.26x faster                                                       |
| float                   | 59.5 ms                                                                  | 47.4 ms: 1.26x faster                                                       |
| deepcopy                | 256 us                                                                   | 205 us: 1.25x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 34.7 ms: 1.24x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 165 ms: 1.22x faster                                                        |
| tornado_http            | 106 ms                                                                   | 87.7 ms: 1.21x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 154 ms: 1.21x faster                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.80 us: 1.21x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.65 ms: 1.20x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                      |
| unpickle                | 8.88 us                                                                  | 7.73 us: 1.15x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.8 ms: 1.15x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.40 sec: 1.15x faster                                                      |
| bench_thread_pool       | 953 us                                                                   | 836 us: 1.14x faster                                                        |
| 2to3                    | 229 ms                                                                   | 202 ms: 1.14x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 57.4 ms: 1.13x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 13.8 ms: 1.13x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.6 ms: 1.13x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 278 ms: 1.12x faster                                                        |
| fannkuch                | 252 ms                                                                   | 225 ms: 1.12x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 696 us: 1.10x faster                                                        |
| comprehensions          | 16.0 us                                                                  | 14.6 us: 1.10x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                       |
| sympy_str               | 189 ms                                                                   | 175 ms: 1.08x faster                                                        |
| meteor_contest          | 74.3 ms                                                                  | 69.1 ms: 1.08x faster                                                       |
| regex_dna               | 131 ms                                                                   | 123 ms: 1.07x faster                                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 89.7 ms: 1.07x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 50.7 ms: 1.06x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.55 ms: 1.06x faster                                                       |
| json_loads              | 14.2 us                                                                  | 13.5 us: 1.05x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 97.7 ms: 1.05x faster                                                       |
| async_generators        | 214 ms                                                                   | 206 ms: 1.04x faster                                                        |
| logging_format          | 6.53 us                                                                  | 6.29 us: 1.04x faster                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 60.4 ms: 1.04x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.78 us: 1.03x faster                                                       |
| logging_simple          | 6.12 us                                                                  | 6.02 us: 1.02x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 19.0 ms: 1.01x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.76 us: 1.02x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.92 ms: 1.04x slower                                                       |
| pickle                  | 6.67 us                                                                  | 7.09 us: 1.06x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.75 us: 1.07x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 16.2 ms: 1.09x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.47 ms: 1.10x slower                                                       |
| pathlib                 | 75.2 ms                                                                  | 83.9 ms: 1.12x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 66.4 ms: 1.12x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| dask                    | 310 ms                                                                   | 355 ms: 1.14x slower                                                        |
| coverage                | 37.5 ms                                                                  | 52.2 ms: 1.39x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.22x faster                                                                |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
