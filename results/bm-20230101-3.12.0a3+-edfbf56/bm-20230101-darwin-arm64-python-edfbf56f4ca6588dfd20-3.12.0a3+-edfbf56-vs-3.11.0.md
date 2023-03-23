
# Results vs. 3.11.0

- fork: python
- ref: edfbf56f4ca6588dfd20
- machine: darwin-arm64
- commit hash: edfbf56
- commit date: 2023-01-01
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 163 ms: 1.01x slower                                                   |
| docutils       | 1.47 sec                                                            | 1.46 sec: 1.00x faster                                                 |
| html5lib       | 34.8 ms                                                             | 34.1 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 53.0 ms                                                             | 51.6 ms: 1.03x faster                                                  |
| nbody          | 65.5 ms                                                             | 63.8 ms: 1.03x faster                                                  |
| pidigits       | 281 ms                                                              | 280 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                               | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 16.1 ms                                                             | 15.7 ms: 1.02x faster                                                  |
| regex_compile  | 76.6 ms                                                             | 74.9 ms: 1.02x faster                                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                   |
| regex_effbot   | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.13 ms: 1.24x faster                                                  |
| unpickle_pure_python | 158 us                                                              | 142 us: 1.12x faster                                                   |
| xml_etree_parse      | 106 ms                                                              | 96.5 ms: 1.10x faster                                                  |
| pickle_pure_python   | 198 us                                                              | 193 us: 1.03x faster                                                   |
| json_loads           | 16.0 us                                                             | 16.1 us: 1.00x slower                                                  |
| xml_etree_process    | 35.0 ms                                                             | 35.2 ms: 1.01x slower                                                  |
| xml_etree_generate   | 48.2 ms                                                             | 48.5 ms: 1.01x slower                                                  |
| pickle_list          | 2.83 us                                                             | 2.84 us: 1.01x slower                                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 69.2 ms                                                             | 69.9 ms: 1.01x slower                                                  |
| unpickle_list        | 2.63 us                                                             | 2.70 us: 1.03x slower                                                  |
| pickle               | 7.17 us                                                             | 7.46 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.03x faster                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 12.3 ms: 1.00x slower                                                  |
| python_startup_no_site | 10.1 ms                                                             | 10.3 ms: 1.02x slower                                                  |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 29.9 ms                                                             | 28.4 ms: 1.05x faster                                                  |
| mako            | 8.42 ms                                                             | 8.15 ms: 1.03x faster                                                  |
| genshi_text     | 15.3 ms                                                             | 15.0 ms: 1.02x faster                                                  |
| django_template | 21.1 ms                                                             | 22.0 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                               | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp             | 651 ms                                                              | 457 ms: 1.42x faster                                                   |
| json_dumps              | 7.59 ms                                                             | 6.13 ms: 1.24x faster                                                  |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.85 ms: 1.12x faster                                                  |
| unpickle_pure_python    | 158 us                                                              | 142 us: 1.12x faster                                                   |
| xml_etree_parse         | 106 ms                                                              | 96.5 ms: 1.10x faster                                                  |
| deltablue               | 2.81 ms                                                             | 2.62 ms: 1.08x faster                                                  |
| coverage                | 58.4 ms                                                             | 54.6 ms: 1.07x faster                                                  |
| richards                | 32.2 ms                                                             | 30.4 ms: 1.06x faster                                                  |
| genshi_xml              | 29.9 ms                                                             | 28.4 ms: 1.05x faster                                                  |
| logging_silent          | 68.0 ns                                                             | 64.7 ns: 1.05x faster                                                  |
| create_gc_cycles        | 722 us                                                              | 695 us: 1.04x faster                                                   |
| mako                    | 8.42 ms                                                             | 8.15 ms: 1.03x faster                                                  |
| pathlib                 | 28.3 ms                                                             | 27.4 ms: 1.03x faster                                                  |
| scimark_sor             | 82.9 ms                                                             | 80.3 ms: 1.03x faster                                                  |
| float                   | 53.0 ms                                                             | 51.6 ms: 1.03x faster                                                  |
| pickle_pure_python      | 198 us                                                              | 193 us: 1.03x faster                                                   |
| unpack_sequence         | 33.5 ns                                                             | 32.7 ns: 1.03x faster                                                  |
| nbody                   | 65.5 ms                                                             | 63.8 ms: 1.03x faster                                                  |
| pycparser               | 695 ms                                                              | 678 ms: 1.03x faster                                                   |
| regex_v8                | 16.1 ms                                                             | 15.7 ms: 1.02x faster                                                  |
| regex_compile           | 76.6 ms                                                             | 74.9 ms: 1.02x faster                                                  |
| genshi_text             | 15.3 ms                                                             | 15.0 ms: 1.02x faster                                                  |
| deepcopy_memo           | 26.3 us                                                             | 25.8 us: 1.02x faster                                                  |
| html5lib                | 34.8 ms                                                             | 34.1 ms: 1.02x faster                                                  |
| bench_thread_pool       | 474 us                                                              | 465 us: 1.02x faster                                                   |
| fannkuch                | 260 ms                                                              | 257 ms: 1.01x faster                                                   |
| go                      | 109 ms                                                              | 108 ms: 1.01x faster                                                   |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                   |
| deepcopy                | 224 us                                                              | 221 us: 1.01x faster                                                   |
| pprint_pformat          | 946 ms                                                              | 936 ms: 1.01x faster                                                   |
| scimark_fft             | 200 ms                                                              | 198 ms: 1.01x faster                                                   |
| regex_effbot            | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                                  |
| pprint_safe_repr        | 463 ms                                                              | 460 ms: 1.01x faster                                                   |
| logging_simple          | 3.49 us                                                             | 3.47 us: 1.01x faster                                                  |
| mdp                     | 1.54 sec                                                            | 1.53 sec: 1.01x faster                                                 |
| dulwich_log             | 29.7 ms                                                             | 29.6 ms: 1.01x faster                                                  |
| scimark_lu              | 72.2 ms                                                             | 71.8 ms: 1.01x faster                                                  |
| docutils                | 1.47 sec                                                            | 1.46 sec: 1.00x faster                                                 |
| deepcopy_reduce         | 1.91 us                                                             | 1.90 us: 1.00x faster                                                  |
| pidigits                | 281 ms                                                              | 280 ms: 1.00x faster                                                   |
| gc_traversal            | 2.41 ms                                                             | 2.42 ms: 1.00x slower                                                  |
| python_startup          | 12.3 ms                                                             | 12.3 ms: 1.00x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.5 ms: 1.00x slower                                                  |
| json_loads              | 16.0 us                                                             | 16.1 us: 1.00x slower                                                  |
| xml_etree_process       | 35.0 ms                                                             | 35.2 ms: 1.01x slower                                                  |
| xml_etree_generate      | 48.2 ms                                                             | 48.5 ms: 1.01x slower                                                  |
| pickle_list             | 2.83 us                                                             | 2.84 us: 1.01x slower                                                  |
| sympy_expand            | 243 ms                                                              | 245 ms: 1.01x slower                                                   |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.01x slower                                                  |
| xml_etree_iterparse     | 69.2 ms                                                             | 69.9 ms: 1.01x slower                                                  |
| 2to3                    | 161 ms                                                              | 163 ms: 1.01x slower                                                   |
| sympy_str               | 151 ms                                                              | 153 ms: 1.01x slower                                                   |
| async_tree_none         | 285 ms                                                              | 289 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed | 534 ms                                                              | 543 ms: 1.02x slower                                                   |
| sqlglot_optimize        | 31.2 ms                                                             | 31.8 ms: 1.02x slower                                                  |
| coroutines              | 17.7 ms                                                             | 18.1 ms: 1.02x slower                                                  |
| thrift                  | 431 us                                                              | 441 us: 1.02x slower                                                   |
| sqlglot_normalize       | 171 ms                                                              | 175 ms: 1.02x slower                                                   |
| spectral_norm           | 72.5 ms                                                             | 74.2 ms: 1.02x slower                                                  |
| python_startup_no_site  | 10.1 ms                                                             | 10.3 ms: 1.02x slower                                                  |
| unpickle_list           | 2.63 us                                                             | 2.70 us: 1.03x slower                                                  |
| async_generators        | 195 ms                                                              | 201 ms: 1.03x slower                                                   |
| chaos                   | 49.4 ms                                                             | 51.0 ms: 1.03x slower                                                  |
| crypto_pyaes            | 51.8 ms                                                             | 53.8 ms: 1.04x slower                                                  |
| pickle                  | 7.17 us                                                             | 7.46 us: 1.04x slower                                                  |
| telco                   | 3.40 ms                                                             | 3.54 ms: 1.04x slower                                                  |
| meteor_contest          | 73.3 ms                                                             | 76.4 ms: 1.04x slower                                                  |
| hexiom                  | 4.73 ms                                                             | 4.93 ms: 1.04x slower                                                  |
| django_template         | 21.1 ms                                                             | 22.0 ms: 1.05x slower                                                  |
| sqlite_synth            | 1.28 us                                                             | 1.34 us: 1.05x slower                                                  |
| raytrace                | 207 ms                                                              | 217 ms: 1.05x slower                                                   |
| pyflate                 | 309 ms                                                              | 325 ms: 1.05x slower                                                   |
| async_tree_io           | 707 ms                                                              | 750 ms: 1.06x slower                                                   |
| scimark_monte_carlo     | 46.5 ms                                                             | 49.8 ms: 1.07x slower                                                  |
| sqlglot_transpile       | 1.12 ms                                                             | 1.20 ms: 1.07x slower                                                  |
| sqlglot_parse           | 956 us                                                              | 1.03 ms: 1.08x slower                                                  |
| comprehensions          | 16.1 us                                                             | 17.9 us: 1.11x slower                                                  |
| generators              | 28.6 ms                                                             | 33.2 ms: 1.16x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (10): async_tree_memoization, nqueens, unpickle, logging_format, dask, sympy_sum, json, chameleon, bench_mp_pool, mypy2
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
