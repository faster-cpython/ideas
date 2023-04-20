
# Results vs. 3.11.0

- fork: python
- ref: f3909b8bc83675b7ab09
- machine: windows-amd64
- commit hash: f3909b8
- commit date: 2023-04-04
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 206 ms: 1.01x slower                                                     |
| chameleon      | 5.15 ms                                                                  | 5.27 ms: 1.02x slower                                                    |
| docutils       | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                   |
| html5lib       | 38.5 ms                                                                  | 39.8 ms: 1.03x slower                                                    |
| tornado_http   | 91.8 ms                                                                  | 90.1 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 69.8 ms: 1.02x faster                                                    |
| float          | 53.3 ms                                                                  | 52.6 ms: 1.01x faster                                                    |
| pidigits       | 147 ms                                                                   | 147 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.57 ms: 1.04x faster                                                    |
| regex_dna      | 115 ms                                                                   | 120 ms: 1.04x slower                                                     |
| regex_v8       | 13.5 ms                                                                  | 14.3 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|--------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_list      | 2.80 us                                                                  | 2.68 us: 1.05x faster                                                    |
| json_loads         | 13.5 us                                                                  | 13.0 us: 1.04x faster                                                    |
| pickle_pure_python | 203 us                                                                   | 198 us: 1.03x faster                                                     |
| json_dumps         | 7.71 ms                                                                  | 7.60 ms: 1.01x faster                                                    |
| xml_etree_generate | 52.3 ms                                                                  | 51.8 ms: 1.01x faster                                                    |
| xml_etree_process  | 36.6 ms                                                                  | 36.3 ms: 1.01x faster                                                    |
| unpickle           | 8.01 us                                                                  | 7.97 us: 1.01x faster                                                    |
| pickle_list        | 2.70 us                                                                  | 2.78 us: 1.03x slower                                                    |
| pickle             | 6.47 us                                                                  | 6.73 us: 1.04x slower                                                    |
| Geometric mean     | (ref)                                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_iterparse, pickle_dict, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_xml, django_template, mako, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|-------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| spectral_norm           | 71.8 ms                                                                  | 67.6 ms: 1.06x faster                                                    |
| richards                | 32.1 ms                                                                  | 30.4 ms: 1.06x faster                                                    |
| unpickle_list           | 2.80 us                                                                  | 2.68 us: 1.05x faster                                                    |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 10.0 ms: 1.04x faster                                                    |
| json_loads              | 13.5 us                                                                  | 13.0 us: 1.04x faster                                                    |
| regex_effbot            | 1.63 ms                                                                  | 1.57 ms: 1.04x faster                                                    |
| coverage                | 55.3 ms                                                                  | 53.2 ms: 1.04x faster                                                    |
| scimark_sor             | 77.7 ms                                                                  | 75.2 ms: 1.03x faster                                                    |
| sympy_expand            | 298 ms                                                                   | 290 ms: 1.03x faster                                                     |
| pickle_pure_python      | 203 us                                                                   | 198 us: 1.03x faster                                                     |
| async_generators        | 180 ms                                                                   | 176 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 500 ms: 1.02x faster                                                     |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 81.1 ms: 1.02x faster                                                    |
| dask                    | 267 ms                                                                   | 261 ms: 1.02x faster                                                     |
| dulwich_log             | 43.4 ms                                                                  | 42.5 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.58 ms: 1.02x faster                                                    |
| deepcopy_memo           | 25.3 us                                                                  | 24.8 us: 1.02x faster                                                    |
| logging_format          | 7.13 us                                                                  | 6.99 us: 1.02x faster                                                    |
| tornado_http            | 91.8 ms                                                                  | 90.1 ms: 1.02x faster                                                    |
| async_tree_memoization  | 374 ms                                                                   | 368 ms: 1.02x faster                                                     |
| nbody                   | 70.9 ms                                                                  | 69.8 ms: 1.02x faster                                                    |
| raytrace                | 206 ms                                                                   | 203 ms: 1.02x faster                                                     |
| json_dumps              | 7.71 ms                                                                  | 7.60 ms: 1.01x faster                                                    |
| scimark_monte_carlo     | 45.8 ms                                                                  | 45.1 ms: 1.01x faster                                                    |
| float                   | 53.3 ms                                                                  | 52.6 ms: 1.01x faster                                                    |
| logging_silent          | 71.0 ns                                                                  | 70.1 ns: 1.01x faster                                                    |
| sympy_str               | 184 ms                                                                   | 182 ms: 1.01x faster                                                     |
| xml_etree_generate      | 52.3 ms                                                                  | 51.8 ms: 1.01x faster                                                    |
| bench_thread_pool       | 856 us                                                                   | 848 us: 1.01x faster                                                     |
| thrift                  | 487 us                                                                   | 482 us: 1.01x faster                                                     |
| deepcopy_reduce         | 2.06 us                                                                  | 2.04 us: 1.01x faster                                                    |
| deltablue               | 2.68 ms                                                                  | 2.65 ms: 1.01x faster                                                    |
| aiohttp                 | 864 us                                                                   | 857 us: 1.01x faster                                                     |
| docutils                | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                   |
| xml_etree_process       | 36.6 ms                                                                  | 36.3 ms: 1.01x faster                                                    |
| unpickle                | 8.01 us                                                                  | 7.97 us: 1.01x faster                                                    |
| sympy_sum               | 98.9 ms                                                                  | 98.4 ms: 1.01x faster                                                    |
| sympy_integrate         | 13.7 ms                                                                  | 13.6 ms: 1.00x faster                                                    |
| pidigits                | 147 ms                                                                   | 147 ms: 1.00x slower                                                     |
| meteor_contest          | 74.4 ms                                                                  | 74.7 ms: 1.00x slower                                                    |
| flaskblogging           | 2.04 sec                                                                 | 2.05 sec: 1.00x slower                                                   |
| sqlglot_optimize        | 34.5 ms                                                                  | 34.7 ms: 1.01x slower                                                    |
| nqueens                 | 65.1 ms                                                                  | 65.6 ms: 1.01x slower                                                    |
| scimark_lu              | 62.8 ms                                                                  | 63.3 ms: 1.01x slower                                                    |
| logging_simple          | 6.60 us                                                                  | 6.67 us: 1.01x slower                                                    |
| scimark_fft             | 183 ms                                                                   | 185 ms: 1.01x slower                                                     |
| pprint_pformat          | 1.05 sec                                                                 | 1.06 sec: 1.01x slower                                                   |
| sqlglot_normalize       | 189 ms                                                                   | 191 ms: 1.01x slower                                                     |
| 2to3                    | 204 ms                                                                   | 206 ms: 1.01x slower                                                     |
| sqlite_synth            | 1.67 us                                                                  | 1.69 us: 1.01x slower                                                    |
| generators              | 33.5 ms                                                                  | 34.0 ms: 1.01x slower                                                    |
| deepcopy                | 240 us                                                                   | 243 us: 1.01x slower                                                     |
| bench_mp_pool           | 61.2 ms                                                                  | 62.0 ms: 1.01x slower                                                    |
| gc_traversal            | 1.40 ms                                                                  | 1.43 ms: 1.02x slower                                                    |
| go                      | 97.5 ms                                                                  | 99.2 ms: 1.02x slower                                                    |
| coroutines              | 14.8 ms                                                                  | 15.1 ms: 1.02x slower                                                    |
| chameleon               | 5.15 ms                                                                  | 5.27 ms: 1.02x slower                                                    |
| hexiom                  | 4.46 ms                                                                  | 4.56 ms: 1.02x slower                                                    |
| telco                   | 3.93 ms                                                                  | 4.02 ms: 1.02x slower                                                    |
| pycparser               | 686 ms                                                                   | 703 ms: 1.02x slower                                                     |
| pprint_safe_repr        | 512 ms                                                                   | 526 ms: 1.03x slower                                                     |
| pickle_list             | 2.70 us                                                                  | 2.78 us: 1.03x slower                                                    |
| html5lib                | 38.5 ms                                                                  | 39.8 ms: 1.03x slower                                                    |
| chaos                   | 47.3 ms                                                                  | 48.9 ms: 1.03x slower                                                    |
| pickle                  | 6.47 us                                                                  | 6.73 us: 1.04x slower                                                    |
| mdp                     | 1.67 sec                                                                 | 1.74 sec: 1.04x slower                                                   |
| regex_dna               | 115 ms                                                                   | 120 ms: 1.04x slower                                                     |
| regex_v8                | 13.5 ms                                                                  | 14.3 ms: 1.06x slower                                                    |
| asyncio_tcp             | 674 ms                                                                   | 718 ms: 1.07x slower                                                     |
| unpack_sequence         | 43.1 ns                                                                  | 46.0 ns: 1.07x slower                                                    |
| Geometric mean          | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (24): genshi_xml, xml_etree_parse, xml_etree_iterparse, async_tree_io, create_gc_cycles, pyflate, crypto_pyaes, python_startup_no_site, django_template, pickle_dict, regex_compile, comprehensions, unpickle_pure_python, sqlglot_parse, fannkuch, python_startup, sqlglot_transpile, mako, async_tree_none, pathlib, genshi_text, pylint, mypy2, json
