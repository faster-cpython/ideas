Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 249 ms: 1.03x faster                                   |
| chameleon      | 6.41 ms                                                | 6.45 ms: 1.01x slower                                  |
| html5lib       | 63.2 ms                                                | 62.0 ms: 1.02x faster                                  |
| tornado_http   | 96.6 ms                                                | 92.1 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 71.1 ms: 1.07x faster                                  |
| pidigits       | 199 ms                                                 | 194 ms: 1.03x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_dna      | 203 ms                                                 | 208 ms: 1.02x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.61 ms: 1.07x slower                                  |
| regex_v8       | 22.3 ms                                                | 21.3 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.0 ms: 1.05x faster                                  |
| json_loads           | 26.2 us                                                | 24.5 us: 1.07x faster                                  |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| pickle_dict          | 31.4 us                                                | 30.1 us: 1.04x faster                                  |
| pickle_list          | 4.17 us                                                | 4.15 us: 1.01x faster                                  |
| pickle_pure_python   | 304 us                                                 | 294 us: 1.04x faster                                   |
| unpickle_pure_python | 225 us                                                 | 198 us: 1.14x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 155 ms: 1.02x faster                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.0 ms: 1.02x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 52.0 ms: 1.03x faster                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (3): unpickle, unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.26 ms: 1.01x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.10 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 31.6 ms: 1.03x faster                                  |
| mako            | 9.85 ms                                                | 9.46 ms: 1.04x faster                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 249 ms: 1.03x faster                                   |
| chameleon               | 6.41 ms                                                | 6.45 ms: 1.01x slower                                  |
| chaos                   | 68.6 ms                                                | 63.8 ms: 1.07x faster                                  |
| deltablue               | 3.64 ms                                                | 3.24 ms: 1.13x faster                                  |
| django_template         | 32.5 ms                                                | 31.6 ms: 1.03x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.7 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 376 ms: 1.03x faster                                   |
| float                   | 76.3 ms                                                | 71.1 ms: 1.07x faster                                  |
| go                      | 143 ms                                                 | 128 ms: 1.12x faster                                   |
| hexiom                  | 6.35 ms                                                | 5.94 ms: 1.07x faster                                  |
| html5lib                | 63.2 ms                                                | 62.0 ms: 1.02x faster                                  |
| json                    | 4.95 ms                                                | 4.72 ms: 1.05x faster                                  |
| json_dumps              | 12.7 ms                                                | 12.0 ms: 1.05x faster                                  |
| json_loads              | 26.2 us                                                | 24.5 us: 1.07x faster                                  |
| logging_format          | 6.62 us                                                | 6.40 us: 1.03x faster                                  |
| logging_silent          | 98.5 ns                                                | 89.6 ns: 1.10x faster                                  |
| logging_simple          | 6.06 us                                                | 5.77 us: 1.05x faster                                  |
| mako                    | 9.85 ms                                                | 9.46 ms: 1.04x faster                                  |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.02x faster                                   |
| nqueens                 | 85.0 ms                                                | 82.2 ms: 1.03x faster                                  |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| pickle_dict             | 31.4 us                                                | 30.1 us: 1.04x faster                                  |
| pickle_list             | 4.17 us                                                | 4.15 us: 1.01x faster                                  |
| pickle_pure_python      | 304 us                                                 | 294 us: 1.04x faster                                   |
| pidigits                | 199 ms                                                 | 194 ms: 1.03x faster                                   |
| pycparser               | 1.17 sec                                               | 1.05 sec: 1.12x faster                                 |
| pyflate                 | 417 ms                                                 | 400 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.26 ms: 1.01x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.10 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 279 ms: 1.04x faster                                   |
| regex_compile           | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_dna               | 203 ms                                                 | 208 ms: 1.02x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.61 ms: 1.07x slower                                  |
| regex_v8                | 22.3 ms                                                | 21.3 ms: 1.05x faster                                  |
| richards                | 46.2 ms                                                | 45.4 ms: 1.02x faster                                  |
| scimark_fft             | 329 ms                                                 | 304 ms: 1.08x faster                                   |
| scimark_lu              | 107 ms                                                 | 104 ms: 1.03x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 62.4 ms: 1.09x faster                                  |
| scimark_sor             | 115 ms                                                 | 110 ms: 1.05x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.89 ms: 1.13x faster                                  |
| spectral_norm           | 99.9 ms                                                | 92.8 ms: 1.08x faster                                  |
| sqlite_synth            | 2.49 us                                                | 2.57 us: 1.03x slower                                  |
| sympy_expand            | 472 ms                                                 | 451 ms: 1.05x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.2 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 159 ms: 1.04x faster                                   |
| sympy_str               | 287 ms                                                 | 277 ms: 1.04x faster                                   |
| telco                   | 6.62 ms                                                | 6.44 ms: 1.03x faster                                  |
| thrift                  | 752 us                                                 | 745 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 92.1 ms: 1.05x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 42.8 ns: 1.01x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 198 us: 1.14x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 155 ms: 1.02x faster                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.0 ms: 1.02x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 52.0 ms: 1.03x faster                                  |
| Geometric mean          | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (6): crypto_pyaes, nbody, pathlib, unpickle, unpickle_list, xml_etree_iterparse
Ignored benchmarks (30) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
