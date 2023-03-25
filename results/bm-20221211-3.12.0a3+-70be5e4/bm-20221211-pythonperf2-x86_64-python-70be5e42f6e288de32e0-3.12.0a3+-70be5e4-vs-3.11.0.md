
# Results vs. 3.11.0

- fork: python
- ref: 70be5e42f6e288de32e0
- machine: linux-x86_64
- commit hash: 70be5e4
- commit date: 2022-12-11
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf2-x86_64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 281 ms: 1.03x faster                                                         |
| docutils       | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 67.6 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf2-x86_64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 73.3 ms: 1.03x faster                                                        |
| nbody          | 92.1 ms                                                                   | 89.3 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf2-x86_64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 23.7 ms: 1.03x faster                                                        |
| regex_compile  | 154 ms                                                                    | 150 ms: 1.03x faster                                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.43 ms: 1.04x slower                                                        |
| regex_dna      | 225 ms                                                                    | 236 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf2-x86_64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.3 ms: 1.30x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.0 us: 1.18x faster                                                        |
| xml_etree_parse      | 161 ms                                                                    | 141 ms: 1.14x faster                                                         |
| unpickle_pure_python | 238 us                                                                    | 216 us: 1.10x faster                                                         |
| unpickle_list        | 4.52 us                                                                   | 4.33 us: 1.04x faster                                                        |
| xml_etree_process    | 55.8 ms                                                                   | 54.3 ms: 1.03x faster                                                        |
| pickle_pure_python   | 319 us                                                                    | 311 us: 1.03x faster                                                         |
| pickle               | 9.92 us                                                                   | 9.71 us: 1.02x faster                                                        |
| pickle_list          | 3.78 us                                                                   | 3.70 us: 1.02x faster                                                        |
| unpickle             | 13.0 us                                                                   | 13.0 us: 1.01x faster                                                        |
| pickle_dict          | 31.1 us                                                                   | 31.6 us: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.06x faster                                                                 |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf2-x86_64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.8 ms: 1.00x slower                                                        |
| python_startup_no_site | 7.73 ms                                                                   | 7.85 ms: 1.02x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf2-x86_64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml     | 57.8 ms                                                                   | 53.1 ms: 1.09x faster                                                        |
| genshi_text    | 26.3 ms                                                                   | 24.4 ms: 1.08x faster                                                        |
| mako           | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.06x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf2-x86_64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps              | 13.4 ms                                                                   | 10.3 ms: 1.30x faster                                                        |
| mypy2                   | 446 ms                                                                    | 373 ms: 1.20x faster                                                         |
| json_loads              | 28.4 us                                                                   | 24.0 us: 1.18x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 141 ms: 1.14x faster                                                         |
| scimark_lu              | 114 ms                                                                    | 101 ms: 1.13x faster                                                         |
| gc_traversal            | 4.22 ms                                                                   | 3.75 ms: 1.12x faster                                                        |
| fannkuch                | 449 ms                                                                    | 405 ms: 1.11x faster                                                         |
| json                    | 5.59 ms                                                                   | 5.04 ms: 1.11x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 216 us: 1.10x faster                                                         |
| genshi_xml              | 57.8 ms                                                                   | 53.1 ms: 1.09x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.74 ms: 1.09x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 24.4 ms: 1.08x faster                                                        |
| deltablue               | 3.99 ms                                                                   | 3.73 ms: 1.07x faster                                                        |
| mako                    | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 27.7 ms: 1.06x faster                                                        |
| asyncio_tcp             | 752 ms                                                                    | 709 ms: 1.06x faster                                                         |
| richards                | 49.1 ms                                                                   | 47.0 ms: 1.05x faster                                                        |
| unpickle_list           | 4.52 us                                                                   | 4.33 us: 1.04x faster                                                        |
| thrift                  | 942 us                                                                    | 905 us: 1.04x faster                                                         |
| create_gc_cycles        | 1.65 ms                                                                   | 1.58 ms: 1.04x faster                                                        |
| html5lib                | 70.2 ms                                                                   | 67.6 ms: 1.04x faster                                                        |
| dulwich_log             | 69.1 ms                                                                   | 66.7 ms: 1.04x faster                                                        |
| async_tree_memoization  | 639 ms                                                                    | 618 ms: 1.03x faster                                                         |
| logging_format          | 7.84 us                                                                   | 7.59 us: 1.03x faster                                                        |
| float                   | 75.7 ms                                                                   | 73.3 ms: 1.03x faster                                                        |
| logging_silent          | 103 ns                                                                    | 99.3 ns: 1.03x faster                                                        |
| nbody                   | 92.1 ms                                                                   | 89.3 ms: 1.03x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 23.7 ms: 1.03x faster                                                        |
| scimark_sor             | 109 ms                                                                    | 106 ms: 1.03x faster                                                         |
| 2to3                    | 289 ms                                                                    | 281 ms: 1.03x faster                                                         |
| docutils                | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                       |
| xml_etree_process       | 55.8 ms                                                                   | 54.3 ms: 1.03x faster                                                        |
| mdp                     | 2.73 sec                                                                  | 2.65 sec: 1.03x faster                                                       |
| deepcopy                | 384 us                                                                    | 373 us: 1.03x faster                                                         |
| pickle_pure_python      | 319 us                                                                    | 311 us: 1.03x faster                                                         |
| bench_thread_pool       | 990 us                                                                    | 963 us: 1.03x faster                                                         |
| nqueens                 | 101 ms                                                                    | 98.2 ms: 1.03x faster                                                        |
| regex_compile           | 154 ms                                                                    | 150 ms: 1.03x faster                                                         |
| pathlib                 | 19.2 ms                                                                   | 18.8 ms: 1.02x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 36.2 us: 1.02x faster                                                        |
| pickle                  | 9.92 us                                                                   | 9.71 us: 1.02x faster                                                        |
| telco                   | 6.70 ms                                                                   | 6.56 ms: 1.02x faster                                                        |
| pickle_list             | 3.78 us                                                                   | 3.70 us: 1.02x faster                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.33 us: 1.02x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 520 ms: 1.02x faster                                                         |
| sqlglot_normalize       | 122 ms                                                                    | 120 ms: 1.01x faster                                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.58 sec: 1.01x faster                                                       |
| logging_simple          | 6.95 us                                                                   | 6.87 us: 1.01x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 84.0 ms: 1.01x faster                                                        |
| dask                    | 418 ms                                                                    | 413 ms: 1.01x faster                                                         |
| sympy_expand            | 547 ms                                                                    | 541 ms: 1.01x faster                                                         |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                       |
| hexiom                  | 7.00 ms                                                                   | 6.94 ms: 1.01x faster                                                        |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.1 ms: 1.01x faster                                                        |
| unpickle                | 13.0 us                                                                   | 13.0 us: 1.01x faster                                                        |
| meteor_contest          | 129 ms                                                                    | 129 ms: 1.00x faster                                                         |
| python_startup          | 10.7 ms                                                                   | 10.8 ms: 1.00x slower                                                        |
| spectral_norm           | 95.1 ms                                                                   | 95.6 ms: 1.01x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 278 ms: 1.01x slower                                                         |
| sympy_str               | 333 ms                                                                    | 335 ms: 1.01x slower                                                         |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 760 ms: 1.01x slower                                                         |
| chaos                   | 76.2 ms                                                                   | 77.2 ms: 1.01x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.85 ms: 1.02x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 31.6 us: 1.02x slower                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.7 ms: 1.02x slower                                                        |
| async_generators        | 318 ms                                                                    | 328 ms: 1.03x slower                                                         |
| regex_effbot            | 3.31 ms                                                                   | 3.43 ms: 1.04x slower                                                        |
| sympy_sum               | 182 ms                                                                    | 189 ms: 1.04x slower                                                         |
| regex_dna               | 225 ms                                                                    | 236 ms: 1.05x slower                                                         |
| sqlite_synth            | 2.49 us                                                                   | 2.61 us: 1.05x slower                                                        |
| raytrace                | 303 ms                                                                    | 320 ms: 1.06x slower                                                         |
| go                      | 158 ms                                                                    | 167 ms: 1.06x slower                                                         |
| comprehensions          | 24.7 us                                                                   | 26.8 us: 1.08x slower                                                        |
| generators              | 56.0 ms                                                                   | 61.2 ms: 1.09x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.02x faster                                                                 |

Benchmark hidden because not significant (14): scimark_monte_carlo, unpack_sequence, chameleon, pycparser, pyflate, django_template, pidigits, sqlglot_parse, coverage, pprint_safe_repr, xml_etree_generate, sqlglot_transpile, xml_etree_iterparse, bench_mp_pool
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
