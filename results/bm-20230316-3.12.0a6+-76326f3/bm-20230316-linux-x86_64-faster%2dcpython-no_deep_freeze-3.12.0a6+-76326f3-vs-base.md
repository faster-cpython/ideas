
# Results vs. base

- fork: faster-cpython
- ref: no_deep_freeze
- machine: linux-x86_64
- commit hash: 76326f3
- commit date: 2023-03-16
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6+-4f5774f | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 252 ms: 1.01x slower                                                       |
| chameleon      | 6.28 ms                                                                | 6.36 ms: 1.01x slower                                                      |
| docutils       | 2.53 sec                                                               | 2.52 sec: 1.00x faster                                                     |
| html5lib       | 60.7 ms                                                                | 59.2 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6+-4f5774f | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 193 ms                                                                 | 189 ms: 1.02x faster                                                       |
| float          | 73.0 ms                                                                | 73.7 ms: 1.01x slower                                                      |
| nbody          | 87.0 ms                                                                | 88.2 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6+-4f5774f | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.55 ms                                                                | 3.45 ms: 1.03x faster                                                      |
| regex_dna      | 202 ms                                                                 | 204 ms: 1.01x slower                                                       |
| regex_v8       | 21.8 ms                                                                | 25.6 ms: 1.17x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6+-4f5774f | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 31.6 us                                                                | 30.0 us: 1.05x faster                                                      |
| pickle               | 10.5 us                                                                | 10.2 us: 1.03x faster                                                      |
| pickle_list          | 4.27 us                                                                | 4.21 us: 1.01x faster                                                      |
| json_loads           | 24.1 us                                                                | 23.9 us: 1.01x faster                                                      |
| xml_etree_iterparse  | 99.0 ms                                                                | 99.7 ms: 1.01x slower                                                      |
| unpickle_pure_python | 197 us                                                                 | 199 us: 1.01x slower                                                       |
| xml_etree_process    | 55.7 ms                                                                | 56.4 ms: 1.01x slower                                                      |
| xml_etree_generate   | 80.6 ms                                                                | 81.8 ms: 1.01x slower                                                      |
| unpickle_list        | 4.92 us                                                                | 5.32 us: 1.08x slower                                                      |
| unpickle             | 13.4 us                                                                | 14.5 us: 1.08x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (3): pickle_pure_python, json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6+-4f5774f | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.51 ms                                                                | 6.48 ms: 1.01x faster                                                      |
| python_startup         | 8.90 ms                                                                | 9.51 ms: 1.07x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6+-4f5774f | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 9.97 ms                                                                | 10.2 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (3): genshi_text, genshi_xml, django_template

All benchmarks:
===============

| Benchmark               | bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6+-4f5774f | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization  | 642 ms                                                                 | 606 ms: 1.06x faster                                                       |
| pickle_dict             | 31.6 us                                                                | 30.0 us: 1.05x faster                                                      |
| pickle                  | 10.5 us                                                                | 10.2 us: 1.03x faster                                                      |
| regex_effbot            | 3.55 ms                                                                | 3.45 ms: 1.03x faster                                                      |
| html5lib                | 60.7 ms                                                                | 59.2 ms: 1.03x faster                                                      |
| scimark_lu              | 109 ms                                                                 | 106 ms: 1.02x faster                                                       |
| scimark_fft             | 311 ms                                                                 | 304 ms: 1.02x faster                                                       |
| json                    | 4.62 ms                                                                | 4.54 ms: 1.02x faster                                                      |
| logging_silent          | 95.0 ns                                                                | 93.4 ns: 1.02x faster                                                      |
| pidigits                | 193 ms                                                                 | 189 ms: 1.02x faster                                                       |
| pickle_list             | 4.27 us                                                                | 4.21 us: 1.01x faster                                                      |
| go                      | 134 ms                                                                 | 132 ms: 1.01x faster                                                       |
| dulwich_log             | 63.1 ms                                                                | 62.3 ms: 1.01x faster                                                      |
| coroutines              | 22.4 ms                                                                | 22.2 ms: 1.01x faster                                                      |
| asyncio_tcp             | 512 ms                                                                 | 507 ms: 1.01x faster                                                       |
| deltablue               | 3.17 ms                                                                | 3.15 ms: 1.01x faster                                                      |
| gunicorn                | 1.08 ms                                                                | 1.07 ms: 1.01x faster                                                      |
| aiohttp                 | 1.00 ms                                                                | 996 us: 1.01x faster                                                       |
| json_loads              | 24.1 us                                                                | 23.9 us: 1.01x faster                                                      |
| comprehensions          | 23.8 us                                                                | 23.6 us: 1.01x faster                                                      |
| python_startup_no_site  | 6.51 ms                                                                | 6.48 ms: 1.01x faster                                                      |
| mdp                     | 2.41 sec                                                               | 2.40 sec: 1.00x faster                                                     |
| docutils                | 2.53 sec                                                               | 2.52 sec: 1.00x faster                                                     |
| crypto_pyaes            | 74.2 ms                                                                | 74.4 ms: 1.00x slower                                                      |
| hexiom                  | 6.07 ms                                                                | 6.10 ms: 1.00x slower                                                      |
| sqlglot_optimize        | 51.2 ms                                                                | 51.4 ms: 1.00x slower                                                      |
| sympy_expand            | 462 ms                                                                 | 464 ms: 1.00x slower                                                       |
| deepcopy                | 327 us                                                                 | 328 us: 1.01x slower                                                       |
| create_gc_cycles        | 1.48 ms                                                                | 1.48 ms: 1.01x slower                                                      |
| bench_thread_pool       | 786 us                                                                 | 791 us: 1.01x slower                                                       |
| xml_etree_iterparse     | 99.0 ms                                                                | 99.7 ms: 1.01x slower                                                      |
| async_tree_io           | 1.29 sec                                                               | 1.30 sec: 1.01x slower                                                     |
| scimark_monte_carlo     | 66.6 ms                                                                | 67.0 ms: 1.01x slower                                                      |
| unpickle_pure_python    | 197 us                                                                 | 199 us: 1.01x slower                                                       |
| deepcopy_reduce         | 2.94 us                                                                | 2.96 us: 1.01x slower                                                      |
| deepcopy_memo           | 33.4 us                                                                | 33.7 us: 1.01x slower                                                      |
| unpack_sequence         | 42.4 ns                                                                | 42.8 ns: 1.01x slower                                                      |
| float                   | 73.0 ms                                                                | 73.7 ms: 1.01x slower                                                      |
| 2to3                    | 249 ms                                                                 | 252 ms: 1.01x slower                                                       |
| spectral_norm           | 89.6 ms                                                                | 90.6 ms: 1.01x slower                                                      |
| xml_etree_process       | 55.7 ms                                                                | 56.4 ms: 1.01x slower                                                      |
| chaos                   | 65.9 ms                                                                | 66.7 ms: 1.01x slower                                                      |
| chameleon               | 6.28 ms                                                                | 6.36 ms: 1.01x slower                                                      |
| nbody                   | 87.0 ms                                                                | 88.2 ms: 1.01x slower                                                      |
| regex_dna               | 202 ms                                                                 | 204 ms: 1.01x slower                                                       |
| xml_etree_generate      | 80.6 ms                                                                | 81.8 ms: 1.01x slower                                                      |
| logging_format          | 6.25 us                                                                | 6.34 us: 1.01x slower                                                      |
| sqlite_synth            | 2.61 us                                                                | 2.65 us: 1.02x slower                                                      |
| richards                | 42.0 ms                                                                | 42.6 ms: 1.02x slower                                                      |
| telco                   | 6.46 ms                                                                | 6.56 ms: 1.02x slower                                                      |
| generators              | 29.4 ms                                                                | 29.9 ms: 1.02x slower                                                      |
| raytrace                | 276 ms                                                                 | 282 ms: 1.02x slower                                                       |
| mako                    | 9.97 ms                                                                | 10.2 ms: 1.02x slower                                                      |
| async_tree_none         | 524 ms                                                                 | 535 ms: 1.02x slower                                                       |
| fannkuch                | 361 ms                                                                 | 371 ms: 1.03x slower                                                       |
| nqueens                 | 78.7 ms                                                                | 81.1 ms: 1.03x slower                                                      |
| async_tree_cpu_io_mixed | 744 ms                                                                 | 770 ms: 1.03x slower                                                       |
| gc_traversal            | 3.54 ms                                                                | 3.68 ms: 1.04x slower                                                      |
| pyflate                 | 405 ms                                                                 | 423 ms: 1.04x slower                                                       |
| scimark_sparse_mat_mult | 4.17 ms                                                                | 4.37 ms: 1.05x slower                                                      |
| pycparser               | 1.11 sec                                                               | 1.17 sec: 1.06x slower                                                     |
| python_startup          | 8.90 ms                                                                | 9.51 ms: 1.07x slower                                                      |
| unpickle_list           | 4.92 us                                                                | 5.32 us: 1.08x slower                                                      |
| unpickle                | 13.4 us                                                                | 14.5 us: 1.08x slower                                                      |
| regex_v8                | 21.8 ms                                                                | 25.6 ms: 1.17x slower                                                      |
| mypy2                   | 333 ms                                                                 | 446 ms: 1.34x slower                                                       |
| Geometric mean          | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (28): djangocms, thrift, sqlalchemy_declarative, pickle_pure_python, dask, coverage, sympy_sum, regex_compile, pathlib, pprint_pformat, tornado_http, sqlglot_transpile, async_generators, sympy_integrate, sympy_str, genshi_text, genshi_xml, bench_mp_pool, pprint_safe_repr, sqlglot_parse, json_dumps, xml_etree_parse, logging_simple, django_template, sqlglot_normalize, scimark_sor, meteor_contest, sqlalchemy_imperative
