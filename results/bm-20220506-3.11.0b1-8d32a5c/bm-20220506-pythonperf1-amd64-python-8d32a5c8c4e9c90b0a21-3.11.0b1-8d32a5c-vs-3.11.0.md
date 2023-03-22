
# Results vs. 3.11.0

- fork: python
- ref: 8d32a5c8c4e9c90b0a21
- machine: windows-amd64
- commit hash: 8d32a5c
- commit date: 2022-05-06
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| chameleon      | 5.15 ms                                                                  | 5.45 ms: 1.06x slower                                                      |
| docutils       | 1.59 sec                                                                 | 1.57 sec: 1.01x faster                                                     |
| tornado_http   | 91.8 ms                                                                  | 89.7 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                               |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 67.9 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.47 ms: 1.11x faster                                                      |
| regex_compile  | 89.7 ms                                                                  | 90.5 ms: 1.01x slower                                                      |
| regex_v8       | 13.5 ms                                                                  | 13.9 ms: 1.03x slower                                                      |
| regex_dna      | 115 ms                                                                   | 121 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 18.6 us                                                                  | 17.1 us: 1.09x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.58 us: 1.09x faster                                                      |
| unpickle             | 8.01 us                                                                  | 7.87 us: 1.02x faster                                                      |
| xml_etree_iterparse  | 61.8 ms                                                                  | 61.1 ms: 1.01x faster                                                      |
| json_loads           | 13.5 us                                                                  | 13.4 us: 1.01x faster                                                      |
| xml_etree_generate   | 52.3 ms                                                                  | 53.0 ms: 1.01x slower                                                      |
| pickle               | 6.47 us                                                                  | 6.59 us: 1.02x slower                                                      |
| unpickle_pure_python | 150 us                                                                   | 152 us: 1.02x slower                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 37.6 ms: 1.03x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (4): pickle_list, json_dumps, pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.2 ms: 1.01x faster                                                      |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                               |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.20 ms                                                                  | 7.13 ms: 1.01x faster                                                      |
| django_template | 23.9 ms                                                                  | 24.0 ms: 1.01x slower                                                      |
| genshi_text     | 17.3 ms                                                                  | 17.7 ms: 1.02x slower                                                      |
| genshi_xml      | 38.0 ms                                                                  | 39.8 ms: 1.05x slower                                                      |
| Geometric mean  | (ref)                                                                    | 1.02x slower                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220506-pythonperf1-amd64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| logging_format          | 7.13 us                                                                  | 6.25 us: 1.14x faster                                                      |
| logging_simple          | 6.60 us                                                                  | 5.80 us: 1.14x faster                                                      |
| regex_effbot            | 1.63 ms                                                                  | 1.47 ms: 1.11x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 17.1 us: 1.09x faster                                                      |
| unpickle_list           | 2.80 us                                                                  | 2.58 us: 1.09x faster                                                      |
| richards                | 32.1 ms                                                                  | 30.1 ms: 1.07x faster                                                      |
| nbody                   | 70.9 ms                                                                  | 67.9 ms: 1.04x faster                                                      |
| spectral_norm           | 71.8 ms                                                                  | 69.6 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 499 ms: 1.03x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.63 sec: 1.02x faster                                                     |
| tornado_http            | 91.8 ms                                                                  | 89.7 ms: 1.02x faster                                                      |
| pathlib                 | 72.9 ms                                                                  | 71.4 ms: 1.02x faster                                                      |
| dulwich_log             | 43.4 ms                                                                  | 42.5 ms: 1.02x faster                                                      |
| unpack_sequence         | 43.1 ns                                                                  | 42.2 ns: 1.02x faster                                                      |
| sympy_sum               | 98.9 ms                                                                  | 96.9 ms: 1.02x faster                                                      |
| unpickle                | 8.01 us                                                                  | 7.87 us: 1.02x faster                                                      |
| sympy_expand            | 298 ms                                                                   | 293 ms: 1.02x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 45.0 ms: 1.02x faster                                                      |
| scimark_fft             | 183 ms                                                                   | 180 ms: 1.02x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.57 sec: 1.01x faster                                                     |
| raytrace                | 206 ms                                                                   | 203 ms: 1.01x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 70.2 ns: 1.01x faster                                                      |
| aiohttp                 | 864 us                                                                   | 854 us: 1.01x faster                                                       |
| fannkuch                | 255 ms                                                                   | 252 ms: 1.01x faster                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 61.1 ms: 1.01x faster                                                      |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.60 ms: 1.01x faster                                                      |
| bench_mp_pool           | 61.2 ms                                                                  | 60.6 ms: 1.01x faster                                                      |
| mako                    | 7.20 ms                                                                  | 7.13 ms: 1.01x faster                                                      |
| deepcopy_memo           | 25.3 us                                                                  | 25.1 us: 1.01x faster                                                      |
| python_startup_no_site  | 15.4 ms                                                                  | 15.2 ms: 1.01x faster                                                      |
| json_loads              | 13.5 us                                                                  | 13.4 us: 1.01x faster                                                      |
| scimark_sor             | 77.7 ms                                                                  | 77.1 ms: 1.01x faster                                                      |
| sympy_str               | 184 ms                                                                   | 183 ms: 1.01x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.66 ms: 1.01x faster                                                      |
| sympy_integrate         | 13.7 ms                                                                  | 13.6 ms: 1.00x faster                                                      |
| pyflate                 | 302 ms                                                                   | 303 ms: 1.00x slower                                                       |
| flaskblogging           | 2.04 sec                                                                 | 2.05 sec: 1.00x slower                                                     |
| go                      | 97.5 ms                                                                  | 97.9 ms: 1.00x slower                                                      |
| telco                   | 3.93 ms                                                                  | 3.94 ms: 1.00x slower                                                      |
| django_template         | 23.9 ms                                                                  | 24.0 ms: 1.01x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.69 us: 1.01x slower                                                      |
| regex_compile           | 89.7 ms                                                                  | 90.5 ms: 1.01x slower                                                      |
| async_tree_io           | 744 ms                                                                   | 751 ms: 1.01x slower                                                       |
| generators              | 33.5 ms                                                                  | 33.9 ms: 1.01x slower                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.42 ms: 1.01x slower                                                      |
| async_generators        | 180 ms                                                                   | 182 ms: 1.01x slower                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 53.0 ms: 1.01x slower                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 49.1 ms: 1.02x slower                                                      |
| meteor_contest          | 74.4 ms                                                                  | 75.5 ms: 1.02x slower                                                      |
| pickle                  | 6.47 us                                                                  | 6.59 us: 1.02x slower                                                      |
| unpickle_pure_python    | 150 us                                                                   | 152 us: 1.02x slower                                                       |
| genshi_text             | 17.3 ms                                                                  | 17.7 ms: 1.02x slower                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 525 ms: 1.03x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 15.2 ms: 1.03x slower                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 37.6 ms: 1.03x slower                                                      |
| pprint_pformat          | 1.05 sec                                                                 | 1.08 sec: 1.03x slower                                                     |
| hexiom                  | 4.46 ms                                                                  | 4.59 ms: 1.03x slower                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 2.12 us: 1.03x slower                                                      |
| sqlglot_optimize        | 34.5 ms                                                                  | 35.6 ms: 1.03x slower                                                      |
| regex_v8                | 13.5 ms                                                                  | 13.9 ms: 1.03x slower                                                      |
| chaos                   | 47.3 ms                                                                  | 48.9 ms: 1.03x slower                                                      |
| sqlglot_normalize       | 189 ms                                                                   | 196 ms: 1.04x slower                                                       |
| thrift                  | 487 us                                                                   | 504 us: 1.04x slower                                                       |
| nqueens                 | 65.1 ms                                                                  | 67.6 ms: 1.04x slower                                                      |
| bench_thread_pool       | 856 us                                                                   | 888 us: 1.04x slower                                                       |
| genshi_xml              | 38.0 ms                                                                  | 39.8 ms: 1.05x slower                                                      |
| regex_dna               | 115 ms                                                                   | 121 ms: 1.05x slower                                                       |
| deepcopy                | 240 us                                                                   | 252 us: 1.05x slower                                                       |
| chameleon               | 5.15 ms                                                                  | 5.45 ms: 1.06x slower                                                      |
| pycparser               | 686 ms                                                                   | 748 ms: 1.09x slower                                                       |
| comprehensions          | 15.4 us                                                                  | 17.8 us: 1.16x slower                                                      |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.37 ms: 1.21x slower                                                      |
| sqlglot_parse           | 929 us                                                                   | 1.15 ms: 1.24x slower                                                      |
| coverage                | 55.3 ms                                                                  | 103 ms: 1.85x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.01x slower                                                               |

Benchmark hidden because not significant (18): pylint, async_tree_memoization, pickle_list, async_tree_none, html5lib, create_gc_cycles, 2to3, scimark_lu, asyncio_tcp, python_startup, pidigits, json_dumps, pickle_pure_python, mypy2, float, dask, xml_etree_parse, json
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative
