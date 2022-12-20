Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 257 ms                                                 | 268 ms: 1.04x slower                                  |
| chameleon      | 6.41 ms                                                | 6.93 ms: 1.08x slower                                 |
| html5lib       | 63.2 ms                                                | 68.6 ms: 1.09x slower                                 |
| tornado_http   | 96.6 ms                                                | 99.2 ms: 1.03x slower                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 76.3 ms                                                | 78.7 ms: 1.03x slower                                 |
| nbody          | 95.0 ms                                                | 97.7 ms: 1.03x slower                                 |
| pidigits       | 199 ms                                                 | 208 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 140 ms: 1.03x slower                                  |
| regex_dna      | 203 ms                                                 | 221 ms: 1.09x slower                                  |
| regex_effbot   | 3.36 ms                                                | 3.49 ms: 1.04x slower                                 |
| regex_v8       | 22.3 ms                                                | 23.0 ms: 1.03x slower                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.6 ms: 1.00x faster                                 |
| json_loads           | 26.2 us                                                | 28.1 us: 1.07x slower                                 |
| pickle               | 9.79 us                                                | 9.69 us: 1.01x faster                                 |
| pickle_dict          | 31.4 us                                                | 28.1 us: 1.12x faster                                 |
| pickle_list          | 4.17 us                                                | 4.51 us: 1.08x slower                                 |
| pickle_pure_python   | 304 us                                                 | 335 us: 1.10x slower                                  |
| unpickle             | 13.3 us                                                | 14.2 us: 1.07x slower                                 |
| unpickle_list        | 4.95 us                                                | 4.92 us: 1.01x faster                                 |
| unpickle_pure_python | 225 us                                                 | 246 us: 1.09x slower                                  |
| xml_etree_parse      | 158 ms                                                 | 156 ms: 1.01x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 105 ms: 1.02x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 79.6 ms: 1.04x slower                                 |
| xml_etree_process    | 53.8 ms                                                | 56.0 ms: 1.04x slower                                 |
| Geometric mean       | (ref)                                                  | 1.03x slower                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.20 ms: 1.02x faster                                 |
| python_startup_no_site | 5.96 ms                                                | 6.07 ms: 1.02x slower                                 |
| Geometric mean         | (ref)                                                  | 1.00x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 32.5 ms                                                | 36.0 ms: 1.11x slower                                 |
| mako            | 9.85 ms                                                | 10.6 ms: 1.08x slower                                 |
| Geometric mean  | (ref)                                                  | 1.09x slower                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220307-linux-x86_64-python-main-3.11.0a6-3ddfa55 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 268 ms: 1.04x slower                                  |
| chameleon               | 6.41 ms                                                | 6.93 ms: 1.08x slower                                 |
| chaos                   | 68.6 ms                                                | 73.5 ms: 1.07x slower                                 |
| crypto_pyaes            | 73.9 ms                                                | 84.6 ms: 1.15x slower                                 |
| deltablue               | 3.64 ms                                                | 4.16 ms: 1.14x slower                                 |
| django_template         | 32.5 ms                                                | 36.0 ms: 1.11x slower                                 |
| dulwich_log             | 63.9 ms                                                | 66.5 ms: 1.04x slower                                 |
| fannkuch                | 388 ms                                                 | 398 ms: 1.03x slower                                  |
| float                   | 76.3 ms                                                | 78.7 ms: 1.03x slower                                 |
| go                      | 143 ms                                                 | 148 ms: 1.03x slower                                  |
| hexiom                  | 6.35 ms                                                | 7.04 ms: 1.11x slower                                 |
| html5lib                | 63.2 ms                                                | 68.6 ms: 1.09x slower                                 |
| json                    | 4.95 ms                                                | 5.00 ms: 1.01x slower                                 |
| json_dumps              | 12.7 ms                                                | 12.6 ms: 1.00x faster                                 |
| json_loads              | 26.2 us                                                | 28.1 us: 1.07x slower                                 |
| logging_format          | 6.62 us                                                | 6.08 us: 1.09x faster                                 |
| logging_silent          | 98.5 ns                                                | 113 ns: 1.14x slower                                  |
| logging_simple          | 6.06 us                                                | 5.52 us: 1.10x faster                                 |
| mako                    | 9.85 ms                                                | 10.6 ms: 1.08x slower                                 |
| meteor_contest          | 105 ms                                                 | 106 ms: 1.01x slower                                  |
| nbody                   | 95.0 ms                                                | 97.7 ms: 1.03x slower                                 |
| nqueens                 | 85.0 ms                                                | 87.0 ms: 1.02x slower                                 |
| pickle                  | 9.79 us                                                | 9.69 us: 1.01x faster                                 |
| pickle_dict             | 31.4 us                                                | 28.1 us: 1.12x faster                                 |
| pickle_list             | 4.17 us                                                | 4.51 us: 1.08x slower                                 |
| pickle_pure_python      | 304 us                                                 | 335 us: 1.10x slower                                  |
| pidigits                | 199 ms                                                 | 208 ms: 1.04x slower                                  |
| pycparser               | 1.17 sec                                               | 1.21 sec: 1.03x slower                                |
| pyflate                 | 417 ms                                                 | 453 ms: 1.09x slower                                  |
| python_startup          | 8.36 ms                                                | 8.20 ms: 1.02x faster                                 |
| python_startup_no_site  | 5.96 ms                                                | 6.07 ms: 1.02x slower                                 |
| raytrace                | 290 ms                                                 | 318 ms: 1.10x slower                                  |
| regex_compile           | 136 ms                                                 | 140 ms: 1.03x slower                                  |
| regex_dna               | 203 ms                                                 | 221 ms: 1.09x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.49 ms: 1.04x slower                                 |
| regex_v8                | 22.3 ms                                                | 23.0 ms: 1.03x slower                                 |
| richards                | 46.2 ms                                                | 48.5 ms: 1.05x slower                                 |
| scimark_fft             | 329 ms                                                 | 336 ms: 1.02x slower                                  |
| scimark_lu              | 107 ms                                                 | 115 ms: 1.07x slower                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 72.9 ms: 1.07x slower                                 |
| scimark_sor             | 115 ms                                                 | 123 ms: 1.07x slower                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.82 ms: 1.10x slower                                 |
| spectral_norm           | 99.9 ms                                                | 107 ms: 1.08x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.51 us: 1.01x slower                                 |
| sympy_expand            | 472 ms                                                 | 481 ms: 1.02x slower                                  |
| sympy_sum               | 166 ms                                                 | 163 ms: 1.02x faster                                  |
| sympy_str               | 287 ms                                                 | 289 ms: 1.01x slower                                  |
| telco                   | 6.62 ms                                                | 6.92 ms: 1.04x slower                                 |
| thrift                  | 752 us                                                 | 789 us: 1.05x slower                                  |
| tornado_http            | 96.6 ms                                                | 99.2 ms: 1.03x slower                                 |
| unpack_sequence         | 43.4 ns                                                | 131 ns: 3.02x slower                                  |
| unpickle                | 13.3 us                                                | 14.2 us: 1.07x slower                                 |
| unpickle_list           | 4.95 us                                                | 4.92 us: 1.01x faster                                 |
| unpickle_pure_python    | 225 us                                                 | 246 us: 1.09x slower                                  |
| xml_etree_parse         | 158 ms                                                 | 156 ms: 1.01x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 105 ms: 1.02x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 79.6 ms: 1.04x slower                                 |
| xml_etree_process       | 53.8 ms                                                | 56.0 ms: 1.04x slower                                 |
| Geometric mean          | (ref)                                                  | 1.06x slower                                          |

Benchmark hidden because not significant (2): pathlib, sympy_integrate
Ignored benchmarks (30) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
