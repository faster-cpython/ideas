
# Results vs. base

- fork: gvanrossum
- ref: call_family
- machine: linux-x86_64
- commit hash: 9595e01
- commit date: 2023-02-07
- overall geometric mean: 1.00x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| chameleon      | 6.44 ms                                                                | 6.36 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 95.0 ms                                                                | 96.0 ms: 1.01x slower                                             |
| pidigits       | 192 ms                                                                 | 197 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 218 ms                                                                 | 205 ms: 1.06x faster                                              |
| regex_effbot   | 3.55 ms                                                                | 3.62 ms: 1.02x slower                                             |
| regex_v8       | 20.8 ms                                                                | 21.7 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_list          | 4.21 us                                                                | 4.14 us: 1.02x faster                                             |
| xml_etree_generate   | 77.0 ms                                                                | 77.4 ms: 1.00x slower                                             |
| unpickle_pure_python | 197 us                                                                 | 199 us: 1.01x slower                                              |
| pickle_dict          | 31.2 us                                                                | 31.6 us: 1.01x slower                                             |
| json_loads           | 24.0 us                                                                | 24.3 us: 1.01x slower                                             |
| xml_etree_parse      | 146 ms                                                                 | 148 ms: 1.01x slower                                              |
| pickle               | 10.2 us                                                                | 10.4 us: 1.02x slower                                             |
| unpickle             | 13.0 us                                                                | 13.3 us: 1.02x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (5): pickle_pure_python, json_dumps, unpickle_list, xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.91 ms                                                                | 8.91 ms: 1.00x slower                                             |
| python_startup_no_site | 6.47 ms                                                                | 6.47 ms: 1.00x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 47.8 ms                                                                | 46.5 ms: 1.03x faster                                             |
| django_template | 33.2 ms                                                                | 32.6 ms: 1.02x faster                                             |
| mako            | 9.72 ms                                                                | 9.92 ms: 1.02x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5+-a9f0144 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna               | 218 ms                                                                 | 205 ms: 1.06x faster                                              |
| mdp                     | 2.71 sec                                                               | 2.59 sec: 1.05x faster                                            |
| go                      | 139 ms                                                                 | 133 ms: 1.04x faster                                              |
| genshi_xml              | 47.8 ms                                                                | 46.5 ms: 1.03x faster                                             |
| coroutines              | 25.2 ms                                                                | 24.5 ms: 1.03x faster                                             |
| fannkuch                | 364 ms                                                                 | 355 ms: 1.03x faster                                              |
| crypto_pyaes            | 74.0 ms                                                                | 72.6 ms: 1.02x faster                                             |
| django_template         | 33.2 ms                                                                | 32.6 ms: 1.02x faster                                             |
| pickle_list             | 4.21 us                                                                | 4.14 us: 1.02x faster                                             |
| unpack_sequence         | 42.2 ns                                                                | 41.6 ns: 1.02x faster                                             |
| coverage                | 97.0 ms                                                                | 95.6 ms: 1.01x faster                                             |
| chameleon               | 6.44 ms                                                                | 6.36 ms: 1.01x faster                                             |
| pyflate                 | 409 ms                                                                 | 404 ms: 1.01x faster                                              |
| sqlite_synth            | 2.60 us                                                                | 2.58 us: 1.01x faster                                             |
| thrift                  | 742 us                                                                 | 735 us: 1.01x faster                                              |
| deltablue               | 3.18 ms                                                                | 3.16 ms: 1.01x faster                                             |
| python_startup          | 8.91 ms                                                                | 8.91 ms: 1.00x slower                                             |
| python_startup_no_site  | 6.47 ms                                                                | 6.47 ms: 1.00x slower                                             |
| dulwich_log             | 62.8 ms                                                                | 63.0 ms: 1.00x slower                                             |
| sympy_integrate         | 19.7 ms                                                                | 19.7 ms: 1.00x slower                                             |
| xml_etree_generate      | 77.0 ms                                                                | 77.4 ms: 1.00x slower                                             |
| create_gc_cycles        | 1.47 ms                                                                | 1.48 ms: 1.01x slower                                             |
| sqlglot_normalize       | 105 ms                                                                 | 105 ms: 1.01x slower                                              |
| async_generators        | 344 ms                                                                 | 347 ms: 1.01x slower                                              |
| chaos                   | 65.7 ms                                                                | 66.1 ms: 1.01x slower                                             |
| sqlglot_optimize        | 51.0 ms                                                                | 51.4 ms: 1.01x slower                                             |
| unpickle_pure_python    | 197 us                                                                 | 199 us: 1.01x slower                                              |
| pprint_safe_repr        | 683 ms                                                                 | 689 ms: 1.01x slower                                              |
| sqlglot_transpile       | 1.70 ms                                                                | 1.72 ms: 1.01x slower                                             |
| sympy_sum               | 154 ms                                                                 | 156 ms: 1.01x slower                                              |
| nbody                   | 95.0 ms                                                                | 96.0 ms: 1.01x slower                                             |
| pickle_dict             | 31.2 us                                                                | 31.6 us: 1.01x slower                                             |
| sqlalchemy_declarative  | 137 ms                                                                 | 138 ms: 1.01x slower                                              |
| hexiom                  | 5.90 ms                                                                | 5.96 ms: 1.01x slower                                             |
| generators              | 74.8 ms                                                                | 75.7 ms: 1.01x slower                                             |
| sqlglot_parse           | 1.41 ms                                                                | 1.43 ms: 1.01x slower                                             |
| json_loads              | 24.0 us                                                                | 24.3 us: 1.01x slower                                             |
| xml_etree_parse         | 146 ms                                                                 | 148 ms: 1.01x slower                                              |
| deepcopy_reduce         | 2.94 us                                                                | 2.98 us: 1.01x slower                                             |
| nqueens                 | 79.8 ms                                                                | 81.0 ms: 1.02x slower                                             |
| scimark_fft             | 305 ms                                                                 | 309 ms: 1.02x slower                                              |
| scimark_sparse_mat_mult | 3.97 ms                                                                | 4.04 ms: 1.02x slower                                             |
| pickle                  | 10.2 us                                                                | 10.4 us: 1.02x slower                                             |
| meteor_contest          | 106 ms                                                                 | 108 ms: 1.02x slower                                              |
| unpickle                | 13.0 us                                                                | 13.3 us: 1.02x slower                                             |
| scimark_sor             | 106 ms                                                                 | 108 ms: 1.02x slower                                              |
| pycparser               | 1.13 sec                                                               | 1.15 sec: 1.02x slower                                            |
| deepcopy                | 329 us                                                                 | 336 us: 1.02x slower                                              |
| logging_silent          | 91.6 ns                                                                | 93.3 ns: 1.02x slower                                             |
| regex_effbot            | 3.55 ms                                                                | 3.62 ms: 1.02x slower                                             |
| mako                    | 9.72 ms                                                                | 9.92 ms: 1.02x slower                                             |
| pathlib                 | 17.6 ms                                                                | 18.0 ms: 1.02x slower                                             |
| logging_format          | 6.32 us                                                                | 6.48 us: 1.03x slower                                             |
| pidigits                | 192 ms                                                                 | 197 ms: 1.03x slower                                              |
| gc_traversal            | 3.80 ms                                                                | 3.91 ms: 1.03x slower                                             |
| deepcopy_memo           | 34.0 us                                                                | 35.0 us: 1.03x slower                                             |
| scimark_monte_carlo     | 64.2 ms                                                                | 66.2 ms: 1.03x slower                                             |
| logging_simple          | 5.68 us                                                                | 5.89 us: 1.04x slower                                             |
| regex_v8                | 20.8 ms                                                                | 21.7 ms: 1.04x slower                                             |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (33): async_tree_memoization, raytrace, spectral_norm, pickle_pure_python, json_dumps, async_tree_cpu_io_mixed, unpickle_list, async_tree_io, tornado_http, telco, sympy_expand, async_tree_none, gunicorn, xml_etree_process, bench_mp_pool, 2to3, genshi_text, bench_thread_pool, scimark_lu, aiohttp, docutils, pprint_pformat, sympy_str, mypy2, regex_compile, asyncio_tcp, json, float, xml_etree_iterparse, richards, djangocms, sqlalchemy_imperative, html5lib
