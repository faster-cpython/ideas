
# Results vs. base

- fork: faster-cpython
- ref: restrict_for_iter_sp
- machine: linux-x86_64
- commit hash: fb5f321
- commit date: 2023-02-17
- overall geometric mean: 1.00x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230217-linux-x86_64-python-3c0a31cbfd1258bd9615-3.12.0a5+-3c0a31c | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                                 | 247 ms: 1.00x slower                                                             |
| chameleon      | 6.44 ms                                                                | 6.39 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230217-linux-x86_64-python-3c0a31cbfd1258bd9615-3.12.0a5+-3c0a31c | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 189 ms                                                                 | 198 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230217-linux-x86_64-python-3c0a31cbfd1258bd9615-3.12.0a5+-3c0a31c | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 205 ms                                                                 | 199 ms: 1.03x faster                                                             |
| regex_v8       | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                            |
| regex_compile  | 130 ms                                                                 | 132 ms: 1.02x slower                                                             |
| regex_effbot   | 3.29 ms                                                                | 3.65 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20230217-linux-x86_64-python-3c0a31cbfd1258bd9615-3.12.0a5+-3c0a31c | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|---------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list         | 4.28 us                                                                | 4.01 us: 1.07x faster                                                            |
| pickle_dict         | 31.7 us                                                                | 30.2 us: 1.05x faster                                                            |
| xml_etree_iterparse | 103 ms                                                                 | 99.7 ms: 1.03x faster                                                            |
| unpickle_list       | 5.14 us                                                                | 5.04 us: 1.02x faster                                                            |
| pickle              | 10.1 us                                                                | 9.98 us: 1.01x faster                                                            |
| json_dumps          | 9.60 ms                                                                | 9.50 ms: 1.01x faster                                                            |
| xml_etree_parse     | 150 ms                                                                 | 148 ms: 1.01x faster                                                             |
| pickle_pure_python  | 283 us                                                                 | 281 us: 1.01x faster                                                             |
| xml_etree_generate  | 81.6 ms                                                                | 81.2 ms: 1.00x faster                                                            |
| json_loads          | 23.9 us                                                                | 24.0 us: 1.00x slower                                                            |
| unpickle            | 13.2 us                                                                | 13.7 us: 1.04x slower                                                            |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230217-linux-x86_64-python-3c0a31cbfd1258bd9615-3.12.0a5+-3c0a31c | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.03 ms                                                                | 8.92 ms: 1.01x faster                                                            |
| python_startup_no_site | 6.54 ms                                                                | 6.47 ms: 1.01x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230217-linux-x86_64-python-3c0a31cbfd1258bd9615-3.12.0a5+-3c0a31c | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 9.80 ms                                                                | 9.89 ms: 1.01x slower                                                            |
| genshi_text    | 20.9 ms                                                                | 21.2 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20230217-linux-x86_64-python-3c0a31cbfd1258bd9615-3.12.0a5+-3c0a31c | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| gc_traversal            | 3.83 ms                                                                | 3.53 ms: 1.08x faster                                                            |
| pickle_list             | 4.28 us                                                                | 4.01 us: 1.07x faster                                                            |
| pickle_dict             | 31.7 us                                                                | 30.2 us: 1.05x faster                                                            |
| regex_dna               | 205 ms                                                                 | 199 ms: 1.03x faster                                                             |
| fannkuch                | 373 ms                                                                 | 362 ms: 1.03x faster                                                             |
| xml_etree_iterparse     | 103 ms                                                                 | 99.7 ms: 1.03x faster                                                            |
| sqlalchemy_declarative  | 140 ms                                                                 | 137 ms: 1.02x faster                                                             |
| unpickle_list           | 5.14 us                                                                | 5.04 us: 1.02x faster                                                            |
| crypto_pyaes            | 75.6 ms                                                                | 74.2 ms: 1.02x faster                                                            |
| coroutines              | 22.5 ms                                                                | 22.1 ms: 1.02x faster                                                            |
| pycparser               | 1.11 sec                                                               | 1.10 sec: 1.02x faster                                                           |
| create_gc_cycles        | 1.50 ms                                                                | 1.48 ms: 1.02x faster                                                            |
| scimark_sor             | 109 ms                                                                 | 107 ms: 1.02x faster                                                             |
| scimark_monte_carlo     | 68.2 ms                                                                | 67.1 ms: 1.02x faster                                                            |
| deepcopy_reduce         | 2.99 us                                                                | 2.94 us: 1.02x faster                                                            |
| spectral_norm           | 95.5 ms                                                                | 94.1 ms: 1.01x faster                                                            |
| deltablue               | 3.23 ms                                                                | 3.19 ms: 1.01x faster                                                            |
| pickle                  | 10.1 us                                                                | 9.98 us: 1.01x faster                                                            |
| generators              | 31.0 ms                                                                | 30.6 ms: 1.01x faster                                                            |
| richards                | 42.8 ms                                                                | 42.2 ms: 1.01x faster                                                            |
| python_startup          | 9.03 ms                                                                | 8.92 ms: 1.01x faster                                                            |
| async_generators        | 415 ms                                                                 | 410 ms: 1.01x faster                                                             |
| python_startup_no_site  | 6.54 ms                                                                | 6.47 ms: 1.01x faster                                                            |
| json_dumps              | 9.60 ms                                                                | 9.50 ms: 1.01x faster                                                            |
| async_tree_io           | 1.33 sec                                                               | 1.32 sec: 1.01x faster                                                           |
| xml_etree_parse         | 150 ms                                                                 | 148 ms: 1.01x faster                                                             |
| chameleon               | 6.44 ms                                                                | 6.39 ms: 1.01x faster                                                            |
| pickle_pure_python      | 283 us                                                                 | 281 us: 1.01x faster                                                             |
| pprint_safe_repr        | 684 ms                                                                 | 680 ms: 1.01x faster                                                             |
| deepcopy                | 335 us                                                                 | 333 us: 1.01x faster                                                             |
| asyncio_tcp             | 506 ms                                                                 | 504 ms: 1.01x faster                                                             |
| chaos                   | 68.4 ms                                                                | 68.0 ms: 1.01x faster                                                            |
| xml_etree_generate      | 81.6 ms                                                                | 81.2 ms: 1.00x faster                                                            |
| sqlglot_optimize        | 51.2 ms                                                                | 51.1 ms: 1.00x faster                                                            |
| 2to3                    | 246 ms                                                                 | 247 ms: 1.00x slower                                                             |
| json_loads              | 23.9 us                                                                | 24.0 us: 1.00x slower                                                            |
| sympy_integrate         | 19.9 ms                                                                | 20.0 ms: 1.00x slower                                                            |
| go                      | 133 ms                                                                 | 134 ms: 1.01x slower                                                             |
| gunicorn                | 1.09 ms                                                                | 1.10 ms: 1.01x slower                                                            |
| pathlib                 | 18.0 ms                                                                | 18.1 ms: 1.01x slower                                                            |
| aiohttp                 | 1.01 ms                                                                | 1.01 ms: 1.01x slower                                                            |
| sqlglot_parse           | 1.43 ms                                                                | 1.44 ms: 1.01x slower                                                            |
| mako                    | 9.80 ms                                                                | 9.89 ms: 1.01x slower                                                            |
| logging_format          | 6.31 us                                                                | 6.37 us: 1.01x slower                                                            |
| deepcopy_memo           | 34.3 us                                                                | 34.6 us: 1.01x slower                                                            |
| regex_v8                | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                            |
| genshi_text             | 20.9 ms                                                                | 21.2 ms: 1.01x slower                                                            |
| regex_compile           | 130 ms                                                                 | 132 ms: 1.02x slower                                                             |
| logging_silent          | 93.8 ns                                                                | 95.7 ns: 1.02x slower                                                            |
| hexiom                  | 6.12 ms                                                                | 6.27 ms: 1.02x slower                                                            |
| sqlite_synth            | 2.59 us                                                                | 2.66 us: 1.02x slower                                                            |
| telco                   | 6.40 ms                                                                | 6.58 ms: 1.03x slower                                                            |
| nqueens                 | 79.2 ms                                                                | 81.7 ms: 1.03x slower                                                            |
| scimark_fft             | 305 ms                                                                 | 314 ms: 1.03x slower                                                             |
| unpickle                | 13.2 us                                                                | 13.7 us: 1.04x slower                                                            |
| pidigits                | 189 ms                                                                 | 198 ms: 1.04x slower                                                             |
| async_tree_memoization  | 644 ms                                                                 | 677 ms: 1.05x slower                                                             |
| mdp                     | 2.49 sec                                                               | 2.66 sec: 1.07x slower                                                           |
| regex_effbot            | 3.29 ms                                                                | 3.65 ms: 1.11x slower                                                            |
| scimark_sparse_mat_mult | 3.97 ms                                                                | 4.60 ms: 1.16x slower                                                            |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (33): djangocms, meteor_contest, html5lib, unpack_sequence, django_template, tornado_http, docutils, pyflate, dask, sympy_str, mypy2, unpickle_pure_python, sympy_expand, thrift, bench_mp_pool, raytrace, sqlglot_normalize, xml_etree_process, dulwich_log, bench_thread_pool, genshi_xml, sqlglot_transpile, pprint_pformat, logging_simple, sympy_sum, async_tree_none, coverage, float, json, sqlalchemy_imperative, scimark_lu, async_tree_cpu_io_mixed, nbody
