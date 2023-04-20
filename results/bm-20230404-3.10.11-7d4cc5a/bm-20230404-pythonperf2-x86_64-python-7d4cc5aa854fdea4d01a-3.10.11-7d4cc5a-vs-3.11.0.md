
# Results vs. 3.11.0

- fork: python
- ref: 7d4cc5aa854fdea4d01a
- machine: linux-x86_64
- commit hash: 7d4cc5a
- commit date: 2023-04-04
- overall geometric mean: 1.21x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf2-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 350 ms: 1.21x slower                                                       |
| chameleon      | 7.50 ms                                                                   | 9.41 ms: 1.25x slower                                                      |
| docutils       | 2.86 sec                                                                  | 3.42 sec: 1.20x slower                                                     |
| html5lib       | 70.2 ms                                                                   | 93.6 ms: 1.33x slower                                                      |
| tornado_http   | 125 ms                                                                    | 150 ms: 1.20x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.24x slower                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf2-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 252 ms                                                                    | 271 ms: 1.08x slower                                                       |
| float          | 75.7 ms                                                                   | 110 ms: 1.46x slower                                                       |
| nbody          | 92.1 ms                                                                   | 137 ms: 1.49x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.33x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf2-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.31 ms                                                                   | 3.25 ms: 1.02x faster                                                      |
| regex_v8       | 24.4 ms                                                                   | 27.1 ms: 1.11x slower                                                      |
| regex_dna      | 225 ms                                                                    | 259 ms: 1.15x slower                                                       |
| regex_compile  | 154 ms                                                                    | 191 ms: 1.24x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.12x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf2-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_list        | 4.52 us                                                                   | 4.61 us: 1.02x slower                                                      |
| pickle               | 9.92 us                                                                   | 10.1 us: 1.02x slower                                                      |
| xml_etree_iterparse  | 106 ms                                                                    | 109 ms: 1.03x slower                                                       |
| json_loads           | 28.4 us                                                                   | 30.2 us: 1.06x slower                                                      |
| pickle_list          | 3.78 us                                                                   | 4.04 us: 1.07x slower                                                      |
| unpickle             | 13.0 us                                                                   | 14.1 us: 1.08x slower                                                      |
| json_dumps           | 13.4 ms                                                                   | 14.4 ms: 1.08x slower                                                      |
| xml_etree_generate   | 79.1 ms                                                                   | 92.8 ms: 1.17x slower                                                      |
| unpickle_pure_python | 238 us                                                                    | 313 us: 1.32x slower                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 76.5 ms: 1.37x slower                                                      |
| pickle_pure_python   | 319 us                                                                    | 454 us: 1.42x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.12x slower                                                               |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf2-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|------------------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                                   | 7.35 ms: 1.05x faster                                                      |
| python_startup         | 10.7 ms                                                                   | 11.5 ms: 1.08x slower                                                      |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf2-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-----------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 63.7 ms: 1.10x slower                                                      |
| genshi_text     | 26.3 ms                                                                   | 31.7 ms: 1.21x slower                                                      |
| django_template | 39.6 ms                                                                   | 53.2 ms: 1.34x slower                                                      |
| mako            | 10.9 ms                                                                   | 14.9 ms: 1.37x slower                                                      |
| Geometric mean  | (ref)                                                                     | 1.25x slower                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf2-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-------------------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| coverage                | 86.0 ms                                                                   | 63.5 ms: 1.35x faster                                                      |
| gc_traversal            | 4.22 ms                                                                   | 3.68 ms: 1.15x faster                                                      |
| python_startup_no_site  | 7.73 ms                                                                   | 7.35 ms: 1.05x faster                                                      |
| regex_effbot            | 3.31 ms                                                                   | 3.25 ms: 1.02x faster                                                      |
| unpickle_list           | 4.52 us                                                                   | 4.61 us: 1.02x slower                                                      |
| pickle                  | 9.92 us                                                                   | 10.1 us: 1.02x slower                                                      |
| coroutines              | 29.5 ms                                                                   | 30.2 ms: 1.02x slower                                                      |
| generators              | 56.0 ms                                                                   | 57.8 ms: 1.03x slower                                                      |
| xml_etree_iterparse     | 106 ms                                                                    | 109 ms: 1.03x slower                                                       |
| asyncio_tcp             | 752 ms                                                                    | 781 ms: 1.04x slower                                                       |
| fannkuch                | 449 ms                                                                    | 477 ms: 1.06x slower                                                       |
| json_loads              | 28.4 us                                                                   | 30.2 us: 1.06x slower                                                      |
| pickle_list             | 3.78 us                                                                   | 4.04 us: 1.07x slower                                                      |
| json                    | 5.59 ms                                                                   | 5.97 ms: 1.07x slower                                                      |
| telco                   | 6.70 ms                                                                   | 7.16 ms: 1.07x slower                                                      |
| meteor_contest          | 129 ms                                                                    | 139 ms: 1.07x slower                                                       |
| python_startup          | 10.7 ms                                                                   | 11.5 ms: 1.08x slower                                                      |
| unpickle                | 13.0 us                                                                   | 14.1 us: 1.08x slower                                                      |
| pidigits                | 252 ms                                                                    | 271 ms: 1.08x slower                                                       |
| json_dumps              | 13.4 ms                                                                   | 14.4 ms: 1.08x slower                                                      |
| sympy_sum               | 182 ms                                                                    | 199 ms: 1.09x slower                                                       |
| comprehensions          | 24.7 us                                                                   | 27.1 us: 1.09x slower                                                      |
| pathlib                 | 19.2 ms                                                                   | 21.0 ms: 1.10x slower                                                      |
| dask                    | 418 ms                                                                    | 459 ms: 1.10x slower                                                       |
| sympy_str               | 333 ms                                                                    | 366 ms: 1.10x slower                                                       |
| genshi_xml              | 57.8 ms                                                                   | 63.7 ms: 1.10x slower                                                      |
| create_gc_cycles        | 1.65 ms                                                                   | 1.82 ms: 1.11x slower                                                      |
| pylint                  | 517 ms                                                                    | 572 ms: 1.11x slower                                                       |
| regex_v8                | 24.4 ms                                                                   | 27.1 ms: 1.11x slower                                                      |
| nqueens                 | 101 ms                                                                    | 112 ms: 1.11x slower                                                       |
| bench_thread_pool       | 990 us                                                                    | 1.10 ms: 1.12x slower                                                      |
| sympy_integrate         | 25.3 ms                                                                   | 28.4 ms: 1.12x slower                                                      |
| sympy_expand            | 547 ms                                                                    | 615 ms: 1.13x slower                                                       |
| flaskblogging           | 3.81 ms                                                                   | 4.33 ms: 1.14x slower                                                      |
| mdp                     | 2.73 sec                                                                  | 3.12 sec: 1.14x slower                                                     |
| regex_dna               | 225 ms                                                                    | 259 ms: 1.15x slower                                                       |
| sqlalchemy_imperative   | 19.8 ms                                                                   | 23.0 ms: 1.16x slower                                                      |
| dulwich_log             | 69.1 ms                                                                   | 80.1 ms: 1.16x slower                                                      |
| xml_etree_generate      | 79.1 ms                                                                   | 92.8 ms: 1.17x slower                                                      |
| deepcopy_reduce         | 3.39 us                                                                   | 3.99 us: 1.18x slower                                                      |
| sqlglot_optimize        | 58.6 ms                                                                   | 69.1 ms: 1.18x slower                                                      |
| sqlglot_normalize       | 122 ms                                                                    | 144 ms: 1.18x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.97 us: 1.19x slower                                                      |
| docutils                | 2.86 sec                                                                  | 3.42 sec: 1.20x slower                                                     |
| aiohttp                 | 959 us                                                                    | 1.15 ms: 1.20x slower                                                      |
| tornado_http            | 125 ms                                                                    | 150 ms: 1.20x slower                                                       |
| gunicorn                | 936 us                                                                    | 1.13 ms: 1.20x slower                                                      |
| genshi_text             | 26.3 ms                                                                   | 31.7 ms: 1.21x slower                                                      |
| 2to3                    | 289 ms                                                                    | 350 ms: 1.21x slower                                                       |
| sqlalchemy_declarative  | 156 ms                                                                    | 188 ms: 1.21x slower                                                       |
| deepcopy                | 384 us                                                                    | 465 us: 1.21x slower                                                       |
| logging_format          | 7.84 us                                                                   | 9.57 us: 1.22x slower                                                      |
| pycparser               | 1.30 sec                                                                  | 1.61 sec: 1.24x slower                                                     |
| thrift                  | 942 us                                                                    | 1.17 ms: 1.24x slower                                                      |
| regex_compile           | 154 ms                                                                    | 191 ms: 1.24x slower                                                       |
| chameleon               | 7.50 ms                                                                   | 9.41 ms: 1.25x slower                                                      |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 952 ms: 1.26x slower                                                       |
| logging_simple          | 6.95 us                                                                   | 8.94 us: 1.29x slower                                                      |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 5.22 ms: 1.29x slower                                                      |
| async_tree_memoization  | 639 ms                                                                    | 827 ms: 1.29x slower                                                       |
| unpack_sequence         | 45.9 ns                                                                   | 59.4 ns: 1.30x slower                                                      |
| scimark_fft             | 276 ms                                                                    | 360 ms: 1.30x slower                                                       |
| async_generators        | 318 ms                                                                    | 418 ms: 1.31x slower                                                       |
| async_tree_none         | 529 ms                                                                    | 695 ms: 1.31x slower                                                       |
| unpickle_pure_python    | 238 us                                                                    | 313 us: 1.32x slower                                                       |
| html5lib                | 70.2 ms                                                                   | 93.6 ms: 1.33x slower                                                      |
| pprint_pformat          | 1.60 sec                                                                  | 2.14 sec: 1.34x slower                                                     |
| django_template         | 39.6 ms                                                                   | 53.2 ms: 1.34x slower                                                      |
| hexiom                  | 7.00 ms                                                                   | 9.43 ms: 1.35x slower                                                      |
| pprint_safe_repr        | 768 ms                                                                    | 1.03 sec: 1.35x slower                                                     |
| crypto_pyaes            | 85.0 ms                                                                   | 115 ms: 1.35x slower                                                       |
| async_tree_io           | 1.18 sec                                                                  | 1.61 sec: 1.36x slower                                                     |
| mako                    | 10.9 ms                                                                   | 14.9 ms: 1.37x slower                                                      |
| xml_etree_process       | 55.8 ms                                                                   | 76.5 ms: 1.37x slower                                                      |
| chaos                   | 76.2 ms                                                                   | 105 ms: 1.38x slower                                                       |
| deepcopy_memo           | 37.0 us                                                                   | 51.1 us: 1.38x slower                                                      |
| scimark_lu              | 114 ms                                                                    | 161 ms: 1.41x slower                                                       |
| pickle_pure_python      | 319 us                                                                    | 454 us: 1.42x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.69 ms: 1.43x slower                                                      |
| spectral_norm           | 95.1 ms                                                                   | 137 ms: 1.44x slower                                                       |
| float                   | 75.7 ms                                                                   | 110 ms: 1.46x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 2.26 ms: 1.47x slower                                                      |
| nbody                   | 92.1 ms                                                                   | 137 ms: 1.49x slower                                                       |
| bench_mp_pool           | 4.54 ms                                                                   | 6.82 ms: 1.50x slower                                                      |
| richards                | 49.1 ms                                                                   | 74.5 ms: 1.52x slower                                                      |
| pyflate                 | 438 ms                                                                    | 693 ms: 1.58x slower                                                       |
| logging_silent          | 103 ns                                                                    | 166 ns: 1.61x slower                                                       |
| scimark_sor             | 109 ms                                                                    | 176 ms: 1.62x slower                                                       |
| raytrace                | 303 ms                                                                    | 491 ms: 1.62x slower                                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 110 ms: 1.63x slower                                                       |
| go                      | 158 ms                                                                    | 264 ms: 1.67x slower                                                       |
| deltablue               | 3.99 ms                                                                   | 7.44 ms: 1.86x slower                                                      |
| Geometric mean          | (ref)                                                                     | 1.21x slower                                                               |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_dict, mypy2
