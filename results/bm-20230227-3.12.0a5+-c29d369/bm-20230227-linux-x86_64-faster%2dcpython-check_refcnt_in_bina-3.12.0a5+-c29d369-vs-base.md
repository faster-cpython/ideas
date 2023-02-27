
# Results vs. base

- fork: faster-cpython
- ref: check_refcnt_in_bina
- machine: linux-x86_64
- commit hash: c29d369
- commit date: 2023-02-27
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                 | 248 ms: 1.00x slower                                                             |
| chameleon      | 6.37 ms                                                                | 6.51 ms: 1.02x slower                                                            |
| docutils       | 2.55 sec                                                               | 2.53 sec: 1.01x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                                | 89.7 ms: 1.07x faster                                                            |
| pidigits       | 193 ms                                                                 | 197 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.63 ms                                                                | 3.36 ms: 1.08x faster                                                            |
| regex_v8       | 21.7 ms                                                                | 22.2 ms: 1.03x slower                                                            |
| regex_dna      | 198 ms                                                                 | 209 ms: 1.06x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                                | 30.7 us: 1.06x faster                                                            |
| pickle_list          | 4.33 us                                                                | 4.12 us: 1.05x faster                                                            |
| unpickle_list        | 5.08 us                                                                | 4.94 us: 1.03x faster                                                            |
| xml_etree_parse      | 150 ms                                                                 | 148 ms: 1.01x faster                                                             |
| xml_etree_iterparse  | 99.8 ms                                                                | 98.7 ms: 1.01x faster                                                            |
| xml_etree_generate   | 80.6 ms                                                                | 79.7 ms: 1.01x faster                                                            |
| xml_etree_process    | 55.1 ms                                                                | 54.9 ms: 1.00x faster                                                            |
| json_loads           | 23.9 us                                                                | 24.0 us: 1.00x slower                                                            |
| unpickle_pure_python | 195 us                                                                 | 196 us: 1.00x slower                                                             |
| json_dumps           | 9.52 ms                                                                | 9.62 ms: 1.01x slower                                                            |
| pickle_pure_python   | 280 us                                                                 | 284 us: 1.01x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.49 ms                                                                | 6.51 ms: 1.00x slower                                                            |
| python_startup         | 8.95 ms                                                                | 8.98 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 9.99 ms                                                                | 9.92 ms: 1.01x faster                                                            |
| django_template | 32.5 ms                                                                | 33.1 ms: 1.02x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| gc_traversal            | 4.30 ms                                                                | 3.83 ms: 1.12x faster                                                            |
| regex_effbot            | 3.63 ms                                                                | 3.36 ms: 1.08x faster                                                            |
| scimark_sparse_mat_mult | 4.48 ms                                                                | 4.17 ms: 1.07x faster                                                            |
| spectral_norm           | 94.0 ms                                                                | 87.7 ms: 1.07x faster                                                            |
| nbody                   | 96.0 ms                                                                | 89.7 ms: 1.07x faster                                                            |
| pickle_dict             | 32.5 us                                                                | 30.7 us: 1.06x faster                                                            |
| pickle_list             | 4.33 us                                                                | 4.12 us: 1.05x faster                                                            |
| scimark_fft             | 313 ms                                                                 | 300 ms: 1.04x faster                                                             |
| coroutines              | 23.7 ms                                                                | 22.7 ms: 1.04x faster                                                            |
| mdp                     | 2.69 sec                                                               | 2.61 sec: 1.03x faster                                                           |
| unpickle_list           | 5.08 us                                                                | 4.94 us: 1.03x faster                                                            |
| async_tree_io           | 1.30 sec                                                               | 1.27 sec: 1.02x faster                                                           |
| deepcopy_reduce         | 3.02 us                                                                | 2.97 us: 1.02x faster                                                            |
| async_tree_cpu_io_mixed | 743 ms                                                                 | 732 ms: 1.02x faster                                                             |
| scimark_sor             | 104 ms                                                                 | 103 ms: 1.02x faster                                                             |
| xml_etree_parse         | 150 ms                                                                 | 148 ms: 1.01x faster                                                             |
| sqlite_synth            | 2.64 us                                                                | 2.61 us: 1.01x faster                                                            |
| xml_etree_iterparse     | 99.8 ms                                                                | 98.7 ms: 1.01x faster                                                            |
| xml_etree_generate      | 80.6 ms                                                                | 79.7 ms: 1.01x faster                                                            |
| generators              | 29.9 ms                                                                | 29.7 ms: 1.01x faster                                                            |
| mako                    | 9.99 ms                                                                | 9.92 ms: 1.01x faster                                                            |
| meteor_contest          | 103 ms                                                                 | 102 ms: 1.01x faster                                                             |
| raytrace                | 280 ms                                                                 | 278 ms: 1.01x faster                                                             |
| thrift                  | 761 us                                                                 | 756 us: 1.01x faster                                                             |
| logging_format          | 6.38 us                                                                | 6.34 us: 1.01x faster                                                            |
| docutils                | 2.55 sec                                                               | 2.53 sec: 1.01x faster                                                           |
| sqlglot_optimize        | 50.8 ms                                                                | 50.5 ms: 1.01x faster                                                            |
| pathlib                 | 17.8 ms                                                                | 17.7 ms: 1.01x faster                                                            |
| xml_etree_process       | 55.1 ms                                                                | 54.9 ms: 1.00x faster                                                            |
| bench_thread_pool       | 786 us                                                                 | 784 us: 1.00x faster                                                             |
| sqlglot_normalize       | 104 ms                                                                 | 103 ms: 1.00x faster                                                             |
| sympy_integrate         | 20.5 ms                                                                | 20.5 ms: 1.00x faster                                                            |
| 2to3                    | 247 ms                                                                 | 248 ms: 1.00x slower                                                             |
| python_startup_no_site  | 6.49 ms                                                                | 6.51 ms: 1.00x slower                                                            |
| json_loads              | 23.9 us                                                                | 24.0 us: 1.00x slower                                                            |
| unpickle_pure_python    | 195 us                                                                 | 196 us: 1.00x slower                                                             |
| pyflate                 | 405 ms                                                                 | 407 ms: 1.00x slower                                                             |
| aiohttp                 | 1.01 ms                                                                | 1.01 ms: 1.00x slower                                                            |
| python_startup          | 8.95 ms                                                                | 8.98 ms: 1.00x slower                                                            |
| create_gc_cycles        | 1.47 ms                                                                | 1.47 ms: 1.00x slower                                                            |
| pycparser               | 1.09 sec                                                               | 1.10 sec: 1.01x slower                                                           |
| sympy_str               | 281 ms                                                                 | 283 ms: 1.01x slower                                                             |
| gunicorn                | 1.08 ms                                                                | 1.09 ms: 1.01x slower                                                            |
| pprint_safe_repr        | 680 ms                                                                 | 685 ms: 1.01x slower                                                             |
| pprint_pformat          | 1.39 sec                                                               | 1.41 sec: 1.01x slower                                                           |
| coverage                | 96.5 ms                                                                | 97.5 ms: 1.01x slower                                                            |
| json_dumps              | 9.52 ms                                                                | 9.62 ms: 1.01x slower                                                            |
| go                      | 132 ms                                                                 | 134 ms: 1.01x slower                                                             |
| sympy_sum               | 165 ms                                                                 | 167 ms: 1.01x slower                                                             |
| pickle_pure_python      | 280 us                                                                 | 284 us: 1.01x slower                                                             |
| hexiom                  | 6.00 ms                                                                | 6.08 ms: 1.01x slower                                                            |
| django_template         | 32.5 ms                                                                | 33.1 ms: 1.02x slower                                                            |
| crypto_pyaes            | 72.1 ms                                                                | 73.5 ms: 1.02x slower                                                            |
| sqlalchemy_declarative  | 136 ms                                                                 | 139 ms: 1.02x slower                                                             |
| chameleon               | 6.37 ms                                                                | 6.51 ms: 1.02x slower                                                            |
| pidigits                | 193 ms                                                                 | 197 ms: 1.02x slower                                                             |
| regex_v8                | 21.7 ms                                                                | 22.2 ms: 1.03x slower                                                            |
| fannkuch                | 352 ms                                                                 | 361 ms: 1.03x slower                                                             |
| unpack_sequence         | 42.2 ns                                                                | 44.3 ns: 1.05x slower                                                            |
| regex_dna               | 198 ms                                                                 | 209 ms: 1.06x slower                                                             |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (33): pickle, scimark_lu, async_tree_memoization, deepcopy_memo, async_tree_none, scimark_monte_carlo, float, genshi_xml, richards, dulwich_log, telco, mypy2, sqlalchemy_imperative, sqlglot_transpile, asyncio_tcp, dask, bench_mp_pool, sqlglot_parse, deepcopy, tornado_http, deltablue, html5lib, logging_simple, genshi_text, async_generators, nqueens, sympy_expand, chaos, logging_silent, unpickle, regex_compile, json, djangocms
