
# Results vs. 3.11.0

- fork: python
- ref: 3d5d3f7af6498effbc60
- machine: darwin-arm64
- commit hash: 3d5d3f7
- commit date: 2023-01-10
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 163 ms: 1.01x slower                                                  |
| chameleon      | 4.55 ms                                                             | 4.53 ms: 1.00x faster                                                 |
| docutils       | 1.47 sec                                                            | 1.45 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                               | 1.00x faster                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 65.5 ms                                                             | 63.9 ms: 1.02x faster                                                 |
| float          | 53.0 ms                                                             | 52.0 ms: 1.02x faster                                                 |
| pidigits       | 281 ms                                                              | 281 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                               | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 76.6 ms                                                             | 74.5 ms: 1.03x faster                                                 |
| regex_v8       | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                                 |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                               | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.05 ms: 1.25x faster                                                 |
| unpickle_pure_python | 158 us                                                              | 143 us: 1.11x faster                                                  |
| xml_etree_parse      | 106 ms                                                              | 96.5 ms: 1.10x faster                                                 |
| pickle_pure_python   | 198 us                                                              | 192 us: 1.03x faster                                                  |
| xml_etree_process    | 35.0 ms                                                             | 34.9 ms: 1.00x faster                                                 |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.01x slower                                                 |
| xml_etree_generate   | 48.2 ms                                                             | 48.6 ms: 1.01x slower                                                 |
| json_loads           | 16.0 us                                                             | 16.2 us: 1.01x slower                                                 |
| unpickle             | 9.66 us                                                             | 9.76 us: 1.01x slower                                                 |
| unpickle_list        | 2.63 us                                                             | 2.70 us: 1.03x slower                                                 |
| pickle               | 7.17 us                                                             | 7.44 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.03x faster                                                          |

Benchmark hidden because not significant (2): pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 12.3 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.1 ms                                                             | 10.2 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 29.9 ms                                                             | 28.4 ms: 1.05x faster                                                 |
| mako            | 8.42 ms                                                             | 8.12 ms: 1.04x faster                                                 |
| genshi_text     | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                                 |
| django_template | 21.1 ms                                                             | 21.6 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp             | 651 ms                                                              | 449 ms: 1.45x faster                                                  |
| json_dumps              | 7.59 ms                                                             | 6.05 ms: 1.25x faster                                                 |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.81 ms: 1.14x faster                                                 |
| unpickle_pure_python    | 158 us                                                              | 143 us: 1.11x faster                                                  |
| xml_etree_parse         | 106 ms                                                              | 96.5 ms: 1.10x faster                                                 |
| deltablue               | 2.81 ms                                                             | 2.64 ms: 1.06x faster                                                 |
| genshi_xml              | 29.9 ms                                                             | 28.4 ms: 1.05x faster                                                 |
| richards                | 32.2 ms                                                             | 30.6 ms: 1.05x faster                                                 |
| create_gc_cycles        | 722 us                                                              | 692 us: 1.04x faster                                                  |
| mako                    | 8.42 ms                                                             | 8.12 ms: 1.04x faster                                                 |
| nqueens                 | 62.4 ms                                                             | 60.5 ms: 1.03x faster                                                 |
| pickle_pure_python      | 198 us                                                              | 192 us: 1.03x faster                                                  |
| regex_compile           | 76.6 ms                                                             | 74.5 ms: 1.03x faster                                                 |
| unpack_sequence         | 33.5 ns                                                             | 32.7 ns: 1.03x faster                                                 |
| pycparser               | 695 ms                                                              | 676 ms: 1.03x faster                                                  |
| fannkuch                | 260 ms                                                              | 254 ms: 1.03x faster                                                  |
| regex_v8                | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                                 |
| nbody                   | 65.5 ms                                                             | 63.9 ms: 1.02x faster                                                 |
| scimark_fft             | 200 ms                                                              | 195 ms: 1.02x faster                                                  |
| bench_thread_pool       | 474 us                                                              | 462 us: 1.02x faster                                                  |
| logging_silent          | 68.0 ns                                                             | 66.4 ns: 1.02x faster                                                 |
| coverage                | 58.4 ms                                                             | 57.2 ms: 1.02x faster                                                 |
| float                   | 53.0 ms                                                             | 52.0 ms: 1.02x faster                                                 |
| pathlib                 | 28.3 ms                                                             | 27.8 ms: 1.02x faster                                                 |
| logging_simple          | 3.49 us                                                             | 3.44 us: 1.02x faster                                                 |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| deepcopy                | 224 us                                                              | 221 us: 1.01x faster                                                  |
| docutils                | 1.47 sec                                                            | 1.45 sec: 1.01x faster                                                |
| logging_format          | 3.77 us                                                             | 3.74 us: 1.01x faster                                                 |
| regex_effbot            | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                                 |
| sympy_integrate         | 11.5 ms                                                             | 11.4 ms: 1.01x faster                                                 |
| pprint_pformat          | 946 ms                                                              | 939 ms: 1.01x faster                                                  |
| sympy_expand            | 243 ms                                                              | 242 ms: 1.01x faster                                                  |
| python_startup          | 12.3 ms                                                             | 12.3 ms: 1.01x faster                                                 |
| genshi_text             | 15.3 ms                                                             | 15.2 ms: 1.01x faster                                                 |
| deepcopy_memo           | 26.3 us                                                             | 26.2 us: 1.00x faster                                                 |
| chameleon               | 4.55 ms                                                             | 4.53 ms: 1.00x faster                                                 |
| dulwich_log             | 29.7 ms                                                             | 29.6 ms: 1.00x faster                                                 |
| go                      | 109 ms                                                              | 109 ms: 1.00x faster                                                  |
| pprint_safe_repr        | 463 ms                                                              | 462 ms: 1.00x faster                                                  |
| xml_etree_process       | 35.0 ms                                                             | 34.9 ms: 1.00x faster                                                 |
| sympy_str               | 151 ms                                                              | 151 ms: 1.00x faster                                                  |
| telco                   | 3.40 ms                                                             | 3.39 ms: 1.00x faster                                                 |
| pidigits                | 281 ms                                                              | 281 ms: 1.00x slower                                                  |
| sqlglot_optimize        | 31.2 ms                                                             | 31.3 ms: 1.00x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 172 ms: 1.00x slower                                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.01x slower                                                 |
| scimark_lu              | 72.2 ms                                                             | 72.7 ms: 1.01x slower                                                 |
| xml_etree_generate      | 48.2 ms                                                             | 48.6 ms: 1.01x slower                                                 |
| 2to3                    | 161 ms                                                              | 163 ms: 1.01x slower                                                  |
| deepcopy_reduce         | 1.91 us                                                             | 1.92 us: 1.01x slower                                                 |
| json_loads              | 16.0 us                                                             | 16.2 us: 1.01x slower                                                 |
| unpickle                | 9.66 us                                                             | 9.76 us: 1.01x slower                                                 |
| async_tree_none         | 285 ms                                                              | 288 ms: 1.01x slower                                                  |
| spectral_norm           | 72.5 ms                                                             | 73.4 ms: 1.01x slower                                                 |
| python_startup_no_site  | 10.1 ms                                                             | 10.2 ms: 1.01x slower                                                 |
| crypto_pyaes            | 51.8 ms                                                             | 52.6 ms: 1.01x slower                                                 |
| thrift                  | 431 us                                                              | 438 us: 1.02x slower                                                  |
| async_tree_cpu_io_mixed | 534 ms                                                              | 546 ms: 1.02x slower                                                  |
| chaos                   | 49.4 ms                                                             | 50.5 ms: 1.02x slower                                                 |
| meteor_contest          | 73.3 ms                                                             | 75.1 ms: 1.02x slower                                                 |
| async_generators        | 195 ms                                                              | 200 ms: 1.03x slower                                                  |
| unpickle_list           | 2.63 us                                                             | 2.70 us: 1.03x slower                                                 |
| django_template         | 21.1 ms                                                             | 21.6 ms: 1.03x slower                                                 |
| pyflate                 | 309 ms                                                              | 318 ms: 1.03x slower                                                  |
| pickle                  | 7.17 us                                                             | 7.44 us: 1.04x slower                                                 |
| hexiom                  | 4.73 ms                                                             | 4.94 ms: 1.04x slower                                                 |
| raytrace                | 207 ms                                                              | 217 ms: 1.05x slower                                                  |
| sqlite_synth            | 1.28 us                                                             | 1.35 us: 1.05x slower                                                 |
| coroutines              | 17.7 ms                                                             | 18.7 ms: 1.05x slower                                                 |
| async_tree_io           | 707 ms                                                              | 748 ms: 1.06x slower                                                  |
| gc_traversal            | 2.41 ms                                                             | 2.56 ms: 1.06x slower                                                 |
| scimark_monte_carlo     | 46.5 ms                                                             | 49.6 ms: 1.07x slower                                                 |
| sqlglot_transpile       | 1.12 ms                                                             | 1.20 ms: 1.07x slower                                                 |
| sqlglot_parse           | 956 us                                                              | 1.04 ms: 1.08x slower                                                 |
| comprehensions          | 16.1 us                                                             | 17.7 us: 1.10x slower                                                 |
| generators              | 28.6 ms                                                             | 33.7 ms: 1.18x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.01x faster                                                          |

Benchmark hidden because not significant (11): async_tree_memoization, dask, sympy_sum, scimark_sor, mdp, pickle_list, json, xml_etree_iterparse, html5lib, bench_mp_pool, mypy2
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
