
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 30a306c
- commit date: 2023-03-25
- overall geometric mean: 1.30x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 254 ms: 1.32x faster                                   |
| chameleon      | 9.13 ms                                                             | 6.54 ms: 1.40x faster                                  |
| docutils       | 3.19 sec                                                            | 2.56 sec: 1.25x faster                                 |
| html5lib       | 86.4 ms                                                             | 62.0 ms: 1.39x faster                                  |
| tornado_http   | 129 ms                                                              | 91.2 ms: 1.41x faster                                  |
| Geometric mean | (ref)                                                               | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 146 ms                                                              | 89.5 ms: 1.63x faster                                  |
| float          | 110 ms                                                              | 73.8 ms: 1.49x faster                                  |
| pidigits       | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                               | 1.35x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 134 ms: 1.32x faster                                   |
| regex_v8       | 24.9 ms                                                             | 22.4 ms: 1.11x faster                                  |
| regex_dna      | 213 ms                                                              | 204 ms: 1.05x faster                                   |
| regex_effbot   | 3.22 ms                                                             | 3.45 ms: 1.07x slower                                  |
| Geometric mean | (ref)                                                               | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 287 us: 1.59x faster                                   |
| unpickle_pure_python | 300 us                                                              | 200 us: 1.50x faster                                   |
| json_dumps           | 13.7 ms                                                             | 9.58 ms: 1.43x faster                                  |
| xml_etree_process    | 74.8 ms                                                             | 56.0 ms: 1.34x faster                                  |
| json_loads           | 29.3 us                                                             | 24.0 us: 1.22x faster                                  |
| xml_etree_generate   | 94.9 ms                                                             | 81.7 ms: 1.16x faster                                  |
| unpickle             | 15.0 us                                                             | 13.2 us: 1.13x faster                                  |
| xml_etree_parse      | 164 ms                                                              | 148 ms: 1.11x faster                                   |
| xml_etree_iterparse  | 111 ms                                                              | 101 ms: 1.10x faster                                   |
| pickle_list          | 4.73 us                                                             | 4.35 us: 1.09x faster                                  |
| pickle               | 10.2 us                                                             | 10.4 us: 1.02x slower                                  |
| pickle_dict          | 27.8 us                                                             | 32.3 us: 1.16x slower                                  |
| Geometric mean       | (ref)                                                               | 1.17x faster                                           |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.86 ms: 1.60x faster                                  |
| python_startup_no_site | 5.80 ms                                                             | 6.54 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                               | 1.19x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.82 ms: 1.50x faster                                  |
| genshi_text     | 30.4 ms                                                             | 21.3 ms: 1.43x faster                                  |
| django_template | 45.8 ms                                                             | 33.5 ms: 1.37x faster                                  |
| genshi_xml      | 64.3 ms                                                             | 48.3 ms: 1.33x faster                                  |
| Geometric mean  | (ref)                                                               | 1.41x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-python-main-3.12.0a6+-30a306c |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.7 ms                                                             | 29.6 ms: 2.56x faster                                  |
| deltablue               | 7.30 ms                                                             | 3.21 ms: 2.27x faster                                  |
| asyncio_tcp             | 922 ms                                                              | 504 ms: 1.83x faster                                   |
| scimark_sor             | 198 ms                                                              | 112 ms: 1.76x faster                                   |
| logging_silent          | 169 ns                                                              | 97.6 ns: 1.73x faster                                  |
| richards                | 74.2 ms                                                             | 44.0 ms: 1.69x faster                                  |
| raytrace                | 470 ms                                                              | 282 ms: 1.66x faster                                   |
| go                      | 226 ms                                                              | 137 ms: 1.65x faster                                   |
| spectral_norm           | 150 ms                                                              | 90.9 ms: 1.65x faster                                  |
| scimark_monte_carlo     | 109 ms                                                              | 65.9 ms: 1.65x faster                                  |
| pyflate                 | 671 ms                                                              | 410 ms: 1.64x faster                                   |
| nbody                   | 146 ms                                                              | 89.5 ms: 1.63x faster                                  |
| chaos                   | 106 ms                                                              | 65.8 ms: 1.61x faster                                  |
| python_startup          | 14.1 ms                                                             | 8.86 ms: 1.60x faster                                  |
| crypto_pyaes            | 117 ms                                                              | 73.2 ms: 1.59x faster                                  |
| pickle_pure_python      | 457 us                                                              | 287 us: 1.59x faster                                   |
| hexiom                  | 9.50 ms                                                             | 5.99 ms: 1.59x faster                                  |
| unpack_sequence         | 65.6 ns                                                             | 42.1 ns: 1.56x faster                                  |
| deepcopy_memo           | 51.8 us                                                             | 34.1 us: 1.52x faster                                  |
| mako                    | 14.7 ms                                                             | 9.82 ms: 1.50x faster                                  |
| unpickle_pure_python    | 300 us                                                              | 200 us: 1.50x faster                                   |
| float                   | 110 ms                                                              | 73.8 ms: 1.49x faster                                  |
| scimark_lu              | 160 ms                                                              | 109 ms: 1.47x faster                                   |
| sqlglot_parse           | 2.07 ms                                                             | 1.42 ms: 1.45x faster                                  |
| logging_format          | 9.07 us                                                             | 6.32 us: 1.43x faster                                  |
| logging_simple          | 8.21 us                                                             | 5.74 us: 1.43x faster                                  |
| genshi_text             | 30.4 ms                                                             | 21.3 ms: 1.43x faster                                  |
| json_dumps              | 13.7 ms                                                             | 9.58 ms: 1.43x faster                                  |
| sqlglot_transpile       | 2.45 ms                                                             | 1.72 ms: 1.43x faster                                  |
| tornado_http            | 129 ms                                                              | 91.2 ms: 1.41x faster                                  |
| chameleon               | 9.13 ms                                                             | 6.54 ms: 1.40x faster                                  |
| scimark_fft             | 425 ms                                                              | 305 ms: 1.40x faster                                   |
| html5lib                | 86.4 ms                                                             | 62.0 ms: 1.39x faster                                  |
| pprint_pformat          | 1.98 sec                                                            | 1.42 sec: 1.39x faster                                 |
| coroutines              | 31.8 ms                                                             | 23.0 ms: 1.38x faster                                  |
| pprint_safe_repr        | 953 ms                                                              | 692 ms: 1.38x faster                                   |
| async_tree_io           | 1.78 sec                                                            | 1.30 sec: 1.38x faster                                 |
| async_tree_none         | 713 ms                                                              | 520 ms: 1.37x faster                                   |
| django_template         | 45.8 ms                                                             | 33.5 ms: 1.37x faster                                  |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.14 ms: 1.36x faster                                  |
| aiohttp                 | 1.35 ms                                                             | 1.01 ms: 1.34x faster                                  |
| xml_etree_process       | 74.8 ms                                                             | 56.0 ms: 1.34x faster                                  |
| deepcopy                | 438 us                                                              | 328 us: 1.33x faster                                   |
| genshi_xml              | 64.3 ms                                                             | 48.3 ms: 1.33x faster                                  |
| async_tree_memoization  | 853 ms                                                              | 643 ms: 1.33x faster                                   |
| regex_compile           | 177 ms                                                              | 134 ms: 1.32x faster                                   |
| 2to3                    | 336 ms                                                              | 254 ms: 1.32x faster                                   |
| gunicorn                | 1.43 ms                                                             | 1.09 ms: 1.32x faster                                  |
| thrift                  | 1.04 ms                                                             | 795 us: 1.30x faster                                   |
| pycparser               | 1.53 sec                                                            | 1.18 sec: 1.30x faster                                 |
| mypy2                   | 432 ms                                                              | 333 ms: 1.30x faster                                   |
| fannkuch                | 485 ms                                                              | 375 ms: 1.29x faster                                   |
| async_tree_cpu_io_mixed | 944 ms                                                              | 734 ms: 1.29x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                             | 51.3 ms: 1.27x faster                                  |
| sqlglot_normalize       | 135 ms                                                              | 106 ms: 1.27x faster                                   |
| deepcopy_reduce         | 3.80 us                                                             | 3.00 us: 1.27x faster                                  |
| docutils                | 3.19 sec                                                            | 2.56 sec: 1.25x faster                                 |
| json_loads              | 29.3 us                                                             | 24.0 us: 1.22x faster                                  |
| bench_thread_pool       | 954 us                                                              | 790 us: 1.21x faster                                   |
| sqlalchemy_declarative  | 166 ms                                                              | 138 ms: 1.21x faster                                   |
| dulwich_log             | 76.3 ms                                                             | 63.7 ms: 1.20x faster                                  |
| nqueens                 | 98.8 ms                                                             | 82.5 ms: 1.20x faster                                  |
| sympy_integrate         | 24.3 ms                                                             | 20.5 ms: 1.19x faster                                  |
| json                    | 5.41 ms                                                             | 4.59 ms: 1.18x faster                                  |
| sqlalchemy_imperative   | 21.2 ms                                                             | 18.0 ms: 1.17x faster                                  |
| sympy_expand            | 540 ms                                                              | 463 ms: 1.17x faster                                   |
| xml_etree_generate      | 94.9 ms                                                             | 81.7 ms: 1.16x faster                                  |
| comprehensions          | 27.3 us                                                             | 23.5 us: 1.16x faster                                  |
| sympy_str               | 328 ms                                                              | 285 ms: 1.15x faster                                   |
| djangocms               | 36.3 us                                                             | 32.0 us: 1.14x faster                                  |
| unpickle                | 15.0 us                                                             | 13.2 us: 1.13x faster                                  |
| sqlite_synth            | 2.97 us                                                             | 2.65 us: 1.12x faster                                  |
| meteor_contest          | 115 ms                                                              | 103 ms: 1.11x faster                                   |
| sympy_sum               | 185 ms                                                              | 166 ms: 1.11x faster                                   |
| regex_v8                | 24.9 ms                                                             | 22.4 ms: 1.11x faster                                  |
| create_gc_cycles        | 1.64 ms                                                             | 1.48 ms: 1.11x faster                                  |
| xml_etree_parse         | 164 ms                                                              | 148 ms: 1.11x faster                                   |
| xml_etree_iterparse     | 111 ms                                                              | 101 ms: 1.10x faster                                   |
| pathlib                 | 19.8 ms                                                             | 17.9 ms: 1.10x faster                                  |
| pickle_list             | 4.73 us                                                             | 4.35 us: 1.09x faster                                  |
| mdp                     | 2.75 sec                                                            | 2.55 sec: 1.08x faster                                 |
| regex_dna               | 213 ms                                                              | 204 ms: 1.05x faster                                   |
| telco                   | 6.67 ms                                                             | 6.44 ms: 1.04x faster                                  |
| async_generators        | 420 ms                                                              | 409 ms: 1.03x faster                                   |
| pidigits                | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| pickle                  | 10.2 us                                                             | 10.4 us: 1.02x slower                                  |
| regex_effbot            | 3.22 ms                                                             | 3.45 ms: 1.07x slower                                  |
| gc_traversal            | 3.53 ms                                                             | 3.93 ms: 1.11x slower                                  |
| python_startup_no_site  | 5.80 ms                                                             | 6.54 ms: 1.13x slower                                  |
| pickle_dict             | 27.8 us                                                             | 32.3 us: 1.16x slower                                  |
| dask                    | 437 ms                                                              | 514 ms: 1.18x slower                                   |
| coverage                | 70.6 ms                                                             | 97.6 ms: 1.38x slower                                  |
| Geometric mean          | (ref)                                                               | 1.30x faster                                           |

Benchmark hidden because not significant (2): bench_mp_pool, unpickle_list
Ignored benchmarks (2) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging, pylint
