
# Results vs. 3.11.0

- fork: python
- ref: 3b9d793efcfd2c00c14f
- machine: darwin-arm64
- commit hash: 3b9d793
- commit date: 2022-11-14
- overall geometric mean: 1.03x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 167 ms: 1.03x slower                                                  |
| chameleon      | 4.55 ms                                                             | 4.44 ms: 1.02x faster                                                 |
| docutils       | 1.47 sec                                                            | 1.48 sec: 1.00x slower                                                |
| html5lib       | 34.8 ms                                                             | 35.9 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 281 ms                                                              | 281 ms: 1.00x slower                                                  |
| nbody          | 65.5 ms                                                             | 65.8 ms: 1.01x slower                                                 |
| float          | 53.0 ms                                                             | 56.3 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                               | 1.02x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                                 |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                                 |
| regex_compile  | 76.6 ms                                                             | 76.0 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                               | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.12 ms: 1.24x faster                                                 |
| xml_etree_parse      | 106 ms                                                              | 96.3 ms: 1.10x faster                                                 |
| unpickle_list        | 2.63 us                                                             | 2.59 us: 1.02x faster                                                 |
| xml_etree_iterparse  | 69.2 ms                                                             | 69.6 ms: 1.01x slower                                                 |
| pickle_list          | 2.83 us                                                             | 2.85 us: 1.01x slower                                                 |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.01x slower                                                 |
| json_loads           | 16.0 us                                                             | 16.2 us: 1.01x slower                                                 |
| xml_etree_generate   | 48.2 ms                                                             | 48.7 ms: 1.01x slower                                                 |
| xml_etree_process    | 35.0 ms                                                             | 35.5 ms: 1.02x slower                                                 |
| unpickle_pure_python | 158 us                                                              | 162 us: 1.02x slower                                                  |
| unpickle             | 9.66 us                                                             | 9.94 us: 1.03x slower                                                 |
| pickle_pure_python   | 198 us                                                              | 205 us: 1.04x slower                                                  |
| pickle               | 7.17 us                                                             | 7.44 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 12.3 ms: 1.00x slower                                                 |
| python_startup_no_site | 10.1 ms                                                             | 10.2 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 8.42 ms                                                             | 7.18 ms: 1.17x faster                                                 |
| genshi_text     | 15.3 ms                                                             | 14.8 ms: 1.04x faster                                                 |
| genshi_xml      | 29.9 ms                                                             | 29.6 ms: 1.01x faster                                                 |
| django_template | 21.1 ms                                                             | 21.4 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps              | 7.59 ms                                                             | 6.12 ms: 1.24x faster                                                 |
| mako                    | 8.42 ms                                                             | 7.18 ms: 1.17x faster                                                 |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.79 ms: 1.15x faster                                                 |
| xml_etree_parse         | 106 ms                                                              | 96.3 ms: 1.10x faster                                                 |
| pathlib                 | 28.3 ms                                                             | 26.9 ms: 1.05x faster                                                 |
| deltablue               | 2.81 ms                                                             | 2.68 ms: 1.05x faster                                                 |
| create_gc_cycles        | 722 us                                                              | 693 us: 1.04x faster                                                  |
| genshi_text             | 15.3 ms                                                             | 14.8 ms: 1.04x faster                                                 |
| scimark_lu              | 72.2 ms                                                             | 70.0 ms: 1.03x faster                                                 |
| regex_v8                | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                                 |
| chameleon               | 4.55 ms                                                             | 4.44 ms: 1.02x faster                                                 |
| unpickle_list           | 2.63 us                                                             | 2.59 us: 1.02x faster                                                 |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| telco                   | 3.40 ms                                                             | 3.35 ms: 1.01x faster                                                 |
| logging_silent          | 68.0 ns                                                             | 67.1 ns: 1.01x faster                                                 |
| genshi_xml              | 29.9 ms                                                             | 29.6 ms: 1.01x faster                                                 |
| regex_effbot            | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                                 |
| regex_compile           | 76.6 ms                                                             | 76.0 ms: 1.01x faster                                                 |
| richards                | 32.2 ms                                                             | 32.0 ms: 1.01x faster                                                 |
| scimark_fft             | 200 ms                                                              | 198 ms: 1.01x faster                                                  |
| bench_thread_pool       | 474 us                                                              | 473 us: 1.00x faster                                                  |
| python_startup          | 12.3 ms                                                             | 12.3 ms: 1.00x slower                                                 |
| pidigits                | 281 ms                                                              | 281 ms: 1.00x slower                                                  |
| crypto_pyaes            | 51.8 ms                                                             | 51.9 ms: 1.00x slower                                                 |
| gc_traversal            | 2.41 ms                                                             | 2.42 ms: 1.00x slower                                                 |
| docutils                | 1.47 sec                                                            | 1.48 sec: 1.00x slower                                                |
| nbody                   | 65.5 ms                                                             | 65.8 ms: 1.01x slower                                                 |
| xml_etree_iterparse     | 69.2 ms                                                             | 69.6 ms: 1.01x slower                                                 |
| mdp                     | 1.54 sec                                                            | 1.55 sec: 1.01x slower                                                |
| pickle_list             | 2.83 us                                                             | 2.85 us: 1.01x slower                                                 |
| spectral_norm           | 72.5 ms                                                             | 73.0 ms: 1.01x slower                                                 |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.01x slower                                                 |
| json_loads              | 16.0 us                                                             | 16.2 us: 1.01x slower                                                 |
| python_startup_no_site  | 10.1 ms                                                             | 10.2 ms: 1.01x slower                                                 |
| xml_etree_generate      | 48.2 ms                                                             | 48.7 ms: 1.01x slower                                                 |
| dask                    | 226 ms                                                              | 229 ms: 1.01x slower                                                  |
| xml_etree_process       | 35.0 ms                                                             | 35.5 ms: 1.02x slower                                                 |
| dulwich_log             | 29.7 ms                                                             | 30.2 ms: 1.02x slower                                                 |
| bench_mp_pool           | 43.8 ms                                                             | 44.5 ms: 1.02x slower                                                 |
| django_template         | 21.1 ms                                                             | 21.4 ms: 1.02x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 174 ms: 1.02x slower                                                  |
| json                    | 2.77 ms                                                             | 2.83 ms: 1.02x slower                                                 |
| sqlglot_optimize        | 31.2 ms                                                             | 31.8 ms: 1.02x slower                                                 |
| sympy_sum               | 86.0 ms                                                             | 87.7 ms: 1.02x slower                                                 |
| unpickle_pure_python    | 158 us                                                              | 162 us: 1.02x slower                                                  |
| sympy_expand            | 243 ms                                                              | 248 ms: 1.02x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.7 ms: 1.02x slower                                                 |
| nqueens                 | 62.4 ms                                                             | 63.9 ms: 1.02x slower                                                 |
| thrift                  | 431 us                                                              | 442 us: 1.02x slower                                                  |
| sympy_str               | 151 ms                                                              | 155 ms: 1.03x slower                                                  |
| unpickle                | 9.66 us                                                             | 9.94 us: 1.03x slower                                                 |
| chaos                   | 49.4 ms                                                             | 51.0 ms: 1.03x slower                                                 |
| html5lib                | 34.8 ms                                                             | 35.9 ms: 1.03x slower                                                 |
| async_tree_none         | 285 ms                                                              | 294 ms: 1.03x slower                                                  |
| 2to3                    | 161 ms                                                              | 167 ms: 1.03x slower                                                  |
| pickle_pure_python      | 198 us                                                              | 205 us: 1.04x slower                                                  |
| coverage                | 58.4 ms                                                             | 60.5 ms: 1.04x slower                                                 |
| raytrace                | 207 ms                                                              | 214 ms: 1.04x slower                                                  |
| pickle                  | 7.17 us                                                             | 7.44 us: 1.04x slower                                                 |
| async_tree_cpu_io_mixed | 534 ms                                                              | 555 ms: 1.04x slower                                                  |
| logging_simple          | 3.49 us                                                             | 3.63 us: 1.04x slower                                                 |
| logging_format          | 3.77 us                                                             | 3.92 us: 1.04x slower                                                 |
| fannkuch                | 260 ms                                                              | 271 ms: 1.04x slower                                                  |
| meteor_contest          | 73.3 ms                                                             | 76.7 ms: 1.05x slower                                                 |
| sqlglot_transpile       | 1.12 ms                                                             | 1.17 ms: 1.05x slower                                                 |
| sqlglot_parse           | 956 us                                                              | 1.01 ms: 1.05x slower                                                 |
| float                   | 53.0 ms                                                             | 56.3 ms: 1.06x slower                                                 |
| hexiom                  | 4.73 ms                                                             | 5.04 ms: 1.06x slower                                                 |
| pprint_pformat          | 946 ms                                                              | 1.01 sec: 1.07x slower                                                |
| async_generators        | 195 ms                                                              | 208 ms: 1.07x slower                                                  |
| async_tree_io           | 707 ms                                                              | 755 ms: 1.07x slower                                                  |
| pprint_safe_repr        | 463 ms                                                              | 497 ms: 1.07x slower                                                  |
| deepcopy_reduce         | 1.91 us                                                             | 2.07 us: 1.09x slower                                                 |
| sqlite_synth            | 1.28 us                                                             | 1.40 us: 1.09x slower                                                 |
| deepcopy                | 224 us                                                              | 243 us: 1.09x slower                                                  |
| go                      | 109 ms                                                              | 119 ms: 1.09x slower                                                  |
| deepcopy_memo           | 26.3 us                                                             | 29.5 us: 1.12x slower                                                 |
| comprehensions          | 16.1 us                                                             | 18.0 us: 1.12x slower                                                 |
| pyflate                 | 309 ms                                                              | 351 ms: 1.14x slower                                                  |
| coroutines              | 17.7 ms                                                             | 20.6 ms: 1.16x slower                                                 |
| scimark_monte_carlo     | 46.5 ms                                                             | 54.6 ms: 1.17x slower                                                 |
| generators              | 28.6 ms                                                             | 35.8 ms: 1.25x slower                                                 |
| scimark_sor             | 82.9 ms                                                             | 105 ms: 1.27x slower                                                  |
| unpack_sequence         | 33.5 ns                                                             | 62.8 ns: 1.87x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.03x slower                                                          |

Benchmark hidden because not significant (5): tornado_http, asyncio_tcp, async_tree_memoization, pycparser, mypy2
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
