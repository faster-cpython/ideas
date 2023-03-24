
# Results vs. 3.10.4

- fork: python
- ref: 3c67ec394faac79d2608
- machine: windows-amd64
- commit hash: 3c67ec3
- commit date: 2023-02-07
- overall geometric mean: 1.22x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 192 ms: 1.20x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 4.41 ms: 1.31x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.50 sec: 1.22x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 34.1 ms: 1.39x faster                                                      |
| tornado_http   | 106 ms                                                                   | 90.5 ms: 1.18x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.26x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 47.3 ms: 1.26x faster                                                      |
| nbody          | 71.5 ms                                                                  | 59.1 ms: 1.21x faster                                                      |
| pidigits       | 145 ms                                                                   | 146 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 78.8 ms: 1.31x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 13.7 ms: 1.10x faster                                                      |
| regex_dna      | 131 ms                                                                   | 121 ms: 1.08x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.68 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.38 ms: 1.67x faster                                                      |
| pickle_pure_python   | 264 us                                                                   | 166 us: 1.59x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 120 us: 1.50x faster                                                       |
| xml_etree_process    | 43.0 ms                                                                  | 33.5 ms: 1.28x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 49.5 ms: 1.09x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 88.5 ms: 1.08x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.65 us: 1.02x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.77 us: 1.01x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.70 us: 1.05x slower                                                      |
| unpickle             | 8.88 us                                                                  | 9.39 us: 1.06x slower                                                      |
| pickle_dict          | 16.7 us                                                                  | 18.5 us: 1.11x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.13x faster                                                               |

Benchmark hidden because not significant (2): xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.5 ms: 1.04x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 20.2 ms: 1.45x faster                                                      |
| mako            | 8.69 ms                                                                  | 6.15 ms: 1.41x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 14.2 ms: 1.30x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 32.6 ms: 1.19x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.34x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.96 ms: 2.12x faster                                                      |
| go                      | 143 ms                                                                   | 78.8 ms: 1.82x faster                                                      |
| richards                | 41.0 ms                                                                  | 23.9 ms: 1.72x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 5.38 ms: 1.67x faster                                                      |
| logging_silent          | 94.6 ns                                                                  | 58.1 ns: 1.63x faster                                                      |
| mypy2                   | 337 ms                                                                   | 208 ms: 1.62x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 166 us: 1.59x faster                                                       |
| raytrace                | 267 ms                                                                   | 170 ms: 1.57x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 67.0 ms: 1.55x faster                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 25.6 ns: 1.54x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 120 us: 1.50x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 37.9 ms: 1.48x faster                                                      |
| chaos                   | 58.4 ms                                                                  | 39.6 ms: 1.48x faster                                                      |
| hexiom                  | 5.45 ms                                                                  | 3.73 ms: 1.46x faster                                                      |
| pyflate                 | 388 ms                                                                   | 267 ms: 1.45x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.2 ms: 1.45x faster                                                      |
| sqlglot_parse           | 1.22 ms                                                                  | 851 us: 1.43x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 58.7 ms: 1.43x faster                                                      |
| asyncio_tcp             | 664 ms                                                                   | 466 ms: 1.42x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.15 ms: 1.41x faster                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.05 ms: 1.40x faster                                                      |
| thrift                  | 632 us                                                                   | 452 us: 1.40x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 44.0 ms: 1.40x faster                                                      |
| html5lib                | 47.3 ms                                                                  | 34.1 ms: 1.39x faster                                                      |
| pycparser               | 873 ms                                                                   | 633 ms: 1.38x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 302 ms: 1.37x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 11.7 us: 1.37x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 748 ms: 1.37x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 356 ms: 1.36x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 907 ms: 1.35x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 21.1 us: 1.34x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 445 ms: 1.33x faster                                                       |
| regex_compile           | 103 ms                                                                   | 78.8 ms: 1.31x faster                                                      |
| chameleon               | 5.77 ms                                                                  | 4.41 ms: 1.31x faster                                                      |
| genshi_text             | 18.5 ms                                                                  | 14.2 ms: 1.30x faster                                                      |
| xml_etree_process       | 43.0 ms                                                                  | 33.5 ms: 1.28x faster                                                      |
| async_generators        | 214 ms                                                                   | 167 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 480 ms: 1.26x faster                                                       |
| float                   | 59.5 ms                                                                  | 47.3 ms: 1.26x faster                                                      |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.18 ms: 1.23x faster                                                      |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.6 ms: 1.22x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.50 sec: 1.22x faster                                                     |
| deepcopy                | 256 us                                                                   | 211 us: 1.21x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 59.1 ms: 1.21x faster                                                      |
| spectral_norm           | 74.3 ms                                                                  | 61.5 ms: 1.21x faster                                                      |
| 2to3                    | 229 ms                                                                   | 192 ms: 1.20x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 32.6 ms: 1.19x faster                                                      |
| nqueens                 | 64.8 ms                                                                  | 54.6 ms: 1.19x faster                                                      |
| sympy_integrate         | 14.7 ms                                                                  | 12.4 ms: 1.18x faster                                                      |
| fannkuch                | 252 ms                                                                   | 213 ms: 1.18x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 171 ms: 1.18x faster                                                       |
| tornado_http            | 106 ms                                                                   | 90.5 ms: 1.18x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.88 us: 1.16x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 269 ms: 1.16x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 823 us: 1.16x faster                                                       |
| sympy_str               | 189 ms                                                                   | 164 ms: 1.15x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 89.5 ms: 1.14x faster                                                      |
| create_gc_cycles        | 764 us                                                                   | 676 us: 1.13x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.81 ms: 1.13x faster                                                      |
| scimark_fft             | 187 ms                                                                   | 166 ms: 1.13x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.9 ms: 1.12x faster                                                      |
| regex_v8                | 15.1 ms                                                                  | 13.7 ms: 1.10x faster                                                      |
| xml_etree_generate      | 53.8 ms                                                                  | 49.5 ms: 1.09x faster                                                      |
| mdp                     | 1.60 sec                                                                 | 1.48 sec: 1.08x faster                                                     |
| regex_dna               | 131 ms                                                                   | 121 ms: 1.08x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 88.5 ms: 1.08x faster                                                      |
| meteor_contest          | 74.3 ms                                                                  | 69.1 ms: 1.07x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| coroutines              | 15.6 ms                                                                  | 14.8 ms: 1.06x faster                                                      |
| logging_format          | 6.53 us                                                                  | 6.28 us: 1.04x faster                                                      |
| unpickle_list           | 2.71 us                                                                  | 2.65 us: 1.02x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 73.7 ms: 1.02x faster                                                      |
| logging_simple          | 6.12 us                                                                  | 6.01 us: 1.02x faster                                                      |
| telco                   | 3.77 ms                                                                  | 3.72 ms: 1.01x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.82 us: 1.01x faster                                                      |
| pidigits                | 145 ms                                                                   | 146 ms: 1.01x slower                                                       |
| pickle                  | 6.67 us                                                                  | 6.77 us: 1.01x slower                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.68 ms: 1.03x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.5 ms: 1.04x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 61.7 ms: 1.04x slower                                                      |
| generators              | 31.4 ms                                                                  | 33.0 ms: 1.05x slower                                                      |
| pickle_list             | 2.57 us                                                                  | 2.70 us: 1.05x slower                                                      |
| unpickle                | 8.88 us                                                                  | 9.39 us: 1.06x slower                                                      |
| gc_traversal            | 1.33 ms                                                                  | 1.45 ms: 1.09x slower                                                      |
| pickle_dict             | 16.7 us                                                                  | 18.5 us: 1.11x slower                                                      |
| dask                    | 310 ms                                                                   | 349 ms: 1.13x slower                                                       |
| coverage                | 37.5 ms                                                                  | 51.8 ms: 1.38x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.22x faster                                                               |

Benchmark hidden because not significant (2): xml_etree_iterparse, json_loads
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
