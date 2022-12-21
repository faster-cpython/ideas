Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 223 ms: 1.00x slower                                                |
| docutils       | 1.76 sec                                               | 1.77 sec: 1.00x slower                                              |
| html5lib       | 44.0 ms                                                | 46.5 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                  | 1.02x slower                                                        |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 92.6 ms: 1.02x faster                                               |
| Geometric mean | (ref)                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 96.5 ms: 1.00x slower                                               |
| regex_dna      | 164 ms                                                 | 180 ms: 1.10x slower                                                |
| regex_effbot   | 2.45 ms                                                | 2.64 ms: 1.08x slower                                               |
| regex_v8       | 17.7 ms                                                | 18.3 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                  | 1.05x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 8.25 ms: 1.01x faster                                               |
| pickle               | 7.50 us                                                | 7.56 us: 1.01x slower                                               |
| pickle_dict          | 18.0 us                                                | 18.8 us: 1.05x slower                                               |
| pickle_list          | 2.83 us                                                | 2.96 us: 1.05x slower                                               |
| unpickle             | 10.0 us                                                | 9.87 us: 1.02x faster                                               |
| unpickle_pure_python | 204 us                                                 | 203 us: 1.00x faster                                                |
| xml_etree_parse      | 100 ms                                                 | 100 ms: 1.00x slower                                                |
| xml_etree_generate   | 54.5 ms                                                | 54.3 ms: 1.00x faster                                               |
| xml_etree_process    | 45.1 ms                                                | 44.9 ms: 1.00x faster                                               |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (4): json_loads, pickle_pure_python, unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.57 ms: 1.00x faster                                               |
| python_startup_no_site | 7.00 ms                                                | 6.95 ms: 1.01x faster                                               |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml     | 37.7 ms                                                | 37.3 ms: 1.01x faster                                               |
| mako           | 10.6 ms                                                | 10.7 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-1dd9be6584413fbfa823-3.10.9-1dd9be6 |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 223 ms: 1.00x slower                                                |
| bench_thread_pool       | 531 us                                                 | 518 us: 1.02x faster                                                |
| coroutines              | 20.1 ms                                                | 20.1 ms: 1.00x slower                                               |
| coverage                | 40.8 ms                                                | 40.6 ms: 1.00x faster                                               |
| deepcopy                | 278 us                                                 | 280 us: 1.01x slower                                                |
| deepcopy_reduce         | 2.36 us                                                | 2.34 us: 1.01x faster                                               |
| deltablue               | 5.37 ms                                                | 5.15 ms: 1.04x faster                                               |
| docutils                | 1.76 sec                                               | 1.77 sec: 1.00x slower                                              |
| dulwich_log             | 36.4 ms                                                | 36.7 ms: 1.01x slower                                               |
| generators              | 32.5 ms                                                | 32.4 ms: 1.00x faster                                               |
| genshi_xml              | 37.7 ms                                                | 37.3 ms: 1.01x faster                                               |
| go                      | 165 ms                                                 | 165 ms: 1.00x slower                                                |
| hexiom                  | 6.31 ms                                                | 6.30 ms: 1.00x faster                                               |
| html5lib                | 44.0 ms                                                | 46.5 ms: 1.06x slower                                               |
| json                    | 3.13 ms                                                | 3.11 ms: 1.00x faster                                               |
| json_dumps              | 8.34 ms                                                | 8.25 ms: 1.01x faster                                               |
| logging_format          | 4.95 us                                                | 4.99 us: 1.01x slower                                               |
| logging_silent          | 119 ns                                                 | 118 ns: 1.01x faster                                                |
| logging_simple          | 4.61 us                                                | 4.63 us: 1.01x slower                                               |
| mako                    | 10.6 ms                                                | 10.7 ms: 1.01x slower                                               |
| mdp                     | 1.66 sec                                               | 1.66 sec: 1.00x slower                                              |
| meteor_contest          | 77.7 ms                                                | 77.4 ms: 1.00x faster                                               |
| mypy                    | 521 ms                                                 | 524 ms: 1.01x slower                                                |
| nbody                   | 94.6 ms                                                | 92.6 ms: 1.02x faster                                               |
| nqueens                 | 68.6 ms                                                | 68.1 ms: 1.01x faster                                               |
| pathlib                 | 22.2 ms                                                | 22.0 ms: 1.01x faster                                               |
| pickle                  | 7.50 us                                                | 7.56 us: 1.01x slower                                               |
| pickle_dict             | 18.0 us                                                | 18.8 us: 1.05x slower                                               |
| pickle_list             | 2.83 us                                                | 2.96 us: 1.05x slower                                               |
| pprint_safe_repr        | 608 ms                                                 | 603 ms: 1.01x faster                                                |
| pprint_pformat          | 1.24 sec                                               | 1.23 sec: 1.01x faster                                              |
| pylint                  | 302 ms                                                 | 300 ms: 1.00x faster                                                |
| python_startup          | 9.59 ms                                                | 9.57 ms: 1.00x faster                                               |
| python_startup_no_site  | 7.00 ms                                                | 6.95 ms: 1.01x faster                                               |
| raytrace                | 329 ms                                                 | 327 ms: 1.01x faster                                                |
| regex_compile           | 96.2 ms                                                | 96.5 ms: 1.00x slower                                               |
| regex_dna               | 164 ms                                                 | 180 ms: 1.10x slower                                                |
| regex_effbot            | 2.45 ms                                                | 2.64 ms: 1.08x slower                                               |
| regex_v8                | 17.7 ms                                                | 18.3 ms: 1.03x slower                                               |
| richards                | 51.4 ms                                                | 51.0 ms: 1.01x faster                                               |
| scimark_fft             | 231 ms                                                 | 230 ms: 1.01x faster                                                |
| scimark_lu              | 110 ms                                                 | 110 ms: 1.00x faster                                                |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.46 ms: 1.00x faster                                               |
| spectral_norm           | 95.8 ms                                                | 96.2 ms: 1.00x slower                                               |
| sqlalchemy_imperative   | 9.01 ms                                                | 8.96 ms: 1.01x faster                                               |
| sqlglot_parse           | 1.33 ms                                                | 1.33 ms: 1.01x slower                                               |
| sqlglot_transpile       | 1.54 ms                                                | 1.55 ms: 1.00x slower                                               |
| sqlglot_optimize        | 38.1 ms                                                | 37.9 ms: 1.00x faster                                               |
| sqlglot_normalize       | 198 ms                                                 | 196 ms: 1.01x faster                                                |
| sqlite_synth            | 1.50 us                                                | 1.49 us: 1.01x faster                                               |
| sympy_expand            | 275 ms                                                 | 276 ms: 1.00x slower                                                |
| sympy_integrate         | 13.3 ms                                                | 13.4 ms: 1.01x slower                                               |
| sympy_sum               | 93.5 ms                                                | 95.4 ms: 1.02x slower                                               |
| sympy_str               | 169 ms                                                 | 170 ms: 1.00x slower                                                |
| telco                   | 3.63 ms                                                | 3.64 ms: 1.00x slower                                               |
| thrift                  | 577 us                                                 | 582 us: 1.01x slower                                                |
| unpack_sequence         | 38.2 ns                                                | 37.4 ns: 1.02x faster                                               |
| unpickle                | 10.0 us                                                | 9.87 us: 1.02x faster                                               |
| unpickle_pure_python    | 204 us                                                 | 203 us: 1.00x faster                                                |
| xml_etree_parse         | 100 ms                                                 | 100 ms: 1.00x slower                                                |
| xml_etree_generate      | 54.5 ms                                                | 54.3 ms: 1.00x faster                                               |
| xml_etree_process       | 45.1 ms                                                | 44.9 ms: 1.00x faster                                               |
| Geometric mean          | (ref)                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (28): aiohttp, async_generators, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, chameleon, chaos, bench_mp_pool, crypto_pyaes, deepcopy_memo, django_template, fannkuch, flaskblogging, float, genshi_text, gunicorn, json_loads, pickle_pure_python, pidigits, pycparser, pyflate, scimark_monte_carlo, scimark_sor, sqlalchemy_declarative, tornado_http, unpickle_list, xml_etree_iterparse
