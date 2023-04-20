
# Results vs. 3.11.0

- fork: python
- ref: 7d4cc5aa854fdea4d01a
- machine: linux-x86_64
- commit hash: 7d4cc5a
- commit date: 2023-04-04
- overall geometric mean: 1.25x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 335 ms: 1.30x slower                                                 |
| chameleon      | 6.52 ms                                                             | 8.93 ms: 1.37x slower                                                |
| docutils       | 2.59 sec                                                            | 3.21 sec: 1.24x slower                                               |
| html5lib       | 64.0 ms                                                             | 85.4 ms: 1.33x slower                                                |
| tornado_http   | 96.7 ms                                                             | 131 ms: 1.35x slower                                                 |
| Geometric mean | (ref)                                                               | 1.32x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 197 ms                                                              | 188 ms: 1.05x faster                                                 |
| float          | 76.0 ms                                                             | 108 ms: 1.42x slower                                                 |
| nbody          | 96.7 ms                                                             | 137 ms: 1.42x slower                                                 |
| Geometric mean | (ref)                                                               | 1.25x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 196 ms                                                              | 213 ms: 1.09x slower                                                 |
| regex_effbot   | 3.32 ms                                                             | 3.63 ms: 1.09x slower                                                |
| regex_v8       | 22.0 ms                                                             | 25.5 ms: 1.16x slower                                                |
| regex_compile  | 137 ms                                                              | 176 ms: 1.29x slower                                                 |
| Geometric mean | (ref)                                                               | 1.15x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_list        | 4.96 us                                                             | 4.80 us: 1.03x faster                                                |
| xml_etree_iterparse  | 108 ms                                                              | 110 ms: 1.02x slower                                                 |
| pickle               | 9.79 us                                                             | 10.4 us: 1.06x slower                                                |
| unpickle             | 13.2 us                                                             | 14.3 us: 1.08x slower                                                |
| pickle_list          | 4.03 us                                                             | 4.38 us: 1.09x slower                                                |
| json_dumps           | 12.5 ms                                                             | 13.6 ms: 1.09x slower                                                |
| pickle_dict          | 30.9 us                                                             | 33.7 us: 1.09x slower                                                |
| json_loads           | 26.2 us                                                             | 29.0 us: 1.11x slower                                                |
| xml_etree_generate   | 76.5 ms                                                             | 93.1 ms: 1.22x slower                                                |
| unpickle_pure_python | 228 us                                                              | 298 us: 1.31x slower                                                 |
| xml_etree_process    | 54.1 ms                                                             | 74.1 ms: 1.37x slower                                                |
| pickle_pure_python   | 307 us                                                              | 452 us: 1.47x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.14x slower                                                         |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|------------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 5.98 ms                                                             | 5.83 ms: 1.02x faster                                                |
| python_startup         | 8.49 ms                                                             | 14.2 ms: 1.67x slower                                                |
| Geometric mean         | (ref)                                                               | 1.28x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 62.6 ms: 1.21x slower                                                |
| genshi_text     | 21.8 ms                                                             | 30.1 ms: 1.38x slower                                                |
| django_template | 32.9 ms                                                             | 45.8 ms: 1.39x slower                                                |
| mako            | 9.82 ms                                                             | 14.7 ms: 1.50x slower                                                |
| Geometric mean  | (ref)                                                               | 1.37x slower                                                         |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-------------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coverage                | 101 ms                                                              | 72.1 ms: 1.40x faster                                                |
| pidigits                | 197 ms                                                              | 188 ms: 1.05x faster                                                 |
| unpickle_list           | 4.96 us                                                             | 4.80 us: 1.03x faster                                                |
| python_startup_no_site  | 5.98 ms                                                             | 5.83 ms: 1.02x faster                                                |
| asyncio_tcp             | 888 ms                                                              | 894 ms: 1.01x slower                                                 |
| gc_traversal            | 3.63 ms                                                             | 3.71 ms: 1.02x slower                                                |
| xml_etree_iterparse     | 108 ms                                                              | 110 ms: 1.02x slower                                                 |
| generators              | 73.4 ms                                                             | 75.5 ms: 1.03x slower                                                |
| telco                   | 6.59 ms                                                             | 6.78 ms: 1.03x slower                                                |
| pickle                  | 9.79 us                                                             | 10.4 us: 1.06x slower                                                |
| meteor_contest          | 106 ms                                                              | 113 ms: 1.06x slower                                                 |
| mdp                     | 2.64 sec                                                            | 2.85 sec: 1.08x slower                                               |
| unpickle                | 13.2 us                                                             | 14.3 us: 1.08x slower                                                |
| regex_dna               | 196 ms                                                              | 213 ms: 1.09x slower                                                 |
| pickle_list             | 4.03 us                                                             | 4.38 us: 1.09x slower                                                |
| json_dumps              | 12.5 ms                                                             | 13.6 ms: 1.09x slower                                                |
| pathlib                 | 18.2 ms                                                             | 19.9 ms: 1.09x slower                                                |
| pickle_dict             | 30.9 us                                                             | 33.7 us: 1.09x slower                                                |
| regex_effbot            | 3.32 ms                                                             | 3.63 ms: 1.09x slower                                                |
| json                    | 4.86 ms                                                             | 5.32 ms: 1.09x slower                                                |
| pylint                  | 476 ms                                                              | 526 ms: 1.11x slower                                                 |
| json_loads              | 26.2 us                                                             | 29.0 us: 1.11x slower                                                |
| create_gc_cycles        | 1.48 ms                                                             | 1.66 ms: 1.12x slower                                                |
| sympy_sum               | 167 ms                                                              | 188 ms: 1.13x slower                                                 |
| bench_thread_pool       | 820 us                                                              | 925 us: 1.13x slower                                                 |
| sympy_str               | 291 ms                                                              | 330 ms: 1.13x slower                                                 |
| dask                    | 368 ms                                                              | 421 ms: 1.14x slower                                                 |
| sympy_expand            | 477 ms                                                              | 545 ms: 1.14x slower                                                 |
| djangocms               | 32.3 us                                                             | 37.3 us: 1.15x slower                                                |
| sympy_integrate         | 21.0 ms                                                             | 24.3 ms: 1.15x slower                                                |
| regex_v8                | 22.0 ms                                                             | 25.5 ms: 1.16x slower                                                |
| sqlalchemy_imperative   | 18.0 ms                                                             | 21.0 ms: 1.16x slower                                                |
| async_generators        | 361 ms                                                              | 421 ms: 1.16x slower                                                 |
| nqueens                 | 84.0 ms                                                             | 97.9 ms: 1.17x slower                                                |
| coroutines              | 26.3 ms                                                             | 31.0 ms: 1.18x slower                                                |
| dulwich_log             | 63.6 ms                                                             | 75.5 ms: 1.19x slower                                                |
| sqlite_synth            | 2.51 us                                                             | 3.02 us: 1.20x slower                                                |
| flaskblogging           | 7.09 ms                                                             | 8.53 ms: 1.20x slower                                                |
| genshi_xml              | 51.8 ms                                                             | 62.6 ms: 1.21x slower                                                |
| sqlalchemy_declarative  | 138 ms                                                              | 168 ms: 1.21x slower                                                 |
| comprehensions          | 22.2 us                                                             | 27.0 us: 1.21x slower                                                |
| xml_etree_generate      | 76.5 ms                                                             | 93.1 ms: 1.22x slower                                                |
| aiohttp                 | 1.05 ms                                                             | 1.29 ms: 1.22x slower                                                |
| fannkuch                | 384 ms                                                              | 471 ms: 1.23x slower                                                 |
| sqlglot_optimize        | 53.4 ms                                                             | 65.5 ms: 1.23x slower                                                |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 5.50 ms: 1.23x slower                                                |
| gunicorn                | 1.13 ms                                                             | 1.39 ms: 1.23x slower                                                |
| docutils                | 2.59 sec                                                            | 3.21 sec: 1.24x slower                                               |
| sqlglot_normalize       | 108 ms                                                              | 136 ms: 1.25x slower                                                 |
| deepcopy                | 339 us                                                              | 429 us: 1.27x slower                                                 |
| scimark_fft             | 328 ms                                                              | 416 ms: 1.27x slower                                                 |
| deepcopy_reduce         | 2.96 us                                                             | 3.77 us: 1.27x slower                                                |
| regex_compile           | 137 ms                                                              | 176 ms: 1.29x slower                                                 |
| 2to3                    | 257 ms                                                              | 335 ms: 1.30x slower                                                 |
| unpickle_pure_python    | 228 us                                                              | 298 us: 1.31x slower                                                 |
| async_tree_cpu_io_mixed | 736 ms                                                              | 975 ms: 1.33x slower                                                 |
| pycparser               | 1.14 sec                                                            | 1.52 sec: 1.33x slower                                               |
| html5lib                | 64.0 ms                                                             | 85.4 ms: 1.33x slower                                                |
| tornado_http            | 96.7 ms                                                             | 131 ms: 1.35x slower                                                 |
| pprint_pformat          | 1.45 sec                                                            | 1.97 sec: 1.36x slower                                               |
| pprint_safe_repr        | 701 ms                                                              | 953 ms: 1.36x slower                                                 |
| thrift                  | 766 us                                                              | 1.04 ms: 1.36x slower                                                |
| unpack_sequence         | 49.5 ns                                                             | 67.6 ns: 1.37x slower                                                |
| deepcopy_memo           | 36.4 us                                                             | 49.8 us: 1.37x slower                                                |
| xml_etree_process       | 54.1 ms                                                             | 74.1 ms: 1.37x slower                                                |
| chameleon               | 6.52 ms                                                             | 8.93 ms: 1.37x slower                                                |
| genshi_text             | 21.8 ms                                                             | 30.1 ms: 1.38x slower                                                |
| logging_simple          | 6.09 us                                                             | 8.40 us: 1.38x slower                                                |
| logging_format          | 6.64 us                                                             | 9.16 us: 1.38x slower                                                |
| django_template         | 32.9 ms                                                             | 45.8 ms: 1.39x slower                                                |
| async_tree_none         | 525 ms                                                              | 732 ms: 1.39x slower                                                 |
| async_tree_memoization  | 621 ms                                                              | 873 ms: 1.41x slower                                                 |
| async_tree_io           | 1.28 sec                                                            | 1.82 sec: 1.42x slower                                               |
| float                   | 76.0 ms                                                             | 108 ms: 1.42x slower                                                 |
| nbody                   | 96.7 ms                                                             | 137 ms: 1.42x slower                                                 |
| spectral_norm           | 99.5 ms                                                             | 142 ms: 1.43x slower                                                 |
| hexiom                  | 6.48 ms                                                             | 9.41 ms: 1.45x slower                                                |
| scimark_lu              | 108 ms                                                              | 159 ms: 1.46x slower                                                 |
| pickle_pure_python      | 307 us                                                              | 452 us: 1.47x slower                                                 |
| sqlglot_transpile       | 1.65 ms                                                             | 2.44 ms: 1.47x slower                                                |
| mako                    | 9.82 ms                                                             | 14.7 ms: 1.50x slower                                                |
| sqlglot_parse           | 1.36 ms                                                             | 2.04 ms: 1.50x slower                                                |
| chaos                   | 68.0 ms                                                             | 105 ms: 1.54x slower                                                 |
| crypto_pyaes            | 73.8 ms                                                             | 114 ms: 1.55x slower                                                 |
| raytrace                | 292 ms                                                              | 462 ms: 1.58x slower                                                 |
| pyflate                 | 414 ms                                                              | 660 ms: 1.60x slower                                                 |
| richards                | 45.7 ms                                                             | 73.1 ms: 1.60x slower                                                |
| scimark_monte_carlo     | 67.8 ms                                                             | 109 ms: 1.61x slower                                                 |
| go                      | 138 ms                                                              | 227 ms: 1.64x slower                                                 |
| python_startup          | 8.49 ms                                                             | 14.2 ms: 1.67x slower                                                |
| scimark_sor             | 115 ms                                                              | 194 ms: 1.69x slower                                                 |
| logging_silent          | 98.7 ns                                                             | 175 ns: 1.77x slower                                                 |
| deltablue               | 3.66 ms                                                             | 7.35 ms: 2.01x slower                                                |
| Geometric mean          | (ref)                                                               | 1.25x slower                                                         |

Benchmark hidden because not significant (3): bench_mp_pool, xml_etree_parse, mypy2
