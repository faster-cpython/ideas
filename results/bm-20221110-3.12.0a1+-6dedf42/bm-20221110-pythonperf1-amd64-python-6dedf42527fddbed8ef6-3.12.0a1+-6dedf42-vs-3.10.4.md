
# Results vs. 3.10.4

- fork: python
- ref: 6dedf42527fddbed8ef6
- machine: windows-amd64
- commit hash: 6dedf42
- commit date: 2022-11-10
- overall geometric mean: 1.16x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 198 ms: 1.16x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.64 ms: 1.24x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.60 sec: 1.15x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.4 ms: 1.34x faster                                                       |
| tornado_http   | 106 ms                                                                   | 93.3 ms: 1.14x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.20x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 51.1 ms: 1.17x faster                                                       |
| nbody          | 71.5 ms                                                                  | 63.7 ms: 1.12x faster                                                       |
| pidigits       | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 85.8 ms: 1.21x faster                                                       |
| regex_dna      | 131 ms                                                                   | 124 ms: 1.06x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 14.4 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.26 ms: 1.71x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 188 us: 1.41x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 128 us: 1.40x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.4 ms: 1.21x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.11 us: 1.10x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.0 us: 1.09x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 90.3 ms: 1.06x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.3 ms: 1.05x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.59 us: 1.05x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.74 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.7 ms: 1.02x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.76 us: 1.08x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.6 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.40 ms: 1.36x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.9 ms: 1.33x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.9 ms: 1.25x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 34.0 ms: 1.14x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.27x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.31 ms: 1.80x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.26 ms: 1.71x faster                                                       |
| go                      | 143 ms                                                                   | 88.7 ms: 1.61x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 61.2 ns: 1.55x faster                                                       |
| richards                | 41.0 ms                                                                  | 27.1 ms: 1.51x faster                                                       |
| mypy2                   | 337 ms                                                                   | 223 ms: 1.51x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 70.5 ms: 1.47x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.0 ms: 1.44x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 58.4 ms: 1.44x faster                                                       |
| pyflate                 | 388 ms                                                                   | 275 ms: 1.41x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 188 us: 1.41x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 128 us: 1.40x faster                                                        |
| raytrace                | 267 ms                                                                   | 192 ms: 1.39x faster                                                        |
| mako                    | 8.69 ms                                                                  | 6.40 ms: 1.36x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 45.7 ms: 1.34x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.4 ms: 1.34x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.10 ms: 1.33x faster                                                       |
| django_template         | 29.2 ms                                                                  | 21.9 ms: 1.33x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 918 us: 1.33x faster                                                        |
| thrift                  | 632 us                                                                   | 478 us: 1.32x faster                                                        |
| pycparser               | 873 ms                                                                   | 665 ms: 1.31x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 4.17 ms: 1.31x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 319 ms: 1.30x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 790 ms: 1.30x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 45.5 ms: 1.28x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 22.6 us: 1.26x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 979 ms: 1.25x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 14.9 ms: 1.25x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 476 ms: 1.25x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.64 ms: 1.24x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 391 ms: 1.24x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 32.0 ns: 1.23x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.17 ms: 1.23x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 35.4 ms: 1.21x faster                                                       |
| regex_compile           | 103 ms                                                                   | 85.8 ms: 1.21x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 511 ms: 1.18x faster                                                        |
| dask                    | 310 ms                                                                   | 263 ms: 1.18x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.70 ms: 1.18x faster                                                       |
| async_generators        | 214 ms                                                                   | 183 ms: 1.17x faster                                                        |
| float                   | 59.5 ms                                                                  | 51.1 ms: 1.17x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 63.8 ms: 1.16x faster                                                       |
| 2to3                    | 229 ms                                                                   | 198 ms: 1.16x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 33.6 ms: 1.15x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.60 sec: 1.15x faster                                                      |
| genshi_xml              | 38.8 ms                                                                  | 34.0 ms: 1.14x faster                                                       |
| tornado_http            | 106 ms                                                                   | 93.3 ms: 1.14x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 838 us: 1.14x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 63.7 ms: 1.12x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 684 us: 1.12x faster                                                        |
| dulwich_log             | 47.0 ms                                                                  | 42.1 ms: 1.11x faster                                                       |
| deepcopy                | 256 us                                                                   | 231 us: 1.11x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 182 ms: 1.11x faster                                                        |
| fannkuch                | 252 ms                                                                   | 228 ms: 1.11x faster                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.97 us: 1.11x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.11 us: 1.10x faster                                                       |
| json_loads              | 14.2 us                                                                  | 13.0 us: 1.09x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.4 ms: 1.09x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 171 ms: 1.09x faster                                                        |
| sympy_str               | 189 ms                                                                   | 176 ms: 1.07x faster                                                        |
| sqlite_synth            | 1.85 us                                                                  | 1.72 us: 1.07x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 292 ms: 1.07x faster                                                        |
| nqueens                 | 64.8 ms                                                                  | 60.6 ms: 1.07x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 90.3 ms: 1.06x faster                                                       |
| regex_dna               | 131 ms                                                                   | 124 ms: 1.06x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 14.4 ms: 1.05x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.3 ms: 1.05x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.59 us: 1.05x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 15.0 ms: 1.04x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.6 ms: 1.03x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 99.0 ms: 1.03x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 73.7 ms: 1.02x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.70 ms: 1.02x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 73.4 ms: 1.01x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.74 us: 1.01x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.7 ms: 1.02x slower                                                       |
| comprehensions          | 16.0 us                                                                  | 16.3 us: 1.02x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.29 us: 1.03x slower                                                       |
| pidigits                | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| logging_format          | 6.53 us                                                                  | 6.81 us: 1.04x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 62.8 ms: 1.06x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.76 us: 1.08x slower                                                       |
| asyncio_tcp             | 664 ms                                                                   | 723 ms: 1.09x slower                                                        |
| gc_traversal            | 1.33 ms                                                                  | 1.47 ms: 1.11x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.9 us: 1.13x slower                                                       |
| generators              | 31.4 ms                                                                  | 37.0 ms: 1.18x slower                                                       |
| coverage                | 37.5 ms                                                                  | 54.4 ms: 1.45x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.16x faster                                                                |

Benchmark hidden because not significant (1): regex_effbot
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
