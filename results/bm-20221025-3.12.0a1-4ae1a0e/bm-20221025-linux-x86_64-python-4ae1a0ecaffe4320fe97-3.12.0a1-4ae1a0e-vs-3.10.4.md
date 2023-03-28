
# Results vs. 3.10.4

- fork: python
- ref: 4ae1a0ecaffe4320fe97
- machine: linux-x86_64
- commit hash: 4ae1a0e
- commit date: 2022-10-25
- overall geometric mean: 1.30x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 249 ms: 1.35x faster                                                  |
| chameleon      | 9.13 ms                                                             | 6.51 ms: 1.40x faster                                                 |
| docutils       | 3.19 sec                                                            | 2.52 sec: 1.27x faster                                                |
| html5lib       | 86.4 ms                                                             | 59.9 ms: 1.44x faster                                                 |
| tornado_http   | 129 ms                                                              | 93.7 ms: 1.38x faster                                                 |
| Geometric mean | (ref)                                                               | 1.37x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 110 ms                                                              | 71.4 ms: 1.54x faster                                                 |
| nbody          | 146 ms                                                              | 96.6 ms: 1.51x faster                                                 |
| pidigits       | 190 ms                                                              | 198 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                               | 1.31x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 127 ms: 1.39x faster                                                  |
| regex_v8       | 24.9 ms                                                             | 21.4 ms: 1.17x faster                                                 |
| regex_dna      | 213 ms                                                              | 201 ms: 1.06x faster                                                  |
| regex_effbot   | 3.22 ms                                                             | 3.37 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                               | 1.13x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 285 us: 1.60x faster                                                  |
| unpickle_pure_python | 300 us                                                              | 202 us: 1.48x faster                                                  |
| json_dumps           | 13.7 ms                                                             | 9.36 ms: 1.46x faster                                                 |
| xml_etree_process    | 74.8 ms                                                             | 53.4 ms: 1.40x faster                                                 |
| json_loads           | 29.3 us                                                             | 23.5 us: 1.25x faster                                                 |
| xml_etree_generate   | 94.9 ms                                                             | 76.0 ms: 1.25x faster                                                 |
| unpickle             | 15.0 us                                                             | 13.2 us: 1.13x faster                                                 |
| pickle_list          | 4.73 us                                                             | 4.19 us: 1.13x faster                                                 |
| xml_etree_parse      | 164 ms                                                              | 145 ms: 1.13x faster                                                  |
| xml_etree_iterparse  | 111 ms                                                              | 101 ms: 1.11x faster                                                  |
| pickle               | 10.2 us                                                             | 10.1 us: 1.01x faster                                                 |
| unpickle_list        | 4.94 us                                                             | 4.91 us: 1.01x faster                                                 |
| pickle_dict          | 27.8 us                                                             | 31.1 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.20x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.42 ms: 1.68x faster                                                 |
| python_startup_no_site | 5.80 ms                                                             | 5.93 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.28x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.64 ms: 1.53x faster                                                 |
| genshi_text     | 30.4 ms                                                             | 21.5 ms: 1.42x faster                                                 |
| django_template | 45.8 ms                                                             | 33.0 ms: 1.39x faster                                                 |
| genshi_xml      | 64.3 ms                                                             | 50.0 ms: 1.29x faster                                                 |
| Geometric mean  | (ref)                                                               | 1.40x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 7.30 ms                                                             | 3.30 ms: 2.21x faster                                                 |
| scimark_sor             | 198 ms                                                              | 106 ms: 1.87x faster                                                  |
| logging_silent          | 169 ns                                                              | 91.6 ns: 1.84x faster                                                 |
| richards                | 74.2 ms                                                             | 42.4 ms: 1.75x faster                                                 |
| python_startup          | 14.1 ms                                                             | 8.42 ms: 1.68x faster                                                 |
| go                      | 226 ms                                                              | 135 ms: 1.67x faster                                                  |
| raytrace                | 470 ms                                                              | 282 ms: 1.66x faster                                                  |
| pyflate                 | 671 ms                                                              | 407 ms: 1.65x faster                                                  |
| scimark_monte_carlo     | 109 ms                                                              | 66.6 ms: 1.63x faster                                                 |
| pickle_pure_python      | 457 us                                                              | 285 us: 1.60x faster                                                  |
| chaos                   | 106 ms                                                              | 67.1 ms: 1.58x faster                                                 |
| spectral_norm           | 150 ms                                                              | 95.2 ms: 1.58x faster                                                 |
| crypto_pyaes            | 117 ms                                                              | 74.8 ms: 1.56x faster                                                 |
| hexiom                  | 9.50 ms                                                             | 6.11 ms: 1.56x faster                                                 |
| sqlglot_parse           | 2.07 ms                                                             | 1.34 ms: 1.54x faster                                                 |
| float                   | 110 ms                                                              | 71.4 ms: 1.54x faster                                                 |
| mako                    | 14.7 ms                                                             | 9.64 ms: 1.53x faster                                                 |
| nbody                   | 146 ms                                                              | 96.6 ms: 1.51x faster                                                 |
| deepcopy_memo           | 51.8 us                                                             | 34.4 us: 1.51x faster                                                 |
| sqlglot_transpile       | 2.45 ms                                                             | 1.63 ms: 1.50x faster                                                 |
| unpack_sequence         | 65.6 ns                                                             | 44.1 ns: 1.49x faster                                                 |
| unpickle_pure_python    | 300 us                                                              | 202 us: 1.48x faster                                                  |
| scimark_lu              | 160 ms                                                              | 108 ms: 1.48x faster                                                  |
| json_dumps              | 13.7 ms                                                             | 9.36 ms: 1.46x faster                                                 |
| html5lib                | 86.4 ms                                                             | 59.9 ms: 1.44x faster                                                 |
| pprint_pformat          | 1.98 sec                                                            | 1.38 sec: 1.44x faster                                                |
| pprint_safe_repr        | 953 ms                                                              | 665 ms: 1.43x faster                                                  |
| logging_format          | 9.07 us                                                             | 6.38 us: 1.42x faster                                                 |
| genshi_text             | 30.4 ms                                                             | 21.5 ms: 1.42x faster                                                 |
| logging_simple          | 8.21 us                                                             | 5.80 us: 1.42x faster                                                 |
| chameleon               | 9.13 ms                                                             | 6.51 ms: 1.40x faster                                                 |
| xml_etree_process       | 74.8 ms                                                             | 53.4 ms: 1.40x faster                                                 |
| regex_compile           | 177 ms                                                              | 127 ms: 1.39x faster                                                  |
| thrift                  | 1.04 ms                                                             | 746 us: 1.39x faster                                                  |
| django_template         | 45.8 ms                                                             | 33.0 ms: 1.39x faster                                                 |
| tornado_http            | 129 ms                                                              | 93.7 ms: 1.38x faster                                                 |
| pycparser               | 1.53 sec                                                            | 1.12 sec: 1.37x faster                                                |
| scimark_fft             | 425 ms                                                              | 312 ms: 1.36x faster                                                  |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.13 ms: 1.36x faster                                                 |
| async_tree_none         | 713 ms                                                              | 529 ms: 1.35x faster                                                  |
| 2to3                    | 336 ms                                                              | 249 ms: 1.35x faster                                                  |
| aiohttp                 | 1.35 ms                                                             | 1.00 ms: 1.34x faster                                                 |
| async_tree_io           | 1.78 sec                                                            | 1.33 sec: 1.34x faster                                                |
| gunicorn                | 1.43 ms                                                             | 1.07 ms: 1.34x faster                                                 |
| deepcopy                | 438 us                                                              | 333 us: 1.32x faster                                                  |
| mypy2                   | 432 ms                                                              | 328 ms: 1.31x faster                                                  |
| fannkuch                | 485 ms                                                              | 370 ms: 1.31x faster                                                  |
| deepcopy_reduce         | 3.80 us                                                             | 2.91 us: 1.31x faster                                                 |
| async_tree_memoization  | 853 ms                                                              | 656 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed | 944 ms                                                              | 730 ms: 1.29x faster                                                  |
| coroutines              | 31.8 ms                                                             | 24.7 ms: 1.29x faster                                                 |
| sqlglot_normalize       | 135 ms                                                              | 104 ms: 1.29x faster                                                  |
| genshi_xml              | 64.3 ms                                                             | 50.0 ms: 1.29x faster                                                 |
| comprehensions          | 27.3 us                                                             | 21.3 us: 1.28x faster                                                 |
| sqlglot_optimize        | 65.3 ms                                                             | 51.2 ms: 1.27x faster                                                 |
| docutils                | 3.19 sec                                                            | 2.52 sec: 1.27x faster                                                |
| json_loads              | 29.3 us                                                             | 23.5 us: 1.25x faster                                                 |
| xml_etree_generate      | 94.9 ms                                                             | 76.0 ms: 1.25x faster                                                 |
| nqueens                 | 98.8 ms                                                             | 80.7 ms: 1.23x faster                                                 |
| dulwich_log             | 76.3 ms                                                             | 62.4 ms: 1.22x faster                                                 |
| bench_thread_pool       | 954 us                                                              | 780 us: 1.22x faster                                                  |
| dask                    | 437 ms                                                              | 360 ms: 1.21x faster                                                  |
| async_generators        | 420 ms                                                              | 349 ms: 1.20x faster                                                  |
| json                    | 5.41 ms                                                             | 4.55 ms: 1.19x faster                                                 |
| sympy_integrate         | 24.3 ms                                                             | 20.4 ms: 1.19x faster                                                 |
| sympy_expand            | 540 ms                                                              | 455 ms: 1.19x faster                                                  |
| regex_v8                | 24.9 ms                                                             | 21.4 ms: 1.17x faster                                                 |
| sympy_str               | 328 ms                                                              | 283 ms: 1.16x faster                                                  |
| pylint                  | 521 ms                                                              | 458 ms: 1.14x faster                                                  |
| unpickle                | 15.0 us                                                             | 13.2 us: 1.13x faster                                                 |
| sqlite_synth            | 2.97 us                                                             | 2.62 us: 1.13x faster                                                 |
| sympy_sum               | 185 ms                                                              | 164 ms: 1.13x faster                                                  |
| pickle_list             | 4.73 us                                                             | 4.19 us: 1.13x faster                                                 |
| create_gc_cycles        | 1.64 ms                                                             | 1.46 ms: 1.13x faster                                                 |
| xml_etree_parse         | 164 ms                                                              | 145 ms: 1.13x faster                                                  |
| djangocms               | 36.3 us                                                             | 32.5 us: 1.12x faster                                                 |
| mdp                     | 2.75 sec                                                            | 2.48 sec: 1.11x faster                                                |
| xml_etree_iterparse     | 111 ms                                                              | 101 ms: 1.11x faster                                                  |
| pathlib                 | 19.8 ms                                                             | 17.9 ms: 1.10x faster                                                 |
| meteor_contest          | 115 ms                                                              | 104 ms: 1.10x faster                                                  |
| regex_dna               | 213 ms                                                              | 201 ms: 1.06x faster                                                  |
| asyncio_tcp             | 922 ms                                                              | 890 ms: 1.04x faster                                                  |
| generators              | 75.7 ms                                                             | 74.1 ms: 1.02x faster                                                 |
| telco                   | 6.67 ms                                                             | 6.55 ms: 1.02x faster                                                 |
| pickle                  | 10.2 us                                                             | 10.1 us: 1.01x faster                                                 |
| unpickle_list           | 4.94 us                                                             | 4.91 us: 1.01x faster                                                 |
| bench_mp_pool           | 24.0 ms                                                             | 24.0 ms: 1.00x slower                                                 |
| gc_traversal            | 3.53 ms                                                             | 3.55 ms: 1.01x slower                                                 |
| python_startup_no_site  | 5.80 ms                                                             | 5.93 ms: 1.02x slower                                                 |
| pidigits                | 190 ms                                                              | 198 ms: 1.04x slower                                                  |
| regex_effbot            | 3.22 ms                                                             | 3.37 ms: 1.05x slower                                                 |
| pickle_dict             | 27.8 us                                                             | 31.1 us: 1.12x slower                                                 |
| coverage                | 70.6 ms                                                             | 102 ms: 1.44x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.30x faster                                                          |
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
