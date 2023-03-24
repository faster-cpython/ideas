
# Results vs. 3.10.4

- fork: python
- ref: e2b4e4bab90b69fbd361
- machine: linux-x86_64
- commit hash: e2b4e4b
- commit date: 2021-11-05
- overall geometric mean: 1.12x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 299 ms: 1.12x faster                                                        |
| chameleon      | 9.13 ms                                                             | 9.27 ms: 1.02x slower                                                       |
| docutils       | 3.19 sec                                                            | 3.05 sec: 1.05x faster                                                      |
| html5lib       | 86.4 ms                                                             | 80.0 ms: 1.08x faster                                                       |
| tornado_http   | 129 ms                                                              | 136 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                               | 1.04x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 113 ms: 1.29x faster                                                        |
| float          | 110 ms                                                              | 86.1 ms: 1.28x faster                                                       |
| pidigits       | 190 ms                                                              | 264 ms: 1.39x slower                                                        |
| Geometric mean | (ref)                                                               | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 158 ms: 1.12x faster                                                        |
| regex_effbot   | 3.22 ms                                                             | 3.06 ms: 1.05x faster                                                       |
| regex_v8       | 24.9 ms                                                             | 25.8 ms: 1.03x slower                                                       |
| regex_dna      | 213 ms                                                              | 262 ms: 1.23x slower                                                        |
| Geometric mean | (ref)                                                               | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_process    | 74.8 ms                                                             | 61.7 ms: 1.21x faster                                                       |
| json_loads           | 29.3 us                                                             | 24.7 us: 1.19x faster                                                       |
| pickle_pure_python   | 457 us                                                              | 386 us: 1.18x faster                                                        |
| pickle_list          | 4.73 us                                                             | 4.17 us: 1.13x faster                                                       |
| unpickle             | 15.0 us                                                             | 13.4 us: 1.12x faster                                                       |
| xml_etree_generate   | 94.9 ms                                                             | 85.8 ms: 1.11x faster                                                       |
| unpickle_list        | 4.94 us                                                             | 4.55 us: 1.09x faster                                                       |
| unpickle_pure_python | 300 us                                                              | 277 us: 1.08x faster                                                        |
| xml_etree_parse      | 164 ms                                                              | 157 ms: 1.04x faster                                                        |
| xml_etree_iterparse  | 111 ms                                                              | 107 ms: 1.04x faster                                                        |
| json_dumps           | 13.7 ms                                                             | 13.4 ms: 1.02x faster                                                       |
| pickle_dict          | 27.8 us                                                             | 30.2 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                               | 1.08x faster                                                                |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 11.2 ms: 1.27x faster                                                       |
| python_startup_no_site | 5.80 ms                                                             | 7.43 ms: 1.28x slower                                                       |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 12.9 ms: 1.14x faster                                                       |
| genshi_xml      | 64.3 ms                                                             | 57.9 ms: 1.11x faster                                                       |
| genshi_text     | 30.4 ms                                                             | 28.2 ms: 1.08x faster                                                       |
| django_template | 45.8 ms                                                             | 47.4 ms: 1.03x slower                                                       |
| Geometric mean  | (ref)                                                               | 1.07x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf2-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| bench_mp_pool           | 24.0 ms                                                             | 5.01 ms: 4.79x faster                                                       |
| flaskblogging           | 8.48 ms                                                             | 4.84 ms: 1.75x faster                                                       |
| gunicorn                | 1.43 ms                                                             | 980 us: 1.46x faster                                                        |
| spectral_norm           | 150 ms                                                              | 104 ms: 1.44x faster                                                        |
| deltablue               | 7.30 ms                                                             | 5.07 ms: 1.44x faster                                                       |
| generators              | 75.7 ms                                                             | 52.7 ms: 1.44x faster                                                       |
| unpack_sequence         | 65.6 ns                                                             | 46.0 ns: 1.43x faster                                                       |
| scimark_sor             | 198 ms                                                              | 140 ms: 1.41x faster                                                        |
| async_tree_io           | 1.78 sec                                                            | 1.27 sec: 1.41x faster                                                      |
| logging_silent          | 169 ns                                                              | 121 ns: 1.40x faster                                                        |
| scimark_fft             | 425 ms                                                              | 311 ms: 1.37x faster                                                        |
| scimark_monte_carlo     | 109 ms                                                              | 79.5 ms: 1.37x faster                                                       |
| raytrace                | 470 ms                                                              | 349 ms: 1.35x faster                                                        |
| async_tree_none         | 713 ms                                                              | 532 ms: 1.34x faster                                                        |
| chaos                   | 106 ms                                                              | 79.2 ms: 1.34x faster                                                       |
| async_generators        | 420 ms                                                              | 325 ms: 1.29x faster                                                        |
| nbody                   | 146 ms                                                              | 113 ms: 1.29x faster                                                        |
| async_tree_memoization  | 853 ms                                                              | 668 ms: 1.28x faster                                                        |
| float                   | 110 ms                                                              | 86.1 ms: 1.28x faster                                                       |
| python_startup          | 14.1 ms                                                             | 11.2 ms: 1.27x faster                                                       |
| richards                | 74.2 ms                                                             | 59.0 ms: 1.26x faster                                                       |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.56 ms: 1.23x faster                                                       |
| crypto_pyaes            | 117 ms                                                              | 94.9 ms: 1.23x faster                                                       |
| xml_etree_process       | 74.8 ms                                                             | 61.7 ms: 1.21x faster                                                       |
| scimark_lu              | 160 ms                                                              | 132 ms: 1.21x faster                                                        |
| hexiom                  | 9.50 ms                                                             | 7.87 ms: 1.21x faster                                                       |
| deepcopy_memo           | 51.8 us                                                             | 42.9 us: 1.21x faster                                                       |
| json_loads              | 29.3 us                                                             | 24.7 us: 1.19x faster                                                       |
| pickle_pure_python      | 457 us                                                              | 386 us: 1.18x faster                                                        |
| go                      | 226 ms                                                              | 194 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed | 944 ms                                                              | 818 ms: 1.15x faster                                                        |
| pyflate                 | 671 ms                                                              | 582 ms: 1.15x faster                                                        |
| mako                    | 14.7 ms                                                             | 12.9 ms: 1.14x faster                                                       |
| pickle_list             | 4.73 us                                                             | 4.17 us: 1.13x faster                                                       |
| 2to3                    | 336 ms                                                              | 299 ms: 1.12x faster                                                        |
| logging_format          | 9.07 us                                                             | 8.08 us: 1.12x faster                                                       |
| regex_compile           | 177 ms                                                              | 158 ms: 1.12x faster                                                        |
| unpickle                | 15.0 us                                                             | 13.4 us: 1.12x faster                                                       |
| logging_simple          | 8.21 us                                                             | 7.35 us: 1.12x faster                                                       |
| genshi_xml              | 64.3 ms                                                             | 57.9 ms: 1.11x faster                                                       |
| xml_etree_generate      | 94.9 ms                                                             | 85.8 ms: 1.11x faster                                                       |
| unpickle_list           | 4.94 us                                                             | 4.55 us: 1.09x faster                                                       |
| pprint_safe_repr        | 953 ms                                                              | 877 ms: 1.09x faster                                                        |
| pprint_pformat          | 1.98 sec                                                            | 1.82 sec: 1.09x faster                                                      |
| unpickle_pure_python    | 300 us                                                              | 277 us: 1.08x faster                                                        |
| sqlite_synth            | 2.97 us                                                             | 2.75 us: 1.08x faster                                                       |
| genshi_text             | 30.4 ms                                                             | 28.2 ms: 1.08x faster                                                       |
| html5lib                | 86.4 ms                                                             | 80.0 ms: 1.08x faster                                                       |
| thrift                  | 1.04 ms                                                             | 961 us: 1.08x faster                                                        |
| coroutines              | 31.8 ms                                                             | 29.5 ms: 1.08x faster                                                       |
| fannkuch                | 485 ms                                                              | 458 ms: 1.06x faster                                                        |
| dulwich_log             | 76.3 ms                                                             | 72.4 ms: 1.05x faster                                                       |
| regex_effbot            | 3.22 ms                                                             | 3.06 ms: 1.05x faster                                                       |
| docutils                | 3.19 sec                                                            | 3.05 sec: 1.05x faster                                                      |
| json                    | 5.41 ms                                                             | 5.19 ms: 1.04x faster                                                       |
| xml_etree_parse         | 164 ms                                                              | 157 ms: 1.04x faster                                                        |
| xml_etree_iterparse     | 111 ms                                                              | 107 ms: 1.04x faster                                                        |
| pycparser               | 1.53 sec                                                            | 1.48 sec: 1.03x faster                                                      |
| coverage                | 70.6 ms                                                             | 68.7 ms: 1.03x faster                                                       |
| deepcopy                | 438 us                                                              | 428 us: 1.02x faster                                                        |
| json_dumps              | 13.7 ms                                                             | 13.4 ms: 1.02x faster                                                       |
| sqlglot_normalize       | 135 ms                                                              | 132 ms: 1.02x faster                                                        |
| sympy_sum               | 185 ms                                                              | 183 ms: 1.01x faster                                                        |
| sqlglot_optimize        | 65.3 ms                                                             | 64.9 ms: 1.01x faster                                                       |
| pathlib                 | 19.8 ms                                                             | 20.0 ms: 1.01x slower                                                       |
| chameleon               | 9.13 ms                                                             | 9.27 ms: 1.02x slower                                                       |
| create_gc_cycles        | 1.64 ms                                                             | 1.67 ms: 1.02x slower                                                       |
| dask                    | 437 ms                                                              | 445 ms: 1.02x slower                                                        |
| telco                   | 6.67 ms                                                             | 6.81 ms: 1.02x slower                                                       |
| nqueens                 | 98.8 ms                                                             | 102 ms: 1.03x slower                                                        |
| django_template         | 45.8 ms                                                             | 47.4 ms: 1.03x slower                                                       |
| regex_v8                | 24.9 ms                                                             | 25.8 ms: 1.03x slower                                                       |
| sympy_str               | 328 ms                                                              | 340 ms: 1.04x slower                                                        |
| mdp                     | 2.75 sec                                                            | 2.87 sec: 1.04x slower                                                      |
| sympy_expand            | 540 ms                                                              | 563 ms: 1.04x slower                                                        |
| tornado_http            | 129 ms                                                              | 136 ms: 1.05x slower                                                        |
| comprehensions          | 27.3 us                                                             | 28.8 us: 1.06x slower                                                       |
| gc_traversal            | 3.53 ms                                                             | 3.77 ms: 1.07x slower                                                       |
| sqlglot_transpile       | 2.45 ms                                                             | 2.63 ms: 1.07x slower                                                       |
| sqlglot_parse           | 2.07 ms                                                             | 2.24 ms: 1.08x slower                                                       |
| pickle_dict             | 27.8 us                                                             | 30.2 us: 1.09x slower                                                       |
| sympy_integrate         | 24.3 ms                                                             | 26.5 ms: 1.09x slower                                                       |
| bench_thread_pool       | 954 us                                                              | 1.05 ms: 1.10x slower                                                       |
| meteor_contest          | 115 ms                                                              | 128 ms: 1.12x slower                                                        |
| regex_dna               | 213 ms                                                              | 262 ms: 1.23x slower                                                        |
| python_startup_no_site  | 5.80 ms                                                             | 7.43 ms: 1.28x slower                                                       |
| pidigits                | 190 ms                                                              | 264 ms: 1.39x slower                                                        |
| Geometric mean          | (ref)                                                               | 1.12x faster                                                                |

Benchmark hidden because not significant (2): deepcopy_reduce, pickle
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, asyncio_tcp, djangocms, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
