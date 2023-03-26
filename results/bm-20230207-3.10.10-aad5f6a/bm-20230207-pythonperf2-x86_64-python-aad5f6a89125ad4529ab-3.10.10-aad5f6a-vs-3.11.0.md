
# Results vs. 3.11.0

- fork: python
- ref: aad5f6a89125ad4529ab
- machine: linux-x86_64
- commit hash: aad5f6a
- commit date: 2023-02-07
- overall geometric mean: 1.22x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 351 ms: 1.21x slower                                                       |
| chameleon      | 7.50 ms                                                                   | 9.41 ms: 1.25x slower                                                      |
| docutils       | 2.86 sec                                                                  | 3.45 sec: 1.21x slower                                                     |
| html5lib       | 70.2 ms                                                                   | 94.4 ms: 1.34x slower                                                      |
| tornado_http   | 125 ms                                                                    | 159 ms: 1.27x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.26x slower                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 252 ms                                                                    | 271 ms: 1.08x slower                                                       |
| float          | 75.7 ms                                                                   | 111 ms: 1.46x slower                                                       |
| nbody          | 92.1 ms                                                                   | 138 ms: 1.49x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.33x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.31 ms                                                                   | 3.49 ms: 1.06x slower                                                      |
| regex_v8       | 24.4 ms                                                                   | 27.2 ms: 1.11x slower                                                      |
| regex_dna      | 225 ms                                                                    | 260 ms: 1.15x slower                                                       |
| regex_compile  | 154 ms                                                                    | 192 ms: 1.25x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.14x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_parse      | 161 ms                                                                    | 164 ms: 1.02x slower                                                       |
| pickle               | 9.92 us                                                                   | 10.1 us: 1.02x slower                                                      |
| pickle_dict          | 31.1 us                                                                   | 32.1 us: 1.03x slower                                                      |
| unpickle_list        | 4.52 us                                                                   | 4.71 us: 1.04x slower                                                      |
| unpickle             | 13.0 us                                                                   | 13.7 us: 1.05x slower                                                      |
| json_loads           | 28.4 us                                                                   | 30.0 us: 1.05x slower                                                      |
| xml_etree_iterparse  | 106 ms                                                                    | 113 ms: 1.07x slower                                                       |
| json_dumps           | 13.4 ms                                                                   | 14.4 ms: 1.08x slower                                                      |
| pickle_list          | 3.78 us                                                                   | 4.17 us: 1.10x slower                                                      |
| xml_etree_generate   | 79.1 ms                                                                   | 94.0 ms: 1.19x slower                                                      |
| unpickle_pure_python | 238 us                                                                    | 320 us: 1.34x slower                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 77.5 ms: 1.39x slower                                                      |
| pickle_pure_python   | 319 us                                                                    | 461 us: 1.44x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.13x slower                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|------------------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                                   | 7.34 ms: 1.05x faster                                                      |
| python_startup         | 10.7 ms                                                                   | 11.5 ms: 1.07x slower                                                      |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|-----------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 62.5 ms: 1.08x slower                                                      |
| genshi_text     | 26.3 ms                                                                   | 32.0 ms: 1.22x slower                                                      |
| mako            | 10.9 ms                                                                   | 14.7 ms: 1.35x slower                                                      |
| django_template | 39.6 ms                                                                   | 53.6 ms: 1.35x slower                                                      |
| Geometric mean  | (ref)                                                                     | 1.24x slower                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|-------------------------|:-------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| coverage                | 86.0 ms                                                                   | 63.3 ms: 1.36x faster                                                      |
| python_startup_no_site  | 7.73 ms                                                                   | 7.34 ms: 1.05x faster                                                      |
| gc_traversal            | 4.22 ms                                                                   | 4.12 ms: 1.02x faster                                                      |
| coroutines              | 29.5 ms                                                                   | 29.9 ms: 1.01x slower                                                      |
| generators              | 56.0 ms                                                                   | 57.0 ms: 1.02x slower                                                      |
| xml_etree_parse         | 161 ms                                                                    | 164 ms: 1.02x slower                                                       |
| pickle                  | 9.92 us                                                                   | 10.1 us: 1.02x slower                                                      |
| pickle_dict             | 31.1 us                                                                   | 32.1 us: 1.03x slower                                                      |
| asyncio_tcp             | 752 ms                                                                    | 779 ms: 1.04x slower                                                       |
| unpickle_list           | 4.52 us                                                                   | 4.71 us: 1.04x slower                                                      |
| fannkuch                | 449 ms                                                                    | 470 ms: 1.05x slower                                                       |
| unpickle                | 13.0 us                                                                   | 13.7 us: 1.05x slower                                                      |
| json_loads              | 28.4 us                                                                   | 30.0 us: 1.05x slower                                                      |
| regex_effbot            | 3.31 ms                                                                   | 3.49 ms: 1.06x slower                                                      |
| json                    | 5.59 ms                                                                   | 5.91 ms: 1.06x slower                                                      |
| xml_etree_iterparse     | 106 ms                                                                    | 113 ms: 1.07x slower                                                       |
| meteor_contest          | 129 ms                                                                    | 139 ms: 1.07x slower                                                       |
| python_startup          | 10.7 ms                                                                   | 11.5 ms: 1.07x slower                                                      |
| pidigits                | 252 ms                                                                    | 271 ms: 1.08x slower                                                       |
| genshi_xml              | 57.8 ms                                                                   | 62.5 ms: 1.08x slower                                                      |
| json_dumps              | 13.4 ms                                                                   | 14.4 ms: 1.08x slower                                                      |
| telco                   | 6.70 ms                                                                   | 7.25 ms: 1.08x slower                                                      |
| sympy_sum               | 182 ms                                                                    | 199 ms: 1.09x slower                                                       |
| comprehensions          | 24.7 us                                                                   | 27.0 us: 1.09x slower                                                      |
| sympy_str               | 333 ms                                                                    | 364 ms: 1.09x slower                                                       |
| create_gc_cycles        | 1.65 ms                                                                   | 1.81 ms: 1.10x slower                                                      |
| pickle_list             | 3.78 us                                                                   | 4.17 us: 1.10x slower                                                      |
| pylint                  | 517 ms                                                                    | 572 ms: 1.11x slower                                                       |
| pathlib                 | 19.2 ms                                                                   | 21.3 ms: 1.11x slower                                                      |
| sympy_expand            | 547 ms                                                                    | 608 ms: 1.11x slower                                                       |
| regex_v8                | 24.4 ms                                                                   | 27.2 ms: 1.11x slower                                                      |
| bench_thread_pool       | 990 us                                                                    | 1.11 ms: 1.12x slower                                                      |
| nqueens                 | 101 ms                                                                    | 113 ms: 1.12x slower                                                       |
| mdp                     | 2.73 sec                                                                  | 3.05 sec: 1.12x slower                                                     |
| sympy_integrate         | 25.3 ms                                                                   | 28.5 ms: 1.13x slower                                                      |
| flaskblogging           | 3.81 ms                                                                   | 4.40 ms: 1.15x slower                                                      |
| regex_dna               | 225 ms                                                                    | 260 ms: 1.15x slower                                                       |
| sqlalchemy_imperative   | 19.8 ms                                                                   | 22.9 ms: 1.16x slower                                                      |
| dask                    | 418 ms                                                                    | 484 ms: 1.16x slower                                                       |
| dulwich_log             | 69.1 ms                                                                   | 81.1 ms: 1.17x slower                                                      |
| xml_etree_generate      | 79.1 ms                                                                   | 94.0 ms: 1.19x slower                                                      |
| sqlglot_optimize        | 58.6 ms                                                                   | 69.6 ms: 1.19x slower                                                      |
| sqlglot_normalize       | 122 ms                                                                    | 146 ms: 1.19x slower                                                       |
| deepcopy_reduce         | 3.39 us                                                                   | 4.05 us: 1.19x slower                                                      |
| aiohttp                 | 959 us                                                                    | 1.15 ms: 1.20x slower                                                      |
| sqlite_synth            | 2.49 us                                                                   | 2.98 us: 1.20x slower                                                      |
| gunicorn                | 936 us                                                                    | 1.13 ms: 1.20x slower                                                      |
| sqlalchemy_declarative  | 156 ms                                                                    | 187 ms: 1.20x slower                                                       |
| docutils                | 2.86 sec                                                                  | 3.45 sec: 1.21x slower                                                     |
| 2to3                    | 289 ms                                                                    | 351 ms: 1.21x slower                                                       |
| deepcopy                | 384 us                                                                    | 466 us: 1.22x slower                                                       |
| genshi_text             | 26.3 ms                                                                   | 32.0 ms: 1.22x slower                                                      |
| logging_format          | 7.84 us                                                                   | 9.67 us: 1.23x slower                                                      |
| regex_compile           | 154 ms                                                                    | 192 ms: 1.25x slower                                                       |
| chameleon               | 7.50 ms                                                                   | 9.41 ms: 1.25x slower                                                      |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 955 ms: 1.27x slower                                                       |
| tornado_http            | 125 ms                                                                    | 159 ms: 1.27x slower                                                       |
| pycparser               | 1.30 sec                                                                  | 1.67 sec: 1.28x slower                                                     |
| thrift                  | 942 us                                                                    | 1.21 ms: 1.28x slower                                                      |
| logging_simple          | 6.95 us                                                                   | 8.96 us: 1.29x slower                                                      |
| unpack_sequence         | 45.9 ns                                                                   | 59.3 ns: 1.29x slower                                                      |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 5.28 ms: 1.30x slower                                                      |
| async_tree_memoization  | 639 ms                                                                    | 832 ms: 1.30x slower                                                       |
| async_generators        | 318 ms                                                                    | 417 ms: 1.31x slower                                                       |
| pprint_pformat          | 1.60 sec                                                                  | 2.11 sec: 1.32x slower                                                     |
| pprint_safe_repr        | 768 ms                                                                    | 1.03 sec: 1.34x slower                                                     |
| unpickle_pure_python    | 238 us                                                                    | 320 us: 1.34x slower                                                       |
| async_tree_none         | 529 ms                                                                    | 711 ms: 1.34x slower                                                       |
| html5lib                | 70.2 ms                                                                   | 94.4 ms: 1.34x slower                                                      |
| mako                    | 10.9 ms                                                                   | 14.7 ms: 1.35x slower                                                      |
| deepcopy_memo           | 37.0 us                                                                   | 50.0 us: 1.35x slower                                                      |
| django_template         | 39.6 ms                                                                   | 53.6 ms: 1.35x slower                                                      |
| hexiom                  | 7.00 ms                                                                   | 9.49 ms: 1.36x slower                                                      |
| async_tree_io           | 1.18 sec                                                                  | 1.62 sec: 1.37x slower                                                     |
| scimark_fft             | 276 ms                                                                    | 383 ms: 1.38x slower                                                       |
| xml_etree_process       | 55.8 ms                                                                   | 77.5 ms: 1.39x slower                                                      |
| crypto_pyaes            | 85.0 ms                                                                   | 118 ms: 1.39x slower                                                       |
| chaos                   | 76.2 ms                                                                   | 109 ms: 1.43x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.70 ms: 1.44x slower                                                      |
| pickle_pure_python      | 319 us                                                                    | 461 us: 1.44x slower                                                       |
| spectral_norm           | 95.1 ms                                                                   | 138 ms: 1.45x slower                                                       |
| float                   | 75.7 ms                                                                   | 111 ms: 1.46x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 2.25 ms: 1.47x slower                                                      |
| richards                | 49.1 ms                                                                   | 72.9 ms: 1.48x slower                                                      |
| scimark_lu              | 114 ms                                                                    | 170 ms: 1.49x slower                                                       |
| nbody                   | 92.1 ms                                                                   | 138 ms: 1.49x slower                                                       |
| pyflate                 | 438 ms                                                                    | 696 ms: 1.59x slower                                                       |
| bench_mp_pool           | 4.54 ms                                                                   | 7.26 ms: 1.60x slower                                                      |
| logging_silent          | 103 ns                                                                    | 165 ns: 1.61x slower                                                       |
| scimark_monte_carlo     | 67.8 ms                                                                   | 110 ms: 1.62x slower                                                       |
| scimark_sor             | 109 ms                                                                    | 177 ms: 1.62x slower                                                       |
| raytrace                | 303 ms                                                                    | 495 ms: 1.63x slower                                                       |
| go                      | 158 ms                                                                    | 260 ms: 1.65x slower                                                       |
| deltablue               | 3.99 ms                                                                   | 7.45 ms: 1.86x slower                                                      |
| Geometric mean          | (ref)                                                                     | 1.22x slower                                                               |

Benchmark hidden because not significant (1): mypy2
