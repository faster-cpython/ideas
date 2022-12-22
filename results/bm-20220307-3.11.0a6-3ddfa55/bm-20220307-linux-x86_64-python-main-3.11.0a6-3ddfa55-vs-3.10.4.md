Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 332 ms                                                 | 268 ms: 1.24x faster                                  |
| chameleon      | 8.86 ms                                                | 6.93 ms: 1.28x faster                                 |
| html5lib       | 85.8 ms                                                | 68.6 ms: 1.25x faster                                 |
| tornado_http   | 128 ms                                                 | 99.2 ms: 1.29x faster                                 |
| Geometric mean | (ref)                                                  | 1.27x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 108 ms                                                 | 78.7 ms: 1.37x faster                                 |
| nbody          | 136 ms                                                 | 97.7 ms: 1.39x faster                                 |
| pidigits       | 190 ms                                                 | 208 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.20x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 140 ms: 1.24x faster                                  |
| regex_dna      | 214 ms                                                 | 221 ms: 1.03x slower                                  |
| regex_effbot   | 3.21 ms                                                | 3.49 ms: 1.09x slower                                 |
| regex_v8       | 25.0 ms                                                | 23.0 ms: 1.09x faster                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.6 ms: 1.07x faster                                 |
| json_loads           | 28.9 us                                                | 28.1 us: 1.03x faster                                 |
| pickle               | 10.1 us                                                | 9.69 us: 1.05x faster                                 |
| pickle_dict          | 28.3 us                                                | 28.1 us: 1.01x faster                                 |
| pickle_pure_python   | 453 us                                                 | 335 us: 1.35x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.92 us: 1.01x faster                                 |
| unpickle_pure_python | 297 us                                                 | 246 us: 1.21x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 156 ms: 1.04x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 105 ms: 1.05x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 79.6 ms: 1.17x faster                                 |
| xml_etree_process    | 74.5 ms                                                | 56.0 ms: 1.33x faster                                 |
| Geometric mean       | (ref)                                                  | 1.10x faster                                          |

Benchmark hidden because not significant (2): pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.20 ms: 1.70x faster                                 |
| python_startup_no_site | 5.76 ms                                                | 6.07 ms: 1.05x slower                                 |
| Geometric mean         | (ref)                                                  | 1.27x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.3 ms                                                | 36.0 ms: 1.29x faster                                 |
| mako            | 14.3 ms                                                | 10.6 ms: 1.34x faster                                 |
| Geometric mean  | (ref)                                                  | 1.31x faster                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 268 ms: 1.24x faster                                  |
| chameleon               | 8.86 ms                                                | 6.93 ms: 1.28x faster                                 |
| chaos                   | 104 ms                                                 | 73.5 ms: 1.42x faster                                 |
| crypto_pyaes            | 118 ms                                                 | 84.6 ms: 1.39x faster                                 |
| deltablue               | 7.39 ms                                                | 4.16 ms: 1.78x faster                                 |
| django_template         | 46.3 ms                                                | 36.0 ms: 1.29x faster                                 |
| dulwich_log             | 75.5 ms                                                | 66.5 ms: 1.13x faster                                 |
| fannkuch                | 477 ms                                                 | 398 ms: 1.20x faster                                  |
| float                   | 108 ms                                                 | 78.7 ms: 1.37x faster                                 |
| go                      | 226 ms                                                 | 148 ms: 1.54x faster                                  |
| hexiom                  | 9.42 ms                                                | 7.04 ms: 1.34x faster                                 |
| html5lib                | 85.8 ms                                                | 68.6 ms: 1.25x faster                                 |
| json                    | 5.35 ms                                                | 5.00 ms: 1.07x faster                                 |
| json_dumps              | 13.5 ms                                                | 12.6 ms: 1.07x faster                                 |
| json_loads              | 28.9 us                                                | 28.1 us: 1.03x faster                                 |
| logging_format          | 8.92 us                                                | 6.08 us: 1.47x faster                                 |
| logging_silent          | 173 ns                                                 | 113 ns: 1.54x faster                                  |
| logging_simple          | 8.06 us                                                | 5.52 us: 1.46x faster                                 |
| mako                    | 14.3 ms                                                | 10.6 ms: 1.34x faster                                 |
| meteor_contest          | 114 ms                                                 | 106 ms: 1.08x faster                                  |
| nbody                   | 136 ms                                                 | 97.7 ms: 1.39x faster                                 |
| nqueens                 | 99.3 ms                                                | 87.0 ms: 1.14x faster                                 |
| pathlib                 | 20.0 ms                                                | 18.2 ms: 1.10x faster                                 |
| pickle                  | 10.1 us                                                | 9.69 us: 1.05x faster                                 |
| pickle_dict             | 28.3 us                                                | 28.1 us: 1.01x faster                                 |
| pickle_pure_python      | 453 us                                                 | 335 us: 1.35x faster                                  |
| pidigits                | 190 ms                                                 | 208 ms: 1.09x slower                                  |
| pycparser               | 1.51 sec                                               | 1.21 sec: 1.25x faster                                |
| pyflate                 | 675 ms                                                 | 453 ms: 1.49x faster                                  |
| python_startup          | 13.9 ms                                                | 8.20 ms: 1.70x faster                                 |
| python_startup_no_site  | 5.76 ms                                                | 6.07 ms: 1.05x slower                                 |
| raytrace                | 461 ms                                                 | 318 ms: 1.45x faster                                  |
| regex_compile           | 174 ms                                                 | 140 ms: 1.24x faster                                  |
| regex_dna               | 214 ms                                                 | 221 ms: 1.03x slower                                  |
| regex_effbot            | 3.21 ms                                                | 3.49 ms: 1.09x slower                                 |
| regex_v8                | 25.0 ms                                                | 23.0 ms: 1.09x faster                                 |
| richards                | 71.4 ms                                                | 48.5 ms: 1.47x faster                                 |
| scimark_fft             | 414 ms                                                 | 336 ms: 1.23x faster                                  |
| scimark_lu              | 158 ms                                                 | 115 ms: 1.37x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 72.9 ms: 1.44x faster                                 |
| scimark_sor             | 193 ms                                                 | 123 ms: 1.56x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.82 ms: 1.14x faster                                 |
| spectral_norm           | 148 ms                                                 | 107 ms: 1.38x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.51 us: 1.16x faster                                 |
| sympy_expand            | 537 ms                                                 | 481 ms: 1.12x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 20.9 ms: 1.15x faster                                 |
| sympy_sum               | 183 ms                                                 | 163 ms: 1.12x faster                                  |
| sympy_str               | 324 ms                                                 | 289 ms: 1.12x faster                                  |
| telco                   | 6.68 ms                                                | 6.92 ms: 1.04x slower                                 |
| thrift                  | 1.03 ms                                                | 789 us: 1.31x faster                                  |
| tornado_http            | 128 ms                                                 | 99.2 ms: 1.29x faster                                 |
| unpack_sequence         | 59.5 ns                                                | 131 ns: 2.20x slower                                  |
| unpickle_list           | 4.99 us                                                | 4.92 us: 1.01x faster                                 |
| unpickle_pure_python    | 297 us                                                 | 246 us: 1.21x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 156 ms: 1.04x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 105 ms: 1.05x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 79.6 ms: 1.17x faster                                 |
| xml_etree_process       | 74.5 ms                                                | 56.0 ms: 1.33x faster                                 |
| Geometric mean          | (ref)                                                  | 1.20x faster                                          |

Benchmark hidden because not significant (2): pickle_list, unpickle
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
