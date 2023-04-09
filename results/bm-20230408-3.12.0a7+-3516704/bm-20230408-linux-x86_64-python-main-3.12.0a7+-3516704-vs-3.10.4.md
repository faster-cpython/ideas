
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3516704
- commit date: 2023-04-08
- overall geometric mean: 1.31x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 251 ms: 1.34x faster                                   |
| chameleon      | 9.13 ms                                                             | 6.51 ms: 1.40x faster                                  |
| docutils       | 3.19 sec                                                            | 2.54 sec: 1.26x faster                                 |
| html5lib       | 86.4 ms                                                             | 61.4 ms: 1.41x faster                                  |
| tornado_http   | 129 ms                                                              | 94.0 ms: 1.37x faster                                  |
| Geometric mean | (ref)                                                               | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 146 ms                                                              | 86.6 ms: 1.68x faster                                  |
| float          | 110 ms                                                              | 73.6 ms: 1.49x faster                                  |
| pidigits       | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                               | 1.36x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 135 ms: 1.32x faster                                   |
| regex_v8       | 24.9 ms                                                             | 22.1 ms: 1.13x faster                                  |
| regex_dna      | 213 ms                                                              | 204 ms: 1.04x faster                                   |
| regex_effbot   | 3.22 ms                                                             | 3.36 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                               | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 288 us: 1.58x faster                                   |
| unpickle_pure_python | 300 us                                                              | 200 us: 1.50x faster                                   |
| json_dumps           | 13.7 ms                                                             | 9.54 ms: 1.44x faster                                  |
| xml_etree_process    | 74.8 ms                                                             | 55.9 ms: 1.34x faster                                  |
| json_loads           | 29.3 us                                                             | 24.3 us: 1.21x faster                                  |
| xml_etree_generate   | 94.9 ms                                                             | 81.2 ms: 1.17x faster                                  |
| xml_etree_parse      | 164 ms                                                              | 148 ms: 1.11x faster                                   |
| pickle_list          | 4.73 us                                                             | 4.29 us: 1.10x faster                                  |
| xml_etree_iterparse  | 111 ms                                                              | 102 ms: 1.09x faster                                   |
| unpickle             | 15.0 us                                                             | 14.0 us: 1.07x faster                                  |
| unpickle_list        | 4.94 us                                                             | 5.07 us: 1.03x slower                                  |
| pickle               | 10.2 us                                                             | 10.7 us: 1.05x slower                                  |
| pickle_dict          | 27.8 us                                                             | 31.9 us: 1.15x slower                                  |
| Geometric mean       | (ref)                                                               | 1.17x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.82 ms: 1.60x faster                                  |
| python_startup_no_site | 5.80 ms                                                             | 6.51 ms: 1.12x slower                                  |
| Geometric mean         | (ref)                                                               | 1.19x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.97 ms: 1.48x faster                                  |
| genshi_text     | 30.4 ms                                                             | 21.3 ms: 1.43x faster                                  |
| django_template | 45.8 ms                                                             | 33.0 ms: 1.39x faster                                  |
| genshi_xml      | 64.3 ms                                                             | 47.8 ms: 1.35x faster                                  |
| Geometric mean  | (ref)                                                               | 1.41x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230408-linux-x86_64-python-main-3.12.0a7+-3516704 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.7 ms                                                             | 29.0 ms: 2.61x faster                                  |
| deltablue               | 7.30 ms                                                             | 3.24 ms: 2.25x faster                                  |
| asyncio_tcp             | 922 ms                                                              | 506 ms: 1.82x faster                                   |
| logging_silent          | 169 ns                                                              | 94.3 ns: 1.79x faster                                  |
| scimark_sor             | 198 ms                                                              | 112 ms: 1.77x faster                                   |
| sqlglot_parse           | 2.07 ms                                                             | 1.21 ms: 1.71x faster                                  |
| richards                | 74.2 ms                                                             | 43.6 ms: 1.70x faster                                  |
| nbody                   | 146 ms                                                              | 86.6 ms: 1.68x faster                                  |
| raytrace                | 470 ms                                                              | 283 ms: 1.66x faster                                   |
| sqlglot_transpile       | 2.45 ms                                                             | 1.49 ms: 1.65x faster                                  |
| go                      | 226 ms                                                              | 137 ms: 1.64x faster                                   |
| scimark_monte_carlo     | 109 ms                                                              | 66.7 ms: 1.63x faster                                  |
| chaos                   | 106 ms                                                              | 65.7 ms: 1.61x faster                                  |
| python_startup          | 14.1 ms                                                             | 8.82 ms: 1.60x faster                                  |
| pyflate                 | 671 ms                                                              | 420 ms: 1.60x faster                                   |
| spectral_norm           | 150 ms                                                              | 94.5 ms: 1.59x faster                                  |
| hexiom                  | 9.50 ms                                                             | 5.98 ms: 1.59x faster                                  |
| pickle_pure_python      | 457 us                                                              | 288 us: 1.58x faster                                   |
| crypto_pyaes            | 117 ms                                                              | 73.7 ms: 1.58x faster                                  |
| scimark_lu              | 160 ms                                                              | 104 ms: 1.54x faster                                   |
| deepcopy_memo           | 51.8 us                                                             | 34.1 us: 1.52x faster                                  |
| unpack_sequence         | 65.6 ns                                                             | 43.5 ns: 1.51x faster                                  |
| unpickle_pure_python    | 300 us                                                              | 200 us: 1.50x faster                                   |
| float                   | 110 ms                                                              | 73.6 ms: 1.49x faster                                  |
| mako                    | 14.7 ms                                                             | 9.97 ms: 1.48x faster                                  |
| logging_simple          | 8.21 us                                                             | 5.65 us: 1.45x faster                                  |
| json_dumps              | 13.7 ms                                                             | 9.54 ms: 1.44x faster                                  |
| logging_format          | 9.07 us                                                             | 6.32 us: 1.44x faster                                  |
| genshi_text             | 30.4 ms                                                             | 21.3 ms: 1.43x faster                                  |
| scimark_fft             | 425 ms                                                              | 298 ms: 1.43x faster                                   |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 3.99 ms: 1.41x faster                                  |
| html5lib                | 86.4 ms                                                             | 61.4 ms: 1.41x faster                                  |
| chameleon               | 9.13 ms                                                             | 6.51 ms: 1.40x faster                                  |
| coroutines              | 31.8 ms                                                             | 22.8 ms: 1.39x faster                                  |
| django_template         | 45.8 ms                                                             | 33.0 ms: 1.39x faster                                  |
| pprint_pformat          | 1.98 sec                                                            | 1.43 sec: 1.38x faster                                 |
| pycparser               | 1.53 sec                                                            | 1.11 sec: 1.38x faster                                 |
| async_tree_io           | 1.78 sec                                                            | 1.30 sec: 1.37x faster                                 |
| tornado_http            | 129 ms                                                              | 94.0 ms: 1.37x faster                                  |
| pprint_safe_repr        | 953 ms                                                              | 697 ms: 1.37x faster                                   |
| async_tree_none         | 713 ms                                                              | 523 ms: 1.36x faster                                   |
| deepcopy                | 438 us                                                              | 324 us: 1.35x faster                                   |
| genshi_xml              | 64.3 ms                                                             | 47.8 ms: 1.35x faster                                  |
| 2to3                    | 336 ms                                                              | 251 ms: 1.34x faster                                   |
| async_tree_memoization  | 853 ms                                                              | 637 ms: 1.34x faster                                   |
| xml_etree_process       | 74.8 ms                                                             | 55.9 ms: 1.34x faster                                  |
| thrift                  | 1.04 ms                                                             | 779 us: 1.33x faster                                   |
| aiohttp                 | 1.35 ms                                                             | 1.01 ms: 1.33x faster                                  |
| regex_compile           | 177 ms                                                              | 135 ms: 1.32x faster                                   |
| deepcopy_reduce         | 3.80 us                                                             | 2.90 us: 1.31x faster                                  |
| gunicorn                | 1.43 ms                                                             | 1.10 ms: 1.30x faster                                  |
| fannkuch                | 485 ms                                                              | 375 ms: 1.29x faster                                   |
| sqlglot_normalize       | 135 ms                                                              | 104 ms: 1.29x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                             | 50.8 ms: 1.29x faster                                  |
| mypy2                   | 432 ms                                                              | 336 ms: 1.28x faster                                   |
| async_tree_cpu_io_mixed | 944 ms                                                              | 739 ms: 1.28x faster                                   |
| docutils                | 3.19 sec                                                            | 2.54 sec: 1.26x faster                                 |
| comprehensions          | 27.3 us                                                             | 21.8 us: 1.25x faster                                  |
| nqueens                 | 98.8 ms                                                             | 80.5 ms: 1.23x faster                                  |
| bench_thread_pool       | 954 us                                                              | 786 us: 1.21x faster                                   |
| json_loads              | 29.3 us                                                             | 24.3 us: 1.21x faster                                  |
| dulwich_log             | 76.3 ms                                                             | 63.6 ms: 1.20x faster                                  |
| sympy_integrate         | 24.3 ms                                                             | 20.3 ms: 1.20x faster                                  |
| sqlalchemy_declarative  | 166 ms                                                              | 139 ms: 1.19x faster                                   |
| sympy_expand            | 540 ms                                                              | 458 ms: 1.18x faster                                   |
| sqlalchemy_imperative   | 21.2 ms                                                             | 18.1 ms: 1.17x faster                                  |
| xml_etree_generate      | 94.9 ms                                                             | 81.2 ms: 1.17x faster                                  |
| sympy_str               | 328 ms                                                              | 282 ms: 1.16x faster                                   |
| json                    | 5.41 ms                                                             | 4.71 ms: 1.15x faster                                  |
| sqlite_synth            | 2.97 us                                                             | 2.63 us: 1.13x faster                                  |
| regex_v8                | 24.9 ms                                                             | 22.1 ms: 1.13x faster                                  |
| sympy_sum               | 185 ms                                                              | 164 ms: 1.13x faster                                   |
| djangocms               | 36.3 us                                                             | 32.3 us: 1.13x faster                                  |
| create_gc_cycles        | 1.64 ms                                                             | 1.46 ms: 1.12x faster                                  |
| meteor_contest          | 115 ms                                                              | 102 ms: 1.12x faster                                   |
| xml_etree_parse         | 164 ms                                                              | 148 ms: 1.11x faster                                   |
| pickle_list             | 4.73 us                                                             | 4.29 us: 1.10x faster                                  |
| xml_etree_iterparse     | 111 ms                                                              | 102 ms: 1.09x faster                                   |
| pathlib                 | 19.8 ms                                                             | 18.3 ms: 1.08x faster                                  |
| unpickle                | 15.0 us                                                             | 14.0 us: 1.07x faster                                  |
| mdp                     | 2.75 sec                                                            | 2.62 sec: 1.05x faster                                 |
| regex_dna               | 213 ms                                                              | 204 ms: 1.04x faster                                   |
| telco                   | 6.67 ms                                                             | 6.52 ms: 1.02x faster                                  |
| async_generators        | 420 ms                                                              | 412 ms: 1.02x faster                                   |
| pidigits                | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| unpickle_list           | 4.94 us                                                             | 5.07 us: 1.03x slower                                  |
| gc_traversal            | 3.53 ms                                                             | 3.65 ms: 1.04x slower                                  |
| regex_effbot            | 3.22 ms                                                             | 3.36 ms: 1.04x slower                                  |
| pickle                  | 10.2 us                                                             | 10.7 us: 1.05x slower                                  |
| python_startup_no_site  | 5.80 ms                                                             | 6.51 ms: 1.12x slower                                  |
| dask                    | 437 ms                                                              | 502 ms: 1.15x slower                                   |
| pickle_dict             | 27.8 us                                                             | 31.9 us: 1.15x slower                                  |
| coverage                | 70.6 ms                                                             | 97.6 ms: 1.38x slower                                  |
| Geometric mean          | (ref)                                                               | 1.31x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (2) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging, pylint
