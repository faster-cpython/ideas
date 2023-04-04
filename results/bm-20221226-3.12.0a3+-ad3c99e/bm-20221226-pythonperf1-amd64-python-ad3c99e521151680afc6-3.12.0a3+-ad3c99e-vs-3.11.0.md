
# Results vs. 3.11.0

- fork: python
- ref: ad3c99e521151680afc6
- machine: windows-amd64
- commit hash: ad3c99e
- commit date: 2022-12-26
- overall geometric mean: 1.05x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 5.15 ms                                                                  | 4.75 ms: 1.09x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 34.7 ms: 1.11x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 66.0 ms: 1.07x faster                                                       |
| float          | 53.3 ms                                                                  | 51.1 ms: 1.04x faster                                                       |
| pidigits       | 147 ms                                                                   | 153 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 83.8 ms: 1.07x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.65 ms: 1.01x slower                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.0 ms: 1.04x slower                                                       |
| regex_dna      | 115 ms                                                                   | 125 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.43 ms: 1.42x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 127 us: 1.18x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 186 us: 1.09x faster                                                        |
| unpickle_list        | 2.80 us                                                                  | 2.62 us: 1.07x faster                                                       |
| json_loads           | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.7 ms: 1.03x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 90.4 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.7 ms: 1.01x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.0 ms: 1.02x slower                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.0 us: 1.02x slower                                                       |
| unpickle             | 8.01 us                                                                  | 8.20 us: 1.02x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.83 us: 1.05x slower                                                       |
| pickle               | 6.47 us                                                                  | 7.29 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.04x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                                       |
| python_startup         | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.6 ms: 1.18x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.35 ms: 1.13x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 33.9 ms: 1.12x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.9 ms: 1.09x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.13x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 29.9 ns: 1.44x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.43 ms: 1.42x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 482 ms: 1.40x faster                                                        |
| richards                | 32.1 ms                                                                  | 25.6 ms: 1.25x faster                                                       |
| mypy2                   | 276 ms                                                                   | 228 ms: 1.21x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 2.25 ms: 1.19x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.69 ms: 1.19x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 14.6 ms: 1.18x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 127 us: 1.18x faster                                                        |
| logging_silent          | 71.0 ns                                                                  | 60.9 ns: 1.17x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 62.4 ms: 1.15x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 56.9 ms: 1.14x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.35 ms: 1.13x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 40.7 ms: 1.12x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 22.6 us: 1.12x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 33.9 ms: 1.12x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 34.7 ms: 1.11x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 70.3 ms: 1.10x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 186 us: 1.09x faster                                                        |
| django_template         | 23.9 ms                                                                  | 21.9 ms: 1.09x faster                                                       |
| raytrace                | 206 ms                                                                   | 190 ms: 1.09x faster                                                        |
| chameleon               | 5.15 ms                                                                  | 4.75 ms: 1.09x faster                                                       |
| pyflate                 | 302 ms                                                                   | 279 ms: 1.08x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 4.12 ms: 1.08x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.0 ms: 1.08x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 66.0 ms: 1.07x faster                                                       |
| deepcopy                | 240 us                                                                   | 223 us: 1.07x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.45 ms: 1.07x faster                                                       |
| fannkuch                | 255 ms                                                                   | 238 ms: 1.07x faster                                                        |
| regex_compile           | 89.7 ms                                                                  | 83.8 ms: 1.07x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.62 us: 1.07x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 59.0 ms: 1.06x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 987 ms: 1.06x faster                                                        |
| go                      | 97.5 ms                                                                  | 91.7 ms: 1.06x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 484 ms: 1.06x faster                                                        |
| sympy_expand            | 298 ms                                                                   | 284 ms: 1.05x faster                                                        |
| json_loads              | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.97 us: 1.04x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 181 ms: 1.04x faster                                                        |
| logging_format          | 7.13 us                                                                  | 6.84 us: 1.04x faster                                                       |
| float                   | 53.3 ms                                                                  | 51.1 ms: 1.04x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 492 ms: 1.04x faster                                                        |
| pycparser               | 686 ms                                                                   | 661 ms: 1.04x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 45.6 ms: 1.04x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.09 ms: 1.04x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 71.8 ms: 1.04x faster                                                       |
| coverage                | 55.3 ms                                                                  | 53.4 ms: 1.04x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 176 ms: 1.03x faster                                                        |
| thrift                  | 487 us                                                                   | 470 us: 1.03x faster                                                        |
| crypto_pyaes            | 48.3 ms                                                                  | 46.7 ms: 1.03x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.80 ms: 1.03x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.63 sec: 1.03x faster                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 35.7 ms: 1.03x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.4 ms: 1.02x faster                                                       |
| sympy_str               | 184 ms                                                                   | 180 ms: 1.02x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 42.6 ms: 1.02x faster                                                       |
| dask                    | 267 ms                                                                   | 262 ms: 1.02x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| xml_etree_parse         | 92.1 ms                                                                  | 90.4 ms: 1.02x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.51 us: 1.01x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 97.7 ms: 1.01x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 51.7 ms: 1.01x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.65 ms: 1.01x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.0 ms: 1.02x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 19.0 us: 1.02x slower                                                       |
| async_tree_memoization  | 374 ms                                                                   | 381 ms: 1.02x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 62.6 ms: 1.02x slower                                                       |
| unpickle                | 8.01 us                                                                  | 8.20 us: 1.02x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 681 us: 1.02x slower                                                        |
| python_startup_no_site  | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 322 ms: 1.03x slower                                                        |
| regex_v8                | 13.5 ms                                                                  | 14.0 ms: 1.04x slower                                                       |
| pidigits                | 147 ms                                                                   | 153 ms: 1.04x slower                                                        |
| comprehensions          | 15.4 us                                                                  | 16.0 us: 1.04x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 76.4 ms: 1.05x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.83 us: 1.05x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 788 ms: 1.06x slower                                                        |
| gc_traversal            | 1.40 ms                                                                  | 1.49 ms: 1.06x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.78 us: 1.06x slower                                                       |
| regex_dna               | 115 ms                                                                   | 125 ms: 1.09x slower                                                        |
| pickle                  | 6.47 us                                                                  | 7.29 us: 1.13x slower                                                       |
| generators              | 33.5 ms                                                                  | 37.8 ms: 1.13x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (5): bench_thread_pool, 2to3, async_generators, sqlglot_parse, coroutines
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
