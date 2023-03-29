
# Results vs. 3.11.0

- fork: python
- ref: 3c67ec394faac79d2608
- machine: linux-x86_64
- commit hash: 3c67ec3
- commit date: 2023-02-07
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 282 ms: 1.03x faster                                                        |
| chameleon      | 7.50 ms                                                                   | 7.46 ms: 1.01x faster                                                       |
| docutils       | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                      |
| html5lib       | 70.2 ms                                                                   | 65.3 ms: 1.07x faster                                                       |
| tornado_http   | 125 ms                                                                    | 117 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 71.9 ms: 1.05x faster                                                       |
| pidigits       | 252 ms                                                                    | 251 ms: 1.00x faster                                                        |
| nbody          | 92.1 ms                                                                   | 101 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 22.7 ms: 1.08x faster                                                       |
| regex_compile  | 154 ms                                                                    | 145 ms: 1.06x faster                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.50 ms: 1.06x slower                                                       |
| regex_dna      | 225 ms                                                                    | 240 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.00x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.0 ms: 1.33x faster                                                       |
| json_loads           | 28.4 us                                                                   | 23.8 us: 1.19x faster                                                       |
| unpickle_pure_python | 238 us                                                                    | 204 us: 1.17x faster                                                        |
| xml_etree_parse      | 161 ms                                                                    | 142 ms: 1.13x faster                                                        |
| xml_etree_iterparse  | 106 ms                                                                    | 103 ms: 1.03x faster                                                        |
| pickle_pure_python   | 319 us                                                                    | 312 us: 1.02x faster                                                        |
| unpickle             | 13.0 us                                                                   | 12.8 us: 1.02x faster                                                       |
| pickle_list          | 3.78 us                                                                   | 3.84 us: 1.02x slower                                                       |
| pickle_dict          | 31.1 us                                                                   | 31.6 us: 1.02x slower                                                       |
| xml_etree_generate   | 79.1 ms                                                                   | 80.6 ms: 1.02x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.06x faster                                                                |

Benchmark hidden because not significant (3): pickle, unpickle_list, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.2 ms: 1.04x slower                                                       |
| python_startup_no_site | 7.73 ms                                                                   | 8.25 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                                     | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 53.4 ms: 1.08x faster                                                       |
| genshi_text     | 26.3 ms                                                                   | 24.6 ms: 1.07x faster                                                       |
| mako            | 10.9 ms                                                                   | 10.3 ms: 1.06x faster                                                       |
| django_template | 39.6 ms                                                                   | 40.5 ms: 1.02x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.05x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 388 ms: 1.94x faster                                                        |
| json_dumps              | 13.4 ms                                                                   | 10.0 ms: 1.33x faster                                                       |
| json_loads              | 28.4 us                                                                   | 23.8 us: 1.19x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 3.55 ms: 1.19x faster                                                       |
| mypy2                   | 446 ms                                                                    | 379 ms: 1.18x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 204 us: 1.17x faster                                                        |
| comprehensions          | 24.7 us                                                                   | 21.3 us: 1.16x faster                                                       |
| json                    | 5.59 ms                                                                   | 4.94 ms: 1.13x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 142 ms: 1.13x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.61 ms: 1.12x faster                                                       |
| deltablue               | 3.99 ms                                                                   | 3.60 ms: 1.11x faster                                                       |
| fannkuch                | 449 ms                                                                    | 409 ms: 1.10x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 104 ms: 1.10x faster                                                        |
| chaos                   | 76.2 ms                                                                   | 69.6 ms: 1.10x faster                                                       |
| genshi_xml              | 57.8 ms                                                                   | 53.4 ms: 1.08x faster                                                       |
| hexiom                  | 7.00 ms                                                                   | 6.49 ms: 1.08x faster                                                       |
| regex_v8                | 24.4 ms                                                                   | 22.7 ms: 1.08x faster                                                       |
| html5lib                | 70.2 ms                                                                   | 65.3 ms: 1.07x faster                                                       |
| tornado_http            | 125 ms                                                                    | 117 ms: 1.07x faster                                                        |
| nqueens                 | 101 ms                                                                    | 94.2 ms: 1.07x faster                                                       |
| genshi_text             | 26.3 ms                                                                   | 24.6 ms: 1.07x faster                                                       |
| richards                | 49.1 ms                                                                   | 46.1 ms: 1.06x faster                                                       |
| regex_compile           | 154 ms                                                                    | 145 ms: 1.06x faster                                                        |
| async_tree_memoization  | 639 ms                                                                    | 601 ms: 1.06x faster                                                        |
| logging_silent          | 103 ns                                                                    | 96.5 ns: 1.06x faster                                                       |
| sympy_str               | 333 ms                                                                    | 313 ms: 1.06x faster                                                        |
| mako                    | 10.9 ms                                                                   | 10.3 ms: 1.06x faster                                                       |
| unpack_sequence         | 45.9 ns                                                                   | 43.3 ns: 1.06x faster                                                       |
| sympy_sum               | 182 ms                                                                    | 172 ms: 1.06x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.43 us: 1.06x faster                                                       |
| float                   | 75.7 ms                                                                   | 71.9 ms: 1.05x faster                                                       |
| async_tree_none         | 529 ms                                                                    | 503 ms: 1.05x faster                                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.53 sec: 1.04x faster                                                      |
| logging_simple          | 6.95 us                                                                   | 6.67 us: 1.04x faster                                                       |
| sympy_integrate         | 25.3 ms                                                                   | 24.3 ms: 1.04x faster                                                       |
| scimark_sor             | 109 ms                                                                    | 105 ms: 1.04x faster                                                        |
| sympy_expand            | 547 ms                                                                    | 526 ms: 1.04x faster                                                        |
| go                      | 158 ms                                                                    | 152 ms: 1.04x faster                                                        |
| dulwich_log             | 69.1 ms                                                                   | 66.6 ms: 1.04x faster                                                       |
| crypto_pyaes            | 85.0 ms                                                                   | 81.8 ms: 1.04x faster                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 744 ms: 1.03x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 35.8 us: 1.03x faster                                                       |
| xml_etree_iterparse     | 106 ms                                                                    | 103 ms: 1.03x faster                                                        |
| docutils                | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                      |
| 2to3                    | 289 ms                                                                    | 282 ms: 1.03x faster                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.30 us: 1.03x faster                                                       |
| pickle_pure_python      | 319 us                                                                    | 312 us: 1.02x faster                                                        |
| mdp                     | 2.73 sec                                                                  | 2.66 sec: 1.02x faster                                                      |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 737 ms: 1.02x faster                                                        |
| pyflate                 | 438 ms                                                                    | 428 ms: 1.02x faster                                                        |
| pycparser               | 1.30 sec                                                                  | 1.28 sec: 1.02x faster                                                      |
| unpickle                | 13.0 us                                                                   | 12.8 us: 1.02x faster                                                       |
| telco                   | 6.70 ms                                                                   | 6.59 ms: 1.02x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 29.1 ms: 1.01x faster                                                       |
| async_tree_io           | 1.18 sec                                                                  | 1.17 sec: 1.01x faster                                                      |
| sqlglot_optimize        | 58.6 ms                                                                   | 57.7 ms: 1.01x faster                                                       |
| sqlglot_normalize       | 122 ms                                                                    | 120 ms: 1.01x faster                                                        |
| raytrace                | 303 ms                                                                    | 301 ms: 1.01x faster                                                        |
| meteor_contest          | 129 ms                                                                    | 128 ms: 1.01x faster                                                        |
| chameleon               | 7.50 ms                                                                   | 7.46 ms: 1.01x faster                                                       |
| pidigits                | 252 ms                                                                    | 251 ms: 1.00x faster                                                        |
| pickle_list             | 3.78 us                                                                   | 3.84 us: 1.02x slower                                                       |
| pickle_dict             | 31.1 us                                                                   | 31.6 us: 1.02x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 1.56 ms: 1.02x slower                                                       |
| xml_etree_generate      | 79.1 ms                                                                   | 80.6 ms: 1.02x slower                                                       |
| async_generators        | 318 ms                                                                    | 325 ms: 1.02x slower                                                        |
| django_template         | 39.6 ms                                                                   | 40.5 ms: 1.02x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.93 ms: 1.03x slower                                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 70.2 ms: 1.03x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.58 us: 1.04x slower                                                       |
| bench_mp_pool           | 4.54 ms                                                                   | 4.71 ms: 1.04x slower                                                       |
| python_startup          | 10.7 ms                                                                   | 11.2 ms: 1.04x slower                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.50 ms: 1.06x slower                                                       |
| regex_dna               | 225 ms                                                                    | 240 ms: 1.07x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.25 ms: 1.07x slower                                                       |
| generators              | 56.0 ms                                                                   | 60.4 ms: 1.08x slower                                                       |
| nbody                   | 92.1 ms                                                                   | 101 ms: 1.10x slower                                                        |
| dask                    | 418 ms                                                                    | 562 ms: 1.35x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.04x faster                                                                |

Benchmark hidden because not significant (11): bench_thread_pool, thrift, pickle, unpickle_list, create_gc_cycles, xml_etree_process, pathlib, deepcopy, coverage, spectral_norm, scimark_fft
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
