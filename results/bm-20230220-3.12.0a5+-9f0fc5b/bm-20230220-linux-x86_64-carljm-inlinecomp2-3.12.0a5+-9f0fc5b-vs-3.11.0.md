
# Results vs. 3.11.0

- fork: carljm
- ref: inlinecomp2
- machine: linux-x86_64
- commit hash: 9f0fc5b
- commit date: 2023-02-20
- overall geometric mean: 1.05x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 248 ms: 1.04x faster                                          |
| chameleon      | 6.41 ms                                                | 6.32 ms: 1.01x faster                                         |
| docutils       | 2.60 sec                                               | 2.53 sec: 1.03x faster                                        |
| html5lib       | 63.2 ms                                                | 60.4 ms: 1.05x faster                                         |
| tornado_http   | 96.6 ms                                                | 94.3 ms: 1.03x faster                                         |
| Geometric mean | (ref)                                                  | 1.03x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.0 ms: 1.06x faster                                         |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                          |
| nbody          | 95.0 ms                                                | 94.0 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                  | 1.04x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                          |
| regex_v8       | 22.3 ms                                                | 21.8 ms: 1.02x faster                                         |
| regex_dna      | 203 ms                                                 | 207 ms: 1.02x slower                                          |
| regex_effbot   | 3.36 ms                                                | 3.69 ms: 1.10x slower                                         |
| Geometric mean | (ref)                                                  | 1.01x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.49 ms: 1.33x faster                                         |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.14x faster                                          |
| json_loads           | 26.2 us                                                | 24.1 us: 1.09x faster                                         |
| pickle_pure_python   | 304 us                                                 | 281 us: 1.08x faster                                          |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                          |
| pickle_list          | 4.17 us                                                | 3.97 us: 1.05x faster                                         |
| pickle_dict          | 31.4 us                                                | 30.0 us: 1.05x faster                                         |
| pickle               | 9.79 us                                                | 10.0 us: 1.02x slower                                         |
| xml_etree_process    | 53.8 ms                                                | 55.5 ms: 1.03x slower                                         |
| unpickle_list        | 4.95 us                                                | 5.13 us: 1.04x slower                                         |
| xml_etree_generate   | 76.2 ms                                                | 80.6 ms: 1.06x slower                                         |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                  |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.96 ms: 1.07x slower                                         |
| python_startup_no_site | 5.96 ms                                                | 6.50 ms: 1.09x slower                                         |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 47.9 ms: 1.09x faster                                         |
| genshi_text     | 22.1 ms                                                | 20.8 ms: 1.06x faster                                         |
| django_template | 32.5 ms                                                | 32.7 ms: 1.01x slower                                         |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                  |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.9 ms: 2.41x faster                                         |
| json_dumps              | 12.7 ms                                                | 9.49 ms: 1.33x faster                                         |
| coroutines              | 26.1 ms                                                | 21.8 ms: 1.19x faster                                         |
| deltablue               | 3.64 ms                                                | 3.16 ms: 1.15x faster                                         |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.14x faster                                          |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.93 ms: 1.12x faster                                         |
| richards                | 46.2 ms                                                | 41.3 ms: 1.12x faster                                         |
| go                      | 143 ms                                                 | 131 ms: 1.09x faster                                          |
| json_loads              | 26.2 us                                                | 24.1 us: 1.09x faster                                         |
| genshi_xml              | 52.1 ms                                                | 47.9 ms: 1.09x faster                                         |
| sqlglot_normalize       | 108 ms                                                 | 99.8 ms: 1.08x faster                                         |
| chaos                   | 68.6 ms                                                | 63.5 ms: 1.08x faster                                         |
| pickle_pure_python      | 304 us                                                 | 281 us: 1.08x faster                                          |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.08x faster                                          |
| logging_silent          | 98.5 ns                                                | 91.7 ns: 1.07x faster                                         |
| json                    | 4.95 ms                                                | 4.61 ms: 1.07x faster                                         |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                          |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                          |
| hexiom                  | 6.35 ms                                                | 5.94 ms: 1.07x faster                                         |
| sqlglot_optimize        | 53.0 ms                                                | 49.7 ms: 1.07x faster                                         |
| deepcopy_memo           | 36.4 us                                                | 34.2 us: 1.07x faster                                         |
| scimark_fft             | 329 ms                                                 | 309 ms: 1.07x faster                                          |
| sympy_expand            | 472 ms                                                 | 444 ms: 1.06x faster                                          |
| genshi_text             | 22.1 ms                                                | 20.8 ms: 1.06x faster                                         |
| float                   | 76.3 ms                                                | 72.0 ms: 1.06x faster                                         |
| nqueens                 | 85.0 ms                                                | 80.3 ms: 1.06x faster                                         |
| mdp                     | 2.62 sec                                               | 2.48 sec: 1.06x faster                                        |
| logging_simple          | 6.06 us                                                | 5.73 us: 1.06x faster                                         |
| fannkuch                | 388 ms                                                 | 368 ms: 1.06x faster                                          |
| scimark_monte_carlo     | 68.3 ms                                                | 64.7 ms: 1.06x faster                                         |
| pycparser               | 1.17 sec                                               | 1.11 sec: 1.05x faster                                        |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                          |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.05x faster                                        |
| pickle_list             | 4.17 us                                                | 3.97 us: 1.05x faster                                         |
| async_tree_none         | 529 ms                                                 | 505 ms: 1.05x faster                                          |
| deepcopy                | 344 us                                                 | 328 us: 1.05x faster                                          |
| pickle_dict             | 31.4 us                                                | 30.0 us: 1.05x faster                                         |
| pyflate                 | 417 ms                                                 | 398 ms: 1.05x faster                                          |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                         |
| coverage                | 101 ms                                                 | 96.1 ms: 1.05x faster                                         |
| html5lib                | 63.2 ms                                                | 60.4 ms: 1.05x faster                                         |
| logging_format          | 6.62 us                                                | 6.33 us: 1.05x faster                                         |
| aiohttp                 | 1.05 ms                                                | 1.00 ms: 1.04x faster                                         |
| sympy_integrate         | 20.9 ms                                                | 20.1 ms: 1.04x faster                                         |
| spectral_norm           | 99.9 ms                                                | 96.2 ms: 1.04x faster                                         |
| 2to3                    | 257 ms                                                 | 248 ms: 1.04x faster                                          |
| async_tree_io           | 1.31 sec                                               | 1.26 sec: 1.04x faster                                        |
| bench_thread_pool       | 810 us                                                 | 783 us: 1.03x faster                                          |
| sympy_str               | 287 ms                                                 | 278 ms: 1.03x faster                                          |
| raytrace                | 290 ms                                                 | 281 ms: 1.03x faster                                          |
| telco                   | 6.62 ms                                                | 6.42 ms: 1.03x faster                                         |
| sqlalchemy_imperative   | 18.0 ms                                                | 17.5 ms: 1.03x faster                                         |
| pprint_safe_repr        | 691 ms                                                 | 671 ms: 1.03x faster                                          |
| docutils                | 2.60 sec                                               | 2.53 sec: 1.03x faster                                        |
| tornado_http            | 96.6 ms                                                | 94.3 ms: 1.03x faster                                         |
| async_tree_memoization  | 625 ms                                                 | 611 ms: 1.02x faster                                          |
| regex_v8                | 22.3 ms                                                | 21.8 ms: 1.02x faster                                         |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.02x faster                                          |
| async_tree_cpu_io_mixed | 752 ms                                                 | 739 ms: 1.02x faster                                          |
| chameleon               | 6.41 ms                                                | 6.32 ms: 1.01x faster                                         |
| unpack_sequence         | 43.4 ns                                                | 42.9 ns: 1.01x faster                                         |
| thrift                  | 752 us                                                 | 742 us: 1.01x faster                                          |
| nbody                   | 95.0 ms                                                | 94.0 ms: 1.01x faster                                         |
| sympy_sum               | 166 ms                                                 | 164 ms: 1.01x faster                                          |
| sqlalchemy_declarative  | 139 ms                                                 | 137 ms: 1.01x faster                                          |
| dulwich_log             | 63.9 ms                                                | 63.6 ms: 1.01x faster                                         |
| pathlib                 | 18.2 ms                                                | 18.3 ms: 1.01x slower                                         |
| django_template         | 32.5 ms                                                | 32.7 ms: 1.01x slower                                         |
| regex_dna               | 203 ms                                                 | 207 ms: 1.02x slower                                          |
| pickle                  | 9.79 us                                                | 10.0 us: 1.02x slower                                         |
| xml_etree_process       | 53.8 ms                                                | 55.5 ms: 1.03x slower                                         |
| unpickle_list           | 4.95 us                                                | 5.13 us: 1.04x slower                                         |
| sqlglot_transpile       | 1.66 ms                                                | 1.72 ms: 1.04x slower                                         |
| sqlglot_parse           | 1.37 ms                                                | 1.44 ms: 1.05x slower                                         |
| sqlite_synth            | 2.49 us                                                | 2.63 us: 1.05x slower                                         |
| xml_etree_generate      | 76.2 ms                                                | 80.6 ms: 1.06x slower                                         |
| python_startup          | 8.36 ms                                                | 8.96 ms: 1.07x slower                                         |
| python_startup_no_site  | 5.96 ms                                                | 6.50 ms: 1.09x slower                                         |
| regex_effbot            | 3.36 ms                                                | 3.69 ms: 1.10x slower                                         |
| async_generators        | 359 ms                                                 | 417 ms: 1.16x slower                                          |
| Geometric mean          | (ref)                                                  | 1.05x faster                                                  |

Benchmark hidden because not significant (7): deepcopy_reduce, xml_etree_iterparse, crypto_pyaes, mako, bench_mp_pool, scimark_lu, unpickle
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230220-3.12.0a5+-9f0fc5b/bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
