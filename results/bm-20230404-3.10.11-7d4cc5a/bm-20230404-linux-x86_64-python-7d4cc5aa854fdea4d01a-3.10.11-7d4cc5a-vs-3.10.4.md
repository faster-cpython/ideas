
# Results vs. 3.10.4

- fork: python
- ref: 7d4cc5aa854fdea4d01a
- machine: linux-x86_64
- commit hash: 7d4cc5a
- commit date: 2023-04-04
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 335 ms: 1.00x faster                                                 |
| chameleon      | 9.13 ms                                                             | 8.93 ms: 1.02x faster                                                |
| docutils       | 3.19 sec                                                            | 3.21 sec: 1.00x slower                                               |
| tornado_http   | 129 ms                                                              | 131 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                               | 1.00x faster                                                         |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 137 ms: 1.06x faster                                                 |
| float          | 110 ms                                                              | 108 ms: 1.02x faster                                                 |
| pidigits       | 190 ms                                                              | 188 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                               | 1.03x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 176 ms: 1.01x faster                                                 |
| regex_v8       | 24.9 ms                                                             | 25.5 ms: 1.02x slower                                                |
| regex_effbot   | 3.22 ms                                                             | 3.63 ms: 1.13x slower                                                |
| Geometric mean | (ref)                                                               | 1.03x slower                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 4.73 us                                                             | 4.38 us: 1.08x faster                                                |
| unpickle             | 15.0 us                                                             | 14.3 us: 1.05x faster                                                |
| unpickle_list        | 4.94 us                                                             | 4.80 us: 1.03x faster                                                |
| xml_etree_generate   | 94.9 ms                                                             | 93.1 ms: 1.02x faster                                                |
| pickle_pure_python   | 457 us                                                              | 452 us: 1.01x faster                                                 |
| json_loads           | 29.3 us                                                             | 29.0 us: 1.01x faster                                                |
| xml_etree_process    | 74.8 ms                                                             | 74.1 ms: 1.01x faster                                                |
| xml_etree_iterparse  | 111 ms                                                              | 110 ms: 1.01x faster                                                 |
| unpickle_pure_python | 300 us                                                              | 298 us: 1.01x faster                                                 |
| pickle               | 10.2 us                                                             | 10.4 us: 1.02x slower                                                |
| pickle_dict          | 27.8 us                                                             | 33.7 us: 1.21x slower                                                |
| Geometric mean       | (ref)                                                               | 1.00x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|------------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 14.2 ms: 1.01x slower                                                |
| python_startup_no_site | 5.80 ms                                                             | 5.83 ms: 1.01x slower                                                |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml     | 64.3 ms                                                             | 62.6 ms: 1.03x faster                                                |
| genshi_text    | 30.4 ms                                                             | 30.1 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                               | 1.01x faster                                                         |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-linux-x86_64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-------------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list             | 4.73 us                                                             | 4.38 us: 1.08x faster                                                |
| nbody                   | 146 ms                                                              | 137 ms: 1.06x faster                                                 |
| spectral_norm           | 150 ms                                                              | 142 ms: 1.05x faster                                                 |
| aiohttp                 | 1.35 ms                                                             | 1.29 ms: 1.05x faster                                                |
| unpickle                | 15.0 us                                                             | 14.3 us: 1.05x faster                                                |
| deepcopy_memo           | 51.8 us                                                             | 49.8 us: 1.04x faster                                                |
| dask                    | 437 ms                                                              | 421 ms: 1.04x faster                                                 |
| bench_thread_pool       | 954 us                                                              | 925 us: 1.03x faster                                                 |
| gunicorn                | 1.43 ms                                                             | 1.39 ms: 1.03x faster                                                |
| asyncio_tcp             | 922 ms                                                              | 894 ms: 1.03x faster                                                 |
| fannkuch                | 485 ms                                                              | 471 ms: 1.03x faster                                                 |
| unpickle_list           | 4.94 us                                                             | 4.80 us: 1.03x faster                                                |
| genshi_xml              | 64.3 ms                                                             | 62.6 ms: 1.03x faster                                                |
| coroutines              | 31.8 ms                                                             | 31.0 ms: 1.03x faster                                                |
| crypto_pyaes            | 117 ms                                                              | 114 ms: 1.02x faster                                                 |
| chameleon               | 9.13 ms                                                             | 8.93 ms: 1.02x faster                                                |
| scimark_fft             | 425 ms                                                              | 416 ms: 1.02x faster                                                 |
| deepcopy                | 438 us                                                              | 429 us: 1.02x faster                                                 |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 5.50 ms: 1.02x faster                                                |
| scimark_sor             | 198 ms                                                              | 194 ms: 1.02x faster                                                 |
| xml_etree_generate      | 94.9 ms                                                             | 93.1 ms: 1.02x faster                                                |
| float                   | 110 ms                                                              | 108 ms: 1.02x faster                                                 |
| json                    | 5.41 ms                                                             | 5.32 ms: 1.02x faster                                                |
| raytrace                | 470 ms                                                              | 462 ms: 1.02x faster                                                 |
| pyflate                 | 671 ms                                                              | 660 ms: 1.02x faster                                                 |
| richards                | 74.2 ms                                                             | 73.1 ms: 1.01x faster                                                |
| meteor_contest          | 115 ms                                                              | 113 ms: 1.01x faster                                                 |
| chaos                   | 106 ms                                                              | 105 ms: 1.01x faster                                                 |
| genshi_text             | 30.4 ms                                                             | 30.1 ms: 1.01x faster                                                |
| sqlglot_parse           | 2.07 ms                                                             | 2.04 ms: 1.01x faster                                                |
| dulwich_log             | 76.3 ms                                                             | 75.5 ms: 1.01x faster                                                |
| pickle_pure_python      | 457 us                                                              | 452 us: 1.01x faster                                                 |
| json_loads              | 29.3 us                                                             | 29.0 us: 1.01x faster                                                |
| hexiom                  | 9.50 ms                                                             | 9.41 ms: 1.01x faster                                                |
| nqueens                 | 98.8 ms                                                             | 97.9 ms: 1.01x faster                                                |
| xml_etree_process       | 74.8 ms                                                             | 74.1 ms: 1.01x faster                                                |
| comprehensions          | 27.3 us                                                             | 27.0 us: 1.01x faster                                                |
| xml_etree_iterparse     | 111 ms                                                              | 110 ms: 1.01x faster                                                 |
| deepcopy_reduce         | 3.80 us                                                             | 3.77 us: 1.01x faster                                                |
| sqlglot_transpile       | 2.45 ms                                                             | 2.44 ms: 1.01x faster                                                |
| regex_compile           | 177 ms                                                              | 176 ms: 1.01x faster                                                 |
| pidigits                | 190 ms                                                              | 188 ms: 1.01x faster                                                 |
| unpickle_pure_python    | 300 us                                                              | 298 us: 1.01x faster                                                 |
| mypy2                   | 432 ms                                                              | 429 ms: 1.01x faster                                                 |
| pprint_pformat          | 1.98 sec                                                            | 1.97 sec: 1.00x faster                                               |
| generators              | 75.7 ms                                                             | 75.5 ms: 1.00x faster                                                |
| 2to3                    | 336 ms                                                              | 335 ms: 1.00x faster                                                 |
| sqlglot_optimize        | 65.3 ms                                                             | 65.5 ms: 1.00x slower                                                |
| docutils                | 3.19 sec                                                            | 3.21 sec: 1.00x slower                                               |
| thrift                  | 1.04 ms                                                             | 1.04 ms: 1.00x slower                                                |
| sympy_str               | 328 ms                                                              | 330 ms: 1.01x slower                                                 |
| python_startup          | 14.1 ms                                                             | 14.2 ms: 1.01x slower                                                |
| python_startup_no_site  | 5.80 ms                                                             | 5.83 ms: 1.01x slower                                                |
| go                      | 226 ms                                                              | 227 ms: 1.01x slower                                                 |
| sympy_expand            | 540 ms                                                              | 545 ms: 1.01x slower                                                 |
| sqlglot_normalize       | 135 ms                                                              | 136 ms: 1.01x slower                                                 |
| sqlalchemy_declarative  | 166 ms                                                              | 168 ms: 1.01x slower                                                 |
| logging_format          | 9.07 us                                                             | 9.16 us: 1.01x slower                                                |
| pylint                  | 521 ms                                                              | 526 ms: 1.01x slower                                                 |
| tornado_http            | 129 ms                                                              | 131 ms: 1.01x slower                                                 |
| create_gc_cycles        | 1.64 ms                                                             | 1.66 ms: 1.01x slower                                                |
| pickle                  | 10.2 us                                                             | 10.4 us: 1.02x slower                                                |
| telco                   | 6.67 ms                                                             | 6.78 ms: 1.02x slower                                                |
| sqlite_synth            | 2.97 us                                                             | 3.02 us: 1.02x slower                                                |
| sympy_sum               | 185 ms                                                              | 188 ms: 1.02x slower                                                 |
| async_tree_io           | 1.78 sec                                                            | 1.82 sec: 1.02x slower                                               |
| coverage                | 70.6 ms                                                             | 72.1 ms: 1.02x slower                                                |
| regex_v8                | 24.9 ms                                                             | 25.5 ms: 1.02x slower                                                |
| logging_simple          | 8.21 us                                                             | 8.40 us: 1.02x slower                                                |
| async_tree_memoization  | 853 ms                                                              | 873 ms: 1.02x slower                                                 |
| async_tree_none         | 713 ms                                                              | 732 ms: 1.03x slower                                                 |
| unpack_sequence         | 65.6 ns                                                             | 67.6 ns: 1.03x slower                                                |
| async_tree_cpu_io_mixed | 944 ms                                                              | 975 ms: 1.03x slower                                                 |
| logging_silent          | 169 ns                                                              | 175 ns: 1.03x slower                                                 |
| mdp                     | 2.75 sec                                                            | 2.85 sec: 1.04x slower                                               |
| gc_traversal            | 3.53 ms                                                             | 3.71 ms: 1.05x slower                                                |
| regex_effbot            | 3.22 ms                                                             | 3.63 ms: 1.13x slower                                                |
| pickle_dict             | 27.8 us                                                             | 33.7 us: 1.21x slower                                                |
| Geometric mean          | (ref)                                                               | 1.00x faster                                                         |

Benchmark hidden because not significant (18): html5lib, scimark_lu, sqlalchemy_imperative, xml_etree_parse, pycparser, json_dumps, django_template, sympy_integrate, mako, pprint_safe_repr, bench_mp_pool, regex_dna, async_generators, pathlib, scimark_monte_carlo, flaskblogging, deltablue, djangocms
