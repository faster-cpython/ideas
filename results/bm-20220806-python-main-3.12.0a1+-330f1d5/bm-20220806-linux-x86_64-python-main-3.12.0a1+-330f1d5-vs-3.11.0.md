Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| chameleon      | 6.41 ms                                                | 6.50 ms: 1.02x slower                                  |
| tornado_http   | 96.6 ms                                                | 91.7 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 74.1 ms: 1.03x faster                                  |
| nbody          | 95.0 ms                                                | 91.3 ms: 1.04x faster                                  |
| pidigits       | 199 ms                                                 | 194 ms: 1.03x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.50 ms: 1.04x slower                                  |
| regex_v8       | 22.3 ms                                                | 20.8 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.51 ms: 1.33x faster                                  |
| json_loads           | 26.2 us                                                | 24.6 us: 1.07x faster                                  |
| pickle               | 9.79 us                                                | 10.4 us: 1.06x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.9 us: 1.02x slower                                  |
| pickle_list          | 4.17 us                                                | 4.26 us: 1.02x slower                                  |
| pickle_pure_python   | 304 us                                                 | 288 us: 1.05x faster                                   |
| unpickle_list        | 4.95 us                                                | 5.06 us: 1.02x slower                                  |
| unpickle_pure_python | 225 us                                                 | 199 us: 1.13x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 156 ms: 1.01x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 105 ms: 1.02x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.0 ms: 1.02x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 52.2 ms: 1.03x faster                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.15 ms: 1.02x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.01 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako           | 9.85 ms                                                | 9.50 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| chameleon               | 6.41 ms                                                | 6.50 ms: 1.02x slower                                  |
| chaos                   | 68.6 ms                                                | 66.8 ms: 1.03x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 72.6 ms: 1.02x faster                                  |
| deltablue               | 3.64 ms                                                | 3.21 ms: 1.13x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.2 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 374 ms: 1.04x faster                                   |
| float                   | 76.3 ms                                                | 74.1 ms: 1.03x faster                                  |
| go                      | 143 ms                                                 | 131 ms: 1.10x faster                                   |
| hexiom                  | 6.35 ms                                                | 5.98 ms: 1.06x faster                                  |
| json                    | 4.95 ms                                                | 4.70 ms: 1.05x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.51 ms: 1.33x faster                                  |
| json_loads              | 26.2 us                                                | 24.6 us: 1.07x faster                                  |
| logging_format          | 6.62 us                                                | 6.34 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 89.9 ns: 1.10x faster                                  |
| logging_simple          | 6.06 us                                                | 5.72 us: 1.06x faster                                  |
| mako                    | 9.85 ms                                                | 9.50 ms: 1.04x faster                                  |
| meteor_contest          | 105 ms                                                 | 101 ms: 1.03x faster                                   |
| nbody                   | 95.0 ms                                                | 91.3 ms: 1.04x faster                                  |
| nqueens                 | 85.0 ms                                                | 79.2 ms: 1.07x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.6 ms: 1.03x faster                                  |
| pickle                  | 9.79 us                                                | 10.4 us: 1.06x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.9 us: 1.02x slower                                  |
| pickle_list             | 4.17 us                                                | 4.26 us: 1.02x slower                                  |
| pickle_pure_python      | 304 us                                                 | 288 us: 1.05x faster                                   |
| pidigits                | 199 ms                                                 | 194 ms: 1.03x faster                                   |
| pycparser               | 1.17 sec                                               | 1.04 sec: 1.13x faster                                 |
| pyflate                 | 417 ms                                                 | 393 ms: 1.06x faster                                   |
| python_startup          | 8.36 ms                                                | 8.15 ms: 1.02x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.01 ms: 1.01x slower                                  |
| raytrace                | 290 ms                                                 | 278 ms: 1.05x faster                                   |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.50 ms: 1.04x slower                                  |
| regex_v8                | 22.3 ms                                                | 20.8 ms: 1.07x faster                                  |
| richards                | 46.2 ms                                                | 44.5 ms: 1.04x faster                                  |
| scimark_fft             | 329 ms                                                 | 311 ms: 1.06x faster                                   |
| scimark_lu              | 107 ms                                                 | 106 ms: 1.01x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 64.2 ms: 1.06x faster                                  |
| scimark_sor             | 115 ms                                                 | 110 ms: 1.05x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.91 ms: 1.13x faster                                  |
| spectral_norm           | 99.9 ms                                                | 93.8 ms: 1.07x faster                                  |
| sqlite_synth            | 2.49 us                                                | 2.59 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 461 ms: 1.02x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.3 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 160 ms: 1.03x faster                                   |
| sympy_str               | 287 ms                                                 | 282 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.41 ms: 1.03x faster                                  |
| tornado_http            | 96.6 ms                                                | 91.7 ms: 1.05x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 45.9 ns: 1.06x slower                                  |
| unpickle_list           | 4.95 us                                                | 5.06 us: 1.02x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 199 us: 1.13x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 156 ms: 1.01x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 105 ms: 1.02x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.0 ms: 1.02x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 52.2 ms: 1.03x faster                                  |
| Geometric mean          | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (5): django_template, html5lib, regex_dna, thrift, unpickle
Ignored benchmarks (30) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
