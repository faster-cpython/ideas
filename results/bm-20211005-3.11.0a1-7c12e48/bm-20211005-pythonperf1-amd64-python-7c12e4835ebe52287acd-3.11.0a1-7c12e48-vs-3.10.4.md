
# Results vs. 3.10.4

- fork: python
- ref: 7c12e4835ebe52287acd
- machine: windows-amd64
- commit hash: 7c12e48
- commit date: 2021-10-05
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 222 ms: 1.03x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 5.68 ms: 1.02x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.73 sec: 1.06x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 41.5 ms: 1.14x faster                                                      |
| tornado_http   | 106 ms                                                                   | 97.6 ms: 1.09x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 57.2 ms: 1.04x faster                                                      |
| pidigits       | 145 ms                                                                   | 150 ms: 1.04x slower                                                       |
| nbody          | 71.5 ms                                                                  | 86.8 ms: 1.21x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.07x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 92.3 ms: 1.12x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 14.4 ms: 1.05x faster                                                      |
| regex_dna      | 131 ms                                                                   | 129 ms: 1.02x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.66 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 8.03 ms: 1.12x faster                                                      |
| pickle_pure_python   | 264 us                                                                   | 240 us: 1.10x faster                                                       |
| xml_etree_process    | 43.0 ms                                                                  | 40.3 ms: 1.07x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.56 us: 1.06x faster                                                      |
| unpickle             | 8.88 us                                                                  | 8.48 us: 1.05x faster                                                      |
| unpickle_pure_python | 179 us                                                                   | 172 us: 1.04x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.58 us: 1.01x faster                                                      |
| pickle_dict          | 16.7 us                                                                  | 16.8 us: 1.00x slower                                                      |
| json_loads           | 14.2 us                                                                  | 14.4 us: 1.02x slower                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 54.8 ms: 1.02x slower                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 98.4 ms: 1.03x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.66 us: 1.04x slower                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 65.6 ms: 1.05x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.02x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 14.8 ms                                                                  | 15.6 ms: 1.05x slower                                                      |
| python_startup         | 19.3 ms                                                                  | 20.7 ms: 1.07x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.06x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 25.8 ms: 1.13x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 17.3 ms: 1.07x faster                                                      |
| mako            | 8.69 ms                                                                  | 8.12 ms: 1.07x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 37.8 ms: 1.03x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.07x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 414 ms                                                                   | 296 ms: 1.40x faster                                                       |
| deltablue               | 4.15 ms                                                                  | 3.12 ms: 1.33x faster                                                      |
| go                      | 143 ms                                                                   | 108 ms: 1.33x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 777 ms: 1.32x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 384 ms: 1.26x faster                                                       |
| raytrace                | 267 ms                                                                   | 224 ms: 1.19x faster                                                       |
| richards                | 41.0 ms                                                                  | 34.7 ms: 1.18x faster                                                      |
| thrift                  | 632 us                                                                   | 535 us: 1.18x faster                                                       |
| logging_simple          | 6.12 us                                                                  | 5.24 us: 1.17x faster                                                      |
| logging_format          | 6.53 us                                                                  | 5.64 us: 1.16x faster                                                      |
| html5lib                | 47.3 ms                                                                  | 41.5 ms: 1.14x faster                                                      |
| logging_silent          | 94.6 ns                                                                  | 83.4 ns: 1.13x faster                                                      |
| django_template         | 29.2 ms                                                                  | 25.8 ms: 1.13x faster                                                      |
| pycparser               | 873 ms                                                                   | 777 ms: 1.12x faster                                                       |
| regex_compile           | 103 ms                                                                   | 92.3 ms: 1.12x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 8.03 ms: 1.12x faster                                                      |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 86.3 ms: 1.12x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 541 ms: 1.12x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 240 us: 1.10x faster                                                       |
| tornado_http            | 106 ms                                                                   | 97.6 ms: 1.09x faster                                                      |
| generators              | 31.4 ms                                                                  | 28.9 ms: 1.09x faster                                                      |
| async_generators        | 214 ms                                                                   | 198 ms: 1.08x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 17.3 ms: 1.07x faster                                                      |
| mako                    | 8.69 ms                                                                  | 8.12 ms: 1.07x faster                                                      |
| xml_etree_process       | 43.0 ms                                                                  | 40.3 ms: 1.07x faster                                                      |
| scimark_monte_carlo     | 56.0 ms                                                                  | 52.6 ms: 1.07x faster                                                      |
| crypto_pyaes            | 61.4 ms                                                                  | 57.7 ms: 1.06x faster                                                      |
| pyflate                 | 388 ms                                                                   | 365 ms: 1.06x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 55.0 ms: 1.06x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.73 sec: 1.06x faster                                                     |
| pylint                  | 337 ms                                                                   | 318 ms: 1.06x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.56 us: 1.06x faster                                                      |
| pprint_pformat          | 1.23 sec                                                                 | 1.16 sec: 1.06x faster                                                     |
| asyncio_tcp             | 664 ms                                                                   | 628 ms: 1.06x faster                                                       |
| json                    | 3.18 ms                                                                  | 3.01 ms: 1.06x faster                                                      |
| hexiom                  | 5.45 ms                                                                  | 5.17 ms: 1.06x faster                                                      |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 10.7 ms: 1.06x faster                                                      |
| dask                    | 310 ms                                                                   | 295 ms: 1.05x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 14.4 ms: 1.05x faster                                                      |
| unpickle                | 8.88 us                                                                  | 8.48 us: 1.05x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 172 us: 1.04x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 570 ms: 1.04x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 915 us: 1.04x faster                                                       |
| float                   | 59.5 ms                                                                  | 57.2 ms: 1.04x faster                                                      |
| 2to3                    | 229 ms                                                                   | 222 ms: 1.03x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 37.8 ms: 1.03x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.80 us: 1.02x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 73.4 ms: 1.02x faster                                                      |
| sqlglot_optimize        | 38.7 ms                                                                  | 37.8 ms: 1.02x faster                                                      |
| sympy_integrate         | 14.7 ms                                                                  | 14.4 ms: 1.02x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 46.1 ms: 1.02x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 100 ms: 1.02x faster                                                       |
| regex_dna               | 131 ms                                                                   | 129 ms: 1.02x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 5.68 ms: 1.02x faster                                                      |
| mdp                     | 1.60 sec                                                                 | 1.58 sec: 1.02x faster                                                     |
| pickle                  | 6.67 us                                                                  | 6.58 us: 1.01x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 309 ms: 1.01x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 2.16 us: 1.01x faster                                                      |
| sympy_str               | 189 ms                                                                   | 188 ms: 1.00x faster                                                       |
| pickle_dict             | 16.7 us                                                                  | 16.8 us: 1.00x slower                                                      |
| deepcopy_memo           | 28.4 us                                                                  | 28.6 us: 1.01x slower                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.66 ms: 1.01x slower                                                      |
| meteor_contest          | 74.3 ms                                                                  | 75.3 ms: 1.01x slower                                                      |
| scimark_sor             | 104 ms                                                                   | 105 ms: 1.02x slower                                                       |
| json_loads              | 14.2 us                                                                  | 14.4 us: 1.02x slower                                                      |
| xml_etree_generate      | 53.8 ms                                                                  | 54.8 ms: 1.02x slower                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 98.4 ms: 1.03x slower                                                      |
| gc_traversal            | 1.33 ms                                                                  | 1.37 ms: 1.03x slower                                                      |
| pidigits                | 145 ms                                                                   | 150 ms: 1.04x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.66 us: 1.04x slower                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.53 ms: 1.04x slower                                                      |
| nqueens                 | 64.8 ms                                                                  | 67.7 ms: 1.04x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.6 ms: 1.05x slower                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 65.6 ms: 1.05x slower                                                      |
| telco                   | 3.77 ms                                                                  | 3.98 ms: 1.05x slower                                                      |
| create_gc_cycles        | 764 us                                                                   | 807 us: 1.06x slower                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 41.7 ns: 1.06x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 63.0 ms: 1.06x slower                                                      |
| python_startup          | 19.3 ms                                                                  | 20.7 ms: 1.07x slower                                                      |
| sqlglot_parse           | 1.22 ms                                                                  | 1.32 ms: 1.08x slower                                                      |
| fannkuch                | 252 ms                                                                   | 279 ms: 1.11x slower                                                       |
| spectral_norm           | 74.3 ms                                                                  | 84.7 ms: 1.14x slower                                                      |
| coroutines              | 15.6 ms                                                                  | 17.9 ms: 1.15x slower                                                      |
| scimark_fft             | 187 ms                                                                   | 216 ms: 1.15x slower                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 3.18 ms: 1.19x slower                                                      |
| comprehensions          | 16.0 us                                                                  | 19.1 us: 1.20x slower                                                      |
| nbody                   | 71.5 ms                                                                  | 86.8 ms: 1.21x slower                                                      |
| coverage                | 37.5 ms                                                                  | 261 ms: 6.98x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (4): scimark_lu, flaskblogging, sqlglot_normalize, deepcopy
Ignored benchmarks (2) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, mypy2
