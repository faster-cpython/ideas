
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 06249ec
- commit date: 2023-04-01
- overall geometric mean: 1.29x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 251 ms: 1.34x faster                                   |
| chameleon      | 9.13 ms                                                             | 6.49 ms: 1.41x faster                                  |
| docutils       | 3.19 sec                                                            | 2.56 sec: 1.25x faster                                 |
| html5lib       | 86.4 ms                                                             | 61.4 ms: 1.41x faster                                  |
| tornado_http   | 129 ms                                                              | 91.1 ms: 1.41x faster                                  |
| Geometric mean | (ref)                                                               | 1.36x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 146 ms                                                              | 87.4 ms: 1.67x faster                                  |
| float          | 110 ms                                                              | 75.2 ms: 1.46x faster                                  |
| pidigits       | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                               | 1.35x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 134 ms: 1.32x faster                                   |
| regex_v8       | 24.9 ms                                                             | 21.9 ms: 1.14x faster                                  |
| regex_dna      | 213 ms                                                              | 207 ms: 1.03x faster                                   |
| regex_effbot   | 3.22 ms                                                             | 3.54 ms: 1.10x slower                                  |
| Geometric mean | (ref)                                                               | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 288 us: 1.59x faster                                   |
| unpickle_pure_python | 300 us                                                              | 202 us: 1.49x faster                                   |
| json_dumps           | 13.7 ms                                                             | 9.43 ms: 1.45x faster                                  |
| xml_etree_process    | 74.8 ms                                                             | 56.0 ms: 1.34x faster                                  |
| json_loads           | 29.3 us                                                             | 24.3 us: 1.21x faster                                  |
| xml_etree_generate   | 94.9 ms                                                             | 80.9 ms: 1.17x faster                                  |
| pickle_list          | 4.73 us                                                             | 4.20 us: 1.13x faster                                  |
| unpickle             | 15.0 us                                                             | 13.3 us: 1.12x faster                                  |
| xml_etree_parse      | 164 ms                                                              | 149 ms: 1.10x faster                                   |
| xml_etree_iterparse  | 111 ms                                                              | 102 ms: 1.09x faster                                   |
| pickle               | 10.2 us                                                             | 10.5 us: 1.03x slower                                  |
| unpickle_list        | 4.94 us                                                             | 5.07 us: 1.03x slower                                  |
| pickle_dict          | 27.8 us                                                             | 30.6 us: 1.10x slower                                  |
| Geometric mean       | (ref)                                                               | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.83 ms: 1.60x faster                                  |
| python_startup_no_site | 5.80 ms                                                             | 6.53 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                               | 1.19x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 10.1 ms: 1.45x faster                                  |
| genshi_text     | 30.4 ms                                                             | 21.3 ms: 1.43x faster                                  |
| django_template | 45.8 ms                                                             | 33.8 ms: 1.36x faster                                  |
| genshi_xml      | 64.3 ms                                                             | 47.8 ms: 1.35x faster                                  |
| Geometric mean  | (ref)                                                               | 1.39x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-linux-x86_64-python-main-3.12.0a6+-06249ec |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.7 ms                                                             | 29.9 ms: 2.53x faster                                  |
| deltablue               | 7.30 ms                                                             | 3.24 ms: 2.25x faster                                  |
| asyncio_tcp             | 922 ms                                                              | 505 ms: 1.83x faster                                   |
| logging_silent          | 169 ns                                                              | 96.6 ns: 1.75x faster                                  |
| scimark_sor             | 198 ms                                                              | 115 ms: 1.72x faster                                   |
| richards                | 74.2 ms                                                             | 44.3 ms: 1.68x faster                                  |
| nbody                   | 146 ms                                                              | 87.4 ms: 1.67x faster                                  |
| raytrace                | 470 ms                                                              | 286 ms: 1.64x faster                                   |
| go                      | 226 ms                                                              | 140 ms: 1.61x faster                                   |
| python_startup          | 14.1 ms                                                             | 8.83 ms: 1.60x faster                                  |
| chaos                   | 106 ms                                                              | 66.2 ms: 1.60x faster                                  |
| pyflate                 | 671 ms                                                              | 420 ms: 1.59x faster                                   |
| scimark_monte_carlo     | 109 ms                                                              | 68.3 ms: 1.59x faster                                  |
| pickle_pure_python      | 457 us                                                              | 288 us: 1.59x faster                                   |
| crypto_pyaes            | 117 ms                                                              | 73.8 ms: 1.58x faster                                  |
| hexiom                  | 9.50 ms                                                             | 6.10 ms: 1.56x faster                                  |
| spectral_norm           | 150 ms                                                              | 96.5 ms: 1.55x faster                                  |
| unpickle_pure_python    | 300 us                                                              | 202 us: 1.49x faster                                   |
| deepcopy_memo           | 51.8 us                                                             | 35.1 us: 1.48x faster                                  |
| scimark_lu              | 160 ms                                                              | 109 ms: 1.46x faster                                   |
| float                   | 110 ms                                                              | 75.2 ms: 1.46x faster                                  |
| sqlglot_parse           | 2.07 ms                                                             | 1.42 ms: 1.45x faster                                  |
| json_dumps              | 13.7 ms                                                             | 9.43 ms: 1.45x faster                                  |
| mako                    | 14.7 ms                                                             | 10.1 ms: 1.45x faster                                  |
| logging_simple          | 8.21 us                                                             | 5.72 us: 1.43x faster                                  |
| sqlglot_transpile       | 2.45 ms                                                             | 1.72 ms: 1.43x faster                                  |
| genshi_text             | 30.4 ms                                                             | 21.3 ms: 1.43x faster                                  |
| tornado_http            | 129 ms                                                              | 91.1 ms: 1.41x faster                                  |
| unpack_sequence         | 65.6 ns                                                             | 46.4 ns: 1.41x faster                                  |
| logging_format          | 9.07 us                                                             | 6.42 us: 1.41x faster                                  |
| chameleon               | 9.13 ms                                                             | 6.49 ms: 1.41x faster                                  |
| html5lib                | 86.4 ms                                                             | 61.4 ms: 1.41x faster                                  |
| pprint_pformat          | 1.98 sec                                                            | 1.42 sec: 1.39x faster                                 |
| coroutines              | 31.8 ms                                                             | 22.9 ms: 1.39x faster                                  |
| pycparser               | 1.53 sec                                                            | 1.11 sec: 1.38x faster                                 |
| async_tree_io           | 1.78 sec                                                            | 1.29 sec: 1.38x faster                                 |
| pprint_safe_repr        | 953 ms                                                              | 694 ms: 1.37x faster                                   |
| async_tree_none         | 713 ms                                                              | 525 ms: 1.36x faster                                   |
| scimark_fft             | 425 ms                                                              | 314 ms: 1.36x faster                                   |
| django_template         | 45.8 ms                                                             | 33.8 ms: 1.36x faster                                  |
| genshi_xml              | 64.3 ms                                                             | 47.8 ms: 1.35x faster                                  |
| aiohttp                 | 1.35 ms                                                             | 1.01 ms: 1.34x faster                                  |
| 2to3                    | 336 ms                                                              | 251 ms: 1.34x faster                                   |
| xml_etree_process       | 74.8 ms                                                             | 56.0 ms: 1.34x faster                                  |
| deepcopy                | 438 us                                                              | 330 us: 1.33x faster                                   |
| thrift                  | 1.04 ms                                                             | 783 us: 1.32x faster                                   |
| regex_compile           | 177 ms                                                              | 134 ms: 1.32x faster                                   |
| gunicorn                | 1.43 ms                                                             | 1.09 ms: 1.32x faster                                  |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.29 ms: 1.31x faster                                  |
| mypy2                   | 432 ms                                                              | 333 ms: 1.30x faster                                   |
| async_tree_memoization  | 853 ms                                                              | 657 ms: 1.30x faster                                   |
| sqlglot_normalize       | 135 ms                                                              | 105 ms: 1.28x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                             | 51.2 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed | 944 ms                                                              | 741 ms: 1.27x faster                                   |
| deepcopy_reduce         | 3.80 us                                                             | 3.00 us: 1.27x faster                                  |
| fannkuch                | 485 ms                                                              | 385 ms: 1.26x faster                                   |
| docutils                | 3.19 sec                                                            | 2.56 sec: 1.25x faster                                 |
| nqueens                 | 98.8 ms                                                             | 81.3 ms: 1.22x faster                                  |
| sqlalchemy_declarative  | 166 ms                                                              | 137 ms: 1.21x faster                                   |
| bench_thread_pool       | 954 us                                                              | 786 us: 1.21x faster                                   |
| json_loads              | 29.3 us                                                             | 24.3 us: 1.21x faster                                  |
| dulwich_log             | 76.3 ms                                                             | 63.4 ms: 1.20x faster                                  |
| sqlalchemy_imperative   | 21.2 ms                                                             | 17.6 ms: 1.20x faster                                  |
| sympy_integrate         | 24.3 ms                                                             | 20.4 ms: 1.19x faster                                  |
| xml_etree_generate      | 94.9 ms                                                             | 80.9 ms: 1.17x faster                                  |
| json                    | 5.41 ms                                                             | 4.62 ms: 1.17x faster                                  |
| sympy_expand            | 540 ms                                                              | 462 ms: 1.17x faster                                   |
| sympy_str               | 328 ms                                                              | 283 ms: 1.16x faster                                   |
| comprehensions          | 27.3 us                                                             | 23.9 us: 1.14x faster                                  |
| regex_v8                | 24.9 ms                                                             | 21.9 ms: 1.14x faster                                  |
| sqlite_synth            | 2.97 us                                                             | 2.61 us: 1.14x faster                                  |
| pickle_list             | 4.73 us                                                             | 4.20 us: 1.13x faster                                  |
| unpickle                | 15.0 us                                                             | 13.3 us: 1.12x faster                                  |
| djangocms               | 36.3 us                                                             | 32.5 us: 1.12x faster                                  |
| meteor_contest          | 115 ms                                                              | 103 ms: 1.11x faster                                   |
| sympy_sum               | 185 ms                                                              | 167 ms: 1.11x faster                                   |
| create_gc_cycles        | 1.64 ms                                                             | 1.49 ms: 1.10x faster                                  |
| pathlib                 | 19.8 ms                                                             | 18.0 ms: 1.10x faster                                  |
| xml_etree_parse         | 164 ms                                                              | 149 ms: 1.10x faster                                   |
| mdp                     | 2.75 sec                                                            | 2.53 sec: 1.09x faster                                 |
| xml_etree_iterparse     | 111 ms                                                              | 102 ms: 1.09x faster                                   |
| regex_dna               | 213 ms                                                              | 207 ms: 1.03x faster                                   |
| telco                   | 6.67 ms                                                             | 6.51 ms: 1.02x faster                                  |
| async_generators        | 420 ms                                                              | 411 ms: 1.02x faster                                   |
| pidigits                | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| gc_traversal            | 3.53 ms                                                             | 3.60 ms: 1.02x slower                                  |
| pickle                  | 10.2 us                                                             | 10.5 us: 1.03x slower                                  |
| unpickle_list           | 4.94 us                                                             | 5.07 us: 1.03x slower                                  |
| regex_effbot            | 3.22 ms                                                             | 3.54 ms: 1.10x slower                                  |
| pickle_dict             | 27.8 us                                                             | 30.6 us: 1.10x slower                                  |
| python_startup_no_site  | 5.80 ms                                                             | 6.53 ms: 1.13x slower                                  |
| dask                    | 437 ms                                                              | 512 ms: 1.17x slower                                   |
| coverage                | 70.6 ms                                                             | 95.5 ms: 1.35x slower                                  |
| Geometric mean          | (ref)                                                               | 1.29x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (2) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging, pylint
