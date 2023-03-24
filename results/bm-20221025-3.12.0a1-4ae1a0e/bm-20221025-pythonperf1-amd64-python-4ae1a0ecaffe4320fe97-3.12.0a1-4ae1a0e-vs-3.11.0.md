
# Results vs. 3.11.0

- fork: python
- ref: 4ae1a0ecaffe4320fe97
- machine: windows-amd64
- commit hash: 4ae1a0e
- commit date: 2022-10-25
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 202 ms: 1.01x faster                                                       |
| chameleon      | 5.15 ms                                                                  | 4.99 ms: 1.03x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 38.1 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 67.2 ms: 1.06x faster                                                      |
| pidigits       | 147 ms                                                                   | 148 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 86.3 ms: 1.04x faster                                                      |
| regex_v8       | 13.5 ms                                                                  | 13.7 ms: 1.01x slower                                                      |
| regex_dna      | 115 ms                                                                   | 119 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                               |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.62 ms: 1.37x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.60 us: 1.08x faster                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 86.8 ms: 1.06x faster                                                      |
| unpickle_pure_python | 150 us                                                                   | 143 us: 1.05x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 196 us: 1.04x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 50.5 ms: 1.03x faster                                                      |
| pickle_list          | 2.70 us                                                                  | 2.64 us: 1.03x faster                                                      |
| pickle_dict          | 18.6 us                                                                  | 18.2 us: 1.02x faster                                                      |
| xml_etree_process    | 36.6 ms                                                                  | 36.3 ms: 1.01x faster                                                      |
| pickle               | 6.47 us                                                                  | 6.55 us: 1.01x slower                                                      |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.6 ms: 1.03x slower                                                      |
| unpickle             | 8.01 us                                                                  | 8.87 us: 1.11x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.04x faster                                                               |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 7.20 ms                                                                  | 6.93 ms: 1.04x faster                                                      |
| genshi_text    | 17.3 ms                                                                  | 17.1 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps              | 7.71 ms                                                                  | 5.62 ms: 1.37x faster                                                      |
| mypy2                   | 276 ms                                                                   | 218 ms: 1.27x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.77 ms: 1.15x faster                                                      |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.37 ms: 1.11x faster                                                      |
| unpickle_list           | 2.80 us                                                                  | 2.60 us: 1.08x faster                                                      |
| fannkuch                | 255 ms                                                                   | 238 ms: 1.07x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.51 ms: 1.07x faster                                                      |
| xml_etree_parse         | 92.1 ms                                                                  | 86.8 ms: 1.06x faster                                                      |
| coverage                | 55.3 ms                                                                  | 52.1 ms: 1.06x faster                                                      |
| nbody                   | 70.9 ms                                                                  | 67.2 ms: 1.06x faster                                                      |
| mdp                     | 1.67 sec                                                                 | 1.59 sec: 1.05x faster                                                     |
| scimark_sor             | 77.7 ms                                                                  | 73.8 ms: 1.05x faster                                                      |
| pprint_pformat          | 1.05 sec                                                                 | 1.00 sec: 1.05x faster                                                     |
| unpickle_pure_python    | 150 us                                                                   | 143 us: 1.05x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 43.8 ms: 1.05x faster                                                      |
| regex_compile           | 89.7 ms                                                                  | 86.3 ms: 1.04x faster                                                      |
| go                      | 97.5 ms                                                                  | 93.8 ms: 1.04x faster                                                      |
| pickle_pure_python      | 203 us                                                                   | 196 us: 1.04x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.93 ms: 1.04x faster                                                      |
| richards                | 32.1 ms                                                                  | 31.0 ms: 1.04x faster                                                      |
| meteor_contest          | 74.4 ms                                                                  | 71.8 ms: 1.04x faster                                                      |
| xml_etree_generate      | 52.3 ms                                                                  | 50.5 ms: 1.03x faster                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 495 ms: 1.03x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.99 ms: 1.03x faster                                                      |
| logging_silent          | 71.0 ns                                                                  | 68.8 ns: 1.03x faster                                                      |
| pickle_list             | 2.70 us                                                                  | 2.64 us: 1.03x faster                                                      |
| deepcopy_memo           | 25.3 us                                                                  | 24.7 us: 1.02x faster                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 47.2 ms: 1.02x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 18.2 us: 1.02x faster                                                      |
| sympy_integrate         | 13.7 ms                                                                  | 13.4 ms: 1.02x faster                                                      |
| telco                   | 3.93 ms                                                                  | 3.85 ms: 1.02x faster                                                      |
| deepcopy                | 240 us                                                                   | 235 us: 1.02x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 42.3 ns: 1.02x faster                                                      |
| chaos                   | 47.3 ms                                                                  | 46.5 ms: 1.02x faster                                                      |
| pyflate                 | 302 ms                                                                   | 297 ms: 1.02x faster                                                       |
| bench_thread_pool       | 856 us                                                                   | 844 us: 1.01x faster                                                       |
| raytrace                | 206 ms                                                                   | 204 ms: 1.01x faster                                                       |
| 2to3                    | 204 ms                                                                   | 202 ms: 1.01x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 17.1 ms: 1.01x faster                                                      |
| html5lib                | 38.5 ms                                                                  | 38.1 ms: 1.01x faster                                                      |
| sympy_expand            | 298 ms                                                                   | 296 ms: 1.01x faster                                                       |
| python_startup          | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 36.3 ms: 1.01x faster                                                      |
| sympy_str               | 184 ms                                                                   | 183 ms: 1.01x faster                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 60.9 ms: 1.00x faster                                                      |
| async_generators        | 180 ms                                                                   | 181 ms: 1.01x slower                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.14 ms: 1.01x slower                                                      |
| pidigits                | 147 ms                                                                   | 148 ms: 1.01x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 15.0 ms: 1.01x slower                                                      |
| hexiom                  | 4.46 ms                                                                  | 4.51 ms: 1.01x slower                                                      |
| pickle                  | 6.47 us                                                                  | 6.55 us: 1.01x slower                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.42 ms: 1.01x slower                                                      |
| regex_v8                | 13.5 ms                                                                  | 13.7 ms: 1.01x slower                                                      |
| pathlib                 | 72.9 ms                                                                  | 74.0 ms: 1.01x slower                                                      |
| async_tree_memoization  | 374 ms                                                                   | 381 ms: 1.02x slower                                                       |
| comprehensions          | 15.4 us                                                                  | 15.6 us: 1.02x slower                                                      |
| logging_format          | 7.13 us                                                                  | 7.28 us: 1.02x slower                                                      |
| sqlglot_parse           | 929 us                                                                   | 951 us: 1.02x slower                                                       |
| scimark_fft             | 183 ms                                                                   | 188 ms: 1.03x slower                                                       |
| generators              | 33.5 ms                                                                  | 34.5 ms: 1.03x slower                                                      |
| spectral_norm           | 71.8 ms                                                                  | 73.8 ms: 1.03x slower                                                      |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.6 ms: 1.03x slower                                                      |
| logging_simple          | 6.60 us                                                                  | 6.80 us: 1.03x slower                                                      |
| regex_dna               | 115 ms                                                                   | 119 ms: 1.04x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 775 ms: 1.04x slower                                                       |
| pycparser               | 686 ms                                                                   | 721 ms: 1.05x slower                                                       |
| scimark_lu              | 62.8 ms                                                                  | 66.6 ms: 1.06x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.80 us: 1.07x slower                                                      |
| unpickle                | 8.01 us                                                                  | 8.87 us: 1.11x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.02x faster                                                               |

Benchmark hidden because not significant (21): async_tree_cpu_io_mixed, dask, genshi_xml, pylint, create_gc_cycles, tornado_http, sqlglot_normalize, django_template, deepcopy_reduce, sqlglot_optimize, docutils, thrift, python_startup_no_site, regex_effbot, sympy_sum, json_loads, dulwich_log, float, nqueens, async_tree_none, asyncio_tcp
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
