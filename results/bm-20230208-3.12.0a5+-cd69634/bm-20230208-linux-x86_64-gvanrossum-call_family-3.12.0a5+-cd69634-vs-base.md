
# Results vs. base

- fork: gvanrossum
- ref: call_family
- machine: linux-x86_64
- commit hash: cd69634
- commit date: 2023-02-08
- overall geometric mean: 1.00x slower

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (5): 2to3, chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 192 ms                                                                 | 189 ms: 1.02x faster                                              |
| float          | 73.4 ms                                                                | 74.0 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 218 ms                                                                 | 206 ms: 1.06x faster                                              |
| regex_v8       | 20.8 ms                                                                | 21.0 ms: 1.01x slower                                             |
| regex_compile  | 128 ms                                                                 | 129 ms: 1.01x slower                                              |
| regex_effbot   | 3.55 ms                                                                | 3.64 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_list          | 4.21 us                                                                | 4.03 us: 1.04x faster                                             |
| pickle_dict          | 31.2 us                                                                | 30.3 us: 1.03x faster                                             |
| json_dumps           | 9.56 ms                                                                | 9.44 ms: 1.01x faster                                             |
| unpickle_list        | 5.02 us                                                                | 4.97 us: 1.01x faster                                             |
| json_loads           | 24.0 us                                                                | 23.8 us: 1.01x faster                                             |
| pickle               | 10.2 us                                                                | 10.1 us: 1.00x faster                                             |
| unpickle_pure_python | 197 us                                                                 | 199 us: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (6): xml_etree_iterparse, xml_etree_parse, pickle_pure_python, xml_etree_process, unpickle, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.91 ms                                                                | 8.91 ms: 1.00x slower                                             |
| python_startup_no_site | 6.47 ms                                                                | 6.47 ms: 1.00x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml     | 47.8 ms                                                                | 47.1 ms: 1.02x faster                                             |
| genshi_text    | 20.7 ms                                                                | 20.5 ms: 1.01x faster                                             |
| mako           | 9.72 ms                                                                | 9.97 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mdp                     | 2.71 sec                                                               | 2.48 sec: 1.09x faster                                            |
| regex_dna               | 218 ms                                                                 | 206 ms: 1.06x faster                                              |
| pickle_list             | 4.21 us                                                                | 4.03 us: 1.04x faster                                             |
| pycparser               | 1.13 sec                                                               | 1.09 sec: 1.04x faster                                            |
| generators              | 74.8 ms                                                                | 72.1 ms: 1.04x faster                                             |
| coroutines              | 25.2 ms                                                                | 24.3 ms: 1.04x faster                                             |
| pickle_dict             | 31.2 us                                                                | 30.3 us: 1.03x faster                                             |
| async_tree_memoization  | 653 ms                                                                 | 637 ms: 1.03x faster                                              |
| fannkuch                | 364 ms                                                                 | 356 ms: 1.02x faster                                              |
| crypto_pyaes            | 74.0 ms                                                                | 72.7 ms: 1.02x faster                                             |
| pidigits                | 192 ms                                                                 | 189 ms: 1.02x faster                                              |
| telco                   | 6.47 ms                                                                | 6.36 ms: 1.02x faster                                             |
| genshi_xml              | 47.8 ms                                                                | 47.1 ms: 1.02x faster                                             |
| scimark_sor             | 106 ms                                                                 | 105 ms: 1.01x faster                                              |
| json_dumps              | 9.56 ms                                                                | 9.44 ms: 1.01x faster                                             |
| json                    | 4.69 ms                                                                | 4.64 ms: 1.01x faster                                             |
| unpickle_list           | 5.02 us                                                                | 4.97 us: 1.01x faster                                             |
| genshi_text             | 20.7 ms                                                                | 20.5 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed | 759 ms                                                                 | 752 ms: 1.01x faster                                              |
| json_loads              | 24.0 us                                                                | 23.8 us: 1.01x faster                                             |
| nqueens                 | 79.8 ms                                                                | 79.2 ms: 1.01x faster                                             |
| go                      | 139 ms                                                                 | 138 ms: 1.01x faster                                              |
| deltablue               | 3.18 ms                                                                | 3.17 ms: 1.01x faster                                             |
| create_gc_cycles        | 1.47 ms                                                                | 1.46 ms: 1.01x faster                                             |
| pickle                  | 10.2 us                                                                | 10.1 us: 1.00x faster                                             |
| pyflate                 | 409 ms                                                                 | 407 ms: 1.00x faster                                              |
| python_startup          | 8.91 ms                                                                | 8.91 ms: 1.00x slower                                             |
| python_startup_no_site  | 6.47 ms                                                                | 6.47 ms: 1.00x slower                                             |
| aiohttp                 | 1.00 ms                                                                | 1.00 ms: 1.00x slower                                             |
| regex_v8                | 20.8 ms                                                                | 21.0 ms: 1.01x slower                                             |
| richards                | 42.0 ms                                                                | 42.3 ms: 1.01x slower                                             |
| sympy_integrate         | 19.7 ms                                                                | 19.8 ms: 1.01x slower                                             |
| async_generators        | 344 ms                                                                 | 346 ms: 1.01x slower                                              |
| mypy2                   | 329 ms                                                                 | 331 ms: 1.01x slower                                              |
| deepcopy_reduce         | 2.94 us                                                                | 2.96 us: 1.01x slower                                             |
| sqlglot_optimize        | 51.0 ms                                                                | 51.4 ms: 1.01x slower                                             |
| float                   | 73.4 ms                                                                | 74.0 ms: 1.01x slower                                             |
| deepcopy                | 329 us                                                                 | 332 us: 1.01x slower                                              |
| dulwich_log             | 62.8 ms                                                                | 63.4 ms: 1.01x slower                                             |
| scimark_sparse_mat_mult | 3.97 ms                                                                | 4.01 ms: 1.01x slower                                             |
| unpickle_pure_python    | 197 us                                                                 | 199 us: 1.01x slower                                              |
| sqlglot_normalize       | 105 ms                                                                 | 106 ms: 1.01x slower                                              |
| regex_compile           | 128 ms                                                                 | 129 ms: 1.01x slower                                              |
| raytrace                | 285 ms                                                                 | 288 ms: 1.01x slower                                              |
| sympy_sum               | 154 ms                                                                 | 156 ms: 1.01x slower                                              |
| scimark_lu              | 107 ms                                                                 | 108 ms: 1.01x slower                                              |
| chaos                   | 65.7 ms                                                                | 66.7 ms: 1.02x slower                                             |
| coverage                | 97.0 ms                                                                | 98.8 ms: 1.02x slower                                             |
| pprint_pformat          | 1.40 sec                                                               | 1.43 sec: 1.02x slower                                            |
| sqlglot_transpile       | 1.70 ms                                                                | 1.74 ms: 1.02x slower                                             |
| pprint_safe_repr        | 683 ms                                                                 | 697 ms: 1.02x slower                                              |
| logging_format          | 6.32 us                                                                | 6.46 us: 1.02x slower                                             |
| sqlglot_parse           | 1.41 ms                                                                | 1.44 ms: 1.02x slower                                             |
| hexiom                  | 5.90 ms                                                                | 6.02 ms: 1.02x slower                                             |
| sqlalchemy_imperative   | 17.7 ms                                                                | 18.1 ms: 1.02x slower                                             |
| pathlib                 | 17.6 ms                                                                | 18.0 ms: 1.02x slower                                             |
| regex_effbot            | 3.55 ms                                                                | 3.64 ms: 1.02x slower                                             |
| mako                    | 9.72 ms                                                                | 9.97 ms: 1.03x slower                                             |
| scimark_monte_carlo     | 64.2 ms                                                                | 65.8 ms: 1.03x slower                                             |
| deepcopy_memo           | 34.0 us                                                                | 34.9 us: 1.03x slower                                             |
| logging_simple          | 5.68 us                                                                | 5.88 us: 1.03x slower                                             |
| unpack_sequence         | 42.2 ns                                                                | 44.4 ns: 1.05x slower                                             |
| logging_silent          | 91.6 ns                                                                | 96.3 ns: 1.05x slower                                             |
| gc_traversal            | 3.80 ms                                                                | 4.17 ms: 1.10x slower                                             |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (28): xml_etree_iterparse, xml_etree_parse, nbody, pickle_pure_python, sympy_expand, thrift, sqlite_synth, django_template, asyncio_tcp, xml_etree_process, unpickle, chameleon, 2to3, bench_mp_pool, gunicorn, spectral_norm, xml_etree_generate, bench_thread_pool, docutils, async_tree_none, async_tree_io, scimark_fft, tornado_http, sympy_str, sqlalchemy_declarative, meteor_contest, html5lib, djangocms
