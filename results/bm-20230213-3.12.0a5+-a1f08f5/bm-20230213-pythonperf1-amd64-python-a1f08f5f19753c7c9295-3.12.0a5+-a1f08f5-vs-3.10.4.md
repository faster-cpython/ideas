
# Results vs. 3.10.4

- fork: python
- ref: a1f08f5f19753c7c9295
- machine: windows-amd64
- commit hash: a1f08f5
- commit date: 2023-02-13
- overall geometric mean: 1.21x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 201 ms: 1.14x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.43 ms: 1.30x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.57 sec: 1.16x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 34.9 ms: 1.36x faster                                                       |
| tornado_http   | 106 ms                                                                   | 90.3 ms: 1.18x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 49.6 ms: 1.20x faster                                                       |
| nbody          | 71.5 ms                                                                  | 62.7 ms: 1.14x faster                                                       |
| pidigits       | 145 ms                                                                   | 150 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 78.6 ms: 1.32x faster                                                       |
| regex_dna      | 131 ms                                                                   | 124 ms: 1.06x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 14.4 ms: 1.05x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.60 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.27 ms: 1.71x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 169 us: 1.56x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 119 us: 1.51x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.9 ms: 1.20x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.06 us: 1.10x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 91.5 ms: 1.04x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.6 ms: 1.04x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.93 us: 1.04x slower                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 65.5 ms: 1.05x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.73 us: 1.06x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.3 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.13x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.8 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 5.99 ms: 1.45x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.0 ms: 1.39x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.5 ms: 1.37x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 30.5 ms: 1.27x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.37x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.96 ms: 2.12x faster                                                       |
| go                      | 143 ms                                                                   | 82.0 ms: 1.75x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 54.7 ns: 1.73x faster                                                       |
| richards                | 41.0 ms                                                                  | 23.9 ms: 1.71x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.27 ms: 1.71x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 66.1 ms: 1.57x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 169 us: 1.56x faster                                                        |
| mypy2                   | 337 ms                                                                   | 216 ms: 1.56x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 25.6 ns: 1.54x faster                                                       |
| raytrace                | 267 ms                                                                   | 174 ms: 1.53x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 119 us: 1.51x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 56.4 ms: 1.49x faster                                                       |
| pyflate                 | 388 ms                                                                   | 265 ms: 1.46x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 3.73 ms: 1.46x faster                                                       |
| mako                    | 8.69 ms                                                                  | 5.99 ms: 1.45x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.4 ms: 1.42x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 41.6 ms: 1.41x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 867 us: 1.40x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 43.9 ms: 1.40x faster                                                       |
| django_template         | 29.2 ms                                                                  | 21.0 ms: 1.39x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.07 ms: 1.38x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 13.5 ms: 1.37x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 485 ms: 1.37x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 20.9 us: 1.36x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 34.9 ms: 1.36x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 12.0 us: 1.33x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 769 ms: 1.33x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 925 ms: 1.33x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 314 ms: 1.32x faster                                                        |
| thrift                  | 632 us                                                                   | 480 us: 1.32x faster                                                        |
| regex_compile           | 103 ms                                                                   | 78.6 ms: 1.32x faster                                                       |
| pycparser               | 873 ms                                                                   | 666 ms: 1.31x faster                                                        |
| async_tree_memoization  | 485 ms                                                                   | 370 ms: 1.31x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.43 ms: 1.30x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 463 ms: 1.28x faster                                                        |
| genshi_xml              | 38.8 ms                                                                  | 30.5 ms: 1.27x faster                                                       |
| deepcopy                | 256 us                                                                   | 205 us: 1.25x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 488 ms: 1.24x faster                                                        |
| float                   | 59.5 ms                                                                  | 49.6 ms: 1.20x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 35.9 ms: 1.20x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 62.0 ms: 1.20x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.3 ms: 1.20x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.24 ms: 1.19x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.85 us: 1.18x faster                                                       |
| tornado_http            | 106 ms                                                                   | 90.3 ms: 1.18x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.6 ms: 1.17x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.57 sec: 1.16x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 270 ms: 1.16x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 56.2 ms: 1.15x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.78 ms: 1.15x faster                                                       |
| 2to3                    | 229 ms                                                                   | 201 ms: 1.14x faster                                                        |
| sympy_str               | 189 ms                                                                   | 165 ms: 1.14x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 176 ms: 1.14x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 62.7 ms: 1.14x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 843 us: 1.13x faster                                                        |
| dulwich_log             | 47.0 ms                                                                  | 41.8 ms: 1.12x faster                                                       |
| fannkuch                | 252 ms                                                                   | 226 ms: 1.11x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 168 ms: 1.11x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 693 us: 1.10x faster                                                        |
| unpickle                | 8.88 us                                                                  | 8.06 us: 1.10x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.2 ms: 1.10x faster                                                       |
| json_loads              | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 93.3 ms: 1.10x faster                                                       |
| regex_dna               | 131 ms                                                                   | 124 ms: 1.06x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 14.4 ms: 1.05x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 70.9 ms: 1.05x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 91.5 ms: 1.04x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.6 ms: 1.04x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.31 us: 1.04x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.79 us: 1.03x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.8 ms: 1.03x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.60 ms: 1.03x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.58 sec: 1.01x faster                                                      |
| logging_simple          | 6.12 us                                                                  | 6.04 us: 1.01x faster                                                       |
| pathlib                 | 75.2 ms                                                                  | 74.3 ms: 1.01x faster                                                       |
| async_generators        | 214 ms                                                                   | 216 ms: 1.01x slower                                                        |
| telco                   | 3.77 ms                                                                  | 3.82 ms: 1.01x slower                                                       |
| pidigits                | 145 ms                                                                   | 150 ms: 1.03x slower                                                        |
| pickle                  | 6.67 us                                                                  | 6.93 us: 1.04x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 65.5 ms: 1.05x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.73 us: 1.06x slower                                                       |
| generators              | 31.4 ms                                                                  | 33.7 ms: 1.07x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 64.0 ms: 1.08x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.49 ms: 1.12x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 19.3 us: 1.16x slower                                                       |
| coverage                | 37.5 ms                                                                  | 52.7 ms: 1.41x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.21x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, dask, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
