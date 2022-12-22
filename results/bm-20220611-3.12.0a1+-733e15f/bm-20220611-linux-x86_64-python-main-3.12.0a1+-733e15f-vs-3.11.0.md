Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 251 ms: 1.03x faster                                   |
| tornado_http   | 96.6 ms                                                | 91.3 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (2): chameleon, html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 71.0 ms: 1.07x faster                                  |
| nbody          | 95.0 ms                                                | 91.3 ms: 1.04x faster                                  |
| pidigits       | 199 ms                                                 | 197 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 132 ms: 1.03x faster                                   |
| regex_dna      | 203 ms                                                 | 198 ms: 1.03x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.01 ms: 1.12x faster                                  |
| regex_v8       | 22.3 ms                                                | 21.3 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.0 ms: 1.05x faster                                  |
| json_loads           | 26.2 us                                                | 25.1 us: 1.05x faster                                  |
| pickle               | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict          | 31.4 us                                                | 30.6 us: 1.03x faster                                  |
| pickle_list          | 4.17 us                                                | 4.11 us: 1.02x faster                                  |
| pickle_pure_python   | 304 us                                                 | 293 us: 1.04x faster                                   |
| unpickle             | 13.3 us                                                | 14.1 us: 1.07x slower                                  |
| unpickle_list        | 4.95 us                                                | 4.89 us: 1.01x faster                                  |
| unpickle_pure_python | 225 us                                                 | 212 us: 1.06x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 104 ms: 1.02x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.4 ms: 1.01x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 52.1 ms: 1.03x faster                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.26 ms: 1.01x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.11 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 31.2 ms: 1.04x faster                                  |
| mako            | 9.85 ms                                                | 9.74 ms: 1.01x faster                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 251 ms: 1.03x faster                                   |
| chaos                   | 68.6 ms                                                | 68.0 ms: 1.01x faster                                  |
| deltablue               | 3.64 ms                                                | 3.51 ms: 1.04x faster                                  |
| django_template         | 32.5 ms                                                | 31.2 ms: 1.04x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.9 ms: 1.03x faster                                  |
| fannkuch                | 388 ms                                                 | 382 ms: 1.02x faster                                   |
| float                   | 76.3 ms                                                | 71.0 ms: 1.07x faster                                  |
| go                      | 143 ms                                                 | 131 ms: 1.09x faster                                   |
| hexiom                  | 6.35 ms                                                | 6.17 ms: 1.03x faster                                  |
| json                    | 4.95 ms                                                | 4.78 ms: 1.04x faster                                  |
| json_dumps              | 12.7 ms                                                | 12.0 ms: 1.05x faster                                  |
| json_loads              | 26.2 us                                                | 25.1 us: 1.05x faster                                  |
| logging_format          | 6.62 us                                                | 6.36 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 99.2 ns: 1.01x slower                                  |
| logging_simple          | 6.06 us                                                | 5.84 us: 1.04x faster                                  |
| mako                    | 9.85 ms                                                | 9.74 ms: 1.01x faster                                  |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.03x faster                                   |
| nbody                   | 95.0 ms                                                | 91.3 ms: 1.04x faster                                  |
| nqueens                 | 85.0 ms                                                | 83.4 ms: 1.02x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict             | 31.4 us                                                | 30.6 us: 1.03x faster                                  |
| pickle_list             | 4.17 us                                                | 4.11 us: 1.02x faster                                  |
| pickle_pure_python      | 304 us                                                 | 293 us: 1.04x faster                                   |
| pidigits                | 199 ms                                                 | 197 ms: 1.01x faster                                   |
| pycparser               | 1.17 sec                                               | 1.07 sec: 1.10x faster                                 |
| pyflate                 | 417 ms                                                 | 400 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.26 ms: 1.01x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.11 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 281 ms: 1.03x faster                                   |
| regex_compile           | 136 ms                                                 | 132 ms: 1.03x faster                                   |
| regex_dna               | 203 ms                                                 | 198 ms: 1.03x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.01 ms: 1.12x faster                                  |
| regex_v8                | 22.3 ms                                                | 21.3 ms: 1.05x faster                                  |
| richards                | 46.2 ms                                                | 43.6 ms: 1.06x faster                                  |
| scimark_fft             | 329 ms                                                 | 315 ms: 1.05x faster                                   |
| scimark_lu              | 107 ms                                                 | 102 ms: 1.06x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 66.7 ms: 1.02x faster                                  |
| scimark_sor             | 115 ms                                                 | 110 ms: 1.04x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.36 ms: 1.01x faster                                  |
| spectral_norm           | 99.9 ms                                                | 95.3 ms: 1.05x faster                                  |
| sympy_expand            | 472 ms                                                 | 457 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.2 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 159 ms: 1.04x faster                                   |
| sympy_str               | 287 ms                                                 | 283 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.46 ms: 1.02x faster                                  |
| thrift                  | 752 us                                                 | 741 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 91.3 ms: 1.06x faster                                  |
| unpickle                | 13.3 us                                                | 14.1 us: 1.07x slower                                  |
| unpickle_list           | 4.95 us                                                | 4.89 us: 1.01x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 212 us: 1.06x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 104 ms: 1.02x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.4 ms: 1.01x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 52.1 ms: 1.03x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (6): chameleon, crypto_pyaes, html5lib, sqlite_synth, unpack_sequence, xml_etree_parse
Ignored benchmarks (30) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
