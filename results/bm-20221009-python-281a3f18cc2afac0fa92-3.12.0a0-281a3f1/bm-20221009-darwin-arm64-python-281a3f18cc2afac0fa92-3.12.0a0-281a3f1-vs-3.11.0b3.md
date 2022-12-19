Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 186 ms: 1.02x slower                                                  |
| chameleon      | 4.73 ms                                                               | 4.61 ms: 1.03x faster                                                 |
| docutils       | 1.46 sec                                                              | 1.47 sec: 1.01x slower                                                |
| html5lib       | 35.8 ms                                                               | 36.6 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 56.1 ms: 1.01x slower                                                 |
| nbody          | 63.8 ms                                                               | 64.3 ms: 1.01x slower                                                 |
| pidigits       | 282 ms                                                                | 282 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 76.5 ms: 1.02x faster                                                 |
| regex_dna      | 149 ms                                                                | 151 ms: 1.01x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.68 ms: 1.12x slower                                                 |
| regex_v8       | 16.8 ms                                                               | 16.3 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.17 ms: 1.25x faster                                                 |
| json_loads           | 16.4 us                                                               | 16.3 us: 1.01x faster                                                 |
| pickle               | 7.14 us                                                               | 7.56 us: 1.06x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.91 us: 1.07x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 208 us: 1.06x faster                                                  |
| unpickle             | 9.97 us                                                               | 9.78 us: 1.02x faster                                                 |
| unpickle_list        | 2.77 us                                                               | 2.54 us: 1.09x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 162 us: 1.08x faster                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 90.0 ms: 1.10x faster                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 64.6 ms: 1.01x faster                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 47.1 ms: 1.02x faster                                                 |
| xml_etree_process    | 34.8 ms                                                               | 34.9 ms: 1.00x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.38 ms: 1.01x slower                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.41 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.7 ms: 1.03x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 15.3 ms: 1.01x faster                                                 |
| genshi_xml      | 31.3 ms                                                               | 30.1 ms: 1.04x faster                                                 |
| mako            | 8.44 ms                                                               | 8.11 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1 |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 186 ms: 1.02x slower                                                  |
| async_generators        | 197 ms                                                                | 199 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed | 533 ms                                                                | 545 ms: 1.02x slower                                                  |
| async_tree_io           | 702 ms                                                                | 736 ms: 1.05x slower                                                  |
| async_tree_memoization  | 346 ms                                                                | 325 ms: 1.06x faster                                                  |
| chameleon               | 4.73 ms                                                               | 4.61 ms: 1.03x faster                                                 |
| chaos                   | 49.5 ms                                                               | 50.4 ms: 1.02x slower                                                 |
| bench_thread_pool       | 462 us                                                                | 452 us: 1.02x faster                                                  |
| coroutines              | 17.4 ms                                                               | 19.0 ms: 1.09x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 51.8 ms: 1.00x slower                                                 |
| deepcopy                | 237 us                                                                | 239 us: 1.01x slower                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 2.06 us: 1.01x slower                                                 |
| deepcopy_memo           | 28.7 us                                                               | 29.2 us: 1.02x slower                                                 |
| deltablue               | 2.83 ms                                                               | 2.74 ms: 1.03x faster                                                 |
| django_template         | 21.0 ms                                                               | 21.7 ms: 1.03x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.47 sec: 1.01x slower                                                |
| dulwich_log             | 29.4 ms                                                               | 29.3 ms: 1.00x faster                                                 |
| fannkuch                | 261 ms                                                                | 269 ms: 1.03x slower                                                  |
| float                   | 55.7 ms                                                               | 56.1 ms: 1.01x slower                                                 |
| generators              | 27.7 ms                                                               | 29.0 ms: 1.05x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.3 ms: 1.01x faster                                                 |
| genshi_xml              | 31.3 ms                                                               | 30.1 ms: 1.04x faster                                                 |
| go                      | 106 ms                                                                | 120 ms: 1.13x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.92 ms: 1.05x slower                                                 |
| html5lib                | 35.8 ms                                                               | 36.6 ms: 1.02x slower                                                 |
| json                    | 2.91 ms                                                               | 2.84 ms: 1.02x faster                                                 |
| json_dumps              | 7.69 ms                                                               | 6.17 ms: 1.25x faster                                                 |
| json_loads              | 16.4 us                                                               | 16.3 us: 1.01x faster                                                 |
| logging_format          | 3.74 us                                                               | 4.00 us: 1.07x slower                                                 |
| logging_silent          | 65.7 ns                                                               | 65.9 ns: 1.00x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.66 us: 1.06x slower                                                 |
| mako                    | 8.44 ms                                                               | 8.11 ms: 1.04x faster                                                 |
| mdp                     | 1.53 sec                                                              | 1.52 sec: 1.00x faster                                                |
| meteor_contest          | 77.8 ms                                                               | 76.2 ms: 1.02x faster                                                 |
| nbody                   | 63.8 ms                                                               | 64.3 ms: 1.01x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 60.3 ms: 1.03x slower                                                 |
| pickle                  | 7.14 us                                                               | 7.56 us: 1.06x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.91 us: 1.07x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 208 us: 1.06x faster                                                  |
| pidigits                | 282 ms                                                                | 282 ms: 1.00x slower                                                  |
| pprint_safe_repr        | 488 ms                                                                | 486 ms: 1.00x faster                                                  |
| pprint_pformat          | 1.00 sec                                                              | 992 ms: 1.01x faster                                                  |
| pyflate                 | 318 ms                                                                | 352 ms: 1.11x slower                                                  |
| python_startup          | 9.25 ms                                                               | 9.38 ms: 1.01x slower                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.41 ms: 1.01x slower                                                 |
| raytrace                | 208 ms                                                                | 219 ms: 1.05x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 76.5 ms: 1.02x faster                                                 |
| regex_dna               | 149 ms                                                                | 151 ms: 1.01x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.68 ms: 1.12x slower                                                 |
| regex_v8                | 16.8 ms                                                               | 16.3 ms: 1.03x faster                                                 |
| richards                | 33.3 ms                                                               | 33.5 ms: 1.01x slower                                                 |
| scimark_lu              | 71.8 ms                                                               | 73.9 ms: 1.03x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 54.6 ms: 1.12x slower                                                 |
| scimark_sor             | 77.6 ms                                                               | 101 ms: 1.30x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.78 ms: 1.15x faster                                                 |
| spectral_norm           | 72.2 ms                                                               | 72.5 ms: 1.00x slower                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 61.0 ms: 1.01x faster                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.16 ms: 1.02x faster                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.01 ms: 1.18x faster                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.18 ms: 1.15x faster                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 31.7 ms: 1.01x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 173 ms: 1.02x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.45 us: 1.07x slower                                                 |
| sympy_expand            | 243 ms                                                                | 246 ms: 1.01x slower                                                  |
| sympy_integrate         | 11.6 ms                                                               | 11.6 ms: 1.00x slower                                                 |
| sympy_sum               | 82.4 ms                                                               | 86.0 ms: 1.04x slower                                                 |
| sympy_str               | 151 ms                                                                | 153 ms: 1.01x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.32 ms: 1.03x faster                                                 |
| thrift                  | 435 us                                                                | 438 us: 1.01x slower                                                  |
| unpack_sequence         | 32.2 ns                                                               | 33.5 ns: 1.04x slower                                                 |
| unpickle                | 9.97 us                                                               | 9.78 us: 1.02x faster                                                 |
| unpickle_list           | 2.77 us                                                               | 2.54 us: 1.09x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 162 us: 1.08x faster                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 90.0 ms: 1.10x faster                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 64.6 ms: 1.01x faster                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 47.1 ms: 1.02x faster                                                 |
| xml_etree_process       | 34.8 ms                                                               | 34.9 ms: 1.00x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (8): async_tree_none, bench_mp_pool, mypy, pathlib, pycparser, pylint, scimark_fft, tornado_http
Ignored benchmarks (3) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, flaskblogging, gunicorn
Ignored benchmarks (1) of public/results/bm-20221009-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1/bm-20221009-darwin-arm64-python-281a3f18cc2afac0fa92-3.12.0a0-281a3f1.json: coverage
