
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 06249ec
- commit date: 2023-04-01
- overall geometric mean: 1.07x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 208 ms: 1.02x slower                                        |
| chameleon      | 5.15 ms                                                                  | 4.75 ms: 1.09x faster                                       |
| docutils       | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                      |
| html5lib       | 38.5 ms                                                                  | 36.4 ms: 1.06x faster                                       |
| tornado_http   | 91.8 ms                                                                  | 88.0 ms: 1.04x faster                                       |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 61.6 ms: 1.15x faster                                       |
| float          | 53.3 ms                                                                  | 50.0 ms: 1.07x faster                                       |
| pidigits       | 147 ms                                                                   | 146 ms: 1.00x faster                                        |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.52 ms: 1.07x faster                                       |
| regex_compile  | 89.7 ms                                                                  | 84.0 ms: 1.07x faster                                       |
| regex_v8       | 13.5 ms                                                                  | 13.2 ms: 1.02x faster                                       |
| regex_dna      | 115 ms                                                                   | 118 ms: 1.03x slower                                        |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.27 ms: 1.46x faster                                       |
| unpickle_pure_python | 150 us                                                                   | 126 us: 1.19x faster                                        |
| pickle_pure_python   | 203 us                                                                   | 185 us: 1.10x faster                                        |
| xml_etree_process    | 36.6 ms                                                                  | 35.9 ms: 1.02x faster                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 52.7 ms: 1.01x slower                                       |
| json_loads           | 13.5 us                                                                  | 13.7 us: 1.01x slower                                       |
| pickle_dict          | 18.6 us                                                                  | 19.1 us: 1.02x slower                                       |
| pickle_list          | 2.70 us                                                                  | 2.89 us: 1.07x slower                                       |
| pickle               | 6.47 us                                                                  | 7.08 us: 1.09x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.04x faster                                                |

Benchmark hidden because not significant (4): xml_etree_iterparse, xml_etree_parse, unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                       |
| python_startup         | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 30.7 ms: 1.24x faster                                       |
| genshi_text     | 17.3 ms                                                                  | 14.0 ms: 1.24x faster                                       |
| mako            | 7.20 ms                                                                  | 6.19 ms: 1.16x faster                                       |
| django_template | 23.9 ms                                                                  | 21.4 ms: 1.12x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.19x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| generators              | 33.5 ms                                                                  | 21.2 ms: 1.59x faster                                       |
| unpack_sequence         | 43.1 ns                                                                  | 28.1 ns: 1.53x faster                                       |
| json_dumps              | 7.71 ms                                                                  | 5.27 ms: 1.46x faster                                       |
| deltablue               | 2.68 ms                                                                  | 1.95 ms: 1.37x faster                                       |
| asyncio_tcp             | 674 ms                                                                   | 495 ms: 1.36x faster                                        |
| logging_silent          | 71.0 ns                                                                  | 54.3 ns: 1.31x faster                                       |
| richards                | 32.1 ms                                                                  | 25.5 ms: 1.26x faster                                       |
| mypy2                   | 276 ms                                                                   | 220 ms: 1.25x faster                                        |
| spectral_norm           | 71.8 ms                                                                  | 57.2 ms: 1.25x faster                                       |
| genshi_xml              | 38.0 ms                                                                  | 30.7 ms: 1.24x faster                                       |
| genshi_text             | 17.3 ms                                                                  | 14.0 ms: 1.24x faster                                       |
| scimark_lu              | 62.8 ms                                                                  | 52.6 ms: 1.20x faster                                       |
| go                      | 97.5 ms                                                                  | 81.9 ms: 1.19x faster                                       |
| unpickle_pure_python    | 150 us                                                                   | 126 us: 1.19x faster                                        |
| raytrace                | 206 ms                                                                   | 174 ms: 1.18x faster                                        |
| deepcopy_memo           | 25.3 us                                                                  | 21.6 us: 1.17x faster                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.24 ms: 1.17x faster                                       |
| mdp                     | 1.67 sec                                                                 | 1.43 sec: 1.17x faster                                      |
| mako                    | 7.20 ms                                                                  | 6.19 ms: 1.16x faster                                       |
| json                    | 3.20 ms                                                                  | 2.77 ms: 1.16x faster                                       |
| nbody                   | 70.9 ms                                                                  | 61.6 ms: 1.15x faster                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.9 ms: 1.15x faster                                       |
| hexiom                  | 4.46 ms                                                                  | 3.90 ms: 1.14x faster                                       |
| chaos                   | 47.3 ms                                                                  | 41.5 ms: 1.14x faster                                       |
| nqueens                 | 65.1 ms                                                                  | 57.4 ms: 1.13x faster                                       |
| django_template         | 23.9 ms                                                                  | 21.4 ms: 1.12x faster                                       |
| scimark_fft             | 183 ms                                                                   | 165 ms: 1.11x faster                                        |
| pickle_pure_python      | 203 us                                                                   | 185 us: 1.10x faster                                        |
| fannkuch                | 255 ms                                                                   | 232 ms: 1.10x faster                                        |
| deepcopy                | 240 us                                                                   | 218 us: 1.10x faster                                        |
| sqlglot_normalize       | 189 ms                                                                   | 173 ms: 1.09x faster                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.7 ms: 1.09x faster                                       |
| pprint_pformat          | 1.05 sec                                                                 | 966 ms: 1.09x faster                                        |
| chameleon               | 5.15 ms                                                                  | 4.75 ms: 1.09x faster                                       |
| logging_simple          | 6.60 us                                                                  | 6.11 us: 1.08x faster                                       |
| coroutines              | 14.8 ms                                                                  | 13.8 ms: 1.08x faster                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 44.9 ms: 1.08x faster                                       |
| sympy_expand            | 298 ms                                                                   | 278 ms: 1.07x faster                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.91 us: 1.07x faster                                       |
| pprint_safe_repr        | 512 ms                                                                   | 477 ms: 1.07x faster                                        |
| regex_effbot            | 1.63 ms                                                                  | 1.52 ms: 1.07x faster                                       |
| sqlglot_parse           | 929 us                                                                   | 869 us: 1.07x faster                                        |
| logging_format          | 7.13 us                                                                  | 6.68 us: 1.07x faster                                       |
| regex_compile           | 89.7 ms                                                                  | 84.0 ms: 1.07x faster                                       |
| float                   | 53.3 ms                                                                  | 50.0 ms: 1.07x faster                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 480 ms: 1.07x faster                                        |
| sympy_integrate         | 13.7 ms                                                                  | 12.9 ms: 1.06x faster                                       |
| html5lib                | 38.5 ms                                                                  | 36.4 ms: 1.06x faster                                       |
| pyflate                 | 302 ms                                                                   | 286 ms: 1.05x faster                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.07 ms: 1.05x faster                                       |
| coverage                | 55.3 ms                                                                  | 52.8 ms: 1.05x faster                                       |
| tornado_http            | 91.8 ms                                                                  | 88.0 ms: 1.04x faster                                       |
| meteor_contest          | 74.4 ms                                                                  | 71.4 ms: 1.04x faster                                       |
| sympy_str               | 184 ms                                                                   | 177 ms: 1.04x faster                                        |
| docutils                | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                      |
| dulwich_log             | 43.4 ms                                                                  | 42.3 ms: 1.03x faster                                       |
| regex_v8                | 13.5 ms                                                                  | 13.2 ms: 1.02x faster                                       |
| pycparser               | 686 ms                                                                   | 672 ms: 1.02x faster                                        |
| xml_etree_process       | 36.6 ms                                                                  | 35.9 ms: 1.02x faster                                       |
| scimark_sor             | 77.7 ms                                                                  | 76.7 ms: 1.01x faster                                       |
| comprehensions          | 15.4 us                                                                  | 15.2 us: 1.01x faster                                       |
| pidigits                | 147 ms                                                                   | 146 ms: 1.00x faster                                        |
| sympy_sum               | 98.9 ms                                                                  | 99.7 ms: 1.01x slower                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 52.7 ms: 1.01x slower                                       |
| json_loads              | 13.5 us                                                                  | 13.7 us: 1.01x slower                                       |
| async_tree_none         | 313 ms                                                                   | 318 ms: 1.02x slower                                        |
| 2to3                    | 204 ms                                                                   | 208 ms: 1.02x slower                                        |
| python_startup_no_site  | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                       |
| pickle_dict             | 18.6 us                                                                  | 19.1 us: 1.02x slower                                       |
| regex_dna               | 115 ms                                                                   | 118 ms: 1.03x slower                                        |
| python_startup          | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                       |
| async_tree_io           | 744 ms                                                                   | 773 ms: 1.04x slower                                        |
| create_gc_cycles        | 666 us                                                                   | 695 us: 1.04x slower                                        |
| pickle_list             | 2.70 us                                                                  | 2.89 us: 1.07x slower                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.51 ms: 1.08x slower                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 67.0 ms: 1.09x slower                                       |
| pickle                  | 6.47 us                                                                  | 7.08 us: 1.09x slower                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.87 us: 1.12x slower                                       |
| pathlib                 | 72.9 ms                                                                  | 86.3 ms: 1.18x slower                                       |
| async_generators        | 180 ms                                                                   | 215 ms: 1.19x slower                                        |
| dask                    | 267 ms                                                                   | 362 ms: 1.36x slower                                        |
| Geometric mean          | (ref)                                                                    | 1.07x faster                                                |

Benchmark hidden because not significant (8): async_tree_memoization, bench_thread_pool, xml_etree_iterparse, xml_etree_parse, telco, unpickle, thrift, unpickle_list
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
