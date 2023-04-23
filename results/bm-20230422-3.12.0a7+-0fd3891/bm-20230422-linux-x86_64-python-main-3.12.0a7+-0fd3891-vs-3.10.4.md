
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 0fd3891
- commit date: 2023-04-22
- overall geometric mean: 1.24x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 268 ms: 1.25x faster                                   |
| chameleon      | 9.13 ms                                                             | 6.93 ms: 1.32x faster                                  |
| docutils       | 3.19 sec                                                            | 2.70 sec: 1.18x faster                                 |
| html5lib       | 86.4 ms                                                             | 65.0 ms: 1.33x faster                                  |
| tornado_http   | 129 ms                                                              | 104 ms: 1.24x faster                                   |
| Geometric mean | (ref)                                                               | 1.26x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 146 ms                                                              | 88.4 ms: 1.65x faster                                  |
| float          | 110 ms                                                              | 80.4 ms: 1.37x faster                                  |
| pidigits       | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                               | 1.31x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 144 ms: 1.23x faster                                   |
| regex_v8       | 24.9 ms                                                             | 22.3 ms: 1.12x faster                                  |
| regex_dna      | 213 ms                                                              | 205 ms: 1.04x faster                                   |
| regex_effbot   | 3.22 ms                                                             | 3.26 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                               | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 311 us: 1.47x faster                                   |
| json_dumps           | 13.7 ms                                                             | 9.75 ms: 1.41x faster                                  |
| unpickle_pure_python | 300 us                                                              | 219 us: 1.37x faster                                   |
| xml_etree_process    | 74.8 ms                                                             | 58.6 ms: 1.28x faster                                  |
| json_loads           | 29.3 us                                                             | 24.8 us: 1.18x faster                                  |
| xml_etree_generate   | 94.9 ms                                                             | 83.2 ms: 1.14x faster                                  |
| xml_etree_iterparse  | 111 ms                                                              | 103 ms: 1.08x faster                                   |
| pickle_list          | 4.73 us                                                             | 4.39 us: 1.08x faster                                  |
| xml_etree_parse      | 164 ms                                                              | 152 ms: 1.08x faster                                   |
| pickle               | 10.2 us                                                             | 10.5 us: 1.03x slower                                  |
| unpickle_list        | 4.94 us                                                             | 5.24 us: 1.06x slower                                  |
| pickle_dict          | 27.8 us                                                             | 30.7 us: 1.11x slower                                  |
| Geometric mean       | (ref)                                                               | 1.13x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 9.05 ms: 1.56x faster                                  |
| python_startup_no_site | 5.80 ms                                                             | 6.65 ms: 1.15x slower                                  |
| Geometric mean         | (ref)                                                               | 1.17x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 10.5 ms: 1.40x faster                                  |
| genshi_text     | 30.4 ms                                                             | 22.7 ms: 1.34x faster                                  |
| django_template | 45.8 ms                                                             | 34.7 ms: 1.32x faster                                  |
| genshi_xml      | 64.3 ms                                                             | 50.7 ms: 1.27x faster                                  |
| Geometric mean  | (ref)                                                               | 1.33x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.7 ms                                                             | 31.2 ms: 2.43x faster                                  |
| deltablue               | 7.30 ms                                                             | 3.64 ms: 2.01x faster                                  |
| asyncio_tcp             | 922 ms                                                              | 511 ms: 1.81x faster                                   |
| richards                | 74.2 ms                                                             | 44.0 ms: 1.69x faster                                  |
| logging_silent          | 169 ns                                                              | 101 ns: 1.67x faster                                   |
| nbody                   | 146 ms                                                              | 88.4 ms: 1.65x faster                                  |
| go                      | 226 ms                                                              | 138 ms: 1.63x faster                                   |
| scimark_sor             | 198 ms                                                              | 124 ms: 1.59x faster                                   |
| sqlglot_parse           | 2.07 ms                                                             | 1.31 ms: 1.58x faster                                  |
| raytrace                | 470 ms                                                              | 300 ms: 1.57x faster                                   |
| python_startup          | 14.1 ms                                                             | 9.05 ms: 1.56x faster                                  |
| chaos                   | 106 ms                                                              | 69.3 ms: 1.53x faster                                  |
| sqlglot_transpile       | 2.45 ms                                                             | 1.63 ms: 1.50x faster                                  |
| hexiom                  | 9.50 ms                                                             | 6.34 ms: 1.50x faster                                  |
| scimark_monte_carlo     | 109 ms                                                              | 73.3 ms: 1.48x faster                                  |
| crypto_pyaes            | 117 ms                                                              | 78.9 ms: 1.48x faster                                  |
| pickle_pure_python      | 457 us                                                              | 311 us: 1.47x faster                                   |
| pyflate                 | 671 ms                                                              | 459 ms: 1.46x faster                                   |
| scimark_lu              | 160 ms                                                              | 110 ms: 1.46x faster                                   |
| spectral_norm           | 150 ms                                                              | 105 ms: 1.43x faster                                   |
| coroutines              | 31.8 ms                                                             | 22.3 ms: 1.42x faster                                  |
| json_dumps              | 13.7 ms                                                             | 9.75 ms: 1.41x faster                                  |
| mako                    | 14.7 ms                                                             | 10.5 ms: 1.40x faster                                  |
| unpack_sequence         | 65.6 ns                                                             | 47.4 ns: 1.38x faster                                  |
| async_tree_io           | 1.78 sec                                                            | 1.30 sec: 1.37x faster                                 |
| unpickle_pure_python    | 300 us                                                              | 219 us: 1.37x faster                                   |
| float                   | 110 ms                                                              | 80.4 ms: 1.37x faster                                  |
| deepcopy_memo           | 51.8 us                                                             | 38.0 us: 1.36x faster                                  |
| async_tree_none         | 713 ms                                                              | 524 ms: 1.36x faster                                   |
| genshi_text             | 30.4 ms                                                             | 22.7 ms: 1.34x faster                                  |
| pprint_pformat          | 1.98 sec                                                            | 1.48 sec: 1.33x faster                                 |
| logging_simple          | 8.21 us                                                             | 6.17 us: 1.33x faster                                  |
| pycparser               | 1.53 sec                                                            | 1.15 sec: 1.33x faster                                 |
| html5lib                | 86.4 ms                                                             | 65.0 ms: 1.33x faster                                  |
| django_template         | 45.8 ms                                                             | 34.7 ms: 1.32x faster                                  |
| async_tree_memoization  | 853 ms                                                              | 646 ms: 1.32x faster                                   |
| chameleon               | 9.13 ms                                                             | 6.93 ms: 1.32x faster                                  |
| logging_format          | 9.07 us                                                             | 6.91 us: 1.31x faster                                  |
| thrift                  | 1.04 ms                                                             | 796 us: 1.30x faster                                   |
| pprint_safe_repr        | 953 ms                                                              | 737 ms: 1.29x faster                                   |
| xml_etree_process       | 74.8 ms                                                             | 58.6 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed | 944 ms                                                              | 742 ms: 1.27x faster                                   |
| genshi_xml              | 64.3 ms                                                             | 50.7 ms: 1.27x faster                                  |
| fannkuch                | 485 ms                                                              | 383 ms: 1.27x faster                                   |
| 2to3                    | 336 ms                                                              | 268 ms: 1.25x faster                                   |
| tornado_http            | 129 ms                                                              | 104 ms: 1.24x faster                                   |
| regex_compile           | 177 ms                                                              | 144 ms: 1.23x faster                                   |
| deepcopy                | 438 us                                                              | 360 us: 1.22x faster                                   |
| nqueens                 | 98.8 ms                                                             | 81.2 ms: 1.22x faster                                  |
| sqlglot_normalize       | 135 ms                                                              | 111 ms: 1.21x faster                                   |
| scimark_fft             | 425 ms                                                              | 353 ms: 1.20x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                             | 54.5 ms: 1.20x faster                                  |
| mypy2                   | 432 ms                                                              | 360 ms: 1.20x faster                                   |
| deepcopy_reduce         | 3.80 us                                                             | 3.18 us: 1.19x faster                                  |
| docutils                | 3.19 sec                                                            | 2.70 sec: 1.18x faster                                 |
| json_loads              | 29.3 us                                                             | 24.8 us: 1.18x faster                                  |
| comprehensions          | 27.3 us                                                             | 23.3 us: 1.17x faster                                  |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.86 ms: 1.16x faster                                  |
| bench_thread_pool       | 954 us                                                              | 836 us: 1.14x faster                                   |
| xml_etree_generate      | 94.9 ms                                                             | 83.2 ms: 1.14x faster                                  |
| json                    | 5.41 ms                                                             | 4.75 ms: 1.14x faster                                  |
| sqlalchemy_declarative  | 166 ms                                                              | 147 ms: 1.13x faster                                   |
| dulwich_log             | 76.3 ms                                                             | 67.8 ms: 1.13x faster                                  |
| regex_v8                | 24.9 ms                                                             | 22.3 ms: 1.12x faster                                  |
| pathlib                 | 19.8 ms                                                             | 17.7 ms: 1.12x faster                                  |
| pylint                  | 521 ms                                                              | 466 ms: 1.12x faster                                   |
| sqlite_synth            | 2.97 us                                                             | 2.66 us: 1.12x faster                                  |
| sympy_integrate         | 24.3 ms                                                             | 21.9 ms: 1.11x faster                                  |
| sqlalchemy_imperative   | 21.2 ms                                                             | 19.2 ms: 1.10x faster                                  |
| create_gc_cycles        | 1.64 ms                                                             | 1.50 ms: 1.10x faster                                  |
| sympy_expand            | 540 ms                                                              | 496 ms: 1.09x faster                                   |
| djangocms               | 36.3 us                                                             | 33.6 us: 1.08x faster                                  |
| xml_etree_iterparse     | 111 ms                                                              | 103 ms: 1.08x faster                                   |
| pickle_list             | 4.73 us                                                             | 4.39 us: 1.08x faster                                  |
| xml_etree_parse         | 164 ms                                                              | 152 ms: 1.08x faster                                   |
| mdp                     | 2.75 sec                                                            | 2.59 sec: 1.06x faster                                 |
| sympy_str               | 328 ms                                                              | 311 ms: 1.05x faster                                   |
| regex_dna               | 213 ms                                                              | 205 ms: 1.04x faster                                   |
| meteor_contest          | 115 ms                                                              | 111 ms: 1.03x faster                                   |
| sympy_sum               | 185 ms                                                              | 181 ms: 1.02x faster                                   |
| pidigits                | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| regex_effbot            | 3.22 ms                                                             | 3.26 ms: 1.01x slower                                  |
| telco                   | 6.67 ms                                                             | 6.83 ms: 1.02x slower                                  |
| pickle                  | 10.2 us                                                             | 10.5 us: 1.03x slower                                  |
| unpickle_list           | 4.94 us                                                             | 5.24 us: 1.06x slower                                  |
| async_generators        | 420 ms                                                              | 445 ms: 1.06x slower                                   |
| pickle_dict             | 27.8 us                                                             | 30.7 us: 1.11x slower                                  |
| gc_traversal            | 3.53 ms                                                             | 3.93 ms: 1.11x slower                                  |
| python_startup_no_site  | 5.80 ms                                                             | 6.65 ms: 1.15x slower                                  |
| dask                    | 437 ms                                                              | 539 ms: 1.23x slower                                   |
| coverage                | 70.6 ms                                                             | 101 ms: 1.43x slower                                   |
| Geometric mean          | (ref)                                                               | 1.24x faster                                           |

Benchmark hidden because not significant (2): unpickle, bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn
