
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: bb396ee
- commit date: 2023-03-11
- overall geometric mean: 1.02x slower \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 166 ms: 1.09x faster                                   |
| chameleon      | 4.61 ms                                                             | 4.51 ms: 1.02x faster                                  |
| docutils       | 1.46 sec                                                            | 1.49 sec: 1.02x slower                                 |
| html5lib       | 34.7 ms                                                             | 35.8 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 64.1 ms: 1.02x faster                                  |
| pidigits       | 282 ms                                                              | 281 ms: 1.00x faster                                   |
| float          | 51.7 ms                                                             | 53.6 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                               | 1.01x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 16.5 ms                                                             | 16.1 ms: 1.02x faster                                  |
| regex_compile  | 76.3 ms                                                             | 75.7 ms: 1.01x faster                                  |
| regex_dna      | 151 ms                                                              | 152 ms: 1.00x slower                                   |
| regex_effbot   | 2.63 ms                                                             | 2.69 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                               | 1.00x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.30 ms: 1.22x faster                                  |
| unpickle_pure_python | 159 us                                                              | 145 us: 1.10x faster                                   |
| pickle_pure_python   | 200 us                                                              | 190 us: 1.05x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 97.2 ms: 1.02x faster                                  |
| pickle_list          | 2.86 us                                                             | 2.81 us: 1.02x faster                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| json_loads           | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| unpickle_list        | 2.64 us                                                             | 2.69 us: 1.02x slower                                  |
| pickle               | 7.21 us                                                             | 7.48 us: 1.04x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 36.8 ms: 1.05x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 51.0 ms: 1.05x slower                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 70.8 ms: 1.08x slower                                  |
| Geometric mean       | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 11.1 ms: 1.20x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 8.93 ms: 1.23x slower                                  |
| Geometric mean         | (ref)                                                               | 1.22x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 8.40 ms                                                             | 7.47 ms: 1.12x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 29.4 ms: 1.04x faster                                  |
| genshi_text     | 15.3 ms                                                             | 14.9 ms: 1.03x faster                                  |
| django_template | 21.1 ms                                                             | 21.7 ms: 1.03x slower                                  |
| Geometric mean  | (ref)                                                               | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps              | 7.67 ms                                                             | 6.30 ms: 1.22x faster                                  |
| mako                    | 8.40 ms                                                             | 7.47 ms: 1.12x faster                                  |
| unpickle_pure_python    | 159 us                                                              | 145 us: 1.10x faster                                   |
| 2to3                    | 181 ms                                                              | 166 ms: 1.09x faster                                   |
| deltablue               | 2.82 ms                                                             | 2.59 ms: 1.09x faster                                  |
| richards                | 32.7 ms                                                             | 30.7 ms: 1.06x faster                                  |
| hexiom                  | 4.73 ms                                                             | 4.45 ms: 1.06x faster                                  |
| pickle_pure_python      | 200 us                                                              | 190 us: 1.05x faster                                   |
| genshi_xml              | 30.5 ms                                                             | 29.4 ms: 1.04x faster                                  |
| genshi_text             | 15.3 ms                                                             | 14.9 ms: 1.03x faster                                  |
| chaos                   | 49.3 ms                                                             | 47.9 ms: 1.03x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.50 sec: 1.03x faster                                 |
| xml_etree_parse         | 99.6 ms                                                             | 97.2 ms: 1.02x faster                                  |
| pycparser               | 694 ms                                                              | 678 ms: 1.02x faster                                   |
| regex_v8                | 16.5 ms                                                             | 16.1 ms: 1.02x faster                                  |
| scimark_fft             | 201 ms                                                              | 196 ms: 1.02x faster                                   |
| chameleon               | 4.61 ms                                                             | 4.51 ms: 1.02x faster                                  |
| pickle_list             | 2.86 us                                                             | 2.81 us: 1.02x faster                                  |
| fannkuch                | 262 ms                                                              | 257 ms: 1.02x faster                                   |
| nbody                   | 65.2 ms                                                             | 64.1 ms: 1.02x faster                                  |
| unpack_sequence         | 33.1 ns                                                             | 32.8 ns: 1.01x faster                                  |
| regex_compile           | 76.3 ms                                                             | 75.7 ms: 1.01x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 3.17 ms: 1.01x faster                                  |
| generators              | 28.4 ms                                                             | 28.2 ms: 1.01x faster                                  |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.18 ms: 1.00x faster                                  |
| pidigits                | 282 ms                                                              | 281 ms: 1.00x faster                                   |
| meteor_contest          | 73.9 ms                                                             | 73.8 ms: 1.00x faster                                  |
| regex_dna               | 151 ms                                                              | 152 ms: 1.00x slower                                   |
| telco                   | 3.39 ms                                                             | 3.40 ms: 1.00x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| json                    | 2.83 ms                                                             | 2.84 ms: 1.01x slower                                  |
| deepcopy_memo           | 26.2 us                                                             | 26.3 us: 1.01x slower                                  |
| json_loads              | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| go                      | 109 ms                                                              | 111 ms: 1.01x slower                                   |
| deepcopy                | 222 us                                                              | 225 us: 1.01x slower                                   |
| coroutines              | 17.8 ms                                                             | 18.1 ms: 1.02x slower                                  |
| unpickle_list           | 2.64 us                                                             | 2.69 us: 1.02x slower                                  |
| dulwich_log             | 29.1 ms                                                             | 29.6 ms: 1.02x slower                                  |
| sqlglot_normalize       | 171 ms                                                              | 175 ms: 1.02x slower                                   |
| docutils                | 1.46 sec                                                            | 1.49 sec: 1.02x slower                                 |
| logging_silent          | 67.4 ns                                                             | 68.9 ns: 1.02x slower                                  |
| coverage                | 58.4 ms                                                             | 59.7 ms: 1.02x slower                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.8 ms: 1.02x slower                                  |
| regex_effbot            | 2.63 ms                                                             | 2.69 ms: 1.02x slower                                  |
| sympy_expand            | 242 ms                                                              | 248 ms: 1.03x slower                                   |
| pprint_pformat          | 953 ms                                                              | 979 ms: 1.03x slower                                   |
| sqlglot_optimize        | 31.3 ms                                                             | 32.2 ms: 1.03x slower                                  |
| sympy_str               | 151 ms                                                              | 155 ms: 1.03x slower                                   |
| django_template         | 21.1 ms                                                             | 21.7 ms: 1.03x slower                                  |
| sqlalchemy_declarative  | 62.4 ms                                                             | 64.3 ms: 1.03x slower                                  |
| async_tree_none         | 281 ms                                                              | 290 ms: 1.03x slower                                   |
| pprint_safe_repr        | 467 ms                                                              | 481 ms: 1.03x slower                                   |
| spectral_norm           | 72.7 ms                                                             | 75.0 ms: 1.03x slower                                  |
| html5lib                | 34.7 ms                                                             | 35.8 ms: 1.03x slower                                  |
| bench_thread_pool       | 457 us                                                              | 473 us: 1.03x slower                                   |
| float                   | 51.7 ms                                                             | 53.6 ms: 1.04x slower                                  |
| sympy_sum               | 85.5 ms                                                             | 88.7 ms: 1.04x slower                                  |
| pickle                  | 7.21 us                                                             | 7.48 us: 1.04x slower                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 548 ms: 1.04x slower                                   |
| scimark_lu              | 72.2 ms                                                             | 75.0 ms: 1.04x slower                                  |
| crypto_pyaes            | 51.7 ms                                                             | 53.7 ms: 1.04x slower                                  |
| deepcopy_reduce         | 1.90 us                                                             | 1.97 us: 1.04x slower                                  |
| xml_etree_process       | 35.1 ms                                                             | 36.8 ms: 1.05x slower                                  |
| sqlite_synth            | 1.29 us                                                             | 1.36 us: 1.05x slower                                  |
| logging_simple          | 3.47 us                                                             | 3.64 us: 1.05x slower                                  |
| thrift                  | 429 us                                                              | 453 us: 1.05x slower                                   |
| xml_etree_generate      | 48.4 ms                                                             | 51.0 ms: 1.05x slower                                  |
| logging_format          | 3.73 us                                                             | 3.94 us: 1.06x slower                                  |
| nqueens                 | 59.5 ms                                                             | 62.9 ms: 1.06x slower                                  |
| async_tree_memoization  | 317 ms                                                              | 336 ms: 1.06x slower                                   |
| scimark_sor             | 83.3 ms                                                             | 88.4 ms: 1.06x slower                                  |
| pyflate                 | 313 ms                                                              | 332 ms: 1.06x slower                                   |
| async_tree_io           | 696 ms                                                              | 745 ms: 1.07x slower                                   |
| xml_etree_iterparse     | 65.6 ms                                                             | 70.8 ms: 1.08x slower                                  |
| bench_mp_pool           | 41.4 ms                                                             | 45.2 ms: 1.09x slower                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 51.3 ms: 1.09x slower                                  |
| raytrace                | 207 ms                                                              | 228 ms: 1.10x slower                                   |
| sqlglot_transpile       | 1.11 ms                                                             | 1.23 ms: 1.10x slower                                  |
| sqlglot_parse           | 948 us                                                              | 1.06 ms: 1.11x slower                                  |
| python_startup          | 9.19 ms                                                             | 11.1 ms: 1.20x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 8.93 ms: 1.23x slower                                  |
| pathlib                 | 20.6 ms                                                             | 27.5 ms: 1.33x slower                                  |
| async_generators        | 195 ms                                                              | 267 ms: 1.37x slower                                   |
| Geometric mean          | (ref)                                                               | 1.02x slower                                           |

Benchmark hidden because not significant (2): tornado_http, unpickle
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230311-3.12.0a6+-bb396ee/bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
