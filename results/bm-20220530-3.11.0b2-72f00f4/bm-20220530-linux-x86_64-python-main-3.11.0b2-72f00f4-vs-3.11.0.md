Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 257 ms                                                 | 256 ms: 1.00x faster                                  |
| chameleon      | 6.41 ms                                                | 6.59 ms: 1.03x slower                                 |
| tornado_http   | 96.6 ms                                                | 93.8 ms: 1.03x faster                                 |
| Geometric mean | (ref)                                                  | 1.00x slower                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 76.3 ms                                                | 72.8 ms: 1.05x faster                                 |
| nbody          | 95.0 ms                                                | 90.9 ms: 1.05x faster                                 |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 136 ms: 1.00x slower                                  |
| regex_dna      | 203 ms                                                 | 196 ms: 1.03x faster                                  |
| regex_effbot   | 3.36 ms                                                | 3.02 ms: 1.11x faster                                 |
| regex_v8       | 22.3 ms                                                | 21.5 ms: 1.04x faster                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.6 ms: 1.01x faster                                 |
| json_loads           | 26.2 us                                                | 24.3 us: 1.08x faster                                 |
| pickle               | 9.79 us                                                | 9.61 us: 1.02x faster                                 |
| pickle_dict          | 31.4 us                                                | 25.9 us: 1.21x faster                                 |
| pickle_list          | 4.17 us                                                | 4.30 us: 1.03x slower                                 |
| pickle_pure_python   | 304 us                                                 | 302 us: 1.01x faster                                  |
| unpickle_list        | 4.95 us                                                | 4.98 us: 1.00x slower                                 |
| unpickle_pure_python | 225 us                                                 | 227 us: 1.01x slower                                  |
| xml_etree_iterparse  | 103 ms                                                 | 104 ms: 1.01x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 75.8 ms: 1.01x faster                                 |
| xml_etree_process    | 53.8 ms                                                | 53.3 ms: 1.01x faster                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                          |

Benchmark hidden because not significant (2): unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.33 ms: 1.00x faster                                 |
| python_startup_no_site | 5.96 ms                                                | 6.17 ms: 1.03x slower                                 |
| Geometric mean         | (ref)                                                  | 1.02x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| mako           | 9.85 ms                                                | 9.71 ms: 1.01x faster                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 256 ms: 1.00x faster                                  |
| chameleon               | 6.41 ms                                                | 6.59 ms: 1.03x slower                                 |
| chaos                   | 68.6 ms                                                | 67.8 ms: 1.01x faster                                 |
| deltablue               | 3.64 ms                                                | 3.60 ms: 1.01x faster                                 |
| dulwich_log             | 63.9 ms                                                | 62.6 ms: 1.02x faster                                 |
| fannkuch                | 388 ms                                                 | 394 ms: 1.02x slower                                  |
| float                   | 76.3 ms                                                | 72.8 ms: 1.05x faster                                 |
| go                      | 143 ms                                                 | 136 ms: 1.05x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.32 ms: 1.00x faster                                 |
| json                    | 4.95 ms                                                | 4.72 ms: 1.05x faster                                 |
| json_dumps              | 12.7 ms                                                | 12.6 ms: 1.01x faster                                 |
| json_loads              | 26.2 us                                                | 24.3 us: 1.08x faster                                 |
| logging_format          | 6.62 us                                                | 6.42 us: 1.03x faster                                 |
| logging_silent          | 98.5 ns                                                | 98.1 ns: 1.00x faster                                 |
| logging_simple          | 6.06 us                                                | 5.82 us: 1.04x faster                                 |
| mako                    | 9.85 ms                                                | 9.71 ms: 1.01x faster                                 |
| nbody                   | 95.0 ms                                                | 90.9 ms: 1.05x faster                                 |
| nqueens                 | 85.0 ms                                                | 82.4 ms: 1.03x faster                                 |
| pickle                  | 9.79 us                                                | 9.61 us: 1.02x faster                                 |
| pickle_dict             | 31.4 us                                                | 25.9 us: 1.21x faster                                 |
| pickle_list             | 4.17 us                                                | 4.30 us: 1.03x slower                                 |
| pickle_pure_python      | 304 us                                                 | 302 us: 1.01x faster                                  |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                  |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.06x faster                                |
| pyflate                 | 417 ms                                                 | 410 ms: 1.02x faster                                  |
| python_startup          | 8.36 ms                                                | 8.33 ms: 1.00x faster                                 |
| python_startup_no_site  | 5.96 ms                                                | 6.17 ms: 1.03x slower                                 |
| regex_compile           | 136 ms                                                 | 136 ms: 1.00x slower                                  |
| regex_dna               | 203 ms                                                 | 196 ms: 1.03x faster                                  |
| regex_effbot            | 3.36 ms                                                | 3.02 ms: 1.11x faster                                 |
| regex_v8                | 22.3 ms                                                | 21.5 ms: 1.04x faster                                 |
| richards                | 46.2 ms                                                | 45.3 ms: 1.02x faster                                 |
| scimark_fft             | 329 ms                                                 | 324 ms: 1.02x faster                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 66.5 ms: 1.03x faster                                 |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.79 ms: 1.09x slower                                 |
| spectral_norm           | 99.9 ms                                                | 96.3 ms: 1.04x faster                                 |
| sympy_expand            | 472 ms                                                 | 465 ms: 1.02x faster                                  |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                 |
| sympy_sum               | 166 ms                                                 | 159 ms: 1.04x faster                                  |
| sympy_str               | 287 ms                                                 | 284 ms: 1.01x faster                                  |
| thrift                  | 752 us                                                 | 756 us: 1.01x slower                                  |
| tornado_http            | 96.6 ms                                                | 93.8 ms: 1.03x faster                                 |
| unpickle_list           | 4.95 us                                                | 4.98 us: 1.00x slower                                 |
| unpickle_pure_python    | 225 us                                                 | 227 us: 1.01x slower                                  |
| xml_etree_iterparse     | 103 ms                                                 | 104 ms: 1.01x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 75.8 ms: 1.01x faster                                 |
| xml_etree_process       | 53.8 ms                                                | 53.3 ms: 1.01x faster                                 |
| Geometric mean          | (ref)                                                  | 1.02x faster                                          |

Benchmark hidden because not significant (13): crypto_pyaes, django_template, html5lib, meteor_contest, pathlib, raytrace, scimark_lu, scimark_sor, sqlite_synth, telco, unpack_sequence, unpickle, xml_etree_parse
Ignored benchmarks (30) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
