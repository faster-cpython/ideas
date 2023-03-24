
# Results vs. 3.10.4

- fork: python
- ref: deaf509e8fc6e0363bd6
- machine: linux-x86_64
- commit hash: deaf509
- commit date: 2022-10-24
- overall geometric mean: 1.25x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 257 ms: 1.31x faster                                                |
| chameleon      | 9.13 ms                                                             | 6.52 ms: 1.40x faster                                               |
| docutils       | 3.19 sec                                                            | 2.59 sec: 1.23x faster                                              |
| html5lib       | 86.4 ms                                                             | 64.0 ms: 1.35x faster                                               |
| tornado_http   | 129 ms                                                              | 96.7 ms: 1.33x faster                                               |
| Geometric mean | (ref)                                                               | 1.32x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 96.7 ms: 1.51x faster                                               |
| float          | 110 ms                                                              | 76.0 ms: 1.45x faster                                               |
| pidigits       | 190 ms                                                              | 197 ms: 1.04x slower                                                |
| Geometric mean | (ref)                                                               | 1.28x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 137 ms: 1.30x faster                                                |
| regex_v8       | 24.9 ms                                                             | 22.0 ms: 1.14x faster                                               |
| regex_dna      | 213 ms                                                              | 196 ms: 1.08x faster                                                |
| regex_effbot   | 3.22 ms                                                             | 3.32 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                               | 1.12x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 307 us: 1.49x faster                                                |
| xml_etree_process    | 74.8 ms                                                             | 54.1 ms: 1.38x faster                                               |
| unpickle_pure_python | 300 us                                                              | 228 us: 1.31x faster                                                |
| xml_etree_generate   | 94.9 ms                                                             | 76.5 ms: 1.24x faster                                               |
| pickle_list          | 4.73 us                                                             | 4.03 us: 1.17x faster                                               |
| unpickle             | 15.0 us                                                             | 13.2 us: 1.13x faster                                               |
| json_loads           | 29.3 us                                                             | 26.2 us: 1.12x faster                                               |
| json_dumps           | 13.7 ms                                                             | 12.5 ms: 1.09x faster                                               |
| pickle               | 10.2 us                                                             | 9.79 us: 1.04x faster                                               |
| xml_etree_iterparse  | 111 ms                                                              | 108 ms: 1.03x faster                                                |
| pickle_dict          | 27.8 us                                                             | 30.9 us: 1.11x slower                                               |
| Geometric mean       | (ref)                                                               | 1.14x faster                                                        |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.49 ms: 1.67x faster                                               |
| python_startup_no_site | 5.80 ms                                                             | 5.98 ms: 1.03x slower                                               |
| Geometric mean         | (ref)                                                               | 1.27x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.82 ms: 1.50x faster                                               |
| django_template | 45.8 ms                                                             | 32.9 ms: 1.39x faster                                               |
| genshi_text     | 30.4 ms                                                             | 21.8 ms: 1.39x faster                                               |
| genshi_xml      | 64.3 ms                                                             | 51.8 ms: 1.24x faster                                               |
| Geometric mean  | (ref)                                                               | 1.38x faster                                                        |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|-------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| deltablue               | 7.30 ms                                                             | 3.66 ms: 1.99x faster                                               |
| scimark_sor             | 198 ms                                                              | 115 ms: 1.72x faster                                                |
| logging_silent          | 169 ns                                                              | 98.7 ns: 1.71x faster                                               |
| python_startup          | 14.1 ms                                                             | 8.49 ms: 1.67x faster                                               |
| go                      | 226 ms                                                              | 138 ms: 1.63x faster                                                |
| richards                | 74.2 ms                                                             | 45.7 ms: 1.62x faster                                               |
| pyflate                 | 671 ms                                                              | 414 ms: 1.62x faster                                                |
| raytrace                | 470 ms                                                              | 292 ms: 1.61x faster                                                |
| scimark_monte_carlo     | 109 ms                                                              | 67.8 ms: 1.60x faster                                               |
| crypto_pyaes            | 117 ms                                                              | 73.8 ms: 1.58x faster                                               |
| chaos                   | 106 ms                                                              | 68.0 ms: 1.56x faster                                               |
| sqlglot_parse           | 2.07 ms                                                             | 1.36 ms: 1.52x faster                                               |
| spectral_norm           | 150 ms                                                              | 99.5 ms: 1.51x faster                                               |
| nbody                   | 146 ms                                                              | 96.7 ms: 1.51x faster                                               |
| mako                    | 14.7 ms                                                             | 9.82 ms: 1.50x faster                                               |
| pickle_pure_python      | 457 us                                                              | 307 us: 1.49x faster                                                |
| sqlglot_transpile       | 2.45 ms                                                             | 1.65 ms: 1.49x faster                                               |
| scimark_lu              | 160 ms                                                              | 108 ms: 1.48x faster                                                |
| hexiom                  | 9.50 ms                                                             | 6.48 ms: 1.47x faster                                               |
| float                   | 110 ms                                                              | 76.0 ms: 1.45x faster                                               |
| deepcopy_memo           | 51.8 us                                                             | 36.4 us: 1.42x faster                                               |
| chameleon               | 9.13 ms                                                             | 6.52 ms: 1.40x faster                                               |
| django_template         | 45.8 ms                                                             | 32.9 ms: 1.39x faster                                               |
| genshi_text             | 30.4 ms                                                             | 21.8 ms: 1.39x faster                                               |
| async_tree_io           | 1.78 sec                                                            | 1.28 sec: 1.39x faster                                              |
| xml_etree_process       | 74.8 ms                                                             | 54.1 ms: 1.38x faster                                               |
| async_tree_memoization  | 853 ms                                                              | 621 ms: 1.37x faster                                                |
| logging_format          | 9.07 us                                                             | 6.64 us: 1.37x faster                                               |
| pprint_pformat          | 1.98 sec                                                            | 1.45 sec: 1.36x faster                                              |
| pprint_safe_repr        | 953 ms                                                              | 701 ms: 1.36x faster                                                |
| async_tree_none         | 713 ms                                                              | 525 ms: 1.36x faster                                                |
| thrift                  | 1.04 ms                                                             | 766 us: 1.35x faster                                                |
| html5lib                | 86.4 ms                                                             | 64.0 ms: 1.35x faster                                               |
| logging_simple          | 8.21 us                                                             | 6.09 us: 1.35x faster                                               |
| pycparser               | 1.53 sec                                                            | 1.14 sec: 1.34x faster                                              |
| tornado_http            | 129 ms                                                              | 96.7 ms: 1.33x faster                                               |
| unpack_sequence         | 65.6 ns                                                             | 49.5 ns: 1.33x faster                                               |
| unpickle_pure_python    | 300 us                                                              | 228 us: 1.31x faster                                                |
| 2to3                    | 336 ms                                                              | 257 ms: 1.31x faster                                                |
| regex_compile           | 177 ms                                                              | 137 ms: 1.30x faster                                                |
| scimark_fft             | 425 ms                                                              | 328 ms: 1.30x faster                                                |
| deepcopy                | 438 us                                                              | 339 us: 1.29x faster                                                |
| deepcopy_reduce         | 3.80 us                                                             | 2.96 us: 1.28x faster                                               |
| async_tree_cpu_io_mixed | 944 ms                                                              | 736 ms: 1.28x faster                                                |
| aiohttp                 | 1.35 ms                                                             | 1.05 ms: 1.28x faster                                               |
| gunicorn                | 1.43 ms                                                             | 1.13 ms: 1.27x faster                                               |
| fannkuch                | 485 ms                                                              | 384 ms: 1.26x faster                                                |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.47 ms: 1.26x faster                                               |
| genshi_xml              | 64.3 ms                                                             | 51.8 ms: 1.24x faster                                               |
| sqlglot_normalize       | 135 ms                                                              | 108 ms: 1.24x faster                                                |
| xml_etree_generate      | 94.9 ms                                                             | 76.5 ms: 1.24x faster                                               |
| docutils                | 3.19 sec                                                            | 2.59 sec: 1.23x faster                                              |
| comprehensions          | 27.3 us                                                             | 22.2 us: 1.23x faster                                               |
| sqlglot_optimize        | 65.3 ms                                                             | 53.4 ms: 1.22x faster                                               |
| coroutines              | 31.8 ms                                                             | 26.3 ms: 1.21x faster                                               |
| sqlalchemy_declarative  | 166 ms                                                              | 138 ms: 1.20x faster                                                |
| dulwich_log             | 76.3 ms                                                             | 63.6 ms: 1.20x faster                                               |
| flaskblogging           | 8.48 ms                                                             | 7.09 ms: 1.20x faster                                               |
| dask                    | 437 ms                                                              | 368 ms: 1.19x faster                                                |
| sqlite_synth            | 2.97 us                                                             | 2.51 us: 1.18x faster                                               |
| nqueens                 | 98.8 ms                                                             | 84.0 ms: 1.18x faster                                               |
| pickle_list             | 4.73 us                                                             | 4.03 us: 1.17x faster                                               |
| sqlalchemy_imperative   | 21.2 ms                                                             | 18.0 ms: 1.17x faster                                               |
| bench_thread_pool       | 954 us                                                              | 820 us: 1.16x faster                                                |
| async_generators        | 420 ms                                                              | 361 ms: 1.16x faster                                                |
| sympy_integrate         | 24.3 ms                                                             | 21.0 ms: 1.15x faster                                               |
| regex_v8                | 24.9 ms                                                             | 22.0 ms: 1.14x faster                                               |
| unpickle                | 15.0 us                                                             | 13.2 us: 1.13x faster                                               |
| sympy_expand            | 540 ms                                                              | 477 ms: 1.13x faster                                                |
| djangocms               | 36.3 us                                                             | 32.3 us: 1.13x faster                                               |
| sympy_str               | 328 ms                                                              | 291 ms: 1.13x faster                                                |
| json_loads              | 29.3 us                                                             | 26.2 us: 1.12x faster                                               |
| json                    | 5.41 ms                                                             | 4.86 ms: 1.11x faster                                               |
| create_gc_cycles        | 1.64 ms                                                             | 1.48 ms: 1.11x faster                                               |
| sympy_sum               | 185 ms                                                              | 167 ms: 1.10x faster                                                |
| json_dumps              | 13.7 ms                                                             | 12.5 ms: 1.09x faster                                               |
| pylint                  | 521 ms                                                              | 476 ms: 1.09x faster                                                |
| pathlib                 | 19.8 ms                                                             | 18.2 ms: 1.09x faster                                               |
| regex_dna               | 213 ms                                                              | 196 ms: 1.08x faster                                                |
| meteor_contest          | 115 ms                                                              | 106 ms: 1.08x faster                                                |
| pickle                  | 10.2 us                                                             | 9.79 us: 1.04x faster                                               |
| mdp                     | 2.75 sec                                                            | 2.64 sec: 1.04x faster                                              |
| asyncio_tcp             | 922 ms                                                              | 888 ms: 1.04x faster                                                |
| xml_etree_iterparse     | 111 ms                                                              | 108 ms: 1.03x faster                                                |
| generators              | 75.7 ms                                                             | 73.4 ms: 1.03x faster                                               |
| telco                   | 6.67 ms                                                             | 6.59 ms: 1.01x faster                                               |
| gc_traversal            | 3.53 ms                                                             | 3.63 ms: 1.03x slower                                               |
| python_startup_no_site  | 5.80 ms                                                             | 5.98 ms: 1.03x slower                                               |
| regex_effbot            | 3.22 ms                                                             | 3.32 ms: 1.03x slower                                               |
| pidigits                | 190 ms                                                              | 197 ms: 1.04x slower                                                |
| pickle_dict             | 27.8 us                                                             | 30.9 us: 1.11x slower                                               |
| coverage                | 70.6 ms                                                             | 101 ms: 1.43x slower                                                |
| Geometric mean          | (ref)                                                               | 1.25x faster                                                        |

Benchmark hidden because not significant (4): mypy2, xml_etree_parse, bench_mp_pool, unpickle_list
