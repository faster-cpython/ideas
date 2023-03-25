
# Results vs. 3.11.0

- fork: python
- ref: cdde29dde90947df9bac
- machine: linux-x86_64
- commit hash: cdde29d
- commit date: 2022-11-21
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 280 ms: 1.04x faster                                                         |
| chameleon      | 7.50 ms                                                                   | 7.42 ms: 1.01x faster                                                        |
| docutils       | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 67.3 ms: 1.04x faster                                                        |
| tornado_http   | 125 ms                                                                    | 121 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 73.6 ms: 1.03x faster                                                        |
| nbody          | 92.1 ms                                                                   | 93.5 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 23.7 ms: 1.03x faster                                                        |
| regex_compile  | 154 ms                                                                    | 150 ms: 1.03x faster                                                         |
| regex_dna      | 225 ms                                                                    | 227 ms: 1.01x slower                                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.46 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.00x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.4 ms: 1.29x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.3 us: 1.17x faster                                                        |
| xml_etree_parse      | 161 ms                                                                    | 138 ms: 1.16x faster                                                         |
| unpickle_pure_python | 238 us                                                                    | 208 us: 1.14x faster                                                         |
| xml_etree_iterparse  | 106 ms                                                                    | 102 ms: 1.04x faster                                                         |
| pickle_pure_python   | 319 us                                                                    | 315 us: 1.02x faster                                                         |
| xml_etree_process    | 55.8 ms                                                                   | 55.2 ms: 1.01x faster                                                        |
| pickle               | 9.92 us                                                                   | 9.96 us: 1.00x slower                                                        |
| xml_etree_generate   | 79.1 ms                                                                   | 79.5 ms: 1.01x slower                                                        |
| unpickle             | 13.0 us                                                                   | 13.4 us: 1.03x slower                                                        |
| pickle_list          | 3.78 us                                                                   | 3.88 us: 1.03x slower                                                        |
| pickle_dict          | 31.1 us                                                                   | 32.3 us: 1.04x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.05x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.8 ms: 1.01x slower                                                        |
| python_startup_no_site | 7.73 ms                                                                   | 7.85 ms: 1.02x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.9 ms                                                                   | 10.2 ms: 1.06x faster                                                        |
| genshi_xml      | 57.8 ms                                                                   | 55.4 ms: 1.04x faster                                                        |
| django_template | 39.6 ms                                                                   | 41.0 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                                     | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps              | 13.4 ms                                                                   | 10.4 ms: 1.29x faster                                                        |
| mypy2                   | 446 ms                                                                    | 374 ms: 1.19x faster                                                         |
| gc_traversal            | 4.22 ms                                                                   | 3.61 ms: 1.17x faster                                                        |
| json_loads              | 28.4 us                                                                   | 24.3 us: 1.17x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 138 ms: 1.16x faster                                                         |
| unpickle_pure_python    | 238 us                                                                    | 208 us: 1.14x faster                                                         |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.65 ms: 1.11x faster                                                        |
| json                    | 5.59 ms                                                                   | 5.07 ms: 1.10x faster                                                        |
| deltablue               | 3.99 ms                                                                   | 3.67 ms: 1.09x faster                                                        |
| fannkuch                | 449 ms                                                                    | 416 ms: 1.08x faster                                                         |
| thrift                  | 942 us                                                                    | 880 us: 1.07x faster                                                         |
| coroutines              | 29.5 ms                                                                   | 27.6 ms: 1.07x faster                                                        |
| aiohttp                 | 959 us                                                                    | 898 us: 1.07x faster                                                         |
| mako                    | 10.9 ms                                                                   | 10.2 ms: 1.06x faster                                                        |
| gunicorn                | 936 us                                                                    | 889 us: 1.05x faster                                                         |
| genshi_xml              | 57.8 ms                                                                   | 55.4 ms: 1.04x faster                                                        |
| html5lib                | 70.2 ms                                                                   | 67.3 ms: 1.04x faster                                                        |
| async_tree_memoization  | 639 ms                                                                    | 614 ms: 1.04x faster                                                         |
| 2to3                    | 289 ms                                                                    | 280 ms: 1.04x faster                                                         |
| xml_etree_iterparse     | 106 ms                                                                    | 102 ms: 1.04x faster                                                         |
| tornado_http            | 125 ms                                                                    | 121 ms: 1.03x faster                                                         |
| bench_thread_pool       | 990 us                                                                    | 957 us: 1.03x faster                                                         |
| regex_v8                | 24.4 ms                                                                   | 23.7 ms: 1.03x faster                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.59 ms: 1.03x faster                                                        |
| richards                | 49.1 ms                                                                   | 47.6 ms: 1.03x faster                                                        |
| logging_silent          | 103 ns                                                                    | 99.6 ns: 1.03x faster                                                        |
| float                   | 75.7 ms                                                                   | 73.6 ms: 1.03x faster                                                        |
| docutils                | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                       |
| regex_compile           | 154 ms                                                                    | 150 ms: 1.03x faster                                                         |
| bench_mp_pool           | 4.54 ms                                                                   | 4.42 ms: 1.03x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 515 ms: 1.03x faster                                                         |
| dulwich_log             | 69.1 ms                                                                   | 67.4 ms: 1.03x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.65 us: 1.02x faster                                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.16 sec: 1.02x faster                                                       |
| meteor_contest          | 129 ms                                                                    | 127 ms: 1.02x faster                                                         |
| crypto_pyaes            | 85.0 ms                                                                   | 83.6 ms: 1.02x faster                                                        |
| pickle_pure_python      | 319 us                                                                    | 315 us: 1.02x faster                                                         |
| deepcopy_reduce         | 3.39 us                                                                   | 3.35 us: 1.01x faster                                                        |
| raytrace                | 303 ms                                                                    | 299 ms: 1.01x faster                                                         |
| chaos                   | 76.2 ms                                                                   | 75.3 ms: 1.01x faster                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 55.2 ms: 1.01x faster                                                        |
| chameleon               | 7.50 ms                                                                   | 7.42 ms: 1.01x faster                                                        |
| asyncio_tcp             | 752 ms                                                                    | 744 ms: 1.01x faster                                                         |
| deepcopy_memo           | 37.0 us                                                                   | 36.6 us: 1.01x faster                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 748 ms: 1.01x faster                                                         |
| spectral_norm           | 95.1 ms                                                                   | 94.6 ms: 1.01x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 114 ms: 1.01x faster                                                         |
| scimark_sor             | 109 ms                                                                    | 109 ms: 1.00x faster                                                         |
| pathlib                 | 19.2 ms                                                                   | 19.3 ms: 1.00x slower                                                        |
| pickle                  | 9.92 us                                                                   | 9.96 us: 1.00x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 79.5 ms: 1.01x slower                                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.89 ms: 1.01x slower                                                        |
| python_startup          | 10.7 ms                                                                   | 10.8 ms: 1.01x slower                                                        |
| telco                   | 6.70 ms                                                                   | 6.74 ms: 1.01x slower                                                        |
| sympy_str               | 333 ms                                                                    | 335 ms: 1.01x slower                                                         |
| go                      | 158 ms                                                                    | 159 ms: 1.01x slower                                                         |
| scimark_monte_carlo     | 67.8 ms                                                                   | 68.5 ms: 1.01x slower                                                        |
| pycparser               | 1.30 sec                                                                  | 1.32 sec: 1.01x slower                                                       |
| regex_dna               | 225 ms                                                                    | 227 ms: 1.01x slower                                                         |
| coverage                | 86.0 ms                                                                   | 86.9 ms: 1.01x slower                                                        |
| hexiom                  | 7.00 ms                                                                   | 7.08 ms: 1.01x slower                                                        |
| deepcopy                | 384 us                                                                    | 388 us: 1.01x slower                                                         |
| sympy_integrate         | 25.3 ms                                                                   | 25.6 ms: 1.01x slower                                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.62 sec: 1.01x slower                                                       |
| nbody                   | 92.1 ms                                                                   | 93.5 ms: 1.02x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.85 ms: 1.02x slower                                                        |
| sympy_sum               | 182 ms                                                                    | 185 ms: 1.02x slower                                                         |
| logging_simple          | 6.95 us                                                                   | 7.08 us: 1.02x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 282 ms: 1.02x slower                                                         |
| mdp                     | 2.73 sec                                                                  | 2.78 sec: 1.02x slower                                                       |
| pprint_safe_repr        | 768 ms                                                                    | 788 ms: 1.03x slower                                                         |
| unpickle                | 13.0 us                                                                   | 13.4 us: 1.03x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 3.88 us: 1.03x slower                                                        |
| pyflate                 | 438 ms                                                                    | 450 ms: 1.03x slower                                                         |
| sqlite_synth            | 2.49 us                                                                   | 2.56 us: 1.03x slower                                                        |
| django_template         | 39.6 ms                                                                   | 41.0 ms: 1.03x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 32.3 us: 1.04x slower                                                        |
| async_generators        | 318 ms                                                                    | 333 ms: 1.05x slower                                                         |
| regex_effbot            | 3.31 ms                                                                   | 3.46 ms: 1.05x slower                                                        |
| generators              | 56.0 ms                                                                   | 60.8 ms: 1.09x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 27.5 us: 1.11x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.02x faster                                                                 |

Benchmark hidden because not significant (10): nqueens, unpack_sequence, dask, sqlglot_parse, sqlglot_normalize, pidigits, sqlglot_optimize, sympy_expand, genshi_text, unpickle_list
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
