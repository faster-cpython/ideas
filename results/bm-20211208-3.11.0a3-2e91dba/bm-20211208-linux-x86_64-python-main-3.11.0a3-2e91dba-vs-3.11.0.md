Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 257 ms                                                 | 264 ms: 1.02x slower                                  |
| chameleon      | 6.41 ms                                                | 7.44 ms: 1.16x slower                                 |
| html5lib       | 63.2 ms                                                | 68.5 ms: 1.08x slower                                 |
| tornado_http   | 96.6 ms                                                | 108 ms: 1.12x slower                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 76.3 ms                                                | 79.2 ms: 1.04x slower                                 |
| nbody          | 95.0 ms                                                | 96.1 ms: 1.01x slower                                 |
| pidigits       | 199 ms                                                 | 198 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 139 ms: 1.02x slower                                  |
| regex_dna      | 203 ms                                                 | 212 ms: 1.04x slower                                  |
| regex_effbot   | 3.36 ms                                                | 3.21 ms: 1.04x faster                                 |
| regex_v8       | 22.3 ms                                                | 24.5 ms: 1.10x slower                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_loads           | 26.2 us                                                | 25.6 us: 1.02x faster                                 |
| pickle               | 9.79 us                                                | 9.95 us: 1.02x slower                                 |
| pickle_dict          | 31.4 us                                                | 27.7 us: 1.14x faster                                 |
| pickle_list          | 4.17 us                                                | 4.68 us: 1.12x slower                                 |
| pickle_pure_python   | 304 us                                                 | 347 us: 1.14x slower                                  |
| unpickle             | 13.3 us                                                | 14.6 us: 1.10x slower                                 |
| unpickle_list        | 4.95 us                                                | 5.21 us: 1.05x slower                                 |
| unpickle_pure_python | 225 us                                                 | 251 us: 1.11x slower                                  |
| xml_etree_parse      | 158 ms                                                 | 156 ms: 1.02x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 105 ms: 1.03x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 80.8 ms: 1.06x slower                                 |
| xml_etree_process    | 53.8 ms                                                | 57.8 ms: 1.08x slower                                 |
| Geometric mean       | (ref)                                                  | 1.04x slower                                          |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.00 ms: 1.04x faster                                 |
| python_startup_no_site | 5.96 ms                                                | 5.78 ms: 1.03x faster                                 |
| Geometric mean         | (ref)                                                  | 1.04x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 32.5 ms                                                | 36.5 ms: 1.13x slower                                 |
| mako            | 9.85 ms                                                | 11.9 ms: 1.21x slower                                 |
| Geometric mean  | (ref)                                                  | 1.17x slower                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211208-linux-x86_64-python-main-3.11.0a3-2e91dba |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 264 ms: 1.02x slower                                  |
| chameleon               | 6.41 ms                                                | 7.44 ms: 1.16x slower                                 |
| chaos                   | 68.6 ms                                                | 73.9 ms: 1.08x slower                                 |
| crypto_pyaes            | 73.9 ms                                                | 88.1 ms: 1.19x slower                                 |
| deltablue               | 3.64 ms                                                | 4.54 ms: 1.25x slower                                 |
| django_template         | 32.5 ms                                                | 36.5 ms: 1.13x slower                                 |
| dulwich_log             | 63.9 ms                                                | 67.2 ms: 1.05x slower                                 |
| float                   | 76.3 ms                                                | 79.2 ms: 1.04x slower                                 |
| go                      | 143 ms                                                 | 158 ms: 1.10x slower                                  |
| hexiom                  | 6.35 ms                                                | 6.77 ms: 1.07x slower                                 |
| html5lib                | 63.2 ms                                                | 68.5 ms: 1.08x slower                                 |
| json                    | 4.95 ms                                                | 4.83 ms: 1.02x faster                                 |
| json_loads              | 26.2 us                                                | 25.6 us: 1.02x faster                                 |
| logging_format          | 6.62 us                                                | 6.49 us: 1.02x faster                                 |
| logging_silent          | 98.5 ns                                                | 110 ns: 1.12x slower                                  |
| logging_simple          | 6.06 us                                                | 5.97 us: 1.02x faster                                 |
| mako                    | 9.85 ms                                                | 11.9 ms: 1.21x slower                                 |
| nbody                   | 95.0 ms                                                | 96.1 ms: 1.01x slower                                 |
| nqueens                 | 85.0 ms                                                | 84.6 ms: 1.01x faster                                 |
| pathlib                 | 18.2 ms                                                | 19.4 ms: 1.07x slower                                 |
| pickle                  | 9.79 us                                                | 9.95 us: 1.02x slower                                 |
| pickle_dict             | 31.4 us                                                | 27.7 us: 1.14x faster                                 |
| pickle_list             | 4.17 us                                                | 4.68 us: 1.12x slower                                 |
| pickle_pure_python      | 304 us                                                 | 347 us: 1.14x slower                                  |
| pidigits                | 199 ms                                                 | 198 ms: 1.01x faster                                  |
| pycparser               | 1.17 sec                                               | 1.24 sec: 1.06x slower                                |
| pyflate                 | 417 ms                                                 | 477 ms: 1.14x slower                                  |
| python_startup          | 8.36 ms                                                | 8.00 ms: 1.04x faster                                 |
| python_startup_no_site  | 5.96 ms                                                | 5.78 ms: 1.03x faster                                 |
| raytrace                | 290 ms                                                 | 333 ms: 1.15x slower                                  |
| regex_compile           | 136 ms                                                 | 139 ms: 1.02x slower                                  |
| regex_dna               | 203 ms                                                 | 212 ms: 1.04x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.21 ms: 1.04x faster                                 |
| regex_v8                | 22.3 ms                                                | 24.5 ms: 1.10x slower                                 |
| richards                | 46.2 ms                                                | 54.5 ms: 1.18x slower                                 |
| scimark_fft             | 329 ms                                                 | 332 ms: 1.01x slower                                  |
| scimark_lu              | 107 ms                                                 | 112 ms: 1.04x slower                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 74.0 ms: 1.08x slower                                 |
| scimark_sor             | 115 ms                                                 | 130 ms: 1.13x slower                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.77 ms: 1.08x slower                                 |
| spectral_norm           | 99.9 ms                                                | 104 ms: 1.04x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.74 us: 1.10x slower                                 |
| sympy_expand            | 472 ms                                                 | 509 ms: 1.08x slower                                  |
| sympy_integrate         | 20.9 ms                                                | 21.7 ms: 1.04x slower                                 |
| sympy_sum               | 166 ms                                                 | 172 ms: 1.04x slower                                  |
| sympy_str               | 287 ms                                                 | 308 ms: 1.07x slower                                  |
| telco                   | 6.62 ms                                                | 6.56 ms: 1.01x faster                                 |
| thrift                  | 752 us                                                 | 814 us: 1.08x slower                                  |
| tornado_http            | 96.6 ms                                                | 108 ms: 1.12x slower                                  |
| unpack_sequence         | 43.4 ns                                                | 49.2 ns: 1.13x slower                                 |
| unpickle                | 13.3 us                                                | 14.6 us: 1.10x slower                                 |
| unpickle_list           | 4.95 us                                                | 5.21 us: 1.05x slower                                 |
| unpickle_pure_python    | 225 us                                                 | 251 us: 1.11x slower                                  |
| xml_etree_parse         | 158 ms                                                 | 156 ms: 1.02x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 105 ms: 1.03x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 80.8 ms: 1.06x slower                                 |
| xml_etree_process       | 53.8 ms                                                | 57.8 ms: 1.08x slower                                 |
| Geometric mean          | (ref)                                                  | 1.06x slower                                          |

Benchmark hidden because not significant (3): fannkuch, json_dumps, meteor_contest
Ignored benchmarks (30) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
