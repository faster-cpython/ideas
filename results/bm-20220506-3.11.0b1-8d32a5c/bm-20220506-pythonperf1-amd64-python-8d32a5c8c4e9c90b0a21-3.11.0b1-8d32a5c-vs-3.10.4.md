
# Results vs. 3.10.4

- fork: python
- ref: 8d32a5c8c4e9c90b0a21
- machine: windows-amd64
- commit hash: 8d32a5c
- commit date: 2022-05-06
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 203 ms: 1.13x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 5.45 ms: 1.06x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.57 sec: 1.17x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 38.3 ms: 1.24x faster                                                      |
| tornado_http   | 106 ms                                                                   | 89.7 ms: 1.19x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 53.5 ms: 1.11x faster                                                      |
| nbody          | 71.5 ms                                                                  | 67.9 ms: 1.05x faster                                                      |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 90.5 ms: 1.14x faster                                                      |
| regex_effbot   | 1.64 ms                                                                  | 1.47 ms: 1.12x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 13.9 ms: 1.08x faster                                                      |
| regex_dna      | 131 ms                                                                   | 121 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 264 us                                                                   | 204 us: 1.30x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 152 us: 1.18x faster                                                       |
| json_dumps           | 9.00 ms                                                                  | 7.72 ms: 1.17x faster                                                      |
| xml_etree_process    | 43.0 ms                                                                  | 37.6 ms: 1.15x faster                                                      |
| unpickle             | 8.88 us                                                                  | 7.87 us: 1.13x faster                                                      |
| json_loads           | 14.2 us                                                                  | 13.4 us: 1.06x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.58 us: 1.05x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 93.1 ms: 1.03x faster                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.1 ms: 1.02x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 53.0 ms: 1.02x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.59 us: 1.01x faster                                                      |
| pickle_dict          | 16.7 us                                                                  | 17.1 us: 1.02x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.67 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.08x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.2 ms: 1.03x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 7.13 ms: 1.22x faster                                                      |
| django_template | 29.2 ms                                                                  | 24.0 ms: 1.22x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 17.7 ms: 1.05x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 39.8 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                                    | 1.11x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.66 ms: 1.56x faster                                                      |
| go                      | 143 ms                                                                   | 97.9 ms: 1.46x faster                                                      |
| richards                | 41.0 ms                                                                  | 30.1 ms: 1.36x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 751 ms: 1.36x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 70.2 ns: 1.35x faster                                                      |
| scimark_sor             | 104 ms                                                                   | 77.1 ms: 1.34x faster                                                      |
| scimark_lu              | 83.9 ms                                                                  | 62.7 ms: 1.34x faster                                                      |
| async_tree_none         | 414 ms                                                                   | 311 ms: 1.33x faster                                                       |
| raytrace                | 267 ms                                                                   | 203 ms: 1.31x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 370 ms: 1.31x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 204 us: 1.30x faster                                                       |
| pyflate                 | 388 ms                                                                   | 303 ms: 1.28x faster                                                       |
| thrift                  | 632 us                                                                   | 504 us: 1.25x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 49.1 ms: 1.25x faster                                                      |
| scimark_monte_carlo     | 56.0 ms                                                                  | 45.0 ms: 1.24x faster                                                      |
| html5lib                | 47.3 ms                                                                  | 38.3 ms: 1.24x faster                                                      |
| mypy2                   | 337 ms                                                                   | 277 ms: 1.22x faster                                                       |
| mako                    | 8.69 ms                                                                  | 7.13 ms: 1.22x faster                                                      |
| django_template         | 29.2 ms                                                                  | 24.0 ms: 1.22x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 499 ms: 1.21x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 48.9 ms: 1.19x faster                                                      |
| hexiom                  | 5.45 ms                                                                  | 4.59 ms: 1.19x faster                                                      |
| tornado_http            | 106 ms                                                                   | 89.7 ms: 1.19x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 152 us: 1.18x faster                                                       |
| async_generators        | 214 ms                                                                   | 182 ms: 1.17x faster                                                       |
| pycparser               | 873 ms                                                                   | 748 ms: 1.17x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.57 sec: 1.17x faster                                                     |
| json_dumps              | 9.00 ms                                                                  | 7.72 ms: 1.17x faster                                                      |
| dask                    | 310 ms                                                                   | 268 ms: 1.16x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 663 us: 1.15x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 37.6 ms: 1.15x faster                                                      |
| regex_compile           | 103 ms                                                                   | 90.5 ms: 1.14x faster                                                      |
| pprint_pformat          | 1.23 sec                                                                 | 1.08 sec: 1.14x faster                                                     |
| aiohttp                 | 968 us                                                                   | 854 us: 1.13x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 25.1 us: 1.13x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 525 ms: 1.13x faster                                                       |
| unpickle                | 8.88 us                                                                  | 7.87 us: 1.13x faster                                                      |
| 2to3                    | 229 ms                                                                   | 203 ms: 1.13x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.47 ms: 1.12x faster                                                      |
| float                   | 59.5 ms                                                                  | 53.5 ms: 1.11x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 42.5 ms: 1.10x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.69 us: 1.09x faster                                                      |
| sqlglot_optimize        | 38.7 ms                                                                  | 35.6 ms: 1.09x faster                                                      |
| regex_v8                | 15.1 ms                                                                  | 13.9 ms: 1.08x faster                                                      |
| regex_dna               | 131 ms                                                                   | 121 ms: 1.08x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.6 ms: 1.08x faster                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.37 ms: 1.08x faster                                                      |
| pylint                  | 337 ms                                                                   | 314 ms: 1.07x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 888 us: 1.07x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 69.6 ms: 1.07x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 293 ms: 1.07x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 5.45 ms: 1.06x faster                                                      |
| json_loads              | 14.2 us                                                                  | 13.4 us: 1.06x faster                                                      |
| sqlglot_parse           | 1.22 ms                                                                  | 1.15 ms: 1.06x faster                                                      |
| logging_simple          | 6.12 us                                                                  | 5.80 us: 1.06x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 96.9 ms: 1.06x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 71.4 ms: 1.05x faster                                                      |
| unpickle_list           | 2.71 us                                                                  | 2.58 us: 1.05x faster                                                      |
| nbody                   | 71.5 ms                                                                  | 67.9 ms: 1.05x faster                                                      |
| genshi_text             | 18.5 ms                                                                  | 17.7 ms: 1.05x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                      |
| logging_format          | 6.53 us                                                                  | 6.25 us: 1.04x faster                                                      |
| scimark_fft             | 187 ms                                                                   | 180 ms: 1.04x faster                                                       |
| sympy_str               | 189 ms                                                                   | 183 ms: 1.03x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 2.12 us: 1.03x faster                                                      |
| coroutines              | 15.6 ms                                                                  | 15.2 ms: 1.03x faster                                                      |
| sqlglot_normalize       | 201 ms                                                                   | 196 ms: 1.03x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.60 ms: 1.03x faster                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 93.1 ms: 1.03x faster                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.1 ms: 1.02x faster                                                      |
| xml_etree_generate      | 53.8 ms                                                                  | 53.0 ms: 1.02x faster                                                      |
| deepcopy                | 256 us                                                                   | 252 us: 1.01x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.59 us: 1.01x faster                                                      |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                       |
| meteor_contest          | 74.3 ms                                                                  | 75.5 ms: 1.02x slower                                                      |
| mdp                     | 1.60 sec                                                                 | 1.63 sec: 1.02x slower                                                     |
| pickle_dict             | 16.7 us                                                                  | 17.1 us: 1.02x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 60.6 ms: 1.02x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.2 ms: 1.03x slower                                                      |
| genshi_xml              | 38.8 ms                                                                  | 39.8 ms: 1.03x slower                                                      |
| pickle_list             | 2.57 us                                                                  | 2.67 us: 1.04x slower                                                      |
| nqueens                 | 64.8 ms                                                                  | 67.6 ms: 1.04x slower                                                      |
| telco                   | 3.77 ms                                                                  | 3.94 ms: 1.05x slower                                                      |
| gc_traversal            | 1.33 ms                                                                  | 1.42 ms: 1.07x slower                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 42.2 ns: 1.07x slower                                                      |
| generators              | 31.4 ms                                                                  | 33.9 ms: 1.08x slower                                                      |
| comprehensions          | 16.0 us                                                                  | 17.8 us: 1.11x slower                                                      |
| coverage                | 37.5 ms                                                                  | 103 ms: 2.74x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                               |

Benchmark hidden because not significant (4): flaskblogging, fannkuch, asyncio_tcp, json
Ignored benchmarks (2) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: sqlalchemy_declarative, sqlalchemy_imperative
