
# Results vs. 3.10.4

- fork: python
- ref: 4ae1a0ecaffe4320fe97
- machine: windows-amd64
- commit hash: 4ae1a0e
- commit date: 2022-10-25
- overall geometric mean: 1.12x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 202 ms: 1.14x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 4.99 ms: 1.16x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.59 sec: 1.15x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 38.1 ms: 1.24x faster                                                      |
| tornado_http   | 106 ms                                                                   | 91.5 ms: 1.16x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.17x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 53.5 ms: 1.11x faster                                                      |
| nbody          | 71.5 ms                                                                  | 67.2 ms: 1.06x faster                                                      |
| pidigits       | 145 ms                                                                   | 148 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 86.3 ms: 1.20x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 13.7 ms: 1.11x faster                                                      |
| regex_dna      | 131 ms                                                                   | 119 ms: 1.10x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.63 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.62 ms: 1.60x faster                                                      |
| pickle_pure_python   | 264 us                                                                   | 196 us: 1.35x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 143 us: 1.25x faster                                                       |
| xml_etree_process    | 43.0 ms                                                                  | 36.3 ms: 1.19x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 86.8 ms: 1.10x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 50.5 ms: 1.06x faster                                                      |
| json_loads           | 14.2 us                                                                  | 13.5 us: 1.05x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.60 us: 1.04x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.55 us: 1.02x faster                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.6 ms: 1.02x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.64 us: 1.03x slower                                                      |
| pickle_dict          | 16.7 us                                                                  | 18.2 us: 1.09x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.11x faster                                                               |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.93 ms: 1.25x faster                                                      |
| django_template | 29.2 ms                                                                  | 23.8 ms: 1.23x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 17.1 ms: 1.09x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 37.8 ms: 1.03x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.14x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.51 ms: 1.65x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 5.62 ms: 1.60x faster                                                      |
| mypy2                   | 337 ms                                                                   | 218 ms: 1.55x faster                                                       |
| go                      | 143 ms                                                                   | 93.8 ms: 1.53x faster                                                      |
| scimark_sor             | 104 ms                                                                   | 73.8 ms: 1.40x faster                                                      |
| logging_silent          | 94.6 ns                                                                  | 68.8 ns: 1.37x faster                                                      |
| pickle_pure_python      | 264 us                                                                   | 196 us: 1.35x faster                                                       |
| richards                | 41.0 ms                                                                  | 31.0 ms: 1.33x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 775 ms: 1.32x faster                                                       |
| raytrace                | 267 ms                                                                   | 204 ms: 1.31x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 316 ms: 1.31x faster                                                       |
| pyflate                 | 388 ms                                                                   | 297 ms: 1.31x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 47.2 ms: 1.30x faster                                                      |
| thrift                  | 632 us                                                                   | 486 us: 1.30x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.14 ms: 1.29x faster                                                      |
| sqlglot_parse           | 1.22 ms                                                                  | 951 us: 1.28x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 43.8 ms: 1.28x faster                                                      |
| async_tree_memoization  | 485 ms                                                                   | 381 ms: 1.27x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 66.6 ms: 1.26x faster                                                      |
| chaos                   | 58.4 ms                                                                  | 46.5 ms: 1.26x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 143 us: 1.25x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.93 ms: 1.25x faster                                                      |
| html5lib                | 47.3 ms                                                                  | 38.1 ms: 1.24x faster                                                      |
| pprint_pformat          | 1.23 sec                                                                 | 1.00 sec: 1.23x faster                                                     |
| django_template         | 29.2 ms                                                                  | 23.8 ms: 1.23x faster                                                      |
| pycparser               | 873 ms                                                                   | 721 ms: 1.21x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.51 ms: 1.21x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 495 ms: 1.20x faster                                                       |
| regex_compile           | 103 ms                                                                   | 86.3 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 506 ms: 1.20x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 36.3 ms: 1.19x faster                                                      |
| async_generators        | 214 ms                                                                   | 181 ms: 1.18x faster                                                       |
| dask                    | 310 ms                                                                   | 265 ms: 1.17x faster                                                       |
| tornado_http            | 106 ms                                                                   | 91.5 ms: 1.16x faster                                                      |
| chameleon               | 5.77 ms                                                                  | 4.99 ms: 1.16x faster                                                      |
| create_gc_cycles        | 764 us                                                                   | 663 us: 1.15x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.59 sec: 1.15x faster                                                     |
| deepcopy_memo           | 28.4 us                                                                  | 24.7 us: 1.15x faster                                                      |
| json                    | 3.18 ms                                                                  | 2.77 ms: 1.15x faster                                                      |
| 2to3                    | 229 ms                                                                   | 202 ms: 1.14x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.37 ms: 1.13x faster                                                      |
| bench_thread_pool       | 953 us                                                                   | 844 us: 1.13x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 34.4 ms: 1.12x faster                                                      |
| float                   | 59.5 ms                                                                  | 53.5 ms: 1.11x faster                                                      |
| regex_v8                | 15.1 ms                                                                  | 13.7 ms: 1.11x faster                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 86.8 ms: 1.10x faster                                                      |
| sympy_integrate         | 14.7 ms                                                                  | 13.4 ms: 1.10x faster                                                      |
| regex_dna               | 131 ms                                                                   | 119 ms: 1.10x faster                                                       |
| deepcopy                | 256 us                                                                   | 235 us: 1.09x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 17.1 ms: 1.09x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 43.5 ms: 1.08x faster                                                      |
| sqlglot_normalize       | 201 ms                                                                   | 188 ms: 1.07x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 50.5 ms: 1.06x faster                                                      |
| nbody                   | 71.5 ms                                                                  | 67.2 ms: 1.06x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 2.05 us: 1.06x faster                                                      |
| pylint                  | 337 ms                                                                   | 317 ms: 1.06x faster                                                       |
| fannkuch                | 252 ms                                                                   | 238 ms: 1.06x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 296 ms: 1.06x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| json_loads              | 14.2 us                                                                  | 13.5 us: 1.05x faster                                                      |
| coroutines              | 15.6 ms                                                                  | 15.0 ms: 1.04x faster                                                      |
| unpickle_list           | 2.71 us                                                                  | 2.60 us: 1.04x faster                                                      |
| meteor_contest          | 74.3 ms                                                                  | 71.8 ms: 1.04x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 98.9 ms: 1.03x faster                                                      |
| sympy_str               | 189 ms                                                                   | 183 ms: 1.03x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.80 us: 1.03x faster                                                      |
| genshi_xml              | 38.8 ms                                                                  | 37.8 ms: 1.03x faster                                                      |
| comprehensions          | 16.0 us                                                                  | 15.6 us: 1.02x faster                                                      |
| pickle                  | 6.67 us                                                                  | 6.55 us: 1.02x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 74.0 ms: 1.02x faster                                                      |
| mdp                     | 1.60 sec                                                                 | 1.59 sec: 1.01x faster                                                     |
| regex_effbot            | 1.64 ms                                                                  | 1.63 ms: 1.01x faster                                                      |
| nqueens                 | 64.8 ms                                                                  | 65.4 ms: 1.01x slower                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.6 ms: 1.02x slower                                                      |
| telco                   | 3.77 ms                                                                  | 3.85 ms: 1.02x slower                                                      |
| pidigits                | 145 ms                                                                   | 148 ms: 1.02x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.64 us: 1.03x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 60.9 ms: 1.03x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                      |
| asyncio_tcp             | 664 ms                                                                   | 694 ms: 1.05x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.42 ms: 1.07x slower                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 42.3 ns: 1.07x slower                                                      |
| pickle_dict             | 16.7 us                                                                  | 18.2 us: 1.09x slower                                                      |
| generators              | 31.4 ms                                                                  | 34.5 ms: 1.10x slower                                                      |
| logging_simple          | 6.12 us                                                                  | 6.80 us: 1.11x slower                                                      |
| logging_format          | 6.53 us                                                                  | 7.28 us: 1.11x slower                                                      |
| coverage                | 37.5 ms                                                                  | 52.1 ms: 1.39x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.12x faster                                                               |

Benchmark hidden because not significant (3): spectral_norm, unpickle, scimark_fft
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
