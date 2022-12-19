Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221106-darwin-arm64-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 187 ms: 1.03x slower                                                   |
| chameleon      | 4.73 ms                                                               | 5.13 ms: 1.08x slower                                                  |
| docutils       | 1.46 sec                                                              | 1.50 sec: 1.03x slower                                                 |
| html5lib       | 35.8 ms                                                               | 37.5 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221106-darwin-arm64-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 57.3 ms: 1.03x slower                                                  |
| nbody          | 63.8 ms                                                               | 65.9 ms: 1.03x slower                                                  |
| pidigits       | 282 ms                                                                | 282 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221106-darwin-arm64-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 149 ms                                                                | 149 ms: 1.00x faster                                                   |
| regex_effbot   | 2.40 ms                                                               | 2.63 ms: 1.10x slower                                                  |
| regex_v8       | 16.8 ms                                                               | 16.1 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221106-darwin-arm64-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.15 ms: 1.25x faster                                                  |
| pickle               | 7.14 us                                                               | 7.55 us: 1.06x slower                                                  |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list          | 2.73 us                                                               | 2.88 us: 1.06x slower                                                  |
| unpickle             | 9.97 us                                                               | 9.86 us: 1.01x faster                                                  |
| unpickle_list        | 2.77 us                                                               | 2.60 us: 1.07x faster                                                  |
| unpickle_pure_python | 175 us                                                                | 167 us: 1.05x faster                                                   |
| xml_etree_parse      | 99.1 ms                                                               | 93.3 ms: 1.06x faster                                                  |
| xml_etree_generate   | 48.0 ms                                                               | 50.5 ms: 1.05x slower                                                  |
| xml_etree_process    | 34.8 ms                                                               | 36.8 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                                           |

Benchmark hidden because not significant (3): json_loads, pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221106-darwin-arm64-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.32 ms: 1.01x slower                                                  |
| python_startup_no_site | 7.30 ms                                                               | 7.38 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221106-darwin-arm64-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 22.2 ms: 1.06x slower                                                  |
| genshi_text     | 15.5 ms                                                               | 16.2 ms: 1.04x slower                                                  |
| genshi_xml      | 31.3 ms                                                               | 32.4 ms: 1.03x slower                                                  |
| mako            | 8.44 ms                                                               | 8.59 ms: 1.02x slower                                                  |
| Geometric mean  | (ref)                                                                 | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221106-darwin-arm64-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f |
|-------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 187 ms: 1.03x slower                                                   |
| async_generators        | 197 ms                                                                | 202 ms: 1.02x slower                                                   |
| async_tree_none         | 287 ms                                                                | 294 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed | 533 ms                                                                | 547 ms: 1.03x slower                                                   |
| async_tree_io           | 702 ms                                                                | 736 ms: 1.05x slower                                                   |
| async_tree_memoization  | 346 ms                                                                | 335 ms: 1.03x faster                                                   |
| chameleon               | 4.73 ms                                                               | 5.13 ms: 1.08x slower                                                  |
| chaos                   | 49.5 ms                                                               | 51.6 ms: 1.04x slower                                                  |
| bench_mp_pool           | 41.0 ms                                                               | 42.8 ms: 1.04x slower                                                  |
| bench_thread_pool       | 462 us                                                                | 463 us: 1.00x slower                                                   |
| coroutines              | 17.4 ms                                                               | 19.1 ms: 1.10x slower                                                  |
| deepcopy                | 237 us                                                                | 263 us: 1.11x slower                                                   |
| deepcopy_reduce         | 2.04 us                                                               | 2.28 us: 1.12x slower                                                  |
| deepcopy_memo           | 28.7 us                                                               | 32.1 us: 1.12x slower                                                  |
| deltablue               | 2.83 ms                                                               | 2.85 ms: 1.01x slower                                                  |
| django_template         | 21.0 ms                                                               | 22.2 ms: 1.06x slower                                                  |
| docutils                | 1.46 sec                                                              | 1.50 sec: 1.03x slower                                                 |
| dulwich_log             | 29.4 ms                                                               | 29.7 ms: 1.01x slower                                                  |
| fannkuch                | 261 ms                                                                | 270 ms: 1.04x slower                                                   |
| float                   | 55.7 ms                                                               | 57.3 ms: 1.03x slower                                                  |
| generators              | 27.7 ms                                                               | 28.1 ms: 1.01x slower                                                  |
| genshi_text             | 15.5 ms                                                               | 16.2 ms: 1.04x slower                                                  |
| genshi_xml              | 31.3 ms                                                               | 32.4 ms: 1.03x slower                                                  |
| go                      | 106 ms                                                                | 121 ms: 1.14x slower                                                   |
| hexiom                  | 4.71 ms                                                               | 4.91 ms: 1.04x slower                                                  |
| html5lib                | 35.8 ms                                                               | 37.5 ms: 1.05x slower                                                  |
| json                    | 2.91 ms                                                               | 2.86 ms: 1.01x faster                                                  |
| json_dumps              | 7.69 ms                                                               | 6.15 ms: 1.25x faster                                                  |
| logging_format          | 3.74 us                                                               | 4.09 us: 1.09x slower                                                  |
| logging_simple          | 3.44 us                                                               | 3.77 us: 1.10x slower                                                  |
| mako                    | 8.44 ms                                                               | 8.59 ms: 1.02x slower                                                  |
| mdp                     | 1.53 sec                                                              | 1.55 sec: 1.02x slower                                                 |
| meteor_contest          | 77.8 ms                                                               | 80.5 ms: 1.03x slower                                                  |
| mypy                    | 418 ms                                                                | 424 ms: 1.01x slower                                                   |
| nbody                   | 63.8 ms                                                               | 65.9 ms: 1.03x slower                                                  |
| nqueens                 | 58.7 ms                                                               | 59.3 ms: 1.01x slower                                                  |
| pickle                  | 7.14 us                                                               | 7.55 us: 1.06x slower                                                  |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list             | 2.73 us                                                               | 2.88 us: 1.06x slower                                                  |
| pidigits                | 282 ms                                                                | 282 ms: 1.00x slower                                                   |
| pprint_safe_repr        | 488 ms                                                                | 514 ms: 1.05x slower                                                   |
| pprint_pformat          | 1.00 sec                                                              | 1.05 sec: 1.05x slower                                                 |
| pycparser               | 704 ms                                                                | 711 ms: 1.01x slower                                                   |
| pyflate                 | 318 ms                                                                | 355 ms: 1.12x slower                                                   |
| pylint                  | 264 ms                                                                | 257 ms: 1.03x faster                                                   |
| python_startup          | 9.25 ms                                                               | 9.32 ms: 1.01x slower                                                  |
| python_startup_no_site  | 7.30 ms                                                               | 7.38 ms: 1.01x slower                                                  |
| raytrace                | 208 ms                                                                | 215 ms: 1.03x slower                                                   |
| regex_dna               | 149 ms                                                                | 149 ms: 1.00x faster                                                   |
| regex_effbot            | 2.40 ms                                                               | 2.63 ms: 1.10x slower                                                  |
| regex_v8                | 16.8 ms                                                               | 16.1 ms: 1.04x faster                                                  |
| richards                | 33.3 ms                                                               | 32.0 ms: 1.04x faster                                                  |
| scimark_fft             | 199 ms                                                                | 200 ms: 1.00x slower                                                   |
| scimark_lu              | 71.8 ms                                                               | 71.2 ms: 1.01x faster                                                  |
| scimark_monte_carlo     | 48.9 ms                                                               | 54.9 ms: 1.12x slower                                                  |
| scimark_sor             | 77.6 ms                                                               | 103 ms: 1.33x slower                                                   |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.76 ms: 1.16x faster                                                  |
| spectral_norm           | 72.2 ms                                                               | 71.9 ms: 1.00x faster                                                  |
| sqlglot_parse           | 1.19 ms                                                               | 1.01 ms: 1.17x faster                                                  |
| sqlglot_transpile       | 1.35 ms                                                               | 1.19 ms: 1.14x faster                                                  |
| sqlglot_optimize        | 31.4 ms                                                               | 32.0 ms: 1.02x slower                                                  |
| sqlglot_normalize       | 169 ms                                                                | 175 ms: 1.03x slower                                                   |
| sqlite_synth            | 1.35 us                                                               | 1.45 us: 1.08x slower                                                  |
| sympy_expand            | 243 ms                                                                | 255 ms: 1.05x slower                                                   |
| sympy_integrate         | 11.6 ms                                                               | 12.1 ms: 1.05x slower                                                  |
| sympy_sum               | 82.4 ms                                                               | 88.0 ms: 1.07x slower                                                  |
| sympy_str               | 151 ms                                                                | 159 ms: 1.05x slower                                                   |
| telco                   | 3.42 ms                                                               | 3.44 ms: 1.00x slower                                                  |
| thrift                  | 435 us                                                                | 443 us: 1.02x slower                                                   |
| unpack_sequence         | 32.2 ns                                                               | 52.1 ns: 1.62x slower                                                  |
| unpickle                | 9.97 us                                                               | 9.86 us: 1.01x faster                                                  |
| unpickle_list           | 2.77 us                                                               | 2.60 us: 1.07x faster                                                  |
| unpickle_pure_python    | 175 us                                                                | 167 us: 1.05x faster                                                   |
| xml_etree_parse         | 99.1 ms                                                               | 93.3 ms: 1.06x faster                                                  |
| xml_etree_generate      | 48.0 ms                                                               | 50.5 ms: 1.05x slower                                                  |
| xml_etree_process       | 34.8 ms                                                               | 36.8 ms: 1.06x slower                                                  |
| Geometric mean          | (ref)                                                                 | 1.03x slower                                                           |

Benchmark hidden because not significant (8): crypto_pyaes, json_loads, logging_silent, pathlib, pickle_pure_python, regex_compile, tornado_http, xml_etree_iterparse
Ignored benchmarks (5) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, flaskblogging, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of public/results/bm-20221106-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f/bm-20221106-darwin-arm64-python-728e42fcf51cbb2108ca-3.12.0a1+-728e42f.json: coverage
