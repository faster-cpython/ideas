
# Results vs. base

- fork: barneygale
- ref: optimize_pathlib_par
- machine: linux-x86_64
- commit hash: d5231b6
- commit date: 2023-02-04
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (5): 2to3, chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 97.5 ms                                                                | 92.6 ms: 1.05x faster                                                      |
| pidigits       | 193 ms                                                                 | 189 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.63 ms                                                                | 3.59 ms: 1.01x faster                                                      |
| regex_compile  | 126 ms                                                                 | 127 ms: 1.01x slower                                                       |
| regex_v8       | 22.2 ms                                                                | 22.6 ms: 1.02x slower                                                      |
| regex_dna      | 210 ms                                                                 | 216 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle           | 14.9 us                                                                | 13.5 us: 1.10x faster                                                      |
| pickle_dict        | 31.9 us                                                                | 30.6 us: 1.04x faster                                                      |
| unpickle_list      | 5.12 us                                                                | 4.98 us: 1.03x faster                                                      |
| json_dumps         | 9.48 ms                                                                | 9.22 ms: 1.03x faster                                                      |
| pickle_list        | 4.24 us                                                                | 4.17 us: 1.02x faster                                                      |
| json_loads         | 24.1 us                                                                | 23.9 us: 1.01x faster                                                      |
| pickle             | 10.1 us                                                                | 10.1 us: 1.01x faster                                                      |
| pickle_pure_python | 281 us                                                                 | 280 us: 1.00x faster                                                       |
| xml_etree_generate | 77.4 ms                                                                | 77.7 ms: 1.01x slower                                                      |
| xml_etree_process  | 53.5 ms                                                                | 54.0 ms: 1.01x slower                                                      |
| Geometric mean     | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (3): xml_etree_parse, unpickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.46 ms                                                                | 6.44 ms: 1.00x faster                                                      |
| python_startup         | 8.93 ms                                                                | 8.91 ms: 1.00x faster                                                      |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml     | 47.0 ms                                                                | 46.5 ms: 1.01x faster                                                      |
| mako           | 9.79 ms                                                                | 9.74 ms: 1.01x faster                                                      |
| genshi_text    | 20.5 ms                                                                | 20.8 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle                | 14.9 us                                                                | 13.5 us: 1.10x faster                                                      |
| mdp                     | 2.61 sec                                                               | 2.44 sec: 1.07x faster                                                     |
| nbody                   | 97.5 ms                                                                | 92.6 ms: 1.05x faster                                                      |
| pickle_dict             | 31.9 us                                                                | 30.6 us: 1.04x faster                                                      |
| scimark_sparse_mat_mult | 4.15 ms                                                                | 3.99 ms: 1.04x faster                                                      |
| coroutines              | 25.7 ms                                                                | 24.8 ms: 1.04x faster                                                      |
| gc_traversal            | 3.65 ms                                                                | 3.53 ms: 1.03x faster                                                      |
| scimark_monte_carlo     | 67.2 ms                                                                | 65.1 ms: 1.03x faster                                                      |
| generators              | 76.4 ms                                                                | 74.2 ms: 1.03x faster                                                      |
| spectral_norm           | 97.2 ms                                                                | 94.5 ms: 1.03x faster                                                      |
| unpickle_list           | 5.12 us                                                                | 4.98 us: 1.03x faster                                                      |
| json_dumps              | 9.48 ms                                                                | 9.22 ms: 1.03x faster                                                      |
| scimark_fft             | 310 ms                                                                 | 302 ms: 1.03x faster                                                       |
| chaos                   | 65.0 ms                                                                | 63.6 ms: 1.02x faster                                                      |
| telco                   | 6.55 ms                                                                | 6.41 ms: 1.02x faster                                                      |
| json                    | 4.72 ms                                                                | 4.63 ms: 1.02x faster                                                      |
| pyflate                 | 404 ms                                                                 | 397 ms: 1.02x faster                                                       |
| pidigits                | 193 ms                                                                 | 189 ms: 1.02x faster                                                       |
| nqueens                 | 78.3 ms                                                                | 77.0 ms: 1.02x faster                                                      |
| scimark_sor             | 109 ms                                                                 | 107 ms: 1.02x faster                                                       |
| pickle_list             | 4.24 us                                                                | 4.17 us: 1.02x faster                                                      |
| fannkuch                | 363 ms                                                                 | 359 ms: 1.01x faster                                                       |
| regex_effbot            | 3.63 ms                                                                | 3.59 ms: 1.01x faster                                                      |
| genshi_xml              | 47.0 ms                                                                | 46.5 ms: 1.01x faster                                                      |
| async_tree_io           | 1.32 sec                                                               | 1.31 sec: 1.01x faster                                                     |
| thrift                  | 758 us                                                                 | 752 us: 1.01x faster                                                       |
| json_loads              | 24.1 us                                                                | 23.9 us: 1.01x faster                                                      |
| gunicorn                | 1.08 ms                                                                | 1.07 ms: 1.01x faster                                                      |
| pickle                  | 10.1 us                                                                | 10.1 us: 1.01x faster                                                      |
| mako                    | 9.79 ms                                                                | 9.74 ms: 1.01x faster                                                      |
| pprint_safe_repr        | 669 ms                                                                 | 666 ms: 1.01x faster                                                       |
| async_generators        | 352 ms                                                                 | 350 ms: 1.00x faster                                                       |
| deltablue               | 3.21 ms                                                                | 3.19 ms: 1.00x faster                                                      |
| hexiom                  | 6.05 ms                                                                | 6.03 ms: 1.00x faster                                                      |
| asyncio_tcp             | 491 ms                                                                 | 489 ms: 1.00x faster                                                       |
| python_startup_no_site  | 6.46 ms                                                                | 6.44 ms: 1.00x faster                                                      |
| pickle_pure_python      | 281 us                                                                 | 280 us: 1.00x faster                                                       |
| aiohttp                 | 997 us                                                                 | 995 us: 1.00x faster                                                       |
| python_startup          | 8.93 ms                                                                | 8.91 ms: 1.00x faster                                                      |
| create_gc_cycles        | 1.46 ms                                                                | 1.47 ms: 1.00x slower                                                      |
| sqlglot_parse           | 1.43 ms                                                                | 1.43 ms: 1.00x slower                                                      |
| sympy_integrate         | 19.7 ms                                                                | 19.8 ms: 1.00x slower                                                      |
| xml_etree_generate      | 77.4 ms                                                                | 77.7 ms: 1.01x slower                                                      |
| go                      | 134 ms                                                                 | 135 ms: 1.01x slower                                                       |
| coverage                | 94.5 ms                                                                | 95.1 ms: 1.01x slower                                                      |
| sqlglot_optimize        | 50.8 ms                                                                | 51.1 ms: 1.01x slower                                                      |
| pycparser               | 1.14 sec                                                               | 1.15 sec: 1.01x slower                                                     |
| regex_compile           | 126 ms                                                                 | 127 ms: 1.01x slower                                                       |
| xml_etree_process       | 53.5 ms                                                                | 54.0 ms: 1.01x slower                                                      |
| sqlglot_normalize       | 105 ms                                                                 | 106 ms: 1.01x slower                                                       |
| deepcopy_memo           | 34.2 us                                                                | 34.5 us: 1.01x slower                                                      |
| genshi_text             | 20.5 ms                                                                | 20.8 ms: 1.01x slower                                                      |
| logging_format          | 6.29 us                                                                | 6.36 us: 1.01x slower                                                      |
| deepcopy                | 323 us                                                                 | 328 us: 1.02x slower                                                       |
| crypto_pyaes            | 72.1 ms                                                                | 73.4 ms: 1.02x slower                                                      |
| regex_v8                | 22.2 ms                                                                | 22.6 ms: 1.02x slower                                                      |
| logging_silent          | 92.3 ns                                                                | 94.0 ns: 1.02x slower                                                      |
| regex_dna               | 210 ms                                                                 | 216 ms: 1.03x slower                                                       |
| unpack_sequence         | 41.7 ns                                                                | 43.1 ns: 1.03x slower                                                      |
| pathlib                 | 18.0 ms                                                                | 19.0 ms: 1.06x slower                                                      |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (31): deepcopy_reduce, raytrace, async_tree_cpu_io_mixed, sympy_sum, xml_etree_parse, sympy_str, float, djangocms, pprint_pformat, django_template, 2to3, unpickle_pure_python, tornado_http, async_tree_none, dulwich_log, xml_etree_iterparse, bench_mp_pool, bench_thread_pool, richards, docutils, logging_simple, sympy_expand, scimark_lu, dask, chameleon, sqlglot_transpile, async_tree_memoization, sqlite_synth, mypy, meteor_contest, html5lib
