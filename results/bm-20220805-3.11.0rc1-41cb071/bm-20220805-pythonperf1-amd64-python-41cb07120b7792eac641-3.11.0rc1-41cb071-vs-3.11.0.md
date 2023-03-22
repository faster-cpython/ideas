
# Results vs. 3.11.0

- fork: python
- ref: 41cb07120b7792eac641
- machine: windows-amd64
- commit hash: 41cb071
- commit date: 2022-08-05
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 5.05 ms: 1.02x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 90.9 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 68.3 ms: 1.04x faster                                                       |
| float          | 53.3 ms                                                                  | 52.9 ms: 1.01x faster                                                       |
| pidigits       | 147 ms                                                                   | 146 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 89.4 ms: 1.00x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.66 ms: 1.02x slower                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.1 ms: 1.05x slower                                                       |
| regex_dna      | 115 ms                                                                   | 123 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list        | 2.80 us                                                                  | 2.64 us: 1.06x faster                                                       |
| pickle_list          | 2.70 us                                                                  | 2.57 us: 1.05x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 202 us: 1.01x faster                                                        |
| pickle               | 6.47 us                                                                  | 6.44 us: 1.00x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 150 us: 1.00x slower                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 36.7 ms: 1.00x slower                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 52.6 ms: 1.01x slower                                                       |
| unpickle             | 8.01 us                                                                  | 8.11 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 62.9 ms: 1.02x slower                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 94.8 ms: 1.03x slower                                                       |
| json_loads           | 13.5 us                                                                  | 14.0 us: 1.04x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.00x faster                                                                |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.2 ms: 1.01x faster                                                       |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text    | 17.3 ms                                                                  | 16.7 ms: 1.03x faster                                                       |
| mako           | 7.20 ms                                                                  | 7.26 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json                    | 3.20 ms                                                                  | 2.94 ms: 1.09x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.64 us: 1.06x faster                                                       |
| pickle_list             | 2.70 us                                                                  | 2.57 us: 1.05x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.60 sec: 1.05x faster                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 491 ms: 1.04x faster                                                        |
| nbody                   | 70.9 ms                                                                  | 68.3 ms: 1.04x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.37 us: 1.04x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.90 us: 1.03x faster                                                       |
| fannkuch                | 255 ms                                                                   | 247 ms: 1.03x faster                                                        |
| genshi_text             | 17.3 ms                                                                  | 16.7 ms: 1.03x faster                                                       |
| coverage                | 55.3 ms                                                                  | 53.6 ms: 1.03x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 44.4 ms: 1.03x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 41.9 ns: 1.03x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 290 ms: 1.03x faster                                                        |
| richards                | 32.1 ms                                                                  | 31.3 ms: 1.03x faster                                                       |
| async_generators        | 180 ms                                                                   | 176 ms: 1.02x faster                                                        |
| sympy_str               | 184 ms                                                                   | 180 ms: 1.02x faster                                                        |
| chameleon               | 5.15 ms                                                                  | 5.05 ms: 1.02x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 97.0 ms: 1.02x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.63 ms: 1.02x faster                                                       |
| async_tree_memoization  | 374 ms                                                                   | 368 ms: 1.02x faster                                                        |
| meteor_contest          | 74.4 ms                                                                  | 73.3 ms: 1.01x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.87 ms: 1.01x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 64.2 ms: 1.01x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.5 ms: 1.01x faster                                                       |
| raytrace                | 206 ms                                                                   | 204 ms: 1.01x faster                                                        |
| comprehensions          | 15.4 us                                                                  | 15.2 us: 1.01x faster                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                       |
| async_tree_none         | 313 ms                                                                   | 310 ms: 1.01x faster                                                        |
| tornado_http            | 91.8 ms                                                                  | 90.9 ms: 1.01x faster                                                       |
| thrift                  | 487 us                                                                   | 482 us: 1.01x faster                                                        |
| 2to3                    | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| float                   | 53.3 ms                                                                  | 52.9 ms: 1.01x faster                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.2 ms: 1.01x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.61 ms: 1.01x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 202 us: 1.01x faster                                                        |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 10.4 ms: 1.01x faster                                                       |
| deepcopy                | 240 us                                                                   | 238 us: 1.01x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 2.05 us: 1.01x faster                                                       |
| pickle                  | 6.47 us                                                                  | 6.44 us: 1.00x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 1.04 sec: 1.00x faster                                                      |
| sqlglot_parse           | 929 us                                                                   | 925 us: 1.00x faster                                                        |
| pidigits                | 147 ms                                                                   | 146 ms: 1.00x faster                                                        |
| regex_compile           | 89.7 ms                                                                  | 89.4 ms: 1.00x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 43.3 ms: 1.00x faster                                                       |
| flaskblogging           | 2.04 sec                                                                 | 2.05 sec: 1.00x slower                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 513 ms: 1.00x slower                                                        |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 83.4 ms: 1.00x slower                                                       |
| unpickle_pure_python    | 150 us                                                                   | 150 us: 1.00x slower                                                        |
| xml_etree_process       | 36.6 ms                                                                  | 36.7 ms: 1.00x slower                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 52.6 ms: 1.01x slower                                                       |
| generators              | 33.5 ms                                                                  | 33.8 ms: 1.01x slower                                                       |
| mako                    | 7.20 ms                                                                  | 7.26 ms: 1.01x slower                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 48.7 ms: 1.01x slower                                                       |
| unpickle                | 8.01 us                                                                  | 8.11 us: 1.01x slower                                                       |
| logging_silent          | 71.0 ns                                                                  | 71.9 ns: 1.01x slower                                                       |
| scimark_lu              | 62.8 ms                                                                  | 63.7 ms: 1.01x slower                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.66 ms: 1.02x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 62.9 ms: 1.02x slower                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 94.8 ms: 1.03x slower                                                       |
| go                      | 97.5 ms                                                                  | 101 ms: 1.03x slower                                                        |
| json_loads              | 13.5 us                                                                  | 14.0 us: 1.04x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 14.1 ms: 1.05x slower                                                       |
| chaos                   | 47.3 ms                                                                  | 49.6 ms: 1.05x slower                                                       |
| regex_dna               | 115 ms                                                                   | 123 ms: 1.07x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (29): asyncio_tcp, genshi_xml, async_tree_io, django_template, pathlib, scimark_sor, aiohttp, pylint, mypy2, coroutines, html5lib, docutils, python_startup, create_gc_cycles, scimark_fft, deepcopy_memo, hexiom, sqlglot_transpile, gc_traversal, spectral_norm, bench_thread_pool, dask, sqlglot_optimize, pyflate, sqlglot_normalize, bench_mp_pool, json_dumps, sqlite_synth, pycparser
