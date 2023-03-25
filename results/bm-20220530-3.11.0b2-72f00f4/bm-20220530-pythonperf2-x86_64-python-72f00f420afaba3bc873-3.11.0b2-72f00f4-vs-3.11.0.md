
# Results vs. 3.11.0

- fork: python
- ref: 72f00f420afaba3bc873
- machine: linux-x86_64
- commit hash: 72f00f4
- commit date: 2022-05-30
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf2-x86_64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 282 ms: 1.03x faster                                                        |
| docutils       | 2.86 sec                                                                  | 2.85 sec: 1.00x faster                                                      |
| tornado_http   | 125 ms                                                                    | 122 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                |

Benchmark hidden because not significant (2): chameleon, html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf2-x86_64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 92.1 ms                                                                   | 89.8 ms: 1.03x faster                                                       |
| float          | 75.7 ms                                                                   | 73.8 ms: 1.03x faster                                                       |
| pidigits       | 252 ms                                                                    | 251 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf2-x86_64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.31 ms                                                                   | 3.17 ms: 1.04x faster                                                       |
| regex_v8       | 24.4 ms                                                                   | 24.1 ms: 1.02x faster                                                       |
| regex_dna      | 225 ms                                                                    | 223 ms: 1.01x faster                                                        |
| regex_compile  | 154 ms                                                                    | 155 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf2-x86_64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                   | 24.8 us: 1.15x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 153 ms: 1.05x faster                                                        |
| pickle               | 9.92 us                                                                   | 9.79 us: 1.01x faster                                                       |
| unpickle_pure_python | 238 us                                                                    | 235 us: 1.01x faster                                                        |
| json_dumps           | 13.4 ms                                                                   | 13.3 ms: 1.01x faster                                                       |
| pickle_dict          | 31.1 us                                                                   | 30.9 us: 1.01x faster                                                       |
| xml_etree_generate   | 79.1 ms                                                                   | 79.9 ms: 1.01x slower                                                       |
| pickle_pure_python   | 319 us                                                                    | 324 us: 1.02x slower                                                        |
| unpickle             | 13.0 us                                                                   | 13.4 us: 1.03x slower                                                       |
| unpickle_list        | 4.52 us                                                                   | 4.66 us: 1.03x slower                                                       |
| pickle_list          | 3.78 us                                                                   | 3.97 us: 1.05x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.01x faster                                                                |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf2-x86_64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.6 ms: 1.01x faster                                                       |
| python_startup_no_site | 7.73 ms                                                                   | 7.67 ms: 1.01x faster                                                       |
| Geometric mean         | (ref)                                                                     | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf2-x86_64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 26.3 ms                                                                   | 25.1 ms: 1.05x faster                                                       |
| genshi_xml      | 57.8 ms                                                                   | 56.9 ms: 1.02x faster                                                       |
| mako            | 10.9 ms                                                                   | 11.0 ms: 1.01x slower                                                       |
| django_template | 39.6 ms                                                                   | 40.4 ms: 1.02x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf2-x86_64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads              | 28.4 us                                                                   | 24.8 us: 1.15x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.70 ms: 1.14x faster                                                       |
| json                    | 5.59 ms                                                                   | 5.19 ms: 1.08x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 153 ms: 1.05x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 25.1 ms: 1.05x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 28.2 ms: 1.05x faster                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.17 ms: 1.04x faster                                                       |
| sympy_sum               | 182 ms                                                                    | 176 ms: 1.04x faster                                                        |
| chaos                   | 76.2 ms                                                                   | 73.9 ms: 1.03x faster                                                       |
| generators              | 56.0 ms                                                                   | 54.2 ms: 1.03x faster                                                       |
| logging_silent          | 103 ns                                                                    | 99.8 ns: 1.03x faster                                                       |
| nqueens                 | 101 ms                                                                    | 98.2 ms: 1.03x faster                                                       |
| 2to3                    | 289 ms                                                                    | 282 ms: 1.03x faster                                                        |
| tornado_http            | 125 ms                                                                    | 122 ms: 1.03x faster                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.61 ms: 1.03x faster                                                       |
| nbody                   | 92.1 ms                                                                   | 89.8 ms: 1.03x faster                                                       |
| float                   | 75.7 ms                                                                   | 73.8 ms: 1.03x faster                                                       |
| dulwich_log             | 69.1 ms                                                                   | 67.5 ms: 1.02x faster                                                       |
| async_tree_memoization  | 639 ms                                                                    | 624 ms: 1.02x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 516 ms: 1.02x faster                                                        |
| sympy_expand            | 547 ms                                                                    | 536 ms: 1.02x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.71 us: 1.02x faster                                                       |
| sympy_str               | 333 ms                                                                    | 327 ms: 1.02x faster                                                        |
| genshi_xml              | 57.8 ms                                                                   | 56.9 ms: 1.02x faster                                                       |
| regex_v8                | 24.4 ms                                                                   | 24.1 ms: 1.02x faster                                                       |
| pickle                  | 9.92 us                                                                   | 9.79 us: 1.01x faster                                                       |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                      |
| sqlalchemy_declarative  | 156 ms                                                                    | 154 ms: 1.01x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 235 us: 1.01x faster                                                        |
| python_startup          | 10.7 ms                                                                   | 10.6 ms: 1.01x faster                                                       |
| aiohttp                 | 959 us                                                                    | 949 us: 1.01x faster                                                        |
| thrift                  | 942 us                                                                    | 933 us: 1.01x faster                                                        |
| sqlalchemy_imperative   | 19.8 ms                                                                   | 19.6 ms: 1.01x faster                                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 746 ms: 1.01x faster                                                        |
| pycparser               | 1.30 sec                                                                  | 1.29 sec: 1.01x faster                                                      |
| regex_dna               | 225 ms                                                                    | 223 ms: 1.01x faster                                                        |
| json_dumps              | 13.4 ms                                                                   | 13.3 ms: 1.01x faster                                                       |
| python_startup_no_site  | 7.73 ms                                                                   | 7.67 ms: 1.01x faster                                                       |
| gunicorn                | 936 us                                                                    | 930 us: 1.01x faster                                                        |
| async_generators        | 318 ms                                                                    | 316 ms: 1.01x faster                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.1 ms: 1.01x faster                                                       |
| pickle_dict             | 31.1 us                                                                   | 30.9 us: 1.01x faster                                                       |
| docutils                | 2.86 sec                                                                  | 2.85 sec: 1.00x faster                                                      |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.04 ms: 1.00x faster                                                       |
| pidigits                | 252 ms                                                                    | 251 ms: 1.00x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 85.4 ms: 1.00x slower                                                       |
| pyflate                 | 438 ms                                                                    | 440 ms: 1.01x slower                                                        |
| sqlglot_normalize       | 122 ms                                                                    | 123 ms: 1.01x slower                                                        |
| raytrace                | 303 ms                                                                    | 305 ms: 1.01x slower                                                        |
| meteor_contest          | 129 ms                                                                    | 130 ms: 1.01x slower                                                        |
| mdp                     | 2.73 sec                                                                  | 2.75 sec: 1.01x slower                                                      |
| regex_compile           | 154 ms                                                                    | 155 ms: 1.01x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 79.9 ms: 1.01x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.51 us: 1.01x slower                                                       |
| sqlglot_optimize        | 58.6 ms                                                                   | 59.2 ms: 1.01x slower                                                       |
| deltablue               | 3.99 ms                                                                   | 4.05 ms: 1.01x slower                                                       |
| scimark_lu              | 114 ms                                                                    | 116 ms: 1.01x slower                                                        |
| mako                    | 10.9 ms                                                                   | 11.0 ms: 1.01x slower                                                       |
| pickle_pure_python      | 319 us                                                                    | 324 us: 1.02x slower                                                        |
| hexiom                  | 7.00 ms                                                                   | 7.12 ms: 1.02x slower                                                       |
| django_template         | 39.6 ms                                                                   | 40.4 ms: 1.02x slower                                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 69.3 ms: 1.02x slower                                                       |
| unpickle                | 13.0 us                                                                   | 13.4 us: 1.03x slower                                                       |
| unpickle_list           | 4.52 us                                                                   | 4.66 us: 1.03x slower                                                       |
| spectral_norm           | 95.1 ms                                                                   | 98.9 ms: 1.04x slower                                                       |
| fannkuch                | 449 ms                                                                    | 469 ms: 1.04x slower                                                        |
| telco                   | 6.70 ms                                                                   | 7.01 ms: 1.05x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 290 ms: 1.05x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 3.97 us: 1.05x slower                                                       |
| comprehensions          | 24.7 us                                                                   | 28.3 us: 1.14x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.29 ms: 1.22x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 1.94 ms: 1.27x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.00x faster                                                                |

Benchmark hidden because not significant (21): bench_mp_pool, pylint, logging_simple, mypy2, xml_etree_iterparse, asyncio_tcp, pprint_pformat, xml_etree_process, dask, unpack_sequence, pathlib, deepcopy, scimark_sor, chameleon, pprint_safe_repr, deepcopy_memo, go, bench_thread_pool, deepcopy_reduce, richards, html5lib
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: coverage, flaskblogging
