
# Results vs. 3.11.0

- fork: faster-cpython
- ref: nogil_latest
- machine: windows-amd64
- commit hash: 1d39009
- commit date: 2023-04-16
- overall geometric mean: 1.05x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 224 ms: 1.10x slower                                                         |
| chameleon      | 5.15 ms                                                                  | 5.66 ms: 1.10x slower                                                        |
| docutils       | 1.59 sec                                                                 | 1.89 sec: 1.18x slower                                                       |
| html5lib       | 38.5 ms                                                                  | 39.3 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.10x slower                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 53.3 ms                                                                  | 49.6 ms: 1.08x faster                                                        |
| pidigits       | 147 ms                                                                   | 141 ms: 1.04x faster                                                         |
| nbody          | 70.9 ms                                                                  | 89.9 ms: 1.27x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.04x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.53 ms: 1.07x faster                                                        |
| regex_dna      | 115 ms                                                                   | 110 ms: 1.05x faster                                                         |
| regex_v8       | 13.5 ms                                                                  | 13.2 ms: 1.02x faster                                                        |
| regex_compile  | 89.7 ms                                                                  | 96.4 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 6.50 ms: 1.19x faster                                                        |
| xml_etree_parse      | 92.1 ms                                                                  | 82.9 ms: 1.11x faster                                                        |
| unpickle_list        | 2.80 us                                                                  | 2.86 us: 1.02x slower                                                        |
| pickle_list          | 2.70 us                                                                  | 2.81 us: 1.04x slower                                                        |
| unpickle_pure_python | 150 us                                                                   | 159 us: 1.06x slower                                                         |
| pickle_pure_python   | 203 us                                                                   | 218 us: 1.07x slower                                                         |
| json_loads           | 13.5 us                                                                  | 14.6 us: 1.08x slower                                                        |
| xml_etree_generate   | 52.3 ms                                                                  | 57.5 ms: 1.10x slower                                                        |
| pickle               | 6.47 us                                                                  | 7.14 us: 1.10x slower                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 41.7 ms: 1.14x slower                                                        |
| unpickle             | 8.01 us                                                                  | 9.19 us: 1.15x slower                                                        |
| pickle_dict          | 18.6 us                                                                  | 21.8 us: 1.17x slower                                                        |
| xml_etree_iterparse  | 61.8 ms                                                                  | 74.7 ms: 1.21x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.06x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 35.3 ms: 1.08x faster                                                        |
| genshi_text     | 17.3 ms                                                                  | 17.7 ms: 1.02x slower                                                        |
| django_template | 23.9 ms                                                                  | 25.5 ms: 1.07x slower                                                        |
| mako            | 7.20 ms                                                                  | 8.95 ms: 1.24x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.06x slower                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io           | 744 ms                                                                   | 405 ms: 1.84x faster                                                         |
| async_tree_none         | 313 ms                                                                   | 189 ms: 1.65x faster                                                         |
| async_tree_memoization  | 374 ms                                                                   | 240 ms: 1.56x faster                                                         |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 371 ms: 1.38x faster                                                         |
| asyncio_tcp             | 674 ms                                                                   | 489 ms: 1.38x faster                                                         |
| sqlite_synth            | 1.67 us                                                                  | 1.35 us: 1.24x faster                                                        |
| json_dumps              | 7.71 ms                                                                  | 6.50 ms: 1.19x faster                                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 82.9 ms: 1.11x faster                                                        |
| json                    | 3.20 ms                                                                  | 2.94 ms: 1.09x faster                                                        |
| genshi_xml              | 38.0 ms                                                                  | 35.3 ms: 1.08x faster                                                        |
| float                   | 53.3 ms                                                                  | 49.6 ms: 1.08x faster                                                        |
| regex_effbot            | 1.63 ms                                                                  | 1.53 ms: 1.07x faster                                                        |
| regex_dna               | 115 ms                                                                   | 110 ms: 1.05x faster                                                         |
| pidigits                | 147 ms                                                                   | 141 ms: 1.04x faster                                                         |
| mdp                     | 1.67 sec                                                                 | 1.63 sec: 1.03x faster                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.2 ms: 1.02x faster                                                        |
| python_startup          | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                        |
| richards                | 32.1 ms                                                                  | 32.3 ms: 1.01x slower                                                        |
| nqueens                 | 65.1 ms                                                                  | 65.6 ms: 1.01x slower                                                        |
| deltablue               | 2.68 ms                                                                  | 2.71 ms: 1.01x slower                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.86 us: 1.02x slower                                                        |
| html5lib                | 38.5 ms                                                                  | 39.3 ms: 1.02x slower                                                        |
| genshi_text             | 17.3 ms                                                                  | 17.7 ms: 1.02x slower                                                        |
| pickle_list             | 2.70 us                                                                  | 2.81 us: 1.04x slower                                                        |
| logging_format          | 7.13 us                                                                  | 7.40 us: 1.04x slower                                                        |
| pycparser               | 686 ms                                                                   | 713 ms: 1.04x slower                                                         |
| bench_mp_pool           | 61.2 ms                                                                  | 63.9 ms: 1.04x slower                                                        |
| logging_simple          | 6.60 us                                                                  | 6.92 us: 1.05x slower                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 199 ms: 1.05x slower                                                         |
| go                      | 97.5 ms                                                                  | 103 ms: 1.06x slower                                                         |
| logging_silent          | 71.0 ns                                                                  | 75.0 ns: 1.06x slower                                                        |
| unpickle_pure_python    | 150 us                                                                   | 159 us: 1.06x slower                                                         |
| sqlglot_optimize        | 34.5 ms                                                                  | 36.8 ms: 1.07x slower                                                        |
| django_template         | 23.9 ms                                                                  | 25.5 ms: 1.07x slower                                                        |
| pickle_pure_python      | 203 us                                                                   | 218 us: 1.07x slower                                                         |
| sympy_expand            | 298 ms                                                                   | 320 ms: 1.07x slower                                                         |
| regex_compile           | 89.7 ms                                                                  | 96.4 ms: 1.07x slower                                                        |
| sympy_str               | 184 ms                                                                   | 198 ms: 1.08x slower                                                         |
| json_loads              | 13.5 us                                                                  | 14.6 us: 1.08x slower                                                        |
| coverage                | 55.3 ms                                                                  | 59.9 ms: 1.08x slower                                                        |
| sympy_integrate         | 13.7 ms                                                                  | 14.8 ms: 1.09x slower                                                        |
| crypto_pyaes            | 48.3 ms                                                                  | 52.7 ms: 1.09x slower                                                        |
| 2to3                    | 204 ms                                                                   | 224 ms: 1.10x slower                                                         |
| spectral_norm           | 71.8 ms                                                                  | 78.8 ms: 1.10x slower                                                        |
| xml_etree_generate      | 52.3 ms                                                                  | 57.5 ms: 1.10x slower                                                        |
| chameleon               | 5.15 ms                                                                  | 5.66 ms: 1.10x slower                                                        |
| pickle                  | 6.47 us                                                                  | 7.14 us: 1.10x slower                                                        |
| sympy_sum               | 98.9 ms                                                                  | 109 ms: 1.10x slower                                                         |
| gc_traversal            | 1.40 ms                                                                  | 1.56 ms: 1.11x slower                                                        |
| thrift                  | 487 us                                                                   | 542 us: 1.11x slower                                                         |
| hexiom                  | 4.46 ms                                                                  | 4.97 ms: 1.11x slower                                                        |
| fannkuch                | 255 ms                                                                   | 285 ms: 1.12x slower                                                         |
| scimark_monte_carlo     | 45.8 ms                                                                  | 51.2 ms: 1.12x slower                                                        |
| generators              | 33.5 ms                                                                  | 37.5 ms: 1.12x slower                                                        |
| telco                   | 3.93 ms                                                                  | 4.41 ms: 1.12x slower                                                        |
| create_gc_cycles        | 666 us                                                                   | 748 us: 1.12x slower                                                         |
| deepcopy                | 240 us                                                                   | 272 us: 1.13x slower                                                         |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.98 ms: 1.13x slower                                                        |
| coroutines              | 14.8 ms                                                                  | 16.8 ms: 1.13x slower                                                        |
| chaos                   | 47.3 ms                                                                  | 53.7 ms: 1.14x slower                                                        |
| async_generators        | 180 ms                                                                   | 205 ms: 1.14x slower                                                         |
| xml_etree_process       | 36.6 ms                                                                  | 41.7 ms: 1.14x slower                                                        |
| pprint_safe_repr        | 512 ms                                                                   | 586 ms: 1.14x slower                                                         |
| scimark_sor             | 77.7 ms                                                                  | 89.1 ms: 1.15x slower                                                        |
| unpickle                | 8.01 us                                                                  | 9.19 us: 1.15x slower                                                        |
| pprint_pformat          | 1.05 sec                                                                 | 1.21 sec: 1.15x slower                                                       |
| scimark_lu              | 62.8 ms                                                                  | 73.1 ms: 1.16x slower                                                        |
| meteor_contest          | 74.4 ms                                                                  | 86.5 ms: 1.16x slower                                                        |
| deepcopy_memo           | 25.3 us                                                                  | 29.5 us: 1.16x slower                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 2.40 us: 1.17x slower                                                        |
| pickle_dict             | 18.6 us                                                                  | 21.8 us: 1.17x slower                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.33 ms: 1.17x slower                                                        |
| raytrace                | 206 ms                                                                   | 241 ms: 1.17x slower                                                         |
| docutils                | 1.59 sec                                                                 | 1.89 sec: 1.18x slower                                                       |
| scimark_fft             | 183 ms                                                                   | 220 ms: 1.20x slower                                                         |
| bench_thread_pool       | 856 us                                                                   | 1.03 ms: 1.20x slower                                                        |
| sqlglot_parse           | 929 us                                                                   | 1.12 ms: 1.20x slower                                                        |
| xml_etree_iterparse     | 61.8 ms                                                                  | 74.7 ms: 1.21x slower                                                        |
| comprehensions          | 15.4 us                                                                  | 19.1 us: 1.24x slower                                                        |
| mako                    | 7.20 ms                                                                  | 8.95 ms: 1.24x slower                                                        |
| nbody                   | 70.9 ms                                                                  | 89.9 ms: 1.27x slower                                                        |
| unpack_sequence         | 43.1 ns                                                                  | 55.2 ns: 1.28x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.05x slower                                                                 |

Benchmark hidden because not significant (5): pyflate, python_startup_no_site, dulwich_log, pathlib, mypy2
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, dask, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
