
# Results vs. base

- fork: itamaro
- ref: eager_tasks_factory
- machine: linux-x86_64
- commit hash: bcf40dc
- commit date: 2023-03-20
- overall geometric mean: 1.00x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230320-linux-x86_64-python-094cf392f49d3c16fe79-3.12.0a6+-094cf39 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 249 ms: 1.00x slower                                                   |
| chameleon      | 6.34 ms                                                                | 6.27 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230320-linux-x86_64-python-094cf392f49d3c16fe79-3.12.0a6+-094cf39 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 72.9 ms                                                                | 74.0 ms: 1.01x slower                                                  |
| pidigits       | 192 ms                                                                 | 197 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230320-linux-x86_64-python-094cf392f49d3c16fe79-3.12.0a6+-094cf39 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.52 ms                                                                | 3.30 ms: 1.07x faster                                                  |
| regex_compile  | 133 ms                                                                 | 132 ms: 1.01x faster                                                   |
| regex_v8       | 21.6 ms                                                                | 22.1 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20230320-linux-x86_64-python-094cf392f49d3c16fe79-3.12.0a6+-094cf39 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python  | 288 us                                                                 | 281 us: 1.02x faster                                                   |
| xml_etree_parse     | 149 ms                                                                 | 148 ms: 1.01x faster                                                   |
| unpickle_list       | 5.02 us                                                                | 4.97 us: 1.01x faster                                                  |
| xml_etree_generate  | 80.7 ms                                                                | 80.1 ms: 1.01x faster                                                  |
| json_dumps          | 9.41 ms                                                                | 9.51 ms: 1.01x slower                                                  |
| xml_etree_iterparse | 99.2 ms                                                                | 102 ms: 1.03x slower                                                   |
| pickle_dict         | 30.3 us                                                                | 31.3 us: 1.03x slower                                                  |
| pickle_list         | 4.07 us                                                                | 4.21 us: 1.03x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (5): unpickle, pickle, xml_etree_process, json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230320-linux-x86_64-python-094cf392f49d3c16fe79-3.12.0a6+-094cf39 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.51 ms                                                                | 6.55 ms: 1.01x slower                                                  |
| python_startup         | 8.89 ms                                                                | 8.96 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230320-linux-x86_64-python-094cf392f49d3c16fe79-3.12.0a6+-094cf39 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 21.8 ms                                                                | 21.0 ms: 1.04x faster                                                  |
| genshi_xml     | 48.5 ms                                                                | 47.8 ms: 1.02x faster                                                  |
| mako           | 9.86 ms                                                                | 9.99 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20230320-linux-x86_64-python-094cf392f49d3c16fe79-3.12.0a6+-094cf39 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|-------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot            | 3.52 ms                                                                | 3.30 ms: 1.07x faster                                                  |
| genshi_text             | 21.8 ms                                                                | 21.0 ms: 1.04x faster                                                  |
| telco                   | 6.60 ms                                                                | 6.36 ms: 1.04x faster                                                  |
| async_tree_memoization  | 641 ms                                                                 | 619 ms: 1.03x faster                                                   |
| nqueens                 | 80.1 ms                                                                | 78.2 ms: 1.02x faster                                                  |
| pickle_pure_python      | 288 us                                                                 | 281 us: 1.02x faster                                                   |
| spectral_norm           | 90.0 ms                                                                | 88.2 ms: 1.02x faster                                                  |
| pyflate                 | 411 ms                                                                 | 403 ms: 1.02x faster                                                   |
| fannkuch                | 372 ms                                                                 | 365 ms: 1.02x faster                                                   |
| sympy_expand            | 463 ms                                                                 | 455 ms: 1.02x faster                                                   |
| genshi_xml              | 48.5 ms                                                                | 47.8 ms: 1.02x faster                                                  |
| scimark_fft             | 302 ms                                                                 | 297 ms: 1.01x faster                                                   |
| sqlglot_normalize       | 105 ms                                                                 | 103 ms: 1.01x faster                                                   |
| sympy_str               | 285 ms                                                                 | 281 ms: 1.01x faster                                                   |
| pathlib                 | 17.9 ms                                                                | 17.7 ms: 1.01x faster                                                  |
| chameleon               | 6.34 ms                                                                | 6.27 ms: 1.01x faster                                                  |
| sympy_integrate         | 20.5 ms                                                                | 20.3 ms: 1.01x faster                                                  |
| comprehensions          | 23.7 us                                                                | 23.4 us: 1.01x faster                                                  |
| sympy_sum               | 166 ms                                                                 | 165 ms: 1.01x faster                                                   |
| xml_etree_parse         | 149 ms                                                                 | 148 ms: 1.01x faster                                                   |
| hexiom                  | 6.14 ms                                                                | 6.08 ms: 1.01x faster                                                  |
| unpickle_list           | 5.02 us                                                                | 4.97 us: 1.01x faster                                                  |
| async_tree_io           | 1.30 sec                                                               | 1.29 sec: 1.01x faster                                                 |
| sqlglot_optimize        | 51.1 ms                                                                | 50.6 ms: 1.01x faster                                                  |
| xml_etree_generate      | 80.7 ms                                                                | 80.1 ms: 1.01x faster                                                  |
| generators              | 29.6 ms                                                                | 29.4 ms: 1.01x faster                                                  |
| logging_format          | 6.27 us                                                                | 6.23 us: 1.01x faster                                                  |
| logging_simple          | 5.73 us                                                                | 5.69 us: 1.01x faster                                                  |
| sqlite_synth            | 2.60 us                                                                | 2.58 us: 1.01x faster                                                  |
| regex_compile           | 133 ms                                                                 | 132 ms: 1.01x faster                                                   |
| sqlglot_parse           | 1.42 ms                                                                | 1.41 ms: 1.01x faster                                                  |
| deepcopy                | 324 us                                                                 | 323 us: 1.01x faster                                                   |
| bench_thread_pool       | 786 us                                                                 | 783 us: 1.01x faster                                                   |
| gunicorn                | 1.09 ms                                                                | 1.08 ms: 1.00x faster                                                  |
| 2to3                    | 249 ms                                                                 | 249 ms: 1.00x slower                                                   |
| aiohttp                 | 1.00 ms                                                                | 1.01 ms: 1.00x slower                                                  |
| deltablue               | 3.13 ms                                                                | 3.14 ms: 1.00x slower                                                  |
| python_startup_no_site  | 6.51 ms                                                                | 6.55 ms: 1.01x slower                                                  |
| python_startup          | 8.89 ms                                                                | 8.96 ms: 1.01x slower                                                  |
| logging_silent          | 95.3 ns                                                                | 96.2 ns: 1.01x slower                                                  |
| json_dumps              | 9.41 ms                                                                | 9.51 ms: 1.01x slower                                                  |
| unpack_sequence         | 42.5 ns                                                                | 42.9 ns: 1.01x slower                                                  |
| scimark_sor             | 106 ms                                                                 | 107 ms: 1.01x slower                                                   |
| create_gc_cycles        | 1.48 ms                                                                | 1.49 ms: 1.01x slower                                                  |
| mako                    | 9.86 ms                                                                | 9.99 ms: 1.01x slower                                                  |
| float                   | 72.9 ms                                                                | 74.0 ms: 1.01x slower                                                  |
| thrift                  | 776 us                                                                 | 788 us: 1.02x slower                                                   |
| deepcopy_reduce         | 2.89 us                                                                | 2.94 us: 1.02x slower                                                  |
| meteor_contest          | 104 ms                                                                 | 106 ms: 1.02x slower                                                   |
| go                      | 132 ms                                                                 | 135 ms: 1.02x slower                                                   |
| regex_v8                | 21.6 ms                                                                | 22.1 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult | 4.08 ms                                                                | 4.18 ms: 1.03x slower                                                  |
| pidigits                | 192 ms                                                                 | 197 ms: 1.03x slower                                                   |
| coverage                | 94.2 ms                                                                | 96.8 ms: 1.03x slower                                                  |
| xml_etree_iterparse     | 99.2 ms                                                                | 102 ms: 1.03x slower                                                   |
| pickle_dict             | 30.3 us                                                                | 31.3 us: 1.03x slower                                                  |
| pickle_list             | 4.07 us                                                                | 4.21 us: 1.03x slower                                                  |
| mdp                     | 2.39 sec                                                               | 2.55 sec: 1.07x slower                                                 |
| gc_traversal            | 3.54 ms                                                                | 3.98 ms: 1.12x slower                                                  |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (34): scimark_lu, async_tree_cpu_io_mixed, unpickle, async_tree_none, pickle, xml_etree_process, sqlglot_transpile, pycparser, nbody, regex_dna, dask, dulwich_log, pprint_pformat, html5lib, sqlalchemy_declarative, scimark_monte_carlo, mypy2, json_loads, docutils, bench_mp_pool, django_template, unpickle_pure_python, asyncio_tcp, crypto_pyaes, richards, deepcopy_memo, chaos, pprint_safe_repr, sqlalchemy_imperative, async_generators, coroutines, raytrace, djangocms, json
Ignored benchmarks (1) of public/results/bm-20230320-3.12.0a6+-094cf39/bm-20230320-linux-x86_64-python-094cf392f49d3c16fe79-3.12.0a6+-094cf39.json: tornado_http
