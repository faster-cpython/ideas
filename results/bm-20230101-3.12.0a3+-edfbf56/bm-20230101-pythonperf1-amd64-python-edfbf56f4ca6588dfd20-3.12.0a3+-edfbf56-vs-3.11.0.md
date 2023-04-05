
# Results vs. 3.11.0

- fork: python
- ref: edfbf56f4ca6588dfd20
- machine: windows-amd64
- commit hash: edfbf56
- commit date: 2023-01-01
- overall geometric mean: 1.06x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 5.15 ms                                                                  | 4.59 ms: 1.12x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.56 sec: 1.03x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 36.5 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 66.2 ms: 1.07x faster                                                       |
| float          | 53.3 ms                                                                  | 50.3 ms: 1.06x faster                                                       |
| pidigits       | 147 ms                                                                   | 152 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.53 ms: 1.07x faster                                                       |
| regex_compile  | 89.7 ms                                                                  | 86.2 ms: 1.04x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.4 ms: 1.01x faster                                                       |
| regex_dna      | 115 ms                                                                   | 117 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.21 ms: 1.48x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 129 us: 1.16x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 181 us: 1.12x faster                                                        |
| json_loads           | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 50.5 ms: 1.04x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.3 ms: 1.04x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 89.5 ms: 1.03x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.72 us: 1.03x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.5 us: 1.01x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 62.4 ms: 1.01x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.71 us: 1.04x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.88 us: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.6 ms: 1.18x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.34 ms: 1.14x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 34.4 ms: 1.11x faster                                                       |
| django_template | 23.9 ms                                                                  | 22.7 ms: 1.05x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.12x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 7.71 ms                                                                  | 5.21 ms: 1.48x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 29.8 ns: 1.44x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 497 ms: 1.36x faster                                                        |
| mypy2                   | 276 ms                                                                   | 224 ms: 1.23x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 2.21 ms: 1.21x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 59.0 ns: 1.20x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 14.6 ms: 1.18x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.73 ms: 1.17x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 21.8 us: 1.16x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.4 ms: 1.16x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 66.9 ms: 1.16x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 129 us: 1.16x faster                                                        |
| richards                | 32.1 ms                                                                  | 28.1 ms: 1.14x faster                                                       |
| raytrace                | 206 ms                                                                   | 181 ms: 1.14x faster                                                        |
| mako                    | 7.20 ms                                                                  | 6.34 ms: 1.14x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.32 ms: 1.13x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 63.3 ms: 1.13x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.59 ms: 1.12x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 181 us: 1.12x faster                                                        |
| go                      | 97.5 ms                                                                  | 87.9 ms: 1.11x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 34.4 ms: 1.11x faster                                                       |
| fannkuch                | 255 ms                                                                   | 232 ms: 1.10x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.88 us: 1.09x faster                                                       |
| deepcopy                | 240 us                                                                   | 220 us: 1.09x faster                                                        |
| pyflate                 | 302 ms                                                                   | 278 ms: 1.09x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.55 sec: 1.08x faster                                                      |
| nqueens                 | 65.1 ms                                                                  | 60.6 ms: 1.07x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 66.2 ms: 1.07x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 58.8 ms: 1.07x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.53 ms: 1.07x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 44.5 ms: 1.06x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 990 ms: 1.06x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 4.21 ms: 1.06x faster                                                       |
| float                   | 53.3 ms                                                                  | 50.3 ms: 1.06x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 36.5 ms: 1.05x faster                                                       |
| django_template         | 23.9 ms                                                                  | 22.7 ms: 1.05x faster                                                       |
| json_loads              | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 180 ms: 1.05x faster                                                        |
| sympy_str               | 184 ms                                                                   | 176 ms: 1.05x faster                                                        |
| sympy_expand            | 298 ms                                                                   | 285 ms: 1.05x faster                                                        |
| async_generators        | 180 ms                                                                   | 173 ms: 1.04x faster                                                        |
| pprint_safe_repr        | 512 ms                                                                   | 490 ms: 1.04x faster                                                        |
| logging_format          | 7.13 us                                                                  | 6.83 us: 1.04x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.7 ms: 1.04x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 86.2 ms: 1.04x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 71.5 ms: 1.04x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.78 ms: 1.04x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 50.5 ms: 1.04x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 35.3 ms: 1.04x faster                                                       |
| pycparser               | 686 ms                                                                   | 662 ms: 1.04x faster                                                        |
| scimark_fft             | 183 ms                                                                   | 177 ms: 1.03x faster                                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 33.4 ms: 1.03x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 89.5 ms: 1.03x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.72 us: 1.03x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 47.1 ms: 1.03x faster                                                       |
| dask                    | 267 ms                                                                   | 260 ms: 1.03x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.56 sec: 1.03x faster                                                      |
| logging_simple          | 6.60 us                                                                  | 6.47 us: 1.02x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.5 ms: 1.02x faster                                                       |
| coverage                | 55.3 ms                                                                  | 54.2 ms: 1.02x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.4 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 504 ms: 1.02x faster                                                        |
| thrift                  | 487 us                                                                   | 479 us: 1.02x faster                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.12 ms: 1.01x faster                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.4 ms: 1.01x faster                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.5 us: 1.01x faster                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 62.4 ms: 1.01x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 318 ms: 1.02x slower                                                        |
| python_startup          | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| regex_dna               | 115 ms                                                                   | 117 ms: 1.02x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 62.6 ms: 1.02x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 75.2 ms: 1.03x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.45 ms: 1.03x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 690 us: 1.04x slower                                                        |
| pidigits                | 147 ms                                                                   | 152 ms: 1.04x slower                                                        |
| async_tree_memoization  | 374 ms                                                                   | 388 ms: 1.04x slower                                                        |
| pickle                  | 6.47 us                                                                  | 6.71 us: 1.04x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.76 us: 1.05x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 789 ms: 1.06x slower                                                        |
| comprehensions          | 15.4 us                                                                  | 16.3 us: 1.06x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.88 us: 1.06x slower                                                       |
| generators              | 33.5 ms                                                                  | 36.8 ms: 1.10x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (5): unpickle, sqlglot_parse, bench_thread_pool, 2to3, sympy_sum
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
