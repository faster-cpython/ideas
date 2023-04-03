
# Results vs. 3.10.4

- fork: python
- ref: 010576c6ea7e687cf2cb
- machine: windows-amd64
- commit hash: 010576c
- commit date: 2023-01-13
- overall geometric mean: 1.20x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 202 ms: 1.14x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.60 ms: 1.26x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.52 sec: 1.20x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 33.5 ms: 1.41x faster                                                       |
| tornado_http   | 106 ms                                                                   | 91.2 ms: 1.17x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 49.3 ms: 1.21x faster                                                       |
| nbody          | 71.5 ms                                                                  | 61.2 ms: 1.17x faster                                                       |
| pidigits       | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 80.4 ms: 1.29x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 14.0 ms: 1.08x faster                                                       |
| regex_dna      | 131 ms                                                                   | 122 ms: 1.07x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.60 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.26 ms: 1.71x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 176 us: 1.50x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 122 us: 1.47x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 34.1 ms: 1.26x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 49.5 ms: 1.09x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 90.3 ms: 1.06x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.48 us: 1.05x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.65 us: 1.02x faster                                                       |
| json_loads           | 14.2 us                                                                  | 14.4 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 64.0 ms: 1.02x slower                                                       |
| pickle               | 6.67 us                                                                  | 7.18 us: 1.08x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.79 us: 1.09x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.3 us: 1.15x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.6 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.07 ms: 1.43x faster                                                       |
| django_template | 29.2 ms                                                                  | 20.7 ms: 1.41x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.8 ms: 1.34x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 30.8 ms: 1.26x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.36x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.96 ms: 2.12x faster                                                       |
| go                      | 143 ms                                                                   | 83.6 ms: 1.71x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.26 ms: 1.71x faster                                                       |
| richards                | 41.0 ms                                                                  | 24.1 ms: 1.70x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 56.7 ns: 1.67x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 66.0 ms: 1.57x faster                                                       |
| mypy2                   | 337 ms                                                                   | 219 ms: 1.54x faster                                                        |
| raytrace                | 267 ms                                                                   | 177 ms: 1.51x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 176 us: 1.50x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 26.4 ns: 1.49x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 122 us: 1.47x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 57.3 ms: 1.46x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.73 ms: 1.46x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.0 ms: 1.44x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.07 ms: 1.43x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 33.5 ms: 1.41x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.7 ms: 1.41x faster                                                       |
| pyflate                 | 388 ms                                                                   | 276 ms: 1.41x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 874 us: 1.39x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.06 ms: 1.39x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 20.7 us: 1.37x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 484 ms: 1.37x faster                                                        |
| pycparser               | 873 ms                                                                   | 640 ms: 1.37x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 13.8 ms: 1.34x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 363 ms: 1.34x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 46.0 ms: 1.34x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 43.8 ms: 1.34x faster                                                       |
| thrift                  | 632 us                                                                   | 475 us: 1.33x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 781 ms: 1.31x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 320 ms: 1.29x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 459 ms: 1.29x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 952 ms: 1.29x faster                                                        |
| regex_compile           | 103 ms                                                                   | 80.4 ms: 1.29x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 34.1 ms: 1.26x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 30.8 ms: 1.26x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.60 ms: 1.26x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 30.9 ms: 1.25x faster                                                       |
| deepcopy                | 256 us                                                                   | 206 us: 1.25x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 487 ms: 1.24x faster                                                        |
| async_generators        | 214 ms                                                                   | 175 ms: 1.22x faster                                                        |
| spectral_norm           | 74.3 ms                                                                  | 61.2 ms: 1.21x faster                                                       |
| float                   | 59.5 ms                                                                  | 49.3 ms: 1.21x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.52 sec: 1.20x faster                                                      |
| dask                    | 310 ms                                                                   | 260 ms: 1.19x faster                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.26 ms: 1.18x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.86 us: 1.18x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 61.2 ms: 1.17x faster                                                       |
| tornado_http            | 106 ms                                                                   | 91.2 ms: 1.17x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 173 ms: 1.16x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 56.6 ms: 1.15x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 669 us: 1.14x faster                                                        |
| 2to3                    | 229 ms                                                                   | 202 ms: 1.14x faster                                                        |
| sympy_expand            | 313 ms                                                                   | 276 ms: 1.13x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 12.9 ms: 1.13x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 841 us: 1.13x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.81 ms: 1.13x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.9 ms: 1.12x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 169 ms: 1.11x faster                                                        |
| fannkuch                | 252 ms                                                                   | 228 ms: 1.10x faster                                                        |
| sympy_str               | 189 ms                                                                   | 173 ms: 1.09x faster                                                        |
| coroutines              | 15.6 ms                                                                  | 14.3 ms: 1.09x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 49.5 ms: 1.09x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 94.9 ms: 1.08x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 14.0 ms: 1.08x faster                                                       |
| regex_dna               | 131 ms                                                                   | 122 ms: 1.07x faster                                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 90.3 ms: 1.06x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.48 us: 1.05x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.3 us: 1.04x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 71.9 ms: 1.03x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.6 ms: 1.03x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.56 sec: 1.03x faster                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.60 ms: 1.03x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.80 us: 1.03x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.65 us: 1.02x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.38 us: 1.02x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.69 ms: 1.02x faster                                                       |
| json_loads              | 14.2 us                                                                  | 14.4 us: 1.01x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 64.0 ms: 1.02x slower                                                       |
| pidigits                | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| python_startup_no_site  | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 62.7 ms: 1.06x slower                                                       |
| pickle                  | 6.67 us                                                                  | 7.18 us: 1.08x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.79 us: 1.09x slower                                                       |
| generators              | 31.4 ms                                                                  | 34.6 ms: 1.10x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.51 ms: 1.13x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 19.3 us: 1.15x slower                                                       |
| coverage                | 37.5 ms                                                                  | 53.2 ms: 1.42x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.20x faster                                                                |

Benchmark hidden because not significant (2): pathlib, logging_simple
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
