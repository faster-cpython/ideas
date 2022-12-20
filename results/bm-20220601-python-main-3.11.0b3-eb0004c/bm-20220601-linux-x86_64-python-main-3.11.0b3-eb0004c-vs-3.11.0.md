Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 257 ms                                                 | 256 ms: 1.01x faster                                  |
| chameleon      | 6.41 ms                                                | 6.67 ms: 1.04x slower                                 |
| tornado_http   | 96.6 ms                                                | 93.8 ms: 1.03x faster                                 |
| Geometric mean | (ref)                                                  | 1.00x faster                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 76.3 ms                                                | 72.9 ms: 1.05x faster                                 |
| nbody          | 95.0 ms                                                | 90.6 ms: 1.05x faster                                 |
| pidigits       | 199 ms                                                 | 194 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 135 ms: 1.01x faster                                  |
| regex_dna      | 203 ms                                                 | 192 ms: 1.06x faster                                  |
| regex_effbot   | 3.36 ms                                                | 2.92 ms: 1.15x faster                                 |
| regex_v8       | 22.3 ms                                                | 21.2 ms: 1.05x faster                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.5 ms: 1.01x faster                                 |
| json_loads           | 26.2 us                                                | 24.4 us: 1.08x faster                                 |
| pickle               | 9.79 us                                                | 9.55 us: 1.02x faster                                 |
| pickle_dict          | 31.4 us                                                | 25.6 us: 1.23x faster                                 |
| pickle_list          | 4.17 us                                                | 4.33 us: 1.04x slower                                 |
| pickle_pure_python   | 304 us                                                 | 302 us: 1.01x faster                                  |
| unpickle_list        | 4.95 us                                                | 4.89 us: 1.01x faster                                 |
| unpickle_pure_python | 225 us                                                 | 228 us: 1.01x slower                                  |
| xml_etree_parse      | 158 ms                                                 | 156 ms: 1.02x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 105 ms: 1.02x slower                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                          |

Benchmark hidden because not significant (3): unpickle, xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.33 ms: 1.00x faster                                 |
| python_startup_no_site | 5.96 ms                                                | 6.17 ms: 1.04x slower                                 |
| Geometric mean         | (ref)                                                  | 1.02x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.9 ms: 1.01x slower                                 |
| mako            | 9.85 ms                                                | 9.82 ms: 1.00x faster                                 |
| Geometric mean  | (ref)                                                  | 1.00x slower                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 256 ms: 1.01x faster                                  |
| chameleon               | 6.41 ms                                                | 6.67 ms: 1.04x slower                                 |
| chaos                   | 68.6 ms                                                | 66.9 ms: 1.03x faster                                 |
| crypto_pyaes            | 73.9 ms                                                | 73.1 ms: 1.01x faster                                 |
| django_template         | 32.5 ms                                                | 32.9 ms: 1.01x slower                                 |
| dulwich_log             | 63.9 ms                                                | 63.1 ms: 1.01x faster                                 |
| fannkuch                | 388 ms                                                 | 372 ms: 1.04x faster                                  |
| float                   | 76.3 ms                                                | 72.9 ms: 1.05x faster                                 |
| go                      | 143 ms                                                 | 137 ms: 1.05x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.32 ms: 1.01x faster                                 |
| json                    | 4.95 ms                                                | 4.75 ms: 1.04x faster                                 |
| json_dumps              | 12.7 ms                                                | 12.5 ms: 1.01x faster                                 |
| json_loads              | 26.2 us                                                | 24.4 us: 1.08x faster                                 |
| logging_format          | 6.62 us                                                | 6.44 us: 1.03x faster                                 |
| logging_silent          | 98.5 ns                                                | 101 ns: 1.03x slower                                  |
| logging_simple          | 6.06 us                                                | 5.95 us: 1.02x faster                                 |
| mako                    | 9.85 ms                                                | 9.82 ms: 1.00x faster                                 |
| meteor_contest          | 105 ms                                                 | 104 ms: 1.01x faster                                  |
| nbody                   | 95.0 ms                                                | 90.6 ms: 1.05x faster                                 |
| nqueens                 | 85.0 ms                                                | 80.7 ms: 1.05x faster                                 |
| pathlib                 | 18.2 ms                                                | 17.9 ms: 1.02x faster                                 |
| pickle                  | 9.79 us                                                | 9.55 us: 1.02x faster                                 |
| pickle_dict             | 31.4 us                                                | 25.6 us: 1.23x faster                                 |
| pickle_list             | 4.17 us                                                | 4.33 us: 1.04x slower                                 |
| pickle_pure_python      | 304 us                                                 | 302 us: 1.01x faster                                  |
| pidigits                | 199 ms                                                 | 194 ms: 1.03x faster                                  |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.06x faster                                |
| pyflate                 | 417 ms                                                 | 411 ms: 1.01x faster                                  |
| python_startup          | 8.36 ms                                                | 8.33 ms: 1.00x faster                                 |
| python_startup_no_site  | 5.96 ms                                                | 6.17 ms: 1.04x slower                                 |
| raytrace                | 290 ms                                                 | 292 ms: 1.01x slower                                  |
| regex_compile           | 136 ms                                                 | 135 ms: 1.01x faster                                  |
| regex_dna               | 203 ms                                                 | 192 ms: 1.06x faster                                  |
| regex_effbot            | 3.36 ms                                                | 2.92 ms: 1.15x faster                                 |
| regex_v8                | 22.3 ms                                                | 21.2 ms: 1.05x faster                                 |
| richards                | 46.2 ms                                                | 46.5 ms: 1.01x slower                                 |
| scimark_fft             | 329 ms                                                 | 317 ms: 1.04x faster                                  |
| scimark_lu              | 107 ms                                                 | 107 ms: 1.01x faster                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 66.0 ms: 1.04x faster                                 |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.54 ms: 1.03x slower                                 |
| spectral_norm           | 99.9 ms                                                | 97.6 ms: 1.02x faster                                 |
| sympy_expand            | 472 ms                                                 | 467 ms: 1.01x faster                                  |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                 |
| sympy_sum               | 166 ms                                                 | 159 ms: 1.04x faster                                  |
| sympy_str               | 287 ms                                                 | 284 ms: 1.01x faster                                  |
| telco                   | 6.62 ms                                                | 6.49 ms: 1.02x faster                                 |
| thrift                  | 752 us                                                 | 759 us: 1.01x slower                                  |
| tornado_http            | 96.6 ms                                                | 93.8 ms: 1.03x faster                                 |
| unpickle_list           | 4.95 us                                                | 4.89 us: 1.01x faster                                 |
| unpickle_pure_python    | 225 us                                                 | 228 us: 1.01x slower                                  |
| xml_etree_parse         | 158 ms                                                 | 156 ms: 1.02x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 105 ms: 1.02x slower                                  |
| Geometric mean          | (ref)                                                  | 1.02x faster                                          |

Benchmark hidden because not significant (8): deltablue, html5lib, scimark_sor, sqlite_synth, unpack_sequence, unpickle, xml_etree_generate, xml_etree_process
Ignored benchmarks (30) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
