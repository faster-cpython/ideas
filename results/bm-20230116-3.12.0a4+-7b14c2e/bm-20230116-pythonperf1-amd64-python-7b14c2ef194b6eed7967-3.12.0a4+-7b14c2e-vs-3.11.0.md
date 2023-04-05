
# Results vs. 3.11.0

- fork: python
- ref: 7b14c2ef194b6eed7967
- machine: windows-amd64
- commit hash: 7b14c2e
- commit date: 2023-01-16
- overall geometric mean: 1.10x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 200 ms: 1.02x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.49 ms: 1.15x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.53 sec: 1.04x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 33.0 ms: 1.17x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 58.5 ms: 1.21x faster                                                       |
| float          | 53.3 ms                                                                  | 47.9 ms: 1.11x faster                                                       |
| pidigits       | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 78.3 ms: 1.15x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.61 ms: 1.02x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| regex_dna      | 115 ms                                                                   | 124 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.24 ms: 1.47x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 119 us: 1.26x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 173 us: 1.18x faster                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 33.9 ms: 1.08x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 50.0 ms: 1.05x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.71 us: 1.03x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 89.1 ms: 1.03x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.0 us: 1.02x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.5 ms: 1.03x slower                                                       |
| json_loads           | 13.5 us                                                                  | 14.0 us: 1.03x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.84 us: 1.06x slower                                                       |
| unpickle             | 8.01 us                                                                  | 8.82 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.9 ms: 1.25x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 31.0 ms: 1.23x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.12 ms: 1.18x faster                                                       |
| django_template | 23.9 ms                                                                  | 20.4 ms: 1.17x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.20x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 26.4 ns: 1.63x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.24 ms: 1.47x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 475 ms: 1.42x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 1.93 ms: 1.38x faster                                                       |
| richards                | 32.1 ms                                                                  | 24.1 ms: 1.33x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 54.9 ns: 1.29x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 19.7 us: 1.28x faster                                                       |
| mypy2                   | 276 ms                                                                   | 216 ms: 1.28x faster                                                        |
| scimark_sor             | 77.7 ms                                                                  | 61.1 ms: 1.27x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 119 us: 1.26x faster                                                        |
| genshi_text             | 17.3 ms                                                                  | 13.9 ms: 1.25x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 37.3 ms: 1.23x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 31.0 ms: 1.23x faster                                                       |
| raytrace                | 206 ms                                                                   | 168 ms: 1.22x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 3.67 ms: 1.22x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 59.2 ms: 1.21x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 58.5 ms: 1.21x faster                                                       |
| go                      | 97.5 ms                                                                  | 81.1 ms: 1.20x faster                                                       |
| deepcopy                | 240 us                                                                   | 201 us: 1.19x faster                                                        |
| fannkuch                | 255 ms                                                                   | 214 ms: 1.19x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.21 ms: 1.19x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 55.3 ms: 1.18x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 173 us: 1.18x faster                                                        |
| mako                    | 7.20 ms                                                                  | 6.12 ms: 1.18x faster                                                       |
| django_template         | 23.9 ms                                                                  | 20.4 ms: 1.17x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.74 ms: 1.17x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 33.0 ms: 1.17x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.49 ms: 1.15x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.80 us: 1.15x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 78.3 ms: 1.15x faster                                                       |
| pyflate                 | 302 ms                                                                   | 265 ms: 1.14x faster                                                        |
| logging_simple          | 6.60 us                                                                  | 5.80 us: 1.14x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 450 ms: 1.14x faster                                                        |
| scimark_fft             | 183 ms                                                                   | 161 ms: 1.13x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 167 ms: 1.13x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 41.8 ms: 1.13x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 933 ms: 1.13x faster                                                        |
| scimark_lu              | 62.8 ms                                                                  | 55.8 ms: 1.13x faster                                                       |
| float                   | 53.3 ms                                                                  | 47.9 ms: 1.11x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.44 us: 1.11x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.5 ms: 1.10x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 273 ms: 1.09x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.53 sec: 1.09x faster                                                      |
| sqlglot_parse           | 929 us                                                                   | 858 us: 1.08x faster                                                        |
| pycparser               | 686 ms                                                                   | 634 ms: 1.08x faster                                                        |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 474 ms: 1.08x faster                                                        |
| xml_etree_process       | 36.6 ms                                                                  | 33.9 ms: 1.08x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 69.2 ms: 1.07x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.06 ms: 1.07x faster                                                       |
| sympy_str               | 184 ms                                                                   | 172 ms: 1.07x faster                                                        |
| async_tree_memoization  | 374 ms                                                                   | 351 ms: 1.07x faster                                                        |
| crypto_pyaes            | 48.3 ms                                                                  | 46.0 ms: 1.05x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.75 ms: 1.05x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 50.0 ms: 1.05x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.1 ms: 1.05x faster                                                       |
| coverage                | 55.3 ms                                                                  | 53.1 ms: 1.04x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 95.0 ms: 1.04x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.53 sec: 1.04x faster                                                      |
| dask                    | 267 ms                                                                   | 256 ms: 1.04x faster                                                        |
| async_generators        | 180 ms                                                                   | 173 ms: 1.04x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 41.9 ms: 1.04x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.71 us: 1.03x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 89.1 ms: 1.03x faster                                                       |
| thrift                  | 487 us                                                                   | 474 us: 1.03x faster                                                        |
| 2to3                    | 204 ms                                                                   | 200 ms: 1.02x faster                                                        |
| bench_thread_pool       | 856 us                                                                   | 839 us: 1.02x faster                                                        |
| async_tree_none         | 313 ms                                                                   | 307 ms: 1.02x faster                                                        |
| regex_effbot            | 1.63 ms                                                                  | 1.61 ms: 1.02x faster                                                       |
| comprehensions          | 15.4 us                                                                  | 15.1 us: 1.02x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.6 ms: 1.01x faster                                                       |
| create_gc_cycles        | 666 us                                                                   | 670 us: 1.01x slower                                                        |
| python_startup          | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.43 ms: 1.02x slower                                                       |
| generators              | 33.5 ms                                                                  | 34.2 ms: 1.02x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 19.0 us: 1.02x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.5 ms: 1.03x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 74.9 ms: 1.03x slower                                                       |
| pidigits                | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 63.1 ms: 1.03x slower                                                       |
| json_loads              | 13.5 us                                                                  | 14.0 us: 1.03x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 768 ms: 1.03x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.76 us: 1.05x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.84 us: 1.06x slower                                                       |
| regex_dna               | 115 ms                                                                   | 124 ms: 1.08x slower                                                        |
| unpickle                | 8.01 us                                                                  | 8.82 us: 1.10x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.10x faster                                                                |

Benchmark hidden because not significant (2): tornado_http, pickle_list
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
