
# Results vs. 3.10.4

- fork: python
- ref: f9774e57d84162ff0cba
- machine: windows-amd64
- commit hash: f9774e5
- commit date: 2023-03-07
- overall geometric mean: 1.20x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 194 ms: 1.18x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 4.76 ms: 1.21x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.51 sec: 1.21x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 34.8 ms: 1.36x faster                                                      |
| tornado_http   | 106 ms                                                                   | 90.6 ms: 1.17x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 47.4 ms: 1.26x faster                                                      |
| nbody          | 71.5 ms                                                                  | 63.3 ms: 1.13x faster                                                      |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 83.5 ms: 1.24x faster                                                      |
| regex_dna      | 131 ms                                                                   | 115 ms: 1.14x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.4 ms: 1.13x faster                                                      |
| regex_effbot   | 1.64 ms                                                                  | 1.50 ms: 1.10x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.51 ms: 1.63x faster                                                      |
| pickle_pure_python   | 264 us                                                                   | 175 us: 1.51x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 124 us: 1.45x faster                                                       |
| xml_etree_process    | 43.0 ms                                                                  | 35.6 ms: 1.21x faster                                                      |
| unpickle             | 8.88 us                                                                  | 7.98 us: 1.11x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 88.4 ms: 1.08x faster                                                      |
| json_loads           | 14.2 us                                                                  | 13.4 us: 1.06x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 52.1 ms: 1.03x faster                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.96 us: 1.04x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.80 us: 1.09x slower                                                      |
| pickle_dict          | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                               |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.5 ms: 1.04x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.20 ms: 1.40x faster                                                      |
| django_template | 29.2 ms                                                                  | 20.9 ms: 1.40x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 13.9 ms: 1.33x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 30.9 ms: 1.26x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.35x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.92 ms: 2.16x faster                                                      |
| go                      | 143 ms                                                                   | 82.6 ms: 1.74x faster                                                      |
| richards                | 41.0 ms                                                                  | 24.5 ms: 1.68x faster                                                      |
| logging_silent          | 94.6 ns                                                                  | 56.5 ns: 1.67x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 5.51 ms: 1.63x faster                                                      |
| mypy2                   | 337 ms                                                                   | 211 ms: 1.60x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 175 us: 1.51x faster                                                       |
| raytrace                | 267 ms                                                                   | 180 ms: 1.48x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 124 us: 1.45x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 71.6 ms: 1.45x faster                                                      |
| pyflate                 | 388 ms                                                                   | 270 ms: 1.44x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 463 ms: 1.43x faster                                                       |
| generators              | 31.4 ms                                                                  | 21.9 ms: 1.43x faster                                                      |
| scimark_lu              | 83.9 ms                                                                  | 58.7 ms: 1.43x faster                                                      |
| hexiom                  | 5.45 ms                                                                  | 3.83 ms: 1.42x faster                                                      |
| crypto_pyaes            | 61.4 ms                                                                  | 43.3 ms: 1.42x faster                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 27.9 ns: 1.41x faster                                                      |
| mako                    | 8.69 ms                                                                  | 6.20 ms: 1.40x faster                                                      |
| sqlglot_parse           | 1.22 ms                                                                  | 871 us: 1.40x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.9 ms: 1.40x faster                                                      |
| chaos                   | 58.4 ms                                                                  | 42.0 ms: 1.39x faster                                                      |
| scimark_monte_carlo     | 56.0 ms                                                                  | 40.4 ms: 1.39x faster                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.06 ms: 1.39x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 744 ms: 1.38x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 356 ms: 1.36x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 304 ms: 1.36x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 34.8 ms: 1.36x faster                                                      |
| genshi_text             | 18.5 ms                                                                  | 13.9 ms: 1.33x faster                                                      |
| thrift                  | 632 us                                                                   | 476 us: 1.33x faster                                                       |
| pycparser               | 873 ms                                                                   | 663 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 479 ms: 1.26x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 22.6 us: 1.26x faster                                                      |
| pprint_pformat          | 1.23 sec                                                                 | 977 ms: 1.26x faster                                                       |
| float                   | 59.5 ms                                                                  | 47.4 ms: 1.26x faster                                                      |
| genshi_xml              | 38.8 ms                                                                  | 30.9 ms: 1.26x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 478 ms: 1.24x faster                                                       |
| regex_compile           | 103 ms                                                                   | 83.5 ms: 1.24x faster                                                      |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.2 ms: 1.24x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.51 sec: 1.21x faster                                                     |
| chameleon               | 5.77 ms                                                                  | 4.76 ms: 1.21x faster                                                      |
| xml_etree_process       | 43.0 ms                                                                  | 35.6 ms: 1.21x faster                                                      |
| sqlglot_normalize       | 201 ms                                                                   | 168 ms: 1.20x faster                                                       |
| 2to3                    | 229 ms                                                                   | 194 ms: 1.18x faster                                                       |
| tornado_http            | 106 ms                                                                   | 90.6 ms: 1.17x faster                                                      |
| deepcopy                | 256 us                                                                   | 219 us: 1.17x faster                                                       |
| fannkuch                | 252 ms                                                                   | 216 ms: 1.17x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.74 ms: 1.16x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.88 us: 1.16x faster                                                      |
| bench_thread_pool       | 953 us                                                                   | 827 us: 1.15x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 671 us: 1.14x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 56.9 ms: 1.14x faster                                                      |
| regex_dna               | 131 ms                                                                   | 115 ms: 1.14x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 13.4 ms: 1.13x faster                                                      |
| nbody                   | 71.5 ms                                                                  | 63.3 ms: 1.13x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 277 ms: 1.13x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.1 ms: 1.12x faster                                                      |
| mdp                     | 1.60 sec                                                                 | 1.43 sec: 1.12x faster                                                     |
| coroutines              | 15.6 ms                                                                  | 14.0 ms: 1.12x faster                                                      |
| unpickle                | 8.88 us                                                                  | 7.98 us: 1.11x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 42.2 ms: 1.11x faster                                                      |
| scimark_fft             | 187 ms                                                                   | 169 ms: 1.11x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 67.2 ms: 1.10x faster                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.50 ms: 1.10x faster                                                      |
| sympy_str               | 189 ms                                                                   | 173 ms: 1.09x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 68.0 ms: 1.09x faster                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 88.4 ms: 1.08x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 96.6 ms: 1.06x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| json_loads              | 14.2 us                                                                  | 13.4 us: 1.06x faster                                                      |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.56 ms: 1.04x faster                                                      |
| xml_etree_generate      | 53.8 ms                                                                  | 52.1 ms: 1.03x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.79 us: 1.03x faster                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 73.9 ms: 1.02x faster                                                      |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.86 ms: 1.02x slower                                                      |
| async_generators        | 214 ms                                                                   | 223 ms: 1.04x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.5 ms: 1.04x slower                                                      |
| pickle                  | 6.67 us                                                                  | 6.96 us: 1.04x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 63.1 ms: 1.07x slower                                                      |
| gc_traversal            | 1.33 ms                                                                  | 1.44 ms: 1.08x slower                                                      |
| pickle_list             | 2.57 us                                                                  | 2.80 us: 1.09x slower                                                      |
| pickle_dict             | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                      |
| dask                    | 310 ms                                                                   | 352 ms: 1.13x slower                                                       |
| coverage                | 37.5 ms                                                                  | 49.9 ms: 1.33x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.20x faster                                                               |

Benchmark hidden because not significant (4): comprehensions, logging_simple, logging_format, unpickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
