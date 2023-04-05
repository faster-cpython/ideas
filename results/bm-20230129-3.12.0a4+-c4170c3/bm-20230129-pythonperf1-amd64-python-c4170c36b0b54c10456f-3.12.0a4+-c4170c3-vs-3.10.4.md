
# Results vs. 3.10.4

- fork: python
- ref: c4170c36b0b54c10456f
- machine: windows-amd64
- commit hash: c4170c3
- commit date: 2023-01-29
- overall geometric mean: 1.21x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 199 ms: 1.15x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.43 ms: 1.30x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.53 sec: 1.20x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.1 ms: 1.35x faster                                                       |
| tornado_http   | 106 ms                                                                   | 91.6 ms: 1.16x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 48.2 ms: 1.23x faster                                                       |
| nbody          | 71.5 ms                                                                  | 61.8 ms: 1.16x faster                                                       |
| pidigits       | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 79.7 ms: 1.30x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                       |
| regex_dna      | 131 ms                                                                   | 121 ms: 1.08x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.15 ms: 1.75x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 176 us: 1.50x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 120 us: 1.49x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 34.3 ms: 1.25x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 87.3 ms: 1.09x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 50.1 ms: 1.07x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.73 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.3 ms: 1.01x slower                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.78 us: 1.02x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.78 us: 1.08x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.5 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.13x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 19.0 ms: 1.01x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 16.3 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.16 ms: 1.41x faster                                                       |
| django_template | 29.2 ms                                                                  | 20.9 ms: 1.39x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.0 ms: 1.32x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 30.8 ms: 1.26x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.35x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.99 ms: 2.09x faster                                                       |
| go                      | 143 ms                                                                   | 80.6 ms: 1.78x faster                                                       |
| richards                | 41.0 ms                                                                  | 23.1 ms: 1.78x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.15 ms: 1.75x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 55.7 ns: 1.70x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 61.9 ms: 1.67x faster                                                       |
| raytrace                | 267 ms                                                                   | 171 ms: 1.56x faster                                                        |
| mypy2                   | 337 ms                                                                   | 216 ms: 1.56x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 37.0 ms: 1.51x faster                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 26.2 ns: 1.50x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 176 us: 1.50x faster                                                        |
| pyflate                 | 388 ms                                                                   | 260 ms: 1.50x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 120 us: 1.49x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 56.7 ms: 1.48x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.76 ms: 1.45x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.16 ms: 1.41x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 41.6 ms: 1.41x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.05 ms: 1.40x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.9 ms: 1.39x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 874 us: 1.39x faster                                                        |
| thrift                  | 632 us                                                                   | 460 us: 1.37x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 20.8 us: 1.37x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 45.0 ms: 1.37x faster                                                       |
| pycparser               | 873 ms                                                                   | 641 ms: 1.36x faster                                                        |
| asyncio_tcp             | 664 ms                                                                   | 489 ms: 1.36x faster                                                        |
| html5lib                | 47.3 ms                                                                  | 35.1 ms: 1.35x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 12.0 us: 1.34x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 768 ms: 1.33x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 14.0 ms: 1.32x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 315 ms: 1.32x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 935 ms: 1.31x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.43 ms: 1.30x faster                                                       |
| regex_compile           | 103 ms                                                                   | 79.7 ms: 1.30x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 378 ms: 1.28x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 465 ms: 1.28x faster                                                        |
| genshi_xml              | 38.8 ms                                                                  | 30.8 ms: 1.26x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 34.3 ms: 1.25x faster                                                       |
| float                   | 59.5 ms                                                                  | 48.2 ms: 1.23x faster                                                       |
| deepcopy                | 256 us                                                                   | 208 us: 1.23x faster                                                        |
| spectral_norm           | 74.3 ms                                                                  | 60.8 ms: 1.22x faster                                                       |
| async_generators        | 214 ms                                                                   | 176 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 498 ms: 1.21x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.0 ms: 1.21x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.53 sec: 1.20x faster                                                      |
| sympy_str               | 189 ms                                                                   | 159 ms: 1.19x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 170 ms: 1.19x faster                                                        |
| dask                    | 310 ms                                                                   | 263 ms: 1.18x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.70 ms: 1.18x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.27 ms: 1.17x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.87 us: 1.17x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 40.3 ms: 1.16x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.6 ms: 1.16x faster                                                       |
| tornado_http            | 106 ms                                                                   | 91.6 ms: 1.16x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 61.8 ms: 1.16x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 271 ms: 1.15x faster                                                        |
| 2to3                    | 229 ms                                                                   | 199 ms: 1.15x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 56.4 ms: 1.15x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 833 us: 1.14x faster                                                        |
| sympy_sum               | 102 ms                                                                   | 90.8 ms: 1.13x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 167 ms: 1.12x faster                                                        |
| json_loads              | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 695 us: 1.10x faster                                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 87.3 ms: 1.09x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.70 us: 1.09x faster                                                       |
| regex_dna               | 131 ms                                                                   | 121 ms: 1.08x faster                                                        |
| xml_etree_generate      | 53.8 ms                                                                  | 50.1 ms: 1.07x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 69.6 ms: 1.07x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.52 sec: 1.06x faster                                                      |
| coroutines              | 15.6 ms                                                                  | 14.8 ms: 1.06x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.62 ms: 1.04x faster                                                       |
| fannkuch                | 252 ms                                                                   | 242 ms: 1.04x faster                                                        |
| pathlib                 | 75.2 ms                                                                  | 74.2 ms: 1.01x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 19.0 ms: 1.01x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.73 us: 1.01x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.3 ms: 1.01x slower                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.78 us: 1.02x slower                                                       |
| pidigits                | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| bench_mp_pool           | 59.2 ms                                                                  | 63.3 ms: 1.07x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.78 us: 1.08x slower                                                       |
| generators              | 31.4 ms                                                                  | 34.4 ms: 1.09x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 16.3 ms: 1.10x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.47 ms: 1.10x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.5 us: 1.11x slower                                                       |
| coverage                | 37.5 ms                                                                  | 54.1 ms: 1.44x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.21x faster                                                                |

Benchmark hidden because not significant (3): logging_format, logging_simple, unpickle
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
