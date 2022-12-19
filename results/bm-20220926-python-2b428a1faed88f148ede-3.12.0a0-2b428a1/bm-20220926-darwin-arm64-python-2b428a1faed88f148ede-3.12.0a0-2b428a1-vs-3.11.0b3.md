Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.73 ms                                                               | 4.67 ms: 1.01x faster                                                 |
| docutils       | 1.46 sec                                                              | 1.47 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 56.5 ms: 1.02x slower                                                 |
| nbody          | 63.8 ms                                                               | 64.8 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 75.6 ms: 1.03x faster                                                 |
| regex_dna      | 149 ms                                                                | 152 ms: 1.01x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.63 ms: 1.10x slower                                                 |
| regex_v8       | 16.8 ms                                                               | 16.3 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.09 ms: 1.26x faster                                                 |
| json_loads           | 16.4 us                                                               | 16.2 us: 1.01x faster                                                 |
| pickle               | 7.14 us                                                               | 7.55 us: 1.06x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.86 us: 1.05x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 205 us: 1.08x faster                                                  |
| unpickle             | 9.97 us                                                               | 9.74 us: 1.02x faster                                                 |
| unpickle_list        | 2.77 us                                                               | 2.54 us: 1.09x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 162 us: 1.08x faster                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 96.6 ms: 1.03x faster                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 47.6 ms: 1.01x faster                                                 |
| xml_etree_process    | 34.8 ms                                                               | 35.0 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.03x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.08 ms: 1.02x faster                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.15 ms: 1.02x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.02x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.8 ms: 1.04x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 15.4 ms: 1.01x faster                                                 |
| genshi_xml      | 31.3 ms                                                               | 30.2 ms: 1.04x faster                                                 |
| mako            | 8.44 ms                                                               | 8.16 ms: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1 |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| async_generators        | 197 ms                                                                | 200 ms: 1.01x slower                                                  |
| async_tree_none         | 287 ms                                                                | 285 ms: 1.01x faster                                                  |
| async_tree_io           | 702 ms                                                                | 736 ms: 1.05x slower                                                  |
| async_tree_memoization  | 346 ms                                                                | 383 ms: 1.11x slower                                                  |
| chameleon               | 4.73 ms                                                               | 4.67 ms: 1.01x faster                                                 |
| chaos                   | 49.5 ms                                                               | 50.9 ms: 1.03x slower                                                 |
| bench_thread_pool       | 462 us                                                                | 455 us: 1.02x faster                                                  |
| coroutines              | 17.4 ms                                                               | 19.5 ms: 1.12x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 51.8 ms: 1.00x slower                                                 |
| deepcopy                | 237 us                                                                | 241 us: 1.02x slower                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 2.08 us: 1.02x slower                                                 |
| deltablue               | 2.83 ms                                                               | 2.83 ms: 1.00x slower                                                 |
| django_template         | 21.0 ms                                                               | 21.8 ms: 1.04x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.47 sec: 1.01x slower                                                |
| dulwich_log             | 29.4 ms                                                               | 29.1 ms: 1.01x faster                                                 |
| fannkuch                | 261 ms                                                                | 270 ms: 1.03x slower                                                  |
| flaskblogging           | 2.27 ms                                                               | 2.22 ms: 1.02x faster                                                 |
| float                   | 55.7 ms                                                               | 56.5 ms: 1.02x slower                                                 |
| generators              | 27.7 ms                                                               | 29.2 ms: 1.05x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.4 ms: 1.01x faster                                                 |
| genshi_xml              | 31.3 ms                                                               | 30.2 ms: 1.04x faster                                                 |
| go                      | 106 ms                                                                | 118 ms: 1.11x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.92 ms: 1.05x slower                                                 |
| json                    | 2.91 ms                                                               | 2.81 ms: 1.03x faster                                                 |
| json_dumps              | 7.69 ms                                                               | 6.09 ms: 1.26x faster                                                 |
| json_loads              | 16.4 us                                                               | 16.2 us: 1.01x faster                                                 |
| logging_format          | 3.74 us                                                               | 3.95 us: 1.06x slower                                                 |
| logging_silent          | 65.7 ns                                                               | 66.2 ns: 1.01x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.67 us: 1.07x slower                                                 |
| mako                    | 8.44 ms                                                               | 8.16 ms: 1.03x faster                                                 |
| mdp                     | 1.53 sec                                                              | 1.52 sec: 1.00x faster                                                |
| meteor_contest          | 77.8 ms                                                               | 78.2 ms: 1.01x slower                                                 |
| nbody                   | 63.8 ms                                                               | 64.8 ms: 1.02x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 61.2 ms: 1.04x slower                                                 |
| pathlib                 | 20.8 ms                                                               | 20.6 ms: 1.01x faster                                                 |
| pickle                  | 7.14 us                                                               | 7.55 us: 1.06x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.86 us: 1.05x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 205 us: 1.08x faster                                                  |
| pprint_safe_repr        | 488 ms                                                                | 495 ms: 1.02x slower                                                  |
| pyflate                 | 318 ms                                                                | 351 ms: 1.10x slower                                                  |
| python_startup          | 9.25 ms                                                               | 9.08 ms: 1.02x faster                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.15 ms: 1.02x faster                                                 |
| raytrace                | 208 ms                                                                | 214 ms: 1.03x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 75.6 ms: 1.03x faster                                                 |
| regex_dna               | 149 ms                                                                | 152 ms: 1.01x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.63 ms: 1.10x slower                                                 |
| regex_v8                | 16.8 ms                                                               | 16.3 ms: 1.03x faster                                                 |
| scimark_fft             | 199 ms                                                                | 199 ms: 1.00x faster                                                  |
| scimark_lu              | 71.8 ms                                                               | 72.3 ms: 1.01x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 54.3 ms: 1.11x slower                                                 |
| scimark_sor             | 77.6 ms                                                               | 102 ms: 1.31x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.83 ms: 1.13x faster                                                 |
| spectral_norm           | 72.2 ms                                                               | 72.9 ms: 1.01x slower                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 61.3 ms: 1.01x faster                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.00 ms: 1.04x faster                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1000 us: 1.19x faster                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.17 ms: 1.16x faster                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 31.9 ms: 1.02x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 174 ms: 1.03x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.46 us: 1.08x slower                                                 |
| sympy_expand            | 243 ms                                                                | 248 ms: 1.02x slower                                                  |
| sympy_integrate         | 11.6 ms                                                               | 11.6 ms: 1.01x slower                                                 |
| sympy_sum               | 82.4 ms                                                               | 85.9 ms: 1.04x slower                                                 |
| sympy_str               | 151 ms                                                                | 153 ms: 1.02x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.36 ms: 1.02x faster                                                 |
| thrift                  | 435 us                                                                | 442 us: 1.02x slower                                                  |
| unpack_sequence         | 32.2 ns                                                               | 34.1 ns: 1.06x slower                                                 |
| unpickle                | 9.97 us                                                               | 9.74 us: 1.02x faster                                                 |
| unpickle_list           | 2.77 us                                                               | 2.54 us: 1.09x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 162 us: 1.08x faster                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 96.6 ms: 1.03x faster                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 47.6 ms: 1.01x faster                                                 |
| xml_etree_process       | 34.8 ms                                                               | 35.0 ms: 1.01x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (12): async_tree_cpu_io_mixed, bench_mp_pool, deepcopy_memo, html5lib, mypy, pidigits, pprint_pformat, pycparser, pylint, richards, tornado_http, xml_etree_iterparse
Ignored benchmarks (2) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, gunicorn
Ignored benchmarks (1) of public/results/bm-20220926-python-2b428a1faed88f148ede-3.12.0a0-2b428a1/bm-20220926-darwin-arm64-python-2b428a1faed88f148ede-3.12.0a0-2b428a1.json: coverage
