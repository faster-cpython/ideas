Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 332 ms                                                 | 256 ms: 1.30x faster                                  |
| chameleon      | 8.86 ms                                                | 6.59 ms: 1.34x faster                                 |
| html5lib       | 85.8 ms                                                | 63.8 ms: 1.35x faster                                 |
| tornado_http   | 128 ms                                                 | 93.8 ms: 1.37x faster                                 |
| Geometric mean | (ref)                                                  | 1.34x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 108 ms                                                 | 72.8 ms: 1.48x faster                                 |
| nbody          | 136 ms                                                 | 90.9 ms: 1.50x faster                                 |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                  |
| Geometric mean | (ref)                                                  | 1.31x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 136 ms: 1.28x faster                                  |
| regex_dna      | 214 ms                                                 | 196 ms: 1.09x faster                                  |
| regex_effbot   | 3.21 ms                                                | 3.02 ms: 1.06x faster                                 |
| regex_v8       | 25.0 ms                                                | 21.5 ms: 1.16x faster                                 |
| Geometric mean | (ref)                                                  | 1.14x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.6 ms: 1.07x faster                                 |
| json_loads           | 28.9 us                                                | 24.3 us: 1.19x faster                                 |
| pickle               | 10.1 us                                                | 9.61 us: 1.05x faster                                 |
| pickle_dict          | 28.3 us                                                | 25.9 us: 1.09x faster                                 |
| pickle_list          | 4.50 us                                                | 4.30 us: 1.05x faster                                 |
| pickle_pure_python   | 453 us                                                 | 302 us: 1.50x faster                                  |
| unpickle             | 14.3 us                                                | 13.3 us: 1.07x faster                                 |
| unpickle_pure_python | 297 us                                                 | 227 us: 1.30x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 157 ms: 1.04x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 104 ms: 1.06x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 75.8 ms: 1.23x faster                                 |
| xml_etree_process    | 74.5 ms                                                | 53.3 ms: 1.40x faster                                 |
| Geometric mean       | (ref)                                                  | 1.15x faster                                          |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.33 ms: 1.67x faster                                 |
| python_startup_no_site | 5.76 ms                                                | 6.17 ms: 1.07x slower                                 |
| Geometric mean         | (ref)                                                  | 1.25x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.4 ms: 1.43x faster                                 |
| mako            | 14.3 ms                                                | 9.71 ms: 1.47x faster                                 |
| Geometric mean  | (ref)                                                  | 1.45x faster                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 256 ms: 1.30x faster                                  |
| chameleon               | 8.86 ms                                                | 6.59 ms: 1.34x faster                                 |
| chaos                   | 104 ms                                                 | 67.8 ms: 1.53x faster                                 |
| crypto_pyaes            | 118 ms                                                 | 73.8 ms: 1.59x faster                                 |
| deltablue               | 7.39 ms                                                | 3.60 ms: 2.05x faster                                 |
| django_template         | 46.3 ms                                                | 32.4 ms: 1.43x faster                                 |
| dulwich_log             | 75.5 ms                                                | 62.6 ms: 1.21x faster                                 |
| fannkuch                | 477 ms                                                 | 394 ms: 1.21x faster                                  |
| float                   | 108 ms                                                 | 72.8 ms: 1.48x faster                                 |
| go                      | 226 ms                                                 | 136 ms: 1.66x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.32 ms: 1.49x faster                                 |
| html5lib                | 85.8 ms                                                | 63.8 ms: 1.35x faster                                 |
| json                    | 5.35 ms                                                | 4.72 ms: 1.13x faster                                 |
| json_dumps              | 13.5 ms                                                | 12.6 ms: 1.07x faster                                 |
| json_loads              | 28.9 us                                                | 24.3 us: 1.19x faster                                 |
| logging_format          | 8.92 us                                                | 6.42 us: 1.39x faster                                 |
| logging_silent          | 173 ns                                                 | 98.1 ns: 1.76x faster                                 |
| logging_simple          | 8.06 us                                                | 5.82 us: 1.38x faster                                 |
| mako                    | 14.3 ms                                                | 9.71 ms: 1.47x faster                                 |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.09x faster                                  |
| nbody                   | 136 ms                                                 | 90.9 ms: 1.50x faster                                 |
| nqueens                 | 99.3 ms                                                | 82.4 ms: 1.20x faster                                 |
| pathlib                 | 20.0 ms                                                | 18.2 ms: 1.10x faster                                 |
| pickle                  | 10.1 us                                                | 9.61 us: 1.05x faster                                 |
| pickle_dict             | 28.3 us                                                | 25.9 us: 1.09x faster                                 |
| pickle_list             | 4.50 us                                                | 4.30 us: 1.05x faster                                 |
| pickle_pure_python      | 453 us                                                 | 302 us: 1.50x faster                                  |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                  |
| pycparser               | 1.51 sec                                               | 1.10 sec: 1.37x faster                                |
| pyflate                 | 675 ms                                                 | 410 ms: 1.65x faster                                  |
| python_startup          | 13.9 ms                                                | 8.33 ms: 1.67x faster                                 |
| python_startup_no_site  | 5.76 ms                                                | 6.17 ms: 1.07x slower                                 |
| raytrace                | 461 ms                                                 | 291 ms: 1.58x faster                                  |
| regex_compile           | 174 ms                                                 | 136 ms: 1.28x faster                                  |
| regex_dna               | 214 ms                                                 | 196 ms: 1.09x faster                                  |
| regex_effbot            | 3.21 ms                                                | 3.02 ms: 1.06x faster                                 |
| regex_v8                | 25.0 ms                                                | 21.5 ms: 1.16x faster                                 |
| richards                | 71.4 ms                                                | 45.3 ms: 1.57x faster                                 |
| scimark_fft             | 414 ms                                                 | 324 ms: 1.28x faster                                  |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.47x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 66.5 ms: 1.58x faster                                 |
| scimark_sor             | 193 ms                                                 | 115 ms: 1.68x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.79 ms: 1.14x faster                                 |
| spectral_norm           | 148 ms                                                 | 96.3 ms: 1.54x faster                                 |
| sqlite_synth            | 2.90 us                                                | 2.50 us: 1.16x faster                                 |
| sympy_expand            | 537 ms                                                 | 465 ms: 1.16x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 20.5 ms: 1.17x faster                                 |
| sympy_sum               | 183 ms                                                 | 159 ms: 1.15x faster                                  |
| sympy_str               | 324 ms                                                 | 284 ms: 1.14x faster                                  |
| thrift                  | 1.03 ms                                                | 756 us: 1.37x faster                                  |
| tornado_http            | 128 ms                                                 | 93.8 ms: 1.37x faster                                 |
| unpack_sequence         | 59.5 ns                                                | 43.2 ns: 1.38x faster                                 |
| unpickle                | 14.3 us                                                | 13.3 us: 1.07x faster                                 |
| unpickle_pure_python    | 297 us                                                 | 227 us: 1.30x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 157 ms: 1.04x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 104 ms: 1.06x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 75.8 ms: 1.23x faster                                 |
| xml_etree_process       | 74.5 ms                                                | 53.3 ms: 1.40x faster                                 |
| Geometric mean          | (ref)                                                  | 1.29x faster                                          |

Benchmark hidden because not significant (2): telco, unpickle_list
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
