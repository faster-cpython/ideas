
# Results vs. 3.11.0

- fork: python
- ref: f3cb15c88afa2e87067d
- machine: linux-x86_64
- commit hash: f3cb15c
- commit date: 2023-02-26
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 285 ms: 1.01x faster                                                         |
| chameleon      | 7.50 ms                                                                   | 6.83 ms: 1.10x faster                                                        |
| docutils       | 2.86 sec                                                                  | 2.82 sec: 1.01x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 67.1 ms: 1.05x faster                                                        |
| tornado_http   | 125 ms                                                                    | 117 ms: 1.07x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.05x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 72.5 ms: 1.05x faster                                                        |
| nbody          | 92.1 ms                                                                   | 94.5 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                        |
| regex_compile  | 154 ms                                                                    | 147 ms: 1.04x faster                                                         |
| regex_dna      | 225 ms                                                                    | 222 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.1 ms: 1.33x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.1 us: 1.18x faster                                                        |
| unpickle_pure_python | 238 us                                                                    | 205 us: 1.16x faster                                                         |
| xml_etree_parse      | 161 ms                                                                    | 144 ms: 1.12x faster                                                         |
| pickle_pure_python   | 319 us                                                                    | 310 us: 1.03x faster                                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 103 ms: 1.02x faster                                                         |
| unpickle_list        | 4.52 us                                                                   | 4.43 us: 1.02x faster                                                        |
| pickle               | 9.92 us                                                                   | 9.80 us: 1.01x faster                                                        |
| pickle_dict          | 31.1 us                                                                   | 31.3 us: 1.01x slower                                                        |
| unpickle             | 13.0 us                                                                   | 13.2 us: 1.01x slower                                                        |
| pickle_list          | 3.78 us                                                                   | 3.92 us: 1.04x slower                                                        |
| xml_etree_process    | 55.8 ms                                                                   | 58.2 ms: 1.04x slower                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 84.2 ms: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.05x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.3 ms: 1.06x slower                                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.39 ms: 1.09x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.07x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|-----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.9 ms                                                                   | 9.87 ms: 1.10x faster                                                        |
| genshi_text     | 26.3 ms                                                                   | 25.1 ms: 1.05x faster                                                        |
| genshi_xml      | 57.8 ms                                                                   | 55.8 ms: 1.04x faster                                                        |
| django_template | 39.6 ms                                                                   | 41.1 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                                     | 1.04x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 387 ms: 1.94x faster                                                         |
| generators              | 56.0 ms                                                                   | 38.6 ms: 1.45x faster                                                        |
| json_dumps              | 13.4 ms                                                                   | 10.1 ms: 1.33x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 24.4 ms: 1.21x faster                                                        |
| deltablue               | 3.99 ms                                                                   | 3.35 ms: 1.19x faster                                                        |
| json_loads              | 28.4 us                                                                   | 24.1 us: 1.18x faster                                                        |
| mypy2                   | 446 ms                                                                    | 381 ms: 1.17x faster                                                         |
| unpickle_pure_python    | 238 us                                                                    | 205 us: 1.16x faster                                                         |
| json                    | 5.59 ms                                                                   | 4.98 ms: 1.12x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 144 ms: 1.12x faster                                                         |
| fannkuch                | 449 ms                                                                    | 404 ms: 1.11x faster                                                         |
| mako                    | 10.9 ms                                                                   | 9.87 ms: 1.10x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 104 ms: 1.10x faster                                                         |
| chameleon               | 7.50 ms                                                                   | 6.83 ms: 1.10x faster                                                        |
| logging_silent          | 103 ns                                                                    | 95.3 ns: 1.08x faster                                                        |
| chaos                   | 76.2 ms                                                                   | 71.0 ms: 1.07x faster                                                        |
| hexiom                  | 7.00 ms                                                                   | 6.53 ms: 1.07x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                        |
| tornado_http            | 125 ms                                                                    | 117 ms: 1.07x faster                                                         |
| dulwich_log             | 69.1 ms                                                                   | 65.0 ms: 1.06x faster                                                        |
| gc_traversal            | 4.22 ms                                                                   | 3.99 ms: 1.06x faster                                                        |
| richards                | 49.1 ms                                                                   | 46.4 ms: 1.06x faster                                                        |
| go                      | 158 ms                                                                    | 150 ms: 1.05x faster                                                         |
| html5lib                | 70.2 ms                                                                   | 67.1 ms: 1.05x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 25.1 ms: 1.05x faster                                                        |
| float                   | 75.7 ms                                                                   | 72.5 ms: 1.05x faster                                                        |
| regex_compile           | 154 ms                                                                    | 147 ms: 1.04x faster                                                         |
| async_tree_memoization  | 639 ms                                                                    | 615 ms: 1.04x faster                                                         |
| genshi_xml              | 57.8 ms                                                                   | 55.8 ms: 1.04x faster                                                        |
| pickle_pure_python      | 319 us                                                                    | 310 us: 1.03x faster                                                         |
| meteor_contest          | 129 ms                                                                    | 126 ms: 1.03x faster                                                         |
| pathlib                 | 19.2 ms                                                                   | 18.8 ms: 1.02x faster                                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 103 ms: 1.02x faster                                                         |
| pycparser               | 1.30 sec                                                                  | 1.27 sec: 1.02x faster                                                       |
| sqlglot_normalize       | 122 ms                                                                    | 120 ms: 1.02x faster                                                         |
| unpickle_list           | 4.52 us                                                                   | 4.43 us: 1.02x faster                                                        |
| unpack_sequence         | 45.9 ns                                                                   | 45.0 ns: 1.02x faster                                                        |
| raytrace                | 303 ms                                                                    | 298 ms: 1.02x faster                                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.57 sec: 1.02x faster                                                       |
| regex_dna               | 225 ms                                                                    | 222 ms: 1.01x faster                                                         |
| 2to3                    | 289 ms                                                                    | 285 ms: 1.01x faster                                                         |
| docutils                | 2.86 sec                                                                  | 2.82 sec: 1.01x faster                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 759 ms: 1.01x faster                                                         |
| pickle                  | 9.92 us                                                                   | 9.80 us: 1.01x faster                                                        |
| deepcopy_memo           | 37.0 us                                                                   | 36.6 us: 1.01x faster                                                        |
| scimark_sor             | 109 ms                                                                    | 108 ms: 1.01x faster                                                         |
| async_tree_none         | 529 ms                                                                    | 524 ms: 1.01x faster                                                         |
| coverage                | 86.0 ms                                                                   | 85.2 ms: 1.01x faster                                                        |
| pyflate                 | 438 ms                                                                    | 434 ms: 1.01x faster                                                         |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.2 ms: 1.01x faster                                                        |
| mdp                     | 2.73 sec                                                                  | 2.71 sec: 1.01x faster                                                       |
| sympy_integrate         | 25.3 ms                                                                   | 25.4 ms: 1.00x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 31.3 us: 1.01x slower                                                        |
| sympy_str               | 333 ms                                                                    | 336 ms: 1.01x slower                                                         |
| unpickle                | 13.0 us                                                                   | 13.2 us: 1.01x slower                                                        |
| spectral_norm           | 95.1 ms                                                                   | 96.4 ms: 1.01x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 281 ms: 1.02x slower                                                         |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.13 ms: 1.02x slower                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.68 ms: 1.02x slower                                                        |
| telco                   | 6.70 ms                                                                   | 6.83 ms: 1.02x slower                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.47 us: 1.02x slower                                                        |
| logging_simple          | 6.95 us                                                                   | 7.11 us: 1.02x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 69.4 ms: 1.02x slower                                                        |
| nbody                   | 92.1 ms                                                                   | 94.5 ms: 1.03x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.57 us: 1.03x slower                                                        |
| sympy_sum               | 182 ms                                                                    | 188 ms: 1.03x slower                                                         |
| sqlglot_parse           | 1.53 ms                                                                   | 1.58 ms: 1.04x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 3.92 us: 1.04x slower                                                        |
| deepcopy                | 384 us                                                                    | 398 us: 1.04x slower                                                         |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.95 ms: 1.04x slower                                                        |
| django_template         | 39.6 ms                                                                   | 41.1 ms: 1.04x slower                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 58.2 ms: 1.04x slower                                                        |
| python_startup          | 10.7 ms                                                                   | 11.3 ms: 1.06x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 84.2 ms: 1.06x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.39 ms: 1.09x slower                                                        |
| bench_mp_pool           | 4.54 ms                                                                   | 4.96 ms: 1.09x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 27.4 us: 1.11x slower                                                        |
| async_generators        | 318 ms                                                                    | 393 ms: 1.24x slower                                                         |
| dask                    | 418 ms                                                                    | 563 ms: 1.35x slower                                                         |
| Geometric mean          | (ref)                                                                     | 1.03x faster                                                                 |

Benchmark hidden because not significant (10): nqueens, bench_thread_pool, crypto_pyaes, pidigits, sympy_expand, async_tree_io, regex_effbot, thrift, async_tree_cpu_io_mixed, logging_format
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
