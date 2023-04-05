
# Results vs. 3.11.0

- fork: python
- ref: ef7c2bfcf1fd618438f9
- machine: windows-amd64
- commit hash: ef7c2bf
- commit date: 2023-02-05
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 200 ms: 1.02x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.59 ms: 1.12x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 34.6 ms: 1.11x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 61.4 ms: 1.15x faster                                                       |
| float          | 53.3 ms                                                                  | 50.4 ms: 1.06x faster                                                       |
| pidigits       | 147 ms                                                                   | 152 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 77.6 ms: 1.16x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.54 ms: 1.06x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.3 ms: 1.01x faster                                                       |
| regex_dna      | 115 ms                                                                   | 119 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.14 ms: 1.50x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 122 us: 1.22x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 175 us: 1.16x faster                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 34.5 ms: 1.06x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 87.7 ms: 1.05x faster                                                       |
| json_loads           | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 49.9 ms: 1.05x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.7 us: 1.00x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.3 ms: 1.02x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.79 us: 1.03x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.79 us: 1.05x slower                                                       |
| unpickle             | 8.01 us                                                                  | 9.39 us: 1.17x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.20 ms                                                                  | 6.14 ms: 1.17x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 32.5 ms: 1.17x faster                                                       |
| genshi_text     | 17.3 ms                                                                  | 14.8 ms: 1.17x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.1 ms: 1.13x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.16x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 26.8 ns: 1.61x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.14 ms: 1.50x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 481 ms: 1.40x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 2.02 ms: 1.32x faster                                                       |
| richards                | 32.1 ms                                                                  | 24.5 ms: 1.31x faster                                                       |
| mypy2                   | 276 ms                                                                   | 217 ms: 1.27x faster                                                        |
| comprehensions          | 15.4 us                                                                  | 12.3 us: 1.25x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 57.2 ns: 1.24x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 122 us: 1.22x faster                                                        |
| fannkuch                | 255 ms                                                                   | 212 ms: 1.20x faster                                                        |
| scimark_monte_carlo     | 45.8 ms                                                                  | 38.4 ms: 1.19x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 65.4 ms: 1.19x faster                                                       |
| raytrace                | 206 ms                                                                   | 174 ms: 1.18x faster                                                        |
| deepcopy_memo           | 25.3 us                                                                  | 21.5 us: 1.18x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 60.8 ms: 1.18x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.24 ms: 1.18x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.14 ms: 1.17x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 32.5 ms: 1.17x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 14.8 ms: 1.17x faster                                                       |
| pyflate                 | 302 ms                                                                   | 259 ms: 1.16x faster                                                        |
| pickle_pure_python      | 203 us                                                                   | 175 us: 1.16x faster                                                        |
| json                    | 3.20 ms                                                                  | 2.76 ms: 1.16x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 40.9 ms: 1.16x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 77.6 ms: 1.16x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 56.3 ms: 1.16x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 3.86 ms: 1.16x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 61.4 ms: 1.15x faster                                                       |
| go                      | 97.5 ms                                                                  | 85.9 ms: 1.14x faster                                                       |
| django_template         | 23.9 ms                                                                  | 21.1 ms: 1.13x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 929 ms: 1.13x faster                                                        |
| sympy_str               | 184 ms                                                                   | 164 ms: 1.12x faster                                                        |
| chameleon               | 5.15 ms                                                                  | 4.59 ms: 1.12x faster                                                       |
| deepcopy                | 240 us                                                                   | 214 us: 1.12x faster                                                        |
| html5lib                | 38.5 ms                                                                  | 34.6 ms: 1.11x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 462 ms: 1.11x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.51 sec: 1.11x faster                                                      |
| scimark_fft             | 183 ms                                                                   | 166 ms: 1.10x faster                                                        |
| scimark_lu              | 62.8 ms                                                                  | 57.5 ms: 1.09x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.5 ms: 1.09x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.89 us: 1.09x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 44.5 ms: 1.09x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 276 ms: 1.08x faster                                                        |
| logging_format          | 7.13 us                                                                  | 6.58 us: 1.08x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 175 ms: 1.08x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 40.6 ms: 1.07x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.19 us: 1.07x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 92.8 ms: 1.07x faster                                                       |
| thrift                  | 487 us                                                                   | 457 us: 1.06x faster                                                        |
| regex_effbot            | 1.63 ms                                                                  | 1.54 ms: 1.06x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.5 ms: 1.06x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 34.5 ms: 1.06x faster                                                       |
| pycparser               | 686 ms                                                                   | 648 ms: 1.06x faster                                                        |
| float                   | 53.3 ms                                                                  | 50.4 ms: 1.06x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 87.7 ms: 1.05x faster                                                       |
| json_loads              | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 49.9 ms: 1.05x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 490 ms: 1.05x faster                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.08 ms: 1.05x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 71.1 ms: 1.05x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 891 us: 1.04x faster                                                        |
| telco                   | 3.93 ms                                                                  | 3.77 ms: 1.04x faster                                                       |
| async_generators        | 180 ms                                                                   | 173 ms: 1.04x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| coverage                | 55.3 ms                                                                  | 53.9 ms: 1.03x faster                                                       |
| bench_thread_pool       | 856 us                                                                   | 836 us: 1.02x faster                                                        |
| 2to3                    | 204 ms                                                                   | 200 ms: 1.02x faster                                                        |
| regex_v8                | 13.5 ms                                                                  | 13.3 ms: 1.01x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.7 ms: 1.01x faster                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.7 us: 1.00x slower                                                       |
| generators              | 33.5 ms                                                                  | 34.2 ms: 1.02x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.3 ms: 1.02x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 75.1 ms: 1.03x slower                                                       |
| regex_dna               | 115 ms                                                                   | 119 ms: 1.03x slower                                                        |
| gc_traversal            | 1.40 ms                                                                  | 1.45 ms: 1.03x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.79 us: 1.03x slower                                                       |
| pidigits                | 147 ms                                                                   | 152 ms: 1.04x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 63.9 ms: 1.04x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 779 ms: 1.05x slower                                                        |
| pickle                  | 6.47 us                                                                  | 6.79 us: 1.05x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.78 us: 1.06x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 718 us: 1.08x slower                                                        |
| unpickle                | 8.01 us                                                                  | 9.39 us: 1.17x slower                                                       |
| dask                    | 267 ms                                                                   | 353 ms: 1.32x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_none, unpickle_list, tornado_http
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
