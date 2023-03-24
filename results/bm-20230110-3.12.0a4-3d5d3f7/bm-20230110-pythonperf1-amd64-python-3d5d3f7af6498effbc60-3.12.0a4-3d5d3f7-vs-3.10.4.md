
# Results vs. 3.10.4

- fork: python
- ref: 3d5d3f7af6498effbc60
- machine: windows-amd64
- commit hash: 3d5d3f7
- commit date: 2023-01-10
- overall geometric mean: 1.23x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 190 ms: 1.21x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 4.34 ms: 1.33x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.50 sec: 1.23x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 35.3 ms: 1.34x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.27x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 46.3 ms: 1.28x faster                                                      |
| nbody          | 71.5 ms                                                                  | 56.6 ms: 1.26x faster                                                      |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.17x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 78.9 ms: 1.31x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 13.7 ms: 1.10x faster                                                      |
| regex_dna      | 131 ms                                                                   | 121 ms: 1.08x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.73 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.36 ms: 1.68x faster                                                      |
| pickle_pure_python   | 264 us                                                                   | 166 us: 1.59x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 118 us: 1.52x faster                                                       |
| xml_etree_process    | 43.0 ms                                                                  | 33.0 ms: 1.31x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 47.6 ms: 1.13x faster                                                      |
| json_loads           | 14.2 us                                                                  | 12.7 us: 1.12x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 87.1 ms: 1.10x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.62 us: 1.04x faster                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.1 ms: 1.02x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.79 us: 1.02x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.74 us: 1.07x slower                                                      |
| pickle_dict          | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.16x faster                                                               |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 5.94 ms: 1.46x faster                                                      |
| django_template | 29.2 ms                                                                  | 20.9 ms: 1.40x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 13.3 ms: 1.40x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 31.5 ms: 1.23x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.37x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.93 ms: 2.15x faster                                                      |
| go                      | 143 ms                                                                   | 80.8 ms: 1.77x faster                                                      |
| richards                | 41.0 ms                                                                  | 23.5 ms: 1.74x faster                                                      |
| logging_silent          | 94.6 ns                                                                  | 55.9 ns: 1.69x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 5.36 ms: 1.68x faster                                                      |
| scimark_sor             | 104 ms                                                                   | 62.4 ms: 1.66x faster                                                      |
| mypy2                   | 337 ms                                                                   | 208 ms: 1.62x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 166 us: 1.59x faster                                                       |
| raytrace                | 267 ms                                                                   | 169 ms: 1.58x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 54.8 ms: 1.53x faster                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 25.8 ns: 1.52x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 118 us: 1.52x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 37.1 ms: 1.51x faster                                                      |
| pyflate                 | 388 ms                                                                   | 262 ms: 1.48x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 829 us: 1.47x faster                                                       |
| mako                    | 8.69 ms                                                                  | 5.94 ms: 1.46x faster                                                      |
| hexiom                  | 5.45 ms                                                                  | 3.75 ms: 1.45x faster                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.02 ms: 1.44x faster                                                      |
| deepcopy_memo           | 28.4 us                                                                  | 19.9 us: 1.43x faster                                                      |
| thrift                  | 632 us                                                                   | 450 us: 1.40x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 474 ms: 1.40x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.9 ms: 1.40x faster                                                      |
| genshi_text             | 18.5 ms                                                                  | 13.3 ms: 1.40x faster                                                      |
| pycparser               | 873 ms                                                                   | 634 ms: 1.38x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 44.6 ms: 1.38x faster                                                      |
| pprint_pformat          | 1.23 sec                                                                 | 894 ms: 1.37x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 42.7 ms: 1.37x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 441 ms: 1.35x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.3 ms: 1.34x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 768 ms: 1.33x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.34 ms: 1.33x faster                                                      |
| regex_compile           | 103 ms                                                                   | 78.9 ms: 1.31x faster                                                      |
| xml_etree_process       | 43.0 ms                                                                  | 33.0 ms: 1.31x faster                                                      |
| deepcopy                | 256 us                                                                   | 198 us: 1.29x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 321 ms: 1.29x faster                                                       |
| async_generators        | 214 ms                                                                   | 166 ms: 1.29x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 377 ms: 1.29x faster                                                       |
| float                   | 59.5 ms                                                                  | 46.3 ms: 1.28x faster                                                      |
| sqlglot_optimize        | 38.7 ms                                                                  | 30.4 ms: 1.27x faster                                                      |
| nbody                   | 71.5 ms                                                                  | 56.6 ms: 1.26x faster                                                      |
| spectral_norm           | 74.3 ms                                                                  | 59.6 ms: 1.24x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.77 us: 1.24x faster                                                      |
| genshi_xml              | 38.8 ms                                                                  | 31.5 ms: 1.23x faster                                                      |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.17 ms: 1.23x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.50 sec: 1.23x faster                                                     |
| dask                    | 310 ms                                                                   | 254 ms: 1.22x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 494 ms: 1.22x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 165 ms: 1.22x faster                                                       |
| 2to3                    | 229 ms                                                                   | 190 ms: 1.21x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.68 ms: 1.19x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 267 ms: 1.17x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 817 us: 1.17x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.6 ms: 1.16x faster                                                      |
| create_gc_cycles        | 764 us                                                                   | 663 us: 1.15x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 47.6 ms: 1.13x faster                                                      |
| scimark_fft             | 187 ms                                                                   | 166 ms: 1.12x faster                                                       |
| sympy_str               | 189 ms                                                                   | 169 ms: 1.12x faster                                                       |
| json_loads              | 14.2 us                                                                  | 12.7 us: 1.12x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 42.3 ms: 1.11x faster                                                      |
| nqueens                 | 64.8 ms                                                                  | 58.4 ms: 1.11x faster                                                      |
| regex_v8                | 15.1 ms                                                                  | 13.7 ms: 1.10x faster                                                      |
| comprehensions          | 16.0 us                                                                  | 14.5 us: 1.10x faster                                                      |
| meteor_contest          | 74.3 ms                                                                  | 67.6 ms: 1.10x faster                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 87.1 ms: 1.10x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 94.2 ms: 1.09x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.70 us: 1.08x faster                                                      |
| regex_dna               | 131 ms                                                                   | 121 ms: 1.08x faster                                                       |
| fannkuch                | 252 ms                                                                   | 237 ms: 1.06x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.51 sec: 1.06x faster                                                     |
| python_startup          | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| coroutines              | 15.6 ms                                                                  | 14.7 ms: 1.06x faster                                                      |
| logging_format          | 6.53 us                                                                  | 6.29 us: 1.04x faster                                                      |
| telco                   | 3.77 ms                                                                  | 3.63 ms: 1.04x faster                                                      |
| unpickle_list           | 2.71 us                                                                  | 2.62 us: 1.04x faster                                                      |
| logging_simple          | 6.12 us                                                                  | 5.91 us: 1.04x faster                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.1 ms: 1.02x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 74.0 ms: 1.02x faster                                                      |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                       |
| pickle                  | 6.67 us                                                                  | 6.79 us: 1.02x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 60.9 ms: 1.03x slower                                                      |
| generators              | 31.4 ms                                                                  | 32.6 ms: 1.04x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.73 ms: 1.05x slower                                                      |
| pickle_list             | 2.57 us                                                                  | 2.74 us: 1.07x slower                                                      |
| gc_traversal            | 1.33 ms                                                                  | 1.43 ms: 1.08x slower                                                      |
| pickle_dict             | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                      |
| coverage                | 37.5 ms                                                                  | 52.4 ms: 1.40x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.23x faster                                                               |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
