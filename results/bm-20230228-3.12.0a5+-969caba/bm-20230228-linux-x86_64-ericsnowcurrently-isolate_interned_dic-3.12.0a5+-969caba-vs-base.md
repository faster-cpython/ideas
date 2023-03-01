
# Results vs. base

- fork: ericsnowcurrently
- ref: isolate_interned_dic
- machine: linux-x86_64
- commit hash: 969caba
- commit date: 2023-02-28
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230228-linux-x86_64-python-880437d4ec65ef35d505-3.12.0a5+-880437d | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 250 ms: 1.01x faster                                                              |
| docutils       | 2.56 sec                                                               | 2.54 sec: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                      |

Benchmark hidden because not significant (3): chameleon, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230228-linux-x86_64-python-880437d4ec65ef35d505-3.12.0a5+-880437d | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                                | 93.6 ms: 1.01x faster                                                             |
| float          | 74.2 ms                                                                | 73.8 ms: 1.01x faster                                                             |
| pidigits       | 189 ms                                                                 | 189 ms: 1.00x faster                                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230228-linux-x86_64-python-880437d4ec65ef35d505-3.12.0a5+-880437d | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 3.70 ms                                                                | 3.55 ms: 1.04x faster                                                             |
| regex_dna      | 206 ms                                                                 | 200 ms: 1.03x faster                                                              |
| regex_compile  | 135 ms                                                                 | 133 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                      |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230228-linux-x86_64-python-880437d4ec65ef35d505-3.12.0a5+-880437d | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pickle_dict          | 32.1 us                                                                | 29.7 us: 1.08x faster                                                             |
| pickle_list          | 4.26 us                                                                | 4.01 us: 1.06x faster                                                             |
| pickle               | 10.4 us                                                                | 9.95 us: 1.04x faster                                                             |
| unpickle_pure_python | 203 us                                                                 | 197 us: 1.03x faster                                                              |
| xml_etree_generate   | 81.8 ms                                                                | 80.7 ms: 1.01x faster                                                             |
| unpickle_list        | 4.96 us                                                                | 4.91 us: 1.01x faster                                                             |
| xml_etree_iterparse  | 99.7 ms                                                                | 99.1 ms: 1.01x faster                                                             |
| xml_etree_process    | 55.9 ms                                                                | 55.6 ms: 1.01x faster                                                             |
| pickle_pure_python   | 287 us                                                                 | 285 us: 1.01x faster                                                              |
| unpickle             | 13.2 us                                                                | 13.3 us: 1.01x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                                      |

Benchmark hidden because not significant (3): xml_etree_parse, json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230228-linux-x86_64-python-880437d4ec65ef35d505-3.12.0a5+-880437d | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 9.02 ms                                                                | 9.03 ms: 1.00x slower                                                             |
| python_startup_no_site | 6.53 ms                                                                | 6.55 ms: 1.00x slower                                                             |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230228-linux-x86_64-python-880437d4ec65ef35d505-3.12.0a5+-880437d | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako           | 9.89 ms                                                                | 10.2 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                      |

Benchmark hidden because not significant (3): django_template, genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20230228-linux-x86_64-python-880437d4ec65ef35d505-3.12.0a5+-880437d | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mdp                     | 2.63 sec                                                               | 2.38 sec: 1.10x faster                                                            |
| pickle_dict             | 32.1 us                                                                | 29.7 us: 1.08x faster                                                             |
| pickle_list             | 4.26 us                                                                | 4.01 us: 1.06x faster                                                             |
| logging_silent          | 98.0 ns                                                                | 92.6 ns: 1.06x faster                                                             |
| go                      | 140 ms                                                                 | 133 ms: 1.05x faster                                                              |
| regex_effbot            | 3.70 ms                                                                | 3.55 ms: 1.04x faster                                                             |
| pickle                  | 10.4 us                                                                | 9.95 us: 1.04x faster                                                             |
| async_tree_memoization  | 653 ms                                                                 | 632 ms: 1.03x faster                                                              |
| richards                | 43.6 ms                                                                | 42.2 ms: 1.03x faster                                                             |
| regex_dna               | 206 ms                                                                 | 200 ms: 1.03x faster                                                              |
| unpickle_pure_python    | 203 us                                                                 | 197 us: 1.03x faster                                                              |
| pycparser               | 1.12 sec                                                               | 1.09 sec: 1.03x faster                                                            |
| deltablue               | 3.26 ms                                                                | 3.19 ms: 1.02x faster                                                             |
| coverage                | 95.8 ms                                                                | 93.7 ms: 1.02x faster                                                             |
| sqlalchemy_declarative  | 140 ms                                                                 | 137 ms: 1.02x faster                                                              |
| deepcopy_memo           | 34.6 us                                                                | 34.1 us: 1.02x faster                                                             |
| thrift                  | 788 us                                                                 | 775 us: 1.02x faster                                                              |
| chaos                   | 67.4 ms                                                                | 66.3 ms: 1.02x faster                                                             |
| hexiom                  | 6.21 ms                                                                | 6.11 ms: 1.02x faster                                                             |
| raytrace                | 289 ms                                                                 | 285 ms: 1.02x faster                                                              |
| pyflate                 | 406 ms                                                                 | 400 ms: 1.01x faster                                                              |
| deepcopy_reduce         | 2.98 us                                                                | 2.94 us: 1.01x faster                                                             |
| regex_compile           | 135 ms                                                                 | 133 ms: 1.01x faster                                                              |
| meteor_contest          | 104 ms                                                                 | 103 ms: 1.01x faster                                                              |
| xml_etree_generate      | 81.8 ms                                                                | 80.7 ms: 1.01x faster                                                             |
| scimark_monte_carlo     | 67.5 ms                                                                | 66.7 ms: 1.01x faster                                                             |
| nbody                   | 94.6 ms                                                                | 93.6 ms: 1.01x faster                                                             |
| unpickle_list           | 4.96 us                                                                | 4.91 us: 1.01x faster                                                             |
| dask                    | 511 ms                                                                 | 506 ms: 1.01x faster                                                              |
| deepcopy                | 333 us                                                                 | 330 us: 1.01x faster                                                              |
| sqlglot_optimize        | 51.0 ms                                                                | 50.6 ms: 1.01x faster                                                             |
| sqlglot_parse           | 1.44 ms                                                                | 1.43 ms: 1.01x faster                                                             |
| xml_etree_iterparse     | 99.7 ms                                                                | 99.1 ms: 1.01x faster                                                             |
| docutils                | 2.56 sec                                                               | 2.54 sec: 1.01x faster                                                            |
| xml_etree_process       | 55.9 ms                                                                | 55.6 ms: 1.01x faster                                                             |
| comprehensions          | 23.9 us                                                                | 23.8 us: 1.01x faster                                                             |
| asyncio_tcp             | 501 ms                                                                 | 498 ms: 1.01x faster                                                              |
| 2to3                    | 252 ms                                                                 | 250 ms: 1.01x faster                                                              |
| pickle_pure_python      | 287 us                                                                 | 285 us: 1.01x faster                                                              |
| float                   | 74.2 ms                                                                | 73.8 ms: 1.01x faster                                                             |
| create_gc_cycles        | 1.47 ms                                                                | 1.46 ms: 1.01x faster                                                             |
| pathlib                 | 17.9 ms                                                                | 17.8 ms: 1.00x faster                                                             |
| sqlglot_normalize       | 103 ms                                                                 | 103 ms: 1.00x faster                                                              |
| pidigits                | 189 ms                                                                 | 189 ms: 1.00x faster                                                              |
| python_startup          | 9.02 ms                                                                | 9.03 ms: 1.00x slower                                                             |
| sympy_integrate         | 20.6 ms                                                                | 20.7 ms: 1.00x slower                                                             |
| python_startup_no_site  | 6.53 ms                                                                | 6.55 ms: 1.00x slower                                                             |
| generators              | 30.6 ms                                                                | 30.7 ms: 1.00x slower                                                             |
| bench_thread_pool       | 793 us                                                                 | 796 us: 1.00x slower                                                              |
| gunicorn                | 1.08 ms                                                                | 1.09 ms: 1.01x slower                                                             |
| unpickle                | 13.2 us                                                                | 13.3 us: 1.01x slower                                                             |
| scimark_fft             | 315 ms                                                                 | 318 ms: 1.01x slower                                                              |
| crypto_pyaes            | 74.3 ms                                                                | 75.1 ms: 1.01x slower                                                             |
| nqueens                 | 81.7 ms                                                                | 82.8 ms: 1.01x slower                                                             |
| pprint_safe_repr        | 677 ms                                                                 | 687 ms: 1.01x slower                                                              |
| pprint_pformat          | 1.39 sec                                                               | 1.41 sec: 1.01x slower                                                            |
| spectral_norm           | 93.7 ms                                                                | 95.8 ms: 1.02x slower                                                             |
| mako                    | 9.89 ms                                                                | 10.2 ms: 1.03x slower                                                             |
| fannkuch                | 357 ms                                                                 | 370 ms: 1.04x slower                                                              |
| unpack_sequence         | 41.6 ns                                                                | 44.3 ns: 1.06x slower                                                             |
| scimark_sparse_mat_mult | 4.43 ms                                                                | 4.73 ms: 1.07x slower                                                             |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                                      |

Benchmark hidden because not significant (33): html5lib, xml_etree_parse, django_template, mypy2, async_generators, scimark_sor, chameleon, sqlglot_transpile, json_loads, async_tree_none, logging_format, sympy_str, sqlite_synth, sympy_expand, json_dumps, telco, tornado_http, json, async_tree_io, aiohttp, genshi_xml, gc_traversal, regex_v8, genshi_text, sympy_sum, scimark_lu, coroutines, async_tree_cpu_io_mixed, bench_mp_pool, logging_simple, dulwich_log, sqlalchemy_imperative, djangocms
