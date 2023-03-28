
# Results vs. 3.11.0

- fork: python
- ref: 4ae1a0ecaffe4320fe97
- machine: linux-x86_64
- commit hash: 4ae1a0e
- commit date: 2022-10-25
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 278 ms: 1.04x faster                                                        |
| chameleon      | 7.50 ms                                                                   | 7.62 ms: 1.02x slower                                                       |
| docutils       | 2.86 sec                                                                  | 2.79 sec: 1.02x faster                                                      |
| html5lib       | 70.2 ms                                                                   | 66.2 ms: 1.06x faster                                                       |
| tornado_http   | 125 ms                                                                    | 114 ms: 1.09x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.04x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 73.2 ms: 1.03x faster                                                       |
| nbody          | 92.1 ms                                                                   | 98.1 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                       |
| regex_compile  | 154 ms                                                                    | 146 ms: 1.06x faster                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.34 ms: 1.01x slower                                                       |
| regex_dna      | 225 ms                                                                    | 232 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.4 ms: 1.29x faster                                                       |
| json_loads           | 28.4 us                                                                   | 24.3 us: 1.17x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 138 ms: 1.16x faster                                                        |
| unpickle_pure_python | 238 us                                                                    | 208 us: 1.14x faster                                                        |
| xml_etree_process    | 55.8 ms                                                                   | 54.1 ms: 1.03x faster                                                       |
| xml_etree_iterparse  | 106 ms                                                                    | 103 ms: 1.03x faster                                                        |
| pickle_pure_python   | 319 us                                                                    | 313 us: 1.02x faster                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 77.6 ms: 1.02x faster                                                       |
| unpickle_list        | 4.52 us                                                                   | 4.47 us: 1.01x faster                                                       |
| pickle_list          | 3.78 us                                                                   | 3.84 us: 1.02x slower                                                       |
| unpickle             | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                       |
| pickle               | 9.92 us                                                                   | 10.1 us: 1.02x slower                                                       |
| pickle_dict          | 31.1 us                                                                   | 31.9 us: 1.03x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.06x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                                   | 7.62 ms: 1.01x faster                                                       |
| python_startup         | 10.7 ms                                                                   | 10.6 ms: 1.01x faster                                                       |
| Geometric mean         | (ref)                                                                     | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 26.3 ms                                                                   | 24.7 ms: 1.06x faster                                                       |
| mako            | 10.9 ms                                                                   | 10.4 ms: 1.04x faster                                                       |
| genshi_xml      | 57.8 ms                                                                   | 55.5 ms: 1.04x faster                                                       |
| django_template | 39.6 ms                                                                   | 40.6 ms: 1.03x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.03x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 13.4 ms                                                                   | 10.4 ms: 1.29x faster                                                       |
| mypy2                   | 446 ms                                                                    | 372 ms: 1.20x faster                                                        |
| gc_traversal            | 4.22 ms                                                                   | 3.54 ms: 1.19x faster                                                       |
| json_loads              | 28.4 us                                                                   | 24.3 us: 1.17x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 138 ms: 1.16x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 208 us: 1.14x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.58 ms: 1.13x faster                                                       |
| fannkuch                | 449 ms                                                                    | 405 ms: 1.11x faster                                                        |
| json                    | 5.59 ms                                                                   | 5.05 ms: 1.11x faster                                                       |
| tornado_http            | 125 ms                                                                    | 114 ms: 1.09x faster                                                        |
| deltablue               | 3.99 ms                                                                   | 3.65 ms: 1.09x faster                                                       |
| coroutines              | 29.5 ms                                                                   | 27.4 ms: 1.07x faster                                                       |
| logging_silent          | 103 ns                                                                    | 95.5 ns: 1.07x faster                                                       |
| aiohttp                 | 959 us                                                                    | 894 us: 1.07x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                       |
| genshi_text             | 26.3 ms                                                                   | 24.7 ms: 1.06x faster                                                       |
| html5lib                | 70.2 ms                                                                   | 66.2 ms: 1.06x faster                                                       |
| hexiom                  | 7.00 ms                                                                   | 6.61 ms: 1.06x faster                                                       |
| regex_compile           | 154 ms                                                                    | 146 ms: 1.06x faster                                                        |
| coverage                | 86.0 ms                                                                   | 81.5 ms: 1.05x faster                                                       |
| gunicorn                | 936 us                                                                    | 888 us: 1.05x faster                                                        |
| dulwich_log             | 69.1 ms                                                                   | 65.9 ms: 1.05x faster                                                       |
| pylint                  | 517 ms                                                                    | 496 ms: 1.04x faster                                                        |
| mako                    | 10.9 ms                                                                   | 10.4 ms: 1.04x faster                                                       |
| 2to3                    | 289 ms                                                                    | 278 ms: 1.04x faster                                                        |
| genshi_xml              | 57.8 ms                                                                   | 55.5 ms: 1.04x faster                                                       |
| pycparser               | 1.30 sec                                                                  | 1.25 sec: 1.04x faster                                                      |
| nqueens                 | 101 ms                                                                    | 97.1 ms: 1.04x faster                                                       |
| chaos                   | 76.2 ms                                                                   | 73.4 ms: 1.04x faster                                                       |
| sympy_expand            | 547 ms                                                                    | 527 ms: 1.04x faster                                                        |
| float                   | 75.7 ms                                                                   | 73.2 ms: 1.03x faster                                                       |
| async_tree_memoization  | 639 ms                                                                    | 618 ms: 1.03x faster                                                        |
| richards                | 49.1 ms                                                                   | 47.6 ms: 1.03x faster                                                       |
| xml_etree_process       | 55.8 ms                                                                   | 54.1 ms: 1.03x faster                                                       |
| xml_etree_iterparse     | 106 ms                                                                    | 103 ms: 1.03x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 111 ms: 1.03x faster                                                        |
| meteor_contest          | 129 ms                                                                    | 126 ms: 1.03x faster                                                        |
| generators              | 56.0 ms                                                                   | 54.6 ms: 1.03x faster                                                       |
| bench_thread_pool       | 990 us                                                                    | 966 us: 1.02x faster                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.61 ms: 1.02x faster                                                       |
| async_tree_none         | 529 ms                                                                    | 516 ms: 1.02x faster                                                        |
| docutils                | 2.86 sec                                                                  | 2.79 sec: 1.02x faster                                                      |
| go                      | 158 ms                                                                    | 155 ms: 1.02x faster                                                        |
| sympy_str               | 333 ms                                                                    | 326 ms: 1.02x faster                                                        |
| comprehensions          | 24.7 us                                                                   | 24.2 us: 1.02x faster                                                       |
| crypto_pyaes            | 85.0 ms                                                                   | 83.2 ms: 1.02x faster                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 1.57 sec: 1.02x faster                                                      |
| dask                    | 418 ms                                                                    | 409 ms: 1.02x faster                                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.16 sec: 1.02x faster                                                      |
| pickle_pure_python      | 319 us                                                                    | 313 us: 1.02x faster                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 77.6 ms: 1.02x faster                                                       |
| unpack_sequence         | 45.9 ns                                                                   | 45.0 ns: 1.02x faster                                                       |
| deepcopy_memo           | 37.0 us                                                                   | 36.4 us: 1.02x faster                                                       |
| sqlglot_normalize       | 122 ms                                                                    | 120 ms: 1.02x faster                                                        |
| raytrace                | 303 ms                                                                    | 298 ms: 1.02x faster                                                        |
| pyflate                 | 438 ms                                                                    | 431 ms: 1.02x faster                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.62 ms: 1.01x faster                                                       |
| python_startup          | 10.7 ms                                                                   | 10.6 ms: 1.01x faster                                                       |
| deepcopy_reduce         | 3.39 us                                                                   | 3.35 us: 1.01x faster                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 1.51 ms: 1.01x faster                                                       |
| pathlib                 | 19.2 ms                                                                   | 19.0 ms: 1.01x faster                                                       |
| unpickle_list           | 4.52 us                                                                   | 4.47 us: 1.01x faster                                                       |
| logging_format          | 7.84 us                                                                   | 7.77 us: 1.01x faster                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 761 ms: 1.01x faster                                                        |
| telco                   | 6.70 ms                                                                   | 6.64 ms: 1.01x faster                                                       |
| scimark_sor             | 109 ms                                                                    | 108 ms: 1.01x faster                                                        |
| asyncio_tcp             | 752 ms                                                                    | 747 ms: 1.01x faster                                                        |
| mdp                     | 2.73 sec                                                                  | 2.71 sec: 1.01x faster                                                      |
| sqlglot_optimize        | 58.6 ms                                                                   | 58.2 ms: 1.01x faster                                                       |
| sympy_sum               | 182 ms                                                                    | 181 ms: 1.01x faster                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.4 ms: 1.00x slower                                                       |
| async_generators        | 318 ms                                                                    | 321 ms: 1.01x slower                                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.90 ms: 1.01x slower                                                       |
| regex_effbot            | 3.31 ms                                                                   | 3.34 ms: 1.01x slower                                                       |
| spectral_norm           | 95.1 ms                                                                   | 96.1 ms: 1.01x slower                                                       |
| thrift                  | 942 us                                                                    | 953 us: 1.01x slower                                                        |
| logging_simple          | 6.95 us                                                                   | 7.06 us: 1.02x slower                                                       |
| chameleon               | 7.50 ms                                                                   | 7.62 ms: 1.02x slower                                                       |
| pickle_list             | 3.78 us                                                                   | 3.84 us: 1.02x slower                                                       |
| unpickle                | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                       |
| pickle                  | 9.92 us                                                                   | 10.1 us: 1.02x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.54 us: 1.02x slower                                                       |
| django_template         | 39.6 ms                                                                   | 40.6 ms: 1.03x slower                                                       |
| pickle_dict             | 31.1 us                                                                   | 31.9 us: 1.03x slower                                                       |
| deepcopy                | 384 us                                                                    | 394 us: 1.03x slower                                                        |
| regex_dna               | 225 ms                                                                    | 232 ms: 1.03x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 288 ms: 1.04x slower                                                        |
| nbody                   | 92.1 ms                                                                   | 98.1 ms: 1.07x slower                                                       |
| Geometric mean          | (ref)                                                                     | 1.03x faster                                                                |

Benchmark hidden because not significant (4): scimark_monte_carlo, pidigits, async_tree_cpu_io_mixed, bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
