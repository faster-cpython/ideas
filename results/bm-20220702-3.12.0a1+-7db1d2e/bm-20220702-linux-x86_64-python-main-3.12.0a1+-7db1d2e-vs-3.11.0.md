Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| html5lib       | 63.2 ms                                                | 62.0 ms: 1.02x faster                                  |
| tornado_http   | 96.6 ms                                                | 91.4 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 69.9 ms: 1.09x faster                                  |
| nbody          | 95.0 ms                                                | 89.9 ms: 1.06x faster                                  |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 125 ms: 1.09x faster                                   |
| regex_dna      | 203 ms                                                 | 197 ms: 1.03x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.49 ms: 1.04x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.0 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 11.9 ms: 1.06x faster                                  |
| json_loads           | 26.2 us                                                | 24.3 us: 1.08x faster                                  |
| pickle               | 9.79 us                                                | 10.5 us: 1.07x slower                                  |
| pickle_dict          | 31.4 us                                                | 30.7 us: 1.02x faster                                  |
| pickle_list          | 4.17 us                                                | 4.28 us: 1.02x slower                                  |
| pickle_pure_python   | 304 us                                                 | 282 us: 1.08x faster                                   |
| unpickle_list        | 4.95 us                                                | 4.93 us: 1.00x faster                                  |
| unpickle_pure_python | 225 us                                                 | 198 us: 1.14x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 156 ms: 1.01x faster                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.0 ms: 1.02x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 52.0 ms: 1.03x faster                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (2): unpickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.22 ms: 1.02x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.07 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.00x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.0 ms: 1.01x faster                                  |
| mako            | 9.85 ms                                                | 9.55 ms: 1.03x faster                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| chaos                   | 68.6 ms                                                | 65.2 ms: 1.05x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 73.3 ms: 1.01x faster                                  |
| deltablue               | 3.64 ms                                                | 3.20 ms: 1.14x faster                                  |
| django_template         | 32.5 ms                                                | 32.0 ms: 1.01x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.2 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 373 ms: 1.04x faster                                   |
| float                   | 76.3 ms                                                | 69.9 ms: 1.09x faster                                  |
| go                      | 143 ms                                                 | 130 ms: 1.10x faster                                   |
| hexiom                  | 6.35 ms                                                | 5.88 ms: 1.08x faster                                  |
| html5lib                | 63.2 ms                                                | 62.0 ms: 1.02x faster                                  |
| json                    | 4.95 ms                                                | 4.70 ms: 1.05x faster                                  |
| json_dumps              | 12.7 ms                                                | 11.9 ms: 1.06x faster                                  |
| json_loads              | 26.2 us                                                | 24.3 us: 1.08x faster                                  |
| logging_format          | 6.62 us                                                | 6.26 us: 1.06x faster                                  |
| logging_silent          | 98.5 ns                                                | 91.7 ns: 1.07x faster                                  |
| logging_simple          | 6.06 us                                                | 5.74 us: 1.06x faster                                  |
| mako                    | 9.85 ms                                                | 9.55 ms: 1.03x faster                                  |
| meteor_contest          | 105 ms                                                 | 101 ms: 1.03x faster                                   |
| nbody                   | 95.0 ms                                                | 89.9 ms: 1.06x faster                                  |
| nqueens                 | 85.0 ms                                                | 81.0 ms: 1.05x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.5 us: 1.07x slower                                  |
| pickle_dict             | 31.4 us                                                | 30.7 us: 1.02x faster                                  |
| pickle_list             | 4.17 us                                                | 4.28 us: 1.02x slower                                  |
| pickle_pure_python      | 304 us                                                 | 282 us: 1.08x faster                                   |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| pycparser               | 1.17 sec                                               | 1.08 sec: 1.08x faster                                 |
| pyflate                 | 417 ms                                                 | 389 ms: 1.07x faster                                   |
| python_startup          | 8.36 ms                                                | 8.22 ms: 1.02x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.07 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 282 ms: 1.03x faster                                   |
| regex_compile           | 136 ms                                                 | 125 ms: 1.09x faster                                   |
| regex_dna               | 203 ms                                                 | 197 ms: 1.03x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.49 ms: 1.04x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.0 ms: 1.01x faster                                  |
| richards                | 46.2 ms                                                | 44.6 ms: 1.03x faster                                  |
| scimark_fft             | 329 ms                                                 | 309 ms: 1.07x faster                                   |
| scimark_lu              | 107 ms                                                 | 105 ms: 1.03x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 62.8 ms: 1.09x faster                                  |
| scimark_sor             | 115 ms                                                 | 111 ms: 1.04x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.21 ms: 1.04x faster                                  |
| spectral_norm           | 99.9 ms                                                | 94.3 ms: 1.06x faster                                  |
| sqlite_synth            | 2.49 us                                                | 2.59 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 450 ms: 1.05x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.1 ms: 1.04x faster                                  |
| sympy_sum               | 166 ms                                                 | 158 ms: 1.05x faster                                   |
| sympy_str               | 287 ms                                                 | 276 ms: 1.04x faster                                   |
| thrift                  | 752 us                                                 | 744 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 91.4 ms: 1.06x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 45.5 ns: 1.05x slower                                  |
| unpickle_list           | 4.95 us                                                | 4.93 us: 1.00x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 198 us: 1.14x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 156 ms: 1.01x faster                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.0 ms: 1.02x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 52.0 ms: 1.03x faster                                  |
| Geometric mean          | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (4): chameleon, telco, unpickle, xml_etree_iterparse
Ignored benchmarks (30) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
