Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 257 ms                                                 | 264 ms: 1.02x slower                                  |
| chameleon      | 6.41 ms                                                | 7.55 ms: 1.18x slower                                 |
| html5lib       | 63.2 ms                                                | 68.1 ms: 1.08x slower                                 |
| tornado_http   | 96.6 ms                                                | 107 ms: 1.10x slower                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 76.3 ms                                                | 78.0 ms: 1.02x slower                                 |
| pidigits       | 199 ms                                                 | 194 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 138 ms: 1.02x slower                                  |
| regex_dna      | 203 ms                                                 | 212 ms: 1.04x slower                                  |
| regex_effbot   | 3.36 ms                                                | 3.25 ms: 1.03x faster                                 |
| regex_v8       | 22.3 ms                                                | 24.8 ms: 1.11x slower                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.4 ms: 1.02x faster                                 |
| json_loads           | 26.2 us                                                | 25.1 us: 1.05x faster                                 |
| pickle               | 9.79 us                                                | 9.95 us: 1.02x slower                                 |
| pickle_dict          | 31.4 us                                                | 26.8 us: 1.17x faster                                 |
| pickle_list          | 4.17 us                                                | 4.37 us: 1.05x slower                                 |
| pickle_pure_python   | 304 us                                                 | 329 us: 1.08x slower                                  |
| unpickle             | 13.3 us                                                | 14.3 us: 1.08x slower                                 |
| unpickle_list        | 4.95 us                                                | 5.20 us: 1.05x slower                                 |
| unpickle_pure_python | 225 us                                                 | 254 us: 1.13x slower                                  |
| xml_etree_parse      | 158 ms                                                 | 155 ms: 1.02x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 107 ms: 1.05x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 80.2 ms: 1.05x slower                                 |
| xml_etree_process    | 53.8 ms                                                | 56.9 ms: 1.06x slower                                 |
| Geometric mean       | (ref)                                                  | 1.02x slower                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.07 ms: 1.03x faster                                 |
| python_startup_no_site | 5.96 ms                                                | 5.85 ms: 1.02x faster                                 |
| Geometric mean         | (ref)                                                  | 1.03x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 32.5 ms                                                | 35.2 ms: 1.08x slower                                 |
| mako            | 9.85 ms                                                | 11.5 ms: 1.17x slower                                 |
| Geometric mean  | (ref)                                                  | 1.13x slower                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 264 ms: 1.02x slower                                  |
| chameleon               | 6.41 ms                                                | 7.55 ms: 1.18x slower                                 |
| chaos                   | 68.6 ms                                                | 72.7 ms: 1.06x slower                                 |
| crypto_pyaes            | 73.9 ms                                                | 83.8 ms: 1.13x slower                                 |
| deltablue               | 3.64 ms                                                | 4.16 ms: 1.14x slower                                 |
| django_template         | 32.5 ms                                                | 35.2 ms: 1.08x slower                                 |
| dulwich_log             | 63.9 ms                                                | 65.8 ms: 1.03x slower                                 |
| fannkuch                | 388 ms                                                 | 392 ms: 1.01x slower                                  |
| float                   | 76.3 ms                                                | 78.0 ms: 1.02x slower                                 |
| go                      | 143 ms                                                 | 148 ms: 1.03x slower                                  |
| hexiom                  | 6.35 ms                                                | 6.63 ms: 1.04x slower                                 |
| html5lib                | 63.2 ms                                                | 68.1 ms: 1.08x slower                                 |
| json                    | 4.95 ms                                                | 4.74 ms: 1.04x faster                                 |
| json_dumps              | 12.7 ms                                                | 12.4 ms: 1.02x faster                                 |
| json_loads              | 26.2 us                                                | 25.1 us: 1.05x faster                                 |
| logging_format          | 6.62 us                                                | 6.51 us: 1.02x faster                                 |
| logging_silent          | 98.5 ns                                                | 113 ns: 1.15x slower                                  |
| logging_simple          | 6.06 us                                                | 5.95 us: 1.02x faster                                 |
| mako                    | 9.85 ms                                                | 11.5 ms: 1.17x slower                                 |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.02x faster                                  |
| nqueens                 | 85.0 ms                                                | 84.0 ms: 1.01x faster                                 |
| pathlib                 | 18.2 ms                                                | 19.1 ms: 1.05x slower                                 |
| pickle                  | 9.79 us                                                | 9.95 us: 1.02x slower                                 |
| pickle_dict             | 31.4 us                                                | 26.8 us: 1.17x faster                                 |
| pickle_list             | 4.17 us                                                | 4.37 us: 1.05x slower                                 |
| pickle_pure_python      | 304 us                                                 | 329 us: 1.08x slower                                  |
| pidigits                | 199 ms                                                 | 194 ms: 1.03x faster                                  |
| pyflate                 | 417 ms                                                 | 444 ms: 1.06x slower                                  |
| python_startup          | 8.36 ms                                                | 8.07 ms: 1.03x faster                                 |
| python_startup_no_site  | 5.96 ms                                                | 5.85 ms: 1.02x faster                                 |
| raytrace                | 290 ms                                                 | 320 ms: 1.10x slower                                  |
| regex_compile           | 136 ms                                                 | 138 ms: 1.02x slower                                  |
| regex_dna               | 203 ms                                                 | 212 ms: 1.04x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.25 ms: 1.03x faster                                 |
| regex_v8                | 22.3 ms                                                | 24.8 ms: 1.11x slower                                 |
| richards                | 46.2 ms                                                | 51.5 ms: 1.12x slower                                 |
| scimark_lu              | 107 ms                                                 | 114 ms: 1.06x slower                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 72.7 ms: 1.06x slower                                 |
| scimark_sor             | 115 ms                                                 | 124 ms: 1.08x slower                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.69 ms: 1.07x slower                                 |
| spectral_norm           | 99.9 ms                                                | 99.0 ms: 1.01x faster                                 |
| sqlite_synth            | 2.49 us                                                | 2.73 us: 1.10x slower                                 |
| sympy_expand            | 472 ms                                                 | 506 ms: 1.07x slower                                  |
| sympy_integrate         | 20.9 ms                                                | 21.4 ms: 1.02x slower                                 |
| sympy_sum               | 166 ms                                                 | 170 ms: 1.02x slower                                  |
| sympy_str               | 287 ms                                                 | 302 ms: 1.05x slower                                  |
| telco                   | 6.62 ms                                                | 6.69 ms: 1.01x slower                                 |
| thrift                  | 752 us                                                 | 812 us: 1.08x slower                                  |
| tornado_http            | 96.6 ms                                                | 107 ms: 1.10x slower                                  |
| unpack_sequence         | 43.4 ns                                                | 44.8 ns: 1.03x slower                                 |
| unpickle                | 13.3 us                                                | 14.3 us: 1.08x slower                                 |
| unpickle_list           | 4.95 us                                                | 5.20 us: 1.05x slower                                 |
| unpickle_pure_python    | 225 us                                                 | 254 us: 1.13x slower                                  |
| xml_etree_parse         | 158 ms                                                 | 155 ms: 1.02x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 107 ms: 1.05x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 80.2 ms: 1.05x slower                                 |
| xml_etree_process       | 53.8 ms                                                | 56.9 ms: 1.06x slower                                 |
| Geometric mean          | (ref)                                                  | 1.04x slower                                          |

Benchmark hidden because not significant (3): nbody, pycparser, scimark_fft
Ignored benchmarks (30) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
