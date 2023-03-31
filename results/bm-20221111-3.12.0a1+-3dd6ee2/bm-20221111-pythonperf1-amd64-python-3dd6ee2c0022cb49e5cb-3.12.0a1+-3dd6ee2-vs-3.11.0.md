
# Results vs. 3.11.0

- fork: python
- ref: 3dd6ee2c0022cb49e5cb
- machine: windows-amd64
- commit hash: 3dd6ee2
- commit date: 2022-11-11
- overall geometric mean: 1.05x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.68 ms: 1.10x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 36.8 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 64.7 ms: 1.10x faster                                                       |
| float          | 53.3 ms                                                                  | 50.8 ms: 1.05x faster                                                       |
| pidigits       | 147 ms                                                                   | 150 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 84.4 ms: 1.06x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.9 ms: 1.03x slower                                                       |
| regex_dna      | 115 ms                                                                   | 121 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.19 ms: 1.49x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 131 us: 1.14x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 189 us: 1.08x faster                                                        |
| unpickle_list        | 2.80 us                                                                  | 2.65 us: 1.06x faster                                                       |
| json_loads           | 13.5 us                                                                  | 13.0 us: 1.04x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 88.9 ms: 1.04x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.7 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.7 ms: 1.01x faster                                                       |
| pickle_list          | 2.70 us                                                                  | 2.79 us: 1.03x slower                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.4 us: 1.04x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 64.8 ms: 1.05x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.90 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.5 ms: 1.01x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.8 ms: 1.17x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 33.2 ms: 1.14x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.37 ms: 1.13x faster                                                       |
| django_template | 23.9 ms                                                                  | 22.4 ms: 1.06x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.13x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 7.71 ms                                                                  | 5.19 ms: 1.49x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 30.6 ns: 1.41x faster                                                       |
| mypy2                   | 276 ms                                                                   | 221 ms: 1.25x faster                                                        |
| richards                | 32.1 ms                                                                  | 26.8 ms: 1.20x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.70 ms: 1.19x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 60.7 ns: 1.17x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.29 ms: 1.17x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 14.8 ms: 1.17x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.6 ms: 1.15x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 33.2 ms: 1.14x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 131 us: 1.14x faster                                                        |
| mako                    | 7.20 ms                                                                  | 6.37 ms: 1.13x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 63.6 ms: 1.13x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 22.6 us: 1.12x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 69.9 ms: 1.11x faster                                                       |
| go                      | 97.5 ms                                                                  | 88.3 ms: 1.10x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.68 ms: 1.10x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 64.7 ms: 1.10x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.40 ms: 1.10x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 57.6 ms: 1.09x faster                                                       |
| fannkuch                | 255 ms                                                                   | 235 ms: 1.09x faster                                                        |
| raytrace                | 206 ms                                                                   | 190 ms: 1.09x faster                                                        |
| scimark_fft             | 183 ms                                                                   | 169 ms: 1.08x faster                                                        |
| pyflate                 | 302 ms                                                                   | 280 ms: 1.08x faster                                                        |
| pickle_pure_python      | 203 us                                                                   | 189 us: 1.08x faster                                                        |
| deepcopy                | 240 us                                                                   | 223 us: 1.08x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 4.15 ms: 1.07x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 478 ms: 1.07x faster                                                        |
| pprint_pformat          | 1.05 sec                                                                 | 985 ms: 1.07x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.93 us: 1.06x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 84.4 ms: 1.06x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 45.4 ms: 1.06x faster                                                       |
| django_template         | 23.9 ms                                                                  | 22.4 ms: 1.06x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 178 ms: 1.06x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.58 sec: 1.06x faster                                                      |
| sympy_str               | 184 ms                                                                   | 174 ms: 1.06x faster                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.65 us: 1.06x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.2 ms: 1.05x faster                                                       |
| pycparser               | 686 ms                                                                   | 653 ms: 1.05x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 45.1 ms: 1.05x faster                                                       |
| float                   | 53.3 ms                                                                  | 50.8 ms: 1.05x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 62.1 ms: 1.05x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 36.8 ms: 1.05x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 286 ms: 1.04x faster                                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 33.0 ms: 1.04x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.0 us: 1.04x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 71.5 ms: 1.04x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.85 us: 1.04x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 88.9 ms: 1.04x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.40 us: 1.03x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.83 ms: 1.03x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.10 ms: 1.03x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| sqlglot_parse           | 929 us                                                                   | 908 us: 1.02x faster                                                        |
| xml_etree_process       | 36.6 ms                                                                  | 35.7 ms: 1.02x faster                                                       |
| dask                    | 267 ms                                                                   | 261 ms: 1.02x faster                                                        |
| sympy_integrate         | 13.7 ms                                                                  | 13.5 ms: 1.01x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 51.7 ms: 1.01x faster                                                       |
| 2to3                    | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| coroutines              | 14.8 ms                                                                  | 14.9 ms: 1.01x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.5 ms: 1.01x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 73.8 ms: 1.01x slower                                                       |
| async_generators        | 180 ms                                                                   | 183 ms: 1.01x slower                                                        |
| async_tree_memoization  | 374 ms                                                                   | 382 ms: 1.02x slower                                                        |
| pidigits                | 147 ms                                                                   | 150 ms: 1.02x slower                                                        |
| comprehensions          | 15.4 us                                                                  | 15.8 us: 1.03x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.9 ms: 1.03x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 63.0 ms: 1.03x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.79 us: 1.03x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 689 us: 1.03x slower                                                        |
| pickle_dict             | 18.6 us                                                                  | 19.4 us: 1.04x slower                                                       |
| regex_dna               | 115 ms                                                                   | 121 ms: 1.05x slower                                                        |
| xml_etree_iterparse     | 61.8 ms                                                                  | 64.8 ms: 1.05x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.76 us: 1.05x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.48 ms: 1.05x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 334 ms: 1.07x slower                                                        |
| pickle                  | 6.47 us                                                                  | 6.90 us: 1.07x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 804 ms: 1.08x slower                                                        |
| generators              | 33.5 ms                                                                  | 37.3 ms: 1.11x slower                                                       |
| asyncio_tcp             | 674 ms                                                                   | 765 ms: 1.14x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (7): bench_thread_pool, thrift, sympy_sum, unpickle, coverage, tornado_http, async_tree_cpu_io_mixed
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
