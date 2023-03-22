
# Results vs. 3.11.0

- fork: python
- ref: ed7c3ff15680c1939fad
- machine: windows-amd64
- commit hash: ed7c3ff
- commit date: 2022-09-11
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 5.09 ms: 1.01x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.57 sec: 1.01x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 37.2 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 68.6 ms: 1.03x faster                                                       |
| float          | 53.3 ms                                                                  | 53.9 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.4 ms: 1.01x faster                                                       |
| regex_dna      | 115 ms                                                                   | 115 ms: 1.00x faster                                                        |
| regex_compile  | 89.7 ms                                                                  | 89.5 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|--------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list      | 2.80 us                                                                  | 2.55 us: 1.10x faster                                                       |
| unpickle           | 8.01 us                                                                  | 7.70 us: 1.04x faster                                                       |
| pickle_pure_python | 203 us                                                                   | 197 us: 1.03x faster                                                        |
| pickle_dict        | 18.6 us                                                                  | 18.2 us: 1.02x faster                                                       |
| xml_etree_generate | 52.3 ms                                                                  | 51.2 ms: 1.02x faster                                                       |
| pickle_list        | 2.70 us                                                                  | 2.65 us: 1.02x faster                                                       |
| xml_etree_process  | 36.6 ms                                                                  | 35.9 ms: 1.02x faster                                                       |
| json_dumps         | 7.71 ms                                                                  | 7.66 ms: 1.01x faster                                                       |
| json_loads         | 13.5 us                                                                  | 13.7 us: 1.01x slower                                                       |
| pickle             | 6.47 us                                                                  | 6.60 us: 1.02x slower                                                       |
| Geometric mean     | (ref)                                                                    | 1.02x faster                                                                |

Benchmark hidden because not significant (3): xml_etree_parse, unpickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.5 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text    | 17.3 ms                                                                  | 16.7 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (3): django_template, mako, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list           | 2.80 us                                                                  | 2.55 us: 1.10x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.59 sec: 1.05x faster                                                      |
| richards                | 32.1 ms                                                                  | 30.6 ms: 1.05x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 488 ms: 1.05x faster                                                        |
| unpickle                | 8.01 us                                                                  | 7.70 us: 1.04x faster                                                       |
| coverage                | 55.3 ms                                                                  | 53.2 ms: 1.04x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 16.7 ms: 1.03x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 197 us: 1.03x faster                                                        |
| html5lib                | 38.5 ms                                                                  | 37.2 ms: 1.03x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 68.6 ms: 1.03x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 44.6 ms: 1.03x faster                                                       |
| async_generators        | 180 ms                                                                   | 176 ms: 1.03x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 2.00 us: 1.03x faster                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.2 us: 1.02x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.61 ms: 1.02x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.97 us: 1.02x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 51.2 ms: 1.02x faster                                                       |
| pickle_list             | 2.70 us                                                                  | 2.65 us: 1.02x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 35.9 ms: 1.02x faster                                                       |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 10.3 ms: 1.02x faster                                                       |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 81.7 ms: 1.02x faster                                                       |
| async_tree_memoization  | 374 ms                                                                   | 368 ms: 1.02x faster                                                        |
| sympy_expand            | 298 ms                                                                   | 294 ms: 1.02x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 186 ms: 1.02x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.57 sec: 1.01x faster                                                      |
| comprehensions          | 15.4 us                                                                  | 15.2 us: 1.01x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 5.09 ms: 1.01x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 34.0 ms: 1.01x faster                                                       |
| pathlib                 | 72.9 ms                                                                  | 72.1 ms: 1.01x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 920 us: 1.01x faster                                                        |
| sympy_str               | 184 ms                                                                   | 182 ms: 1.01x faster                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.12 ms: 1.01x faster                                                       |
| async_tree_none         | 313 ms                                                                   | 310 ms: 1.01x faster                                                        |
| sympy_integrate         | 13.7 ms                                                                  | 13.5 ms: 1.01x faster                                                       |
| 2to3                    | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| regex_v8                | 13.5 ms                                                                  | 13.4 ms: 1.01x faster                                                       |
| aiohttp                 | 864 us                                                                   | 857 us: 1.01x faster                                                        |
| bench_thread_pool       | 856 us                                                                   | 849 us: 1.01x faster                                                        |
| sympy_sum               | 98.9 ms                                                                  | 98.2 ms: 1.01x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 64.6 ms: 1.01x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 7.66 ms: 1.01x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.57 us: 1.01x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.91 ms: 1.00x faster                                                       |
| deepcopy                | 240 us                                                                   | 239 us: 1.00x faster                                                        |
| regex_dna               | 115 ms                                                                   | 115 ms: 1.00x faster                                                        |
| regex_compile           | 89.7 ms                                                                  | 89.5 ms: 1.00x faster                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.41 ms: 1.00x slower                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 48.5 ms: 1.00x slower                                                       |
| dulwich_log             | 43.4 ms                                                                  | 43.6 ms: 1.00x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 14.9 ms: 1.00x slower                                                       |
| hexiom                  | 4.46 ms                                                                  | 4.48 ms: 1.00x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.5 ms: 1.01x slower                                                       |
| scimark_lu              | 62.8 ms                                                                  | 63.4 ms: 1.01x slower                                                       |
| json_loads              | 13.5 us                                                                  | 13.7 us: 1.01x slower                                                       |
| thrift                  | 487 us                                                                   | 491 us: 1.01x slower                                                        |
| float                   | 53.3 ms                                                                  | 53.9 ms: 1.01x slower                                                       |
| chaos                   | 47.3 ms                                                                  | 48.0 ms: 1.02x slower                                                       |
| spectral_norm           | 71.8 ms                                                                  | 73.2 ms: 1.02x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.60 us: 1.02x slower                                                       |
| raytrace                | 206 ms                                                                   | 211 ms: 1.02x slower                                                        |
| scimark_fft             | 183 ms                                                                   | 189 ms: 1.04x slower                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.81 ms: 1.07x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (31): json, unpack_sequence, pylint, xml_etree_parse, scimark_sor, async_tree_io, pycparser, unpickle_pure_python, python_startup_no_site, logging_silent, django_template, meteor_contest, dask, generators, go, pidigits, bench_mp_pool, mypy2, sqlite_synth, pprint_safe_repr, xml_etree_iterparse, pprint_pformat, flaskblogging, pyflate, create_gc_cycles, deepcopy_memo, tornado_http, mako, fannkuch, genshi_xml, asyncio_tcp
