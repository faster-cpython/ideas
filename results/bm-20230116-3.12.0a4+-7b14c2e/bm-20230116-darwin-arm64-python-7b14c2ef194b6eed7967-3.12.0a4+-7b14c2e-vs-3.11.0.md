
# Results vs. 3.11.0

- fork: python
- ref: 7b14c2ef194b6eed7967
- machine: darwin-arm64
- commit hash: 7b14c2e
- commit date: 2023-01-16
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 163 ms: 1.01x slower                                                   |
| docutils       | 1.47 sec                                                            | 1.46 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (3): chameleon, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 53.0 ms                                                             | 51.7 ms: 1.02x faster                                                  |
| nbody          | 65.5 ms                                                             | 64.1 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 76.6 ms                                                             | 74.6 ms: 1.03x faster                                                  |
| regex_v8       | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                   |
| regex_effbot   | 2.63 ms                                                             | 2.62 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.15 ms: 1.23x faster                                                  |
| unpickle_pure_python | 158 us                                                              | 144 us: 1.10x faster                                                   |
| xml_etree_parse      | 106 ms                                                              | 96.9 ms: 1.09x faster                                                  |
| pickle_pure_python   | 198 us                                                              | 193 us: 1.03x faster                                                   |
| xml_etree_generate   | 48.2 ms                                                             | 48.2 ms: 1.00x slower                                                  |
| json_loads           | 16.0 us                                                             | 16.2 us: 1.01x slower                                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.01x slower                                                  |
| pickle_list          | 2.83 us                                                             | 2.85 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 69.2 ms                                                             | 70.1 ms: 1.01x slower                                                  |
| unpickle_list        | 2.63 us                                                             | 2.73 us: 1.04x slower                                                  |
| pickle               | 7.17 us                                                             | 7.50 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                             | 12.4 ms: 1.01x slower                                                  |
| python_startup_no_site | 10.1 ms                                                             | 10.4 ms: 1.03x slower                                                  |
| Geometric mean         | (ref)                                                               | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 29.9 ms                                                             | 28.2 ms: 1.06x faster                                                  |
| mako            | 8.42 ms                                                             | 8.14 ms: 1.03x faster                                                  |
| genshi_text     | 15.3 ms                                                             | 15.2 ms: 1.00x faster                                                  |
| django_template | 21.1 ms                                                             | 21.7 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                               | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp             | 651 ms                                                              | 464 ms: 1.40x faster                                                   |
| json_dumps              | 7.59 ms                                                             | 6.15 ms: 1.23x faster                                                  |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.80 ms: 1.14x faster                                                  |
| unpickle_pure_python    | 158 us                                                              | 144 us: 1.10x faster                                                   |
| xml_etree_parse         | 106 ms                                                              | 96.9 ms: 1.09x faster                                                  |
| deltablue               | 2.81 ms                                                             | 2.63 ms: 1.07x faster                                                  |
| genshi_xml              | 29.9 ms                                                             | 28.2 ms: 1.06x faster                                                  |
| scimark_sor             | 82.9 ms                                                             | 78.5 ms: 1.06x faster                                                  |
| coverage                | 58.4 ms                                                             | 55.4 ms: 1.05x faster                                                  |
| richards                | 32.2 ms                                                             | 30.8 ms: 1.05x faster                                                  |
| mako                    | 8.42 ms                                                             | 8.14 ms: 1.03x faster                                                  |
| create_gc_cycles        | 722 us                                                              | 700 us: 1.03x faster                                                   |
| pycparser               | 695 ms                                                              | 673 ms: 1.03x faster                                                   |
| logging_silent          | 68.0 ns                                                             | 66.1 ns: 1.03x faster                                                  |
| regex_compile           | 76.6 ms                                                             | 74.6 ms: 1.03x faster                                                  |
| pathlib                 | 28.3 ms                                                             | 27.5 ms: 1.03x faster                                                  |
| pickle_pure_python      | 198 us                                                              | 193 us: 1.03x faster                                                   |
| unpack_sequence         | 33.5 ns                                                             | 32.7 ns: 1.03x faster                                                  |
| regex_v8                | 16.1 ms                                                             | 15.7 ms: 1.03x faster                                                  |
| fannkuch                | 260 ms                                                              | 254 ms: 1.02x faster                                                   |
| float                   | 53.0 ms                                                             | 51.7 ms: 1.02x faster                                                  |
| scimark_fft             | 200 ms                                                              | 195 ms: 1.02x faster                                                   |
| bench_thread_pool       | 474 us                                                              | 464 us: 1.02x faster                                                   |
| nbody                   | 65.5 ms                                                             | 64.1 ms: 1.02x faster                                                  |
| mdp                     | 1.54 sec                                                            | 1.51 sec: 1.02x faster                                                 |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                   |
| deepcopy_memo           | 26.3 us                                                             | 26.0 us: 1.01x faster                                                  |
| sympy_expand            | 243 ms                                                              | 241 ms: 1.01x faster                                                   |
| docutils                | 1.47 sec                                                            | 1.46 sec: 1.01x faster                                                 |
| go                      | 109 ms                                                              | 108 ms: 1.01x faster                                                   |
| genshi_text             | 15.3 ms                                                             | 15.2 ms: 1.00x faster                                                  |
| regex_effbot            | 2.63 ms                                                             | 2.62 ms: 1.00x faster                                                  |
| deepcopy                | 224 us                                                              | 223 us: 1.00x faster                                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.5 ms: 1.00x faster                                                  |
| dulwich_log             | 29.7 ms                                                             | 29.7 ms: 1.00x faster                                                  |
| xml_etree_generate      | 48.2 ms                                                             | 48.2 ms: 1.00x slower                                                  |
| gc_traversal            | 2.41 ms                                                             | 2.42 ms: 1.00x slower                                                  |
| pprint_safe_repr        | 463 ms                                                              | 465 ms: 1.00x slower                                                   |
| sqlglot_optimize        | 31.2 ms                                                             | 31.4 ms: 1.01x slower                                                  |
| sympy_sum               | 86.0 ms                                                             | 86.6 ms: 1.01x slower                                                  |
| scimark_lu              | 72.2 ms                                                             | 72.6 ms: 1.01x slower                                                  |
| sqlglot_normalize       | 171 ms                                                              | 172 ms: 1.01x slower                                                   |
| json_loads              | 16.0 us                                                             | 16.2 us: 1.01x slower                                                  |
| python_startup          | 12.3 ms                                                             | 12.4 ms: 1.01x slower                                                  |
| logging_format          | 3.77 us                                                             | 3.80 us: 1.01x slower                                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.01x slower                                                  |
| pickle_list             | 2.83 us                                                             | 2.85 us: 1.01x slower                                                  |
| 2to3                    | 161 ms                                                              | 163 ms: 1.01x slower                                                   |
| hexiom                  | 4.73 ms                                                             | 4.79 ms: 1.01x slower                                                  |
| xml_etree_iterparse     | 69.2 ms                                                             | 70.1 ms: 1.01x slower                                                  |
| bench_mp_pool           | 43.8 ms                                                             | 44.3 ms: 1.01x slower                                                  |
| async_tree_none         | 285 ms                                                              | 289 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed | 534 ms                                                              | 543 ms: 1.02x slower                                                   |
| spectral_norm           | 72.5 ms                                                             | 73.7 ms: 1.02x slower                                                  |
| thrift                  | 431 us                                                              | 440 us: 1.02x slower                                                   |
| crypto_pyaes            | 51.8 ms                                                             | 52.9 ms: 1.02x slower                                                  |
| pyflate                 | 309 ms                                                              | 316 ms: 1.02x slower                                                   |
| chaos                   | 49.4 ms                                                             | 50.7 ms: 1.03x slower                                                  |
| django_template         | 21.1 ms                                                             | 21.7 ms: 1.03x slower                                                  |
| meteor_contest          | 73.3 ms                                                             | 75.6 ms: 1.03x slower                                                  |
| python_startup_no_site  | 10.1 ms                                                             | 10.4 ms: 1.03x slower                                                  |
| telco                   | 3.40 ms                                                             | 3.51 ms: 1.03x slower                                                  |
| async_generators        | 195 ms                                                              | 202 ms: 1.03x slower                                                   |
| unpickle_list           | 2.63 us                                                             | 2.73 us: 1.04x slower                                                  |
| pickle                  | 7.17 us                                                             | 7.50 us: 1.05x slower                                                  |
| sqlite_synth            | 1.28 us                                                             | 1.34 us: 1.05x slower                                                  |
| raytrace                | 207 ms                                                              | 219 ms: 1.06x slower                                                   |
| coroutines              | 17.7 ms                                                             | 18.7 ms: 1.06x slower                                                  |
| async_tree_io           | 707 ms                                                              | 750 ms: 1.06x slower                                                   |
| scimark_monte_carlo     | 46.5 ms                                                             | 49.8 ms: 1.07x slower                                                  |
| sqlglot_transpile       | 1.12 ms                                                             | 1.20 ms: 1.07x slower                                                  |
| sqlglot_parse           | 956 us                                                              | 1.04 ms: 1.09x slower                                                  |
| comprehensions          | 16.1 us                                                             | 17.8 us: 1.10x slower                                                  |
| generators              | 28.6 ms                                                             | 33.9 ms: 1.19x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.00x faster                                                           |

Benchmark hidden because not significant (15): async_tree_memoization, tornado_http, nqueens, sympy_str, pprint_pformat, dask, xml_etree_process, pidigits, logging_simple, json, deepcopy_reduce, html5lib, chameleon, unpickle, mypy2
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
