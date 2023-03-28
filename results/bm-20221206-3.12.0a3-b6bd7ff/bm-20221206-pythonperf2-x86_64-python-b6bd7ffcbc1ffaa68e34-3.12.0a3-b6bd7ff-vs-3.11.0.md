
# Results vs. 3.11.0

- fork: python
- ref: b6bd7ffcbc1ffaa68e34
- machine: linux-x86_64
- commit hash: b6bd7ff
- commit date: 2022-12-06
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf2-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 280 ms: 1.04x faster                                                        |
| chameleon      | 7.50 ms                                                                   | 7.70 ms: 1.03x slower                                                       |
| docutils       | 2.86 sec                                                                  | 2.79 sec: 1.03x faster                                                      |
| html5lib       | 70.2 ms                                                                   | 67.0 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf2-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 74.6 ms: 1.01x faster                                                       |
| pidigits       | 252 ms                                                                    | 252 ms: 1.00x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.00x faster                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf2-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                    | 148 ms: 1.04x faster                                                        |
| regex_v8       | 24.4 ms                                                                   | 23.7 ms: 1.03x faster                                                       |
| regex_dna      | 225 ms                                                                    | 233 ms: 1.03x slower                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.51 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf2-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.5 ms: 1.28x faster                                                       |
| json_loads           | 28.4 us                                                                   | 24.2 us: 1.17x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 142 ms: 1.13x faster                                                        |
| unpickle_pure_python | 238 us                                                                    | 214 us: 1.11x faster                                                        |
| pickle_pure_python   | 319 us                                                                    | 313 us: 1.02x faster                                                        |
| unpickle_list        | 4.52 us                                                                   | 4.44 us: 1.02x faster                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 55.2 ms: 1.01x faster                                                       |
| pickle_dict          | 31.1 us                                                                   | 31.2 us: 1.00x slower                                                       |
| pickle               | 9.92 us                                                                   | 10.0 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 106 ms                                                                    | 107 ms: 1.02x slower                                                        |
| pickle_list          | 3.78 us                                                                   | 3.94 us: 1.04x slower                                                       |
| unpickle             | 13.0 us                                                                   | 13.7 us: 1.05x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.04x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf2-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.9 ms: 1.01x slower                                                       |
| python_startup_no_site | 7.73 ms                                                                   | 7.92 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                     | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf2-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 53.0 ms: 1.09x faster                                                       |
| mako            | 10.9 ms                                                                   | 10.4 ms: 1.05x faster                                                       |
| genshi_text     | 26.3 ms                                                                   | 25.1 ms: 1.05x faster                                                       |
| django_template | 39.6 ms                                                                   | 40.0 ms: 1.01x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.04x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf2-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 13.4 ms                                                                   | 10.5 ms: 1.28x faster                                                       |
| mypy2                   | 446 ms                                                                    | 375 ms: 1.19x faster                                                        |
| json_loads              | 28.4 us                                                                   | 24.2 us: 1.17x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 142 ms: 1.13x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 102 ms: 1.11x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 214 us: 1.11x faster                                                        |
| json                    | 5.59 ms                                                                   | 5.10 ms: 1.10x faster                                                       |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.71 ms: 1.09x faster                                                       |
| genshi_xml              | 57.8 ms                                                                   | 53.0 ms: 1.09x faster                                                       |
| deltablue               | 3.99 ms                                                                   | 3.69 ms: 1.08x faster                                                       |
| richards                | 49.1 ms                                                                   | 46.2 ms: 1.06x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 28.0 ms: 1.05x faster                                                       |
| mako                    | 10.9 ms                                                                   | 10.4 ms: 1.05x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 4.01 ms: 1.05x faster                                                       |
| genshi_text             | 26.3 ms                                                                   | 25.1 ms: 1.05x faster                                                       |
| html5lib                | 70.2 ms                                                                   | 67.0 ms: 1.05x faster                                                       |
| dulwich_log             | 69.1 ms                                                                   | 66.6 ms: 1.04x faster                                                       |
| regex_compile           | 154 ms                                                                    | 148 ms: 1.04x faster                                                        |
| hexiom                  | 7.00 ms                                                                   | 6.75 ms: 1.04x faster                                                       |
| 2to3                    | 289 ms                                                                    | 280 ms: 1.04x faster                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.59 ms: 1.03x faster                                                       |
| thrift                  | 942 us                                                                    | 912 us: 1.03x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 23.7 ms: 1.03x faster                                                       |
| logging_silent          | 103 ns                                                                    | 99.6 ns: 1.03x faster                                                       |
| logging_format          | 7.84 us                                                                   | 7.63 us: 1.03x faster                                                       |
| docutils                | 2.86 sec                                                                  | 2.79 sec: 1.03x faster                                                      |
| async_tree_memoization  | 639 ms                                                                    | 624 ms: 1.02x faster                                                        |
| bench_thread_pool       | 990 us                                                                    | 968 us: 1.02x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 83.2 ms: 1.02x faster                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.57 sec: 1.02x faster                                                      |
| pickle_pure_python      | 319 us                                                                    | 313 us: 1.02x faster                                                        |
| unpickle_list           | 4.52 us                                                                   | 4.44 us: 1.02x faster                                                       |
| pycparser               | 1.30 sec                                                                  | 1.28 sec: 1.02x faster                                                      |
| float                   | 75.7 ms                                                                   | 74.6 ms: 1.01x faster                                                       |
| fannkuch                | 449 ms                                                                    | 443 ms: 1.01x faster                                                        |
| dask                    | 418 ms                                                                    | 412 ms: 1.01x faster                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 55.2 ms: 1.01x faster                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 760 ms: 1.01x faster                                                        |
| sympy_expand            | 547 ms                                                                    | 542 ms: 1.01x faster                                                        |
| sqlglot_parse           | 1.53 ms                                                                   | 1.52 ms: 1.01x faster                                                       |
| mdp                     | 2.73 sec                                                                  | 2.71 sec: 1.01x faster                                                      |
| meteor_contest          | 129 ms                                                                    | 129 ms: 1.00x faster                                                        |
| asyncio_tcp             | 752 ms                                                                    | 749 ms: 1.00x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 36.9 us: 1.00x faster                                                       |
| pidigits                | 252 ms                                                                    | 252 ms: 1.00x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 31.2 us: 1.00x slower                                                       |
| telco                   | 6.70 ms                                                                   | 6.73 ms: 1.00x slower                                                       |
| scimark_fft             | 276 ms                                                                    | 278 ms: 1.01x slower                                                        |
| sympy_str               | 333 ms                                                                    | 335 ms: 1.01x slower                                                        |
| django_template         | 39.6 ms                                                                   | 40.0 ms: 1.01x slower                                                       |
| logging_simple          | 6.95 us                                                                   | 7.02 us: 1.01x slower                                                       |
| pickle                  | 9.92 us                                                                   | 10.0 us: 1.01x slower                                                       |
| async_tree_io           | 1.18 sec                                                                  | 1.19 sec: 1.01x slower                                                      |
| pathlib                 | 19.2 ms                                                                   | 19.4 ms: 1.01x slower                                                       |
| python_startup          | 10.7 ms                                                                   | 10.9 ms: 1.01x slower                                                       |
| pyflate                 | 438 ms                                                                    | 443 ms: 1.01x slower                                                        |
| scimark_sor             | 109 ms                                                                    | 111 ms: 1.01x slower                                                        |
| deepcopy                | 384 us                                                                    | 390 us: 1.02x slower                                                        |
| sympy_sum               | 182 ms                                                                    | 185 ms: 1.02x slower                                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 107 ms: 1.02x slower                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.7 ms: 1.02x slower                                                       |
| chaos                   | 76.2 ms                                                                   | 77.8 ms: 1.02x slower                                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 770 ms: 1.02x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.92 ms: 1.03x slower                                                       |
| chameleon               | 7.50 ms                                                                   | 7.70 ms: 1.03x slower                                                       |
| deepcopy_reduce         | 3.39 us                                                                   | 3.49 us: 1.03x slower                                                       |
| spectral_norm           | 95.1 ms                                                                   | 98.0 ms: 1.03x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.56 us: 1.03x slower                                                       |
| regex_dna               | 225 ms                                                                    | 233 ms: 1.03x slower                                                        |
| go                      | 158 ms                                                                    | 164 ms: 1.04x slower                                                        |
| raytrace                | 303 ms                                                                    | 316 ms: 1.04x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 3.94 us: 1.04x slower                                                       |
| unpickle                | 13.0 us                                                                   | 13.7 us: 1.05x slower                                                       |
| async_generators        | 318 ms                                                                    | 334 ms: 1.05x slower                                                        |
| coverage                | 86.0 ms                                                                   | 90.9 ms: 1.06x slower                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.51 ms: 1.06x slower                                                       |
| generators              | 56.0 ms                                                                   | 60.6 ms: 1.08x slower                                                       |
| comprehensions          | 24.7 us                                                                   | 27.1 us: 1.10x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.01x faster                                                                |

Benchmark hidden because not significant (10): unpack_sequence, sqlglot_normalize, sqlglot_optimize, scimark_monte_carlo, nbody, xml_etree_generate, async_tree_none, sqlglot_transpile, bench_mp_pool, nqueens
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
