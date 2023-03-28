
# Results vs. 3.11.0

- fork: python
- ref: b6bd7ffcbc1ffaa68e34
- machine: darwin-arm64
- commit hash: b6bd7ff
- commit date: 2022-12-06
- overall geometric mean: 1.10x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 161 ms                                                              | 178 ms: 1.10x slower                                                  |
| chameleon      | 4.55 ms                                                             | 5.09 ms: 1.12x slower                                                 |
| docutils       | 1.47 sec                                                            | 1.53 sec: 1.04x slower                                                |
| html5lib       | 34.8 ms                                                             | 38.5 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                               | 1.09x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 65.5 ms                                                             | 65.2 ms: 1.00x faster                                                 |
| pidigits       | 281 ms                                                              | 282 ms: 1.00x slower                                                  |
| float          | 53.0 ms                                                             | 59.1 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                               | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 16.1 ms                                                             | 15.8 ms: 1.02x faster                                                 |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| regex_effbot   | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                                 |
| regex_compile  | 76.6 ms                                                             | 83.2 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                               | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.59 ms                                                             | 6.32 ms: 1.20x faster                                                 |
| xml_etree_parse      | 106 ms                                                              | 97.6 ms: 1.08x faster                                                 |
| unpickle_list        | 2.63 us                                                             | 2.57 us: 1.02x faster                                                 |
| json_loads           | 16.0 us                                                             | 16.4 us: 1.02x slower                                                 |
| pickle               | 7.17 us                                                             | 7.61 us: 1.06x slower                                                 |
| xml_etree_iterparse  | 69.2 ms                                                             | 74.3 ms: 1.07x slower                                                 |
| xml_etree_generate   | 48.2 ms                                                             | 53.8 ms: 1.12x slower                                                 |
| unpickle_pure_python | 158 us                                                              | 177 us: 1.12x slower                                                  |
| xml_etree_process    | 35.0 ms                                                             | 40.4 ms: 1.16x slower                                                 |
| pickle_pure_python   | 198 us                                                              | 229 us: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.03x slower                                                          |

Benchmark hidden because not significant (3): unpickle, pickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 10.1 ms                                                             | 10.2 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.00x slower                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 8.42 ms                                                             | 7.37 ms: 1.14x faster                                                 |
| genshi_text     | 15.3 ms                                                             | 17.5 ms: 1.14x slower                                                 |
| genshi_xml      | 29.9 ms                                                             | 34.6 ms: 1.16x slower                                                 |
| django_template | 21.1 ms                                                             | 24.6 ms: 1.17x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.08x slower                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps              | 7.59 ms                                                             | 6.32 ms: 1.20x faster                                                 |
| scimark_sparse_mat_mult | 3.19 ms                                                             | 2.78 ms: 1.15x faster                                                 |
| mako                    | 8.42 ms                                                             | 7.37 ms: 1.14x faster                                                 |
| xml_etree_parse         | 106 ms                                                              | 97.6 ms: 1.08x faster                                                 |
| create_gc_cycles        | 722 us                                                              | 695 us: 1.04x faster                                                  |
| unpickle_list           | 2.63 us                                                             | 2.57 us: 1.02x faster                                                 |
| regex_v8                | 16.1 ms                                                             | 15.8 ms: 1.02x faster                                                 |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| scimark_fft             | 200 ms                                                              | 198 ms: 1.01x faster                                                  |
| telco                   | 3.40 ms                                                             | 3.37 ms: 1.01x faster                                                 |
| regex_effbot            | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                                 |
| nbody                   | 65.5 ms                                                             | 65.2 ms: 1.00x faster                                                 |
| gc_traversal            | 2.41 ms                                                             | 2.42 ms: 1.00x slower                                                 |
| pidigits                | 281 ms                                                              | 282 ms: 1.00x slower                                                  |
| python_startup_no_site  | 10.1 ms                                                             | 10.2 ms: 1.01x slower                                                 |
| json_loads              | 16.0 us                                                             | 16.4 us: 1.02x slower                                                 |
| bench_mp_pool           | 43.8 ms                                                             | 44.8 ms: 1.02x slower                                                 |
| json                    | 2.77 ms                                                             | 2.88 ms: 1.04x slower                                                 |
| docutils                | 1.47 sec                                                            | 1.53 sec: 1.04x slower                                                |
| fannkuch                | 260 ms                                                              | 273 ms: 1.05x slower                                                  |
| dask                    | 226 ms                                                              | 238 ms: 1.05x slower                                                  |
| pycparser               | 695 ms                                                              | 734 ms: 1.06x slower                                                  |
| pickle                  | 7.17 us                                                             | 7.61 us: 1.06x slower                                                 |
| crypto_pyaes            | 51.8 ms                                                             | 55.1 ms: 1.06x slower                                                 |
| sympy_sum               | 86.0 ms                                                             | 92.1 ms: 1.07x slower                                                 |
| async_tree_cpu_io_mixed | 534 ms                                                              | 573 ms: 1.07x slower                                                  |
| xml_etree_iterparse     | 69.2 ms                                                             | 74.3 ms: 1.07x slower                                                 |
| dulwich_log             | 29.7 ms                                                             | 32.0 ms: 1.08x slower                                                 |
| chaos                   | 49.4 ms                                                             | 53.3 ms: 1.08x slower                                                 |
| meteor_contest          | 73.3 ms                                                             | 79.4 ms: 1.08x slower                                                 |
| mdp                     | 1.54 sec                                                            | 1.67 sec: 1.08x slower                                                |
| regex_compile           | 76.6 ms                                                             | 83.2 ms: 1.09x slower                                                 |
| deltablue               | 2.81 ms                                                             | 3.06 ms: 1.09x slower                                                 |
| bench_thread_pool       | 474 us                                                              | 516 us: 1.09x slower                                                  |
| 2to3                    | 161 ms                                                              | 178 ms: 1.10x slower                                                  |
| raytrace                | 207 ms                                                              | 228 ms: 1.10x slower                                                  |
| html5lib                | 34.8 ms                                                             | 38.5 ms: 1.11x slower                                                 |
| thrift                  | 431 us                                                              | 478 us: 1.11x slower                                                  |
| sqlite_synth            | 1.28 us                                                             | 1.42 us: 1.11x slower                                                 |
| sympy_str               | 151 ms                                                              | 168 ms: 1.11x slower                                                  |
| async_tree_none         | 285 ms                                                              | 316 ms: 1.11x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 12.8 ms: 1.11x slower                                                 |
| coverage                | 58.4 ms                                                             | 64.8 ms: 1.11x slower                                                 |
| sympy_expand            | 243 ms                                                              | 270 ms: 1.11x slower                                                  |
| float                   | 53.0 ms                                                             | 59.1 ms: 1.11x slower                                                 |
| xml_etree_generate      | 48.2 ms                                                             | 53.8 ms: 1.12x slower                                                 |
| unpickle_pure_python    | 158 us                                                              | 177 us: 1.12x slower                                                  |
| chameleon               | 4.55 ms                                                             | 5.09 ms: 1.12x slower                                                 |
| async_tree_io           | 707 ms                                                              | 792 ms: 1.12x slower                                                  |
| nqueens                 | 62.4 ms                                                             | 70.0 ms: 1.12x slower                                                 |
| async_tree_memoization  | 338 ms                                                              | 384 ms: 1.14x slower                                                  |
| sqlglot_parse           | 956 us                                                              | 1.09 ms: 1.14x slower                                                 |
| sqlglot_transpile       | 1.12 ms                                                             | 1.27 ms: 1.14x slower                                                 |
| genshi_text             | 15.3 ms                                                             | 17.5 ms: 1.14x slower                                                 |
| go                      | 109 ms                                                              | 125 ms: 1.14x slower                                                  |
| pprint_pformat          | 946 ms                                                              | 1.08 sec: 1.15x slower                                                |
| pprint_safe_repr        | 463 ms                                                              | 531 ms: 1.15x slower                                                  |
| richards                | 32.2 ms                                                             | 37.0 ms: 1.15x slower                                                 |
| sqlglot_optimize        | 31.2 ms                                                             | 35.8 ms: 1.15x slower                                                 |
| sqlglot_normalize       | 171 ms                                                              | 197 ms: 1.15x slower                                                  |
| xml_etree_process       | 35.0 ms                                                             | 40.4 ms: 1.16x slower                                                 |
| pickle_pure_python      | 198 us                                                              | 229 us: 1.16x slower                                                  |
| genshi_xml              | 29.9 ms                                                             | 34.6 ms: 1.16x slower                                                 |
| spectral_norm           | 72.5 ms                                                             | 84.2 ms: 1.16x slower                                                 |
| django_template         | 21.1 ms                                                             | 24.6 ms: 1.17x slower                                                 |
| logging_format          | 3.77 us                                                             | 4.46 us: 1.18x slower                                                 |
| hexiom                  | 4.73 ms                                                             | 5.60 ms: 1.18x slower                                                 |
| comprehensions          | 16.1 us                                                             | 19.0 us: 1.18x slower                                                 |
| pyflate                 | 309 ms                                                              | 366 ms: 1.18x slower                                                  |
| logging_simple          | 3.49 us                                                             | 4.16 us: 1.19x slower                                                 |
| async_generators        | 195 ms                                                              | 233 ms: 1.19x slower                                                  |
| deepcopy_reduce         | 1.91 us                                                             | 2.32 us: 1.22x slower                                                 |
| deepcopy                | 224 us                                                              | 272 us: 1.22x slower                                                  |
| scimark_lu              | 72.2 ms                                                             | 88.5 ms: 1.23x slower                                                 |
| deepcopy_memo           | 26.3 us                                                             | 32.6 us: 1.24x slower                                                 |
| scimark_monte_carlo     | 46.5 ms                                                             | 57.9 ms: 1.25x slower                                                 |
| logging_silent          | 68.0 ns                                                             | 86.1 ns: 1.27x slower                                                 |
| scimark_sor             | 82.9 ms                                                             | 109 ms: 1.31x slower                                                  |
| coroutines              | 17.7 ms                                                             | 24.5 ms: 1.39x slower                                                 |
| generators              | 28.6 ms                                                             | 42.2 ms: 1.48x slower                                                 |
| unpack_sequence         | 33.5 ns                                                             | 52.7 ns: 1.57x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.10x slower                                                          |

Benchmark hidden because not significant (7): pathlib, unpickle, python_startup, asyncio_tcp, pickle_list, pickle_dict, mypy2
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
