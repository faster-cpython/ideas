Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 332 ms                                                 | 264 ms: 1.26x faster                                  |
| chameleon      | 8.86 ms                                                | 7.44 ms: 1.19x faster                                 |
| html5lib       | 85.8 ms                                                | 68.5 ms: 1.25x faster                                 |
| tornado_http   | 128 ms                                                 | 108 ms: 1.19x faster                                  |
| Geometric mean | (ref)                                                  | 1.22x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 108 ms                                                 | 79.2 ms: 1.36x faster                                 |
| nbody          | 136 ms                                                 | 96.1 ms: 1.42x faster                                 |
| pidigits       | 190 ms                                                 | 198 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 139 ms: 1.25x faster                                  |
| regex_dna      | 214 ms                                                 | 212 ms: 1.01x faster                                  |
| regex_v8       | 25.0 ms                                                | 24.5 ms: 1.02x faster                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.6 ms: 1.07x faster                                 |
| json_loads           | 28.9 us                                                | 25.6 us: 1.13x faster                                 |
| pickle               | 10.1 us                                                | 9.95 us: 1.02x faster                                 |
| pickle_dict          | 28.3 us                                                | 27.7 us: 1.02x faster                                 |
| pickle_list          | 4.50 us                                                | 4.68 us: 1.04x slower                                 |
| pickle_pure_python   | 453 us                                                 | 347 us: 1.31x faster                                  |
| unpickle             | 14.3 us                                                | 14.6 us: 1.02x slower                                 |
| unpickle_list        | 4.99 us                                                | 5.21 us: 1.04x slower                                 |
| unpickle_pure_python | 297 us                                                 | 251 us: 1.18x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 156 ms: 1.05x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 105 ms: 1.05x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 80.8 ms: 1.15x faster                                 |
| xml_etree_process    | 74.5 ms                                                | 57.8 ms: 1.29x faster                                 |
| Geometric mean       | (ref)                                                  | 1.08x faster                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.00 ms: 1.74x faster                                 |
| python_startup_no_site | 5.76 ms                                                | 5.78 ms: 1.00x slower                                 |
| Geometric mean         | (ref)                                                  | 1.32x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.3 ms                                                | 36.5 ms: 1.27x faster                                 |
| mako            | 14.3 ms                                                | 11.9 ms: 1.20x faster                                 |
| Geometric mean  | (ref)                                                  | 1.23x faster                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 264 ms: 1.26x faster                                  |
| chameleon               | 8.86 ms                                                | 7.44 ms: 1.19x faster                                 |
| chaos                   | 104 ms                                                 | 73.9 ms: 1.41x faster                                 |
| crypto_pyaes            | 118 ms                                                 | 88.1 ms: 1.33x faster                                 |
| deltablue               | 7.39 ms                                                | 4.54 ms: 1.63x faster                                 |
| django_template         | 46.3 ms                                                | 36.5 ms: 1.27x faster                                 |
| dulwich_log             | 75.5 ms                                                | 67.2 ms: 1.12x faster                                 |
| fannkuch                | 477 ms                                                 | 386 ms: 1.23x faster                                  |
| float                   | 108 ms                                                 | 79.2 ms: 1.36x faster                                 |
| go                      | 226 ms                                                 | 158 ms: 1.44x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.77 ms: 1.39x faster                                 |
| html5lib                | 85.8 ms                                                | 68.5 ms: 1.25x faster                                 |
| json                    | 5.35 ms                                                | 4.83 ms: 1.11x faster                                 |
| json_dumps              | 13.5 ms                                                | 12.6 ms: 1.07x faster                                 |
| json_loads              | 28.9 us                                                | 25.6 us: 1.13x faster                                 |
| logging_format          | 8.92 us                                                | 6.49 us: 1.38x faster                                 |
| logging_silent          | 173 ns                                                 | 110 ns: 1.57x faster                                  |
| logging_simple          | 8.06 us                                                | 5.97 us: 1.35x faster                                 |
| mako                    | 14.3 ms                                                | 11.9 ms: 1.20x faster                                 |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.09x faster                                  |
| nbody                   | 136 ms                                                 | 96.1 ms: 1.42x faster                                 |
| nqueens                 | 99.3 ms                                                | 84.6 ms: 1.17x faster                                 |
| pathlib                 | 20.0 ms                                                | 19.4 ms: 1.03x faster                                 |
| pickle                  | 10.1 us                                                | 9.95 us: 1.02x faster                                 |
| pickle_dict             | 28.3 us                                                | 27.7 us: 1.02x faster                                 |
| pickle_list             | 4.50 us                                                | 4.68 us: 1.04x slower                                 |
| pickle_pure_python      | 453 us                                                 | 347 us: 1.31x faster                                  |
| pidigits                | 190 ms                                                 | 198 ms: 1.04x slower                                  |
| pycparser               | 1.51 sec                                               | 1.24 sec: 1.22x faster                                |
| pyflate                 | 675 ms                                                 | 477 ms: 1.42x faster                                  |
| python_startup          | 13.9 ms                                                | 8.00 ms: 1.74x faster                                 |
| python_startup_no_site  | 5.76 ms                                                | 5.78 ms: 1.00x slower                                 |
| raytrace                | 461 ms                                                 | 333 ms: 1.38x faster                                  |
| regex_compile           | 174 ms                                                 | 139 ms: 1.25x faster                                  |
| regex_dna               | 214 ms                                                 | 212 ms: 1.01x faster                                  |
| regex_v8                | 25.0 ms                                                | 24.5 ms: 1.02x faster                                 |
| richards                | 71.4 ms                                                | 54.5 ms: 1.31x faster                                 |
| scimark_fft             | 414 ms                                                 | 332 ms: 1.25x faster                                  |
| scimark_lu              | 158 ms                                                 | 112 ms: 1.42x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 74.0 ms: 1.42x faster                                 |
| scimark_sor             | 193 ms                                                 | 130 ms: 1.48x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.77 ms: 1.15x faster                                 |
| spectral_norm           | 148 ms                                                 | 104 ms: 1.43x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.74 us: 1.06x faster                                 |
| sympy_expand            | 537 ms                                                 | 509 ms: 1.05x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 21.7 ms: 1.10x faster                                 |
| sympy_sum               | 183 ms                                                 | 172 ms: 1.07x faster                                  |
| sympy_str               | 324 ms                                                 | 308 ms: 1.05x faster                                  |
| telco                   | 6.68 ms                                                | 6.56 ms: 1.02x faster                                 |
| thrift                  | 1.03 ms                                                | 814 us: 1.27x faster                                  |
| tornado_http            | 128 ms                                                 | 108 ms: 1.19x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 49.2 ns: 1.21x faster                                 |
| unpickle                | 14.3 us                                                | 14.6 us: 1.02x slower                                 |
| unpickle_list           | 4.99 us                                                | 5.21 us: 1.04x slower                                 |
| unpickle_pure_python    | 297 us                                                 | 251 us: 1.18x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 156 ms: 1.05x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 105 ms: 1.05x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 80.8 ms: 1.15x faster                                 |
| xml_etree_process       | 74.5 ms                                                | 57.8 ms: 1.29x faster                                 |
| Geometric mean          | (ref)                                                  | 1.20x faster                                          |

Benchmark hidden because not significant (1): regex_effbot
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
