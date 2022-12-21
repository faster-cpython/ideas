Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 250 ms: 1.03x faster                                   |
| chameleon      | 6.41 ms                                                | 6.30 ms: 1.02x faster                                  |
| tornado_http   | 96.6 ms                                                | 91.6 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.6 ms: 1.05x faster                                  |
| nbody          | 95.0 ms                                                | 91.3 ms: 1.04x faster                                  |
| pidigits       | 199 ms                                                 | 201 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna      | 203 ms                                                 | 205 ms: 1.01x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.42 ms: 1.02x slower                                  |
| regex_v8       | 22.3 ms                                                | 20.9 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.67 ms: 1.31x faster                                  |
| json_loads           | 26.2 us                                                | 24.2 us: 1.08x faster                                  |
| pickle               | 9.79 us                                                | 10.5 us: 1.07x slower                                  |
| pickle_list          | 4.17 us                                                | 4.25 us: 1.02x slower                                  |
| pickle_pure_python   | 304 us                                                 | 287 us: 1.06x faster                                   |
| unpickle_pure_python | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 155 ms: 1.02x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 105 ms: 1.02x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 74.3 ms: 1.03x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 51.3 ms: 1.05x faster                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (3): pickle_dict, unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.17 ms: 1.02x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.04 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako           | 9.85 ms                                                | 9.21 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 250 ms: 1.03x faster                                   |
| chameleon               | 6.41 ms                                                | 6.30 ms: 1.02x faster                                  |
| chaos                   | 68.6 ms                                                | 66.8 ms: 1.03x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 74.2 ms: 1.00x slower                                  |
| deltablue               | 3.64 ms                                                | 3.20 ms: 1.14x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.6 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 375 ms: 1.03x faster                                   |
| float                   | 76.3 ms                                                | 72.6 ms: 1.05x faster                                  |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                   |
| hexiom                  | 6.35 ms                                                | 5.97 ms: 1.06x faster                                  |
| json                    | 4.95 ms                                                | 4.68 ms: 1.06x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.67 ms: 1.31x faster                                  |
| json_loads              | 26.2 us                                                | 24.2 us: 1.08x faster                                  |
| logging_format          | 6.62 us                                                | 6.39 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 89.6 ns: 1.10x faster                                  |
| logging_simple          | 6.06 us                                                | 5.81 us: 1.04x faster                                  |
| mako                    | 9.85 ms                                                | 9.21 ms: 1.07x faster                                  |
| meteor_contest          | 105 ms                                                 | 101 ms: 1.04x faster                                   |
| nbody                   | 95.0 ms                                                | 91.3 ms: 1.04x faster                                  |
| nqueens                 | 85.0 ms                                                | 80.9 ms: 1.05x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.9 ms: 1.01x faster                                  |
| pickle                  | 9.79 us                                                | 10.5 us: 1.07x slower                                  |
| pickle_list             | 4.17 us                                                | 4.25 us: 1.02x slower                                  |
| pickle_pure_python      | 304 us                                                 | 287 us: 1.06x faster                                   |
| pidigits                | 199 ms                                                 | 201 ms: 1.01x slower                                   |
| pycparser               | 1.17 sec                                               | 1.05 sec: 1.12x faster                                 |
| pyflate                 | 417 ms                                                 | 397 ms: 1.05x faster                                   |
| python_startup          | 8.36 ms                                                | 8.17 ms: 1.02x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.04 ms: 1.01x slower                                  |
| raytrace                | 290 ms                                                 | 293 ms: 1.01x slower                                   |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna               | 203 ms                                                 | 205 ms: 1.01x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.42 ms: 1.02x slower                                  |
| regex_v8                | 22.3 ms                                                | 20.9 ms: 1.07x faster                                  |
| richards                | 46.2 ms                                                | 45.1 ms: 1.02x faster                                  |
| scimark_fft             | 329 ms                                                 | 308 ms: 1.07x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 64.7 ms: 1.06x faster                                  |
| scimark_sor             | 115 ms                                                 | 111 ms: 1.03x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.15 ms: 1.06x faster                                  |
| spectral_norm           | 99.9 ms                                                | 95.1 ms: 1.05x faster                                  |
| sqlite_synth            | 2.49 us                                                | 2.58 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 457 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.1 ms: 1.04x faster                                  |
| sympy_sum               | 166 ms                                                 | 159 ms: 1.04x faster                                   |
| sympy_str               | 287 ms                                                 | 278 ms: 1.04x faster                                   |
| telco                   | 6.62 ms                                                | 6.47 ms: 1.02x faster                                  |
| thrift                  | 752 us                                                 | 728 us: 1.03x faster                                   |
| tornado_http            | 96.6 ms                                                | 91.6 ms: 1.06x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 43.0 ns: 1.01x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 155 ms: 1.02x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 105 ms: 1.02x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 74.3 ms: 1.03x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 51.3 ms: 1.05x faster                                  |
| Geometric mean          | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (6): django_template, html5lib, pickle_dict, scimark_lu, unpickle, unpickle_list
Ignored benchmarks (30) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
