
# Results vs. 3.11.0

- fork: python
- ref: 3d5d3f7af6498effbc60
- machine: linux-x86_64
- commit hash: 3d5d3f7
- commit date: 2023-01-10
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 252 ms: 1.02x faster                                                  |
| chameleon      | 6.52 ms                                                             | 6.33 ms: 1.03x faster                                                 |
| docutils       | 2.59 sec                                                            | 2.48 sec: 1.04x faster                                                |
| html5lib       | 64.0 ms                                                             | 59.3 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                               | 1.04x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.0 ms                                                             | 71.4 ms: 1.06x faster                                                 |
| pidigits       | 197 ms                                                              | 190 ms: 1.04x faster                                                  |
| nbody          | 96.7 ms                                                             | 94.2 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                               | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                             | 20.5 ms: 1.07x faster                                                 |
| regex_compile  | 137 ms                                                              | 131 ms: 1.04x faster                                                  |
| regex_effbot   | 3.32 ms                                                             | 3.36 ms: 1.01x slower                                                 |
| regex_dna      | 196 ms                                                              | 201 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.53 ms: 1.32x faster                                                 |
| unpickle_pure_python | 228 us                                                              | 200 us: 1.14x faster                                                  |
| xml_etree_parse      | 162 ms                                                              | 148 ms: 1.10x faster                                                  |
| json_loads           | 26.2 us                                                             | 24.1 us: 1.08x faster                                                 |
| pickle_pure_python   | 307 us                                                              | 284 us: 1.08x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                              | 105 ms: 1.03x faster                                                  |
| unpickle             | 13.2 us                                                             | 13.1 us: 1.01x faster                                                 |
| xml_etree_process    | 54.1 ms                                                             | 53.7 ms: 1.01x faster                                                 |
| pickle_dict          | 30.9 us                                                             | 31.0 us: 1.00x slower                                                 |
| unpickle_list        | 4.96 us                                                             | 5.00 us: 1.01x slower                                                 |
| pickle_list          | 4.03 us                                                             | 4.15 us: 1.03x slower                                                 |
| pickle               | 9.79 us                                                             | 10.2 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.05x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.54 ms: 1.01x slower                                                 |
| python_startup_no_site | 5.98 ms                                                             | 6.08 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 46.5 ms: 1.11x faster                                                 |
| genshi_text     | 21.8 ms                                                             | 20.6 ms: 1.06x faster                                                 |
| django_template | 32.9 ms                                                             | 31.9 ms: 1.03x faster                                                 |
| mako            | 9.82 ms                                                             | 9.67 ms: 1.02x faster                                                 |
| Geometric mean  | (ref)                                                               | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp             | 888 ms                                                              | 506 ms: 1.76x faster                                                  |
| json_dumps              | 12.5 ms                                                             | 9.53 ms: 1.32x faster                                                 |
| mypy2                   | 422 ms                                                              | 332 ms: 1.27x faster                                                  |
| unpack_sequence         | 49.5 ns                                                             | 42.9 ns: 1.15x faster                                                 |
| unpickle_pure_python    | 228 us                                                              | 200 us: 1.14x faster                                                  |
| genshi_xml              | 51.8 ms                                                             | 46.5 ms: 1.11x faster                                                 |
| deltablue               | 3.66 ms                                                             | 3.29 ms: 1.11x faster                                                 |
| richards                | 45.7 ms                                                             | 41.6 ms: 1.10x faster                                                 |
| xml_etree_parse         | 162 ms                                                              | 148 ms: 1.10x faster                                                  |
| json_loads              | 26.2 us                                                             | 24.1 us: 1.08x faster                                                 |
| pickle_pure_python      | 307 us                                                              | 284 us: 1.08x faster                                                  |
| html5lib                | 64.0 ms                                                             | 59.3 ms: 1.08x faster                                                 |
| deepcopy_memo           | 36.4 us                                                             | 34.0 us: 1.07x faster                                                 |
| regex_v8                | 22.0 ms                                                             | 20.5 ms: 1.07x faster                                                 |
| nqueens                 | 84.0 ms                                                             | 78.6 ms: 1.07x faster                                                 |
| scimark_sor             | 115 ms                                                              | 107 ms: 1.07x faster                                                  |
| float                   | 76.0 ms                                                             | 71.4 ms: 1.06x faster                                                 |
| logging_simple          | 6.09 us                                                             | 5.74 us: 1.06x faster                                                 |
| genshi_text             | 21.8 ms                                                             | 20.6 ms: 1.06x faster                                                 |
| coroutines              | 26.3 ms                                                             | 24.8 ms: 1.06x faster                                                 |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.22 ms: 1.06x faster                                                 |
| hexiom                  | 6.48 ms                                                             | 6.13 ms: 1.06x faster                                                 |
| pycparser               | 1.14 sec                                                            | 1.08 sec: 1.06x faster                                                |
| telco                   | 6.59 ms                                                             | 6.24 ms: 1.06x faster                                                 |
| scimark_monte_carlo     | 67.8 ms                                                             | 64.3 ms: 1.05x faster                                                 |
| logging_silent          | 98.7 ns                                                             | 93.8 ns: 1.05x faster                                                 |
| sqlglot_optimize        | 53.4 ms                                                             | 50.7 ms: 1.05x faster                                                 |
| pyflate                 | 414 ms                                                              | 395 ms: 1.05x faster                                                  |
| bench_thread_pool       | 820 us                                                              | 783 us: 1.05x faster                                                  |
| regex_compile           | 137 ms                                                              | 131 ms: 1.04x faster                                                  |
| raytrace                | 292 ms                                                              | 280 ms: 1.04x faster                                                  |
| logging_format          | 6.64 us                                                             | 6.37 us: 1.04x faster                                                 |
| docutils                | 2.59 sec                                                            | 2.48 sec: 1.04x faster                                                |
| scimark_fft             | 328 ms                                                              | 315 ms: 1.04x faster                                                  |
| spectral_norm           | 99.5 ms                                                             | 95.6 ms: 1.04x faster                                                 |
| fannkuch                | 384 ms                                                              | 369 ms: 1.04x faster                                                  |
| pidigits                | 197 ms                                                              | 190 ms: 1.04x faster                                                  |
| sqlglot_normalize       | 108 ms                                                              | 104 ms: 1.04x faster                                                  |
| sympy_integrate         | 21.0 ms                                                             | 20.3 ms: 1.04x faster                                                 |
| sympy_expand            | 477 ms                                                              | 461 ms: 1.03x faster                                                  |
| meteor_contest          | 106 ms                                                              | 103 ms: 1.03x faster                                                  |
| django_template         | 32.9 ms                                                             | 31.9 ms: 1.03x faster                                                 |
| create_gc_cycles        | 1.48 ms                                                             | 1.43 ms: 1.03x faster                                                 |
| chameleon               | 6.52 ms                                                             | 6.33 ms: 1.03x faster                                                 |
| xml_etree_iterparse     | 108 ms                                                              | 105 ms: 1.03x faster                                                  |
| nbody                   | 96.7 ms                                                             | 94.2 ms: 1.03x faster                                                 |
| pprint_pformat          | 1.45 sec                                                            | 1.41 sec: 1.03x faster                                                |
| sympy_str               | 291 ms                                                              | 284 ms: 1.03x faster                                                  |
| go                      | 138 ms                                                              | 135 ms: 1.02x faster                                                  |
| thrift                  | 766 us                                                              | 748 us: 1.02x faster                                                  |
| sympy_sum               | 167 ms                                                              | 164 ms: 1.02x faster                                                  |
| async_generators        | 361 ms                                                              | 353 ms: 1.02x faster                                                  |
| pathlib                 | 18.2 ms                                                             | 17.8 ms: 1.02x faster                                                 |
| dask                    | 368 ms                                                              | 361 ms: 1.02x faster                                                  |
| json                    | 4.86 ms                                                             | 4.77 ms: 1.02x faster                                                 |
| 2to3                    | 257 ms                                                              | 252 ms: 1.02x faster                                                  |
| dulwich_log             | 63.6 ms                                                             | 62.5 ms: 1.02x faster                                                 |
| deepcopy                | 339 us                                                              | 334 us: 1.02x faster                                                  |
| mako                    | 9.82 ms                                                             | 9.67 ms: 1.02x faster                                                 |
| pprint_safe_repr        | 701 ms                                                              | 691 ms: 1.02x faster                                                  |
| deepcopy_reduce         | 2.96 us                                                             | 2.92 us: 1.01x faster                                                 |
| coverage                | 101 ms                                                              | 100 ms: 1.01x faster                                                  |
| unpickle                | 13.2 us                                                             | 13.1 us: 1.01x faster                                                 |
| xml_etree_process       | 54.1 ms                                                             | 53.7 ms: 1.01x faster                                                 |
| pickle_dict             | 30.9 us                                                             | 31.0 us: 1.00x slower                                                 |
| python_startup          | 8.49 ms                                                             | 8.54 ms: 1.01x slower                                                 |
| unpickle_list           | 4.96 us                                                             | 5.00 us: 1.01x slower                                                 |
| mdp                     | 2.64 sec                                                            | 2.66 sec: 1.01x slower                                                |
| regex_effbot            | 3.32 ms                                                             | 3.36 ms: 1.01x slower                                                 |
| crypto_pyaes            | 73.8 ms                                                             | 75.1 ms: 1.02x slower                                                 |
| python_startup_no_site  | 5.98 ms                                                             | 6.08 ms: 1.02x slower                                                 |
| sqlglot_transpile       | 1.65 ms                                                             | 1.69 ms: 1.02x slower                                                 |
| sqlite_synth            | 2.51 us                                                             | 2.56 us: 1.02x slower                                                 |
| regex_dna               | 196 ms                                                              | 201 ms: 1.02x slower                                                  |
| sqlglot_parse           | 1.36 ms                                                             | 1.40 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed | 736 ms                                                              | 753 ms: 1.02x slower                                                  |
| pickle_list             | 4.03 us                                                             | 4.15 us: 1.03x slower                                                 |
| async_tree_io           | 1.28 sec                                                            | 1.33 sec: 1.03x slower                                                |
| pickle                  | 9.79 us                                                             | 10.2 us: 1.04x slower                                                 |
| generators              | 73.4 ms                                                             | 77.0 ms: 1.05x slower                                                 |
| comprehensions          | 22.2 us                                                             | 23.6 us: 1.06x slower                                                 |
| gc_traversal            | 3.63 ms                                                             | 4.15 ms: 1.14x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.04x faster                                                          |

Benchmark hidden because not significant (7): chaos, bench_mp_pool, xml_etree_generate, djangocms, scimark_lu, async_tree_none, async_tree_memoization
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
