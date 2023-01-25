
# Results vs. base

- fork: brandtbucher
- ref: load_attr_class_from
- machine: linux-x86_64
- commit hash: 8b346a3
- commit date: 2023-01-16
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230124-linux-x86_64-python-1a9d8c750be83e6abb65-3.12.0a4+-1a9d8c7 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| chameleon      | 6.39 ms                                                                | 6.33 ms: 1.01x faster                                                        |
| docutils       | 2.58 sec                                                               | 2.50 sec: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230124-linux-x86_64-python-1a9d8c750be83e6abb65-3.12.0a4+-1a9d8c7 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 189 ms                                                                 | 193 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                 |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230124-linux-x86_64-python-1a9d8c750be83e6abb65-3.12.0a4+-1a9d8c7 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                                 | 127 ms: 1.01x faster                                                         |
| regex_dna      | 211 ms                                                                 | 210 ms: 1.00x faster                                                         |
| regex_effbot   | 3.57 ms                                                                | 3.47 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20230124-linux-x86_64-python-1a9d8c750be83e6abb65-3.12.0a4+-1a9d8c7 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_loads          | 23.7 us                                                                | 24.0 us: 1.01x slower                                                        |
| pickle              | 10.1 us                                                                | 10.2 us: 1.01x slower                                                        |
| pickle_dict         | 30.0 us                                                                | 30.5 us: 1.02x slower                                                        |
| pickle_list         | 4.00 us                                                                | 4.10 us: 1.02x slower                                                        |
| pickle_pure_python  | 283 us                                                                 | 272 us: 1.04x faster                                                         |
| unpickle            | 13.0 us                                                                | 13.3 us: 1.03x slower                                                        |
| unpickle_list       | 5.18 us                                                                | 5.03 us: 1.03x faster                                                        |
| xml_etree_iterparse | 107 ms                                                                 | 102 ms: 1.05x faster                                                         |
| xml_etree_generate  | 77.8 ms                                                                | 78.4 ms: 1.01x slower                                                        |
| xml_etree_process   | 53.7 ms                                                                | 54.1 ms: 1.01x slower                                                        |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (3): json_dumps, unpickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230124-linux-x86_64-python-1a9d8c750be83e6abb65-3.12.0a4+-1a9d8c7 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.93 ms                                                                | 8.93 ms: 1.00x faster                                                        |
| python_startup_no_site | 6.45 ms                                                                | 6.46 ms: 1.00x slower                                                        |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230124-linux-x86_64-python-1a9d8c750be83e6abb65-3.12.0a4+-1a9d8c7 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 32.7 ms                                                                | 32.3 ms: 1.01x faster                                                        |
| genshi_text     | 20.8 ms                                                                | 20.5 ms: 1.01x faster                                                        |
| genshi_xml      | 47.4 ms                                                                | 47.1 ms: 1.01x faster                                                        |
| mako            | 9.64 ms                                                                | 9.58 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20230124-linux-x86_64-python-1a9d8c750be83e6abb65-3.12.0a4+-1a9d8c7 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|-------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_generators        | 353 ms                                                                 | 349 ms: 1.01x faster                                                         |
| chameleon               | 6.39 ms                                                                | 6.33 ms: 1.01x faster                                                        |
| chaos                   | 63.9 ms                                                                | 64.8 ms: 1.02x slower                                                        |
| bench_thread_pool       | 778 us                                                                 | 774 us: 1.01x faster                                                         |
| coroutines              | 25.9 ms                                                                | 25.3 ms: 1.02x faster                                                        |
| crypto_pyaes            | 71.4 ms                                                                | 67.2 ms: 1.06x faster                                                        |
| deepcopy                | 330 us                                                                 | 326 us: 1.01x faster                                                         |
| deepcopy_reduce         | 2.93 us                                                                | 2.95 us: 1.01x slower                                                        |
| deepcopy_memo           | 34.2 us                                                                | 34.0 us: 1.01x faster                                                        |
| deltablue               | 3.19 ms                                                                | 3.21 ms: 1.00x slower                                                        |
| django_template         | 32.7 ms                                                                | 32.3 ms: 1.01x faster                                                        |
| docutils                | 2.58 sec                                                               | 2.50 sec: 1.03x faster                                                       |
| dulwich_log             | 62.2 ms                                                                | 62.5 ms: 1.00x slower                                                        |
| fannkuch                | 355 ms                                                                 | 371 ms: 1.04x slower                                                         |
| create_gc_cycles        | 1.44 ms                                                                | 1.46 ms: 1.01x slower                                                        |
| gc_traversal            | 3.82 ms                                                                | 4.16 ms: 1.09x slower                                                        |
| generators              | 75.2 ms                                                                | 77.2 ms: 1.03x slower                                                        |
| genshi_text             | 20.8 ms                                                                | 20.5 ms: 1.01x faster                                                        |
| genshi_xml              | 47.4 ms                                                                | 47.1 ms: 1.01x faster                                                        |
| go                      | 138 ms                                                                 | 133 ms: 1.04x faster                                                         |
| gunicorn                | 1.08 ms                                                                | 1.07 ms: 1.01x faster                                                        |
| json                    | 4.63 ms                                                                | 4.57 ms: 1.01x faster                                                        |
| json_loads              | 23.7 us                                                                | 24.0 us: 1.01x slower                                                        |
| logging_format          | 6.45 us                                                                | 6.31 us: 1.02x faster                                                        |
| logging_silent          | 90.8 ns                                                                | 93.6 ns: 1.03x slower                                                        |
| logging_simple          | 5.80 us                                                                | 5.69 us: 1.02x faster                                                        |
| mako                    | 9.64 ms                                                                | 9.58 ms: 1.01x faster                                                        |
| mdp                     | 2.66 sec                                                               | 2.46 sec: 1.08x faster                                                       |
| nqueens                 | 76.2 ms                                                                | 78.0 ms: 1.02x slower                                                        |
| pathlib                 | 17.6 ms                                                                | 17.7 ms: 1.00x slower                                                        |
| pickle                  | 10.1 us                                                                | 10.2 us: 1.01x slower                                                        |
| pickle_dict             | 30.0 us                                                                | 30.5 us: 1.02x slower                                                        |
| pickle_list             | 4.00 us                                                                | 4.10 us: 1.02x slower                                                        |
| pickle_pure_python      | 283 us                                                                 | 272 us: 1.04x faster                                                         |
| pidigits                | 189 ms                                                                 | 193 ms: 1.02x slower                                                         |
| pprint_safe_repr        | 684 ms                                                                 | 679 ms: 1.01x faster                                                         |
| pprint_pformat          | 1.39 sec                                                               | 1.39 sec: 1.01x faster                                                       |
| pyflate                 | 416 ms                                                                 | 403 ms: 1.03x faster                                                         |
| python_startup          | 8.93 ms                                                                | 8.93 ms: 1.00x faster                                                        |
| python_startup_no_site  | 6.45 ms                                                                | 6.46 ms: 1.00x slower                                                        |
| raytrace                | 286 ms                                                                 | 283 ms: 1.01x faster                                                         |
| regex_compile           | 129 ms                                                                 | 127 ms: 1.01x faster                                                         |
| regex_dna               | 211 ms                                                                 | 210 ms: 1.00x faster                                                         |
| regex_effbot            | 3.57 ms                                                                | 3.47 ms: 1.03x faster                                                        |
| scimark_fft             | 305 ms                                                                 | 300 ms: 1.02x faster                                                         |
| scimark_lu              | 107 ms                                                                 | 106 ms: 1.01x faster                                                         |
| scimark_monte_carlo     | 65.8 ms                                                                | 62.1 ms: 1.06x faster                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                | 3.97 ms: 1.02x faster                                                        |
| sqlglot_optimize        | 51.2 ms                                                                | 50.9 ms: 1.01x faster                                                        |
| sympy_expand            | 451 ms                                                                 | 456 ms: 1.01x slower                                                         |
| sympy_integrate         | 19.7 ms                                                                | 19.8 ms: 1.00x slower                                                        |
| sympy_str               | 268 ms                                                                 | 269 ms: 1.00x slower                                                         |
| telco                   | 6.28 ms                                                                | 6.50 ms: 1.04x slower                                                        |
| unpack_sequence         | 41.3 ns                                                                | 41.6 ns: 1.01x slower                                                        |
| unpickle                | 13.0 us                                                                | 13.3 us: 1.03x slower                                                        |
| unpickle_list           | 5.18 us                                                                | 5.03 us: 1.03x faster                                                        |
| xml_etree_iterparse     | 107 ms                                                                 | 102 ms: 1.05x faster                                                         |
| xml_etree_generate      | 77.8 ms                                                                | 78.4 ms: 1.01x slower                                                        |
| xml_etree_process       | 53.7 ms                                                                | 54.1 ms: 1.01x slower                                                        |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (32): 2to3, aiohttp, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, asyncio_tcp, bench_mp_pool, coverage, dask, djangocms, float, hexiom, html5lib, json_dumps, meteor_contest, mypy, nbody, pycparser, regex_v8, richards, scimark_sor, spectral_norm, sqlglot_parse, sqlglot_transpile, sqlglot_normalize, sqlite_synth, sympy_sum, thrift, tornado_http, unpickle_pure_python, xml_etree_parse
