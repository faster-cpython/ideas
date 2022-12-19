Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| chameleon      | 4.73 ms                                                               | 4.70 ms: 1.01x faster                                                 |
| docutils       | 1.46 sec                                                              | 1.45 sec: 1.01x faster                                                |
| html5lib       | 35.8 ms                                                               | 34.0 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 51.6 ms: 1.08x faster                                                 |
| nbody          | 63.8 ms                                                               | 65.6 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 75.6 ms: 1.03x faster                                                 |
| regex_dna      | 149 ms                                                                | 169 ms: 1.13x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.20 ms: 1.09x faster                                                 |
| regex_v8       | 16.8 ms                                                               | 20.5 ms: 1.22x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 7.58 ms: 1.01x faster                                                 |
| json_loads           | 16.4 us                                                               | 16.3 us: 1.01x faster                                                 |
| pickle               | 7.14 us                                                               | 7.18 us: 1.01x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 19.2 us: 1.09x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.80 us: 1.03x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 200 us: 1.11x faster                                                  |
| unpickle             | 9.97 us                                                               | 9.82 us: 1.02x faster                                                 |
| unpickle_list        | 2.77 us                                                               | 2.62 us: 1.06x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 157 us: 1.11x faster                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 95.7 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 64.4 ms: 1.01x faster                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 47.9 ms: 1.00x faster                                                 |
| xml_etree_process    | 34.8 ms                                                               | 35.1 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.13 ms: 1.01x faster                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.18 ms: 1.02x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.1 ms: 1.01x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 15.2 ms: 1.02x faster                                                 |
| genshi_xml      | 31.3 ms                                                               | 31.4 ms: 1.00x slower                                                 |
| mako            | 8.44 ms                                                               | 8.21 ms: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0 |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators        | 197 ms                                                                | 191 ms: 1.03x faster                                                  |
| async_tree_none         | 287 ms                                                                | 280 ms: 1.03x faster                                                  |
| async_tree_io           | 702 ms                                                                | 693 ms: 1.01x faster                                                  |
| async_tree_memoization  | 346 ms                                                                | 316 ms: 1.09x faster                                                  |
| chameleon               | 4.73 ms                                                               | 4.70 ms: 1.01x faster                                                 |
| chaos                   | 49.5 ms                                                               | 49.7 ms: 1.00x slower                                                 |
| bench_mp_pool           | 41.0 ms                                                               | 37.1 ms: 1.11x faster                                                 |
| bench_thread_pool       | 462 us                                                                | 476 us: 1.03x slower                                                  |
| coroutines              | 17.4 ms                                                               | 17.3 ms: 1.01x faster                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 56.5 ms: 1.09x slower                                                 |
| deepcopy                | 237 us                                                                | 220 us: 1.08x faster                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 1.91 us: 1.07x faster                                                 |
| deepcopy_memo           | 28.7 us                                                               | 25.4 us: 1.13x faster                                                 |
| deltablue               | 2.83 ms                                                               | 2.67 ms: 1.06x faster                                                 |
| django_template         | 21.0 ms                                                               | 21.1 ms: 1.01x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.45 sec: 1.01x faster                                                |
| fannkuch                | 261 ms                                                                | 262 ms: 1.00x slower                                                  |
| flaskblogging           | 2.27 ms                                                               | 2.30 ms: 1.01x slower                                                 |
| float                   | 55.7 ms                                                               | 51.6 ms: 1.08x faster                                                 |
| generators              | 27.7 ms                                                               | 27.9 ms: 1.01x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.2 ms: 1.02x faster                                                 |
| genshi_xml              | 31.3 ms                                                               | 31.4 ms: 1.00x slower                                                 |
| go                      | 106 ms                                                                | 107 ms: 1.01x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.87 ms: 1.04x slower                                                 |
| html5lib                | 35.8 ms                                                               | 34.0 ms: 1.05x faster                                                 |
| json                    | 2.91 ms                                                               | 2.92 ms: 1.00x slower                                                 |
| json_dumps              | 7.69 ms                                                               | 7.58 ms: 1.01x faster                                                 |
| json_loads              | 16.4 us                                                               | 16.3 us: 1.01x faster                                                 |
| logging_format          | 3.74 us                                                               | 3.65 us: 1.03x faster                                                 |
| logging_silent          | 65.7 ns                                                               | 69.4 ns: 1.06x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.38 us: 1.02x faster                                                 |
| mako                    | 8.44 ms                                                               | 8.21 ms: 1.03x faster                                                 |
| mdp                     | 1.53 sec                                                              | 1.66 sec: 1.09x slower                                                |
| meteor_contest          | 77.8 ms                                                               | 75.2 ms: 1.03x faster                                                 |
| mypy                    | 418 ms                                                                | 422 ms: 1.01x slower                                                  |
| nbody                   | 63.8 ms                                                               | 65.6 ms: 1.03x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 60.6 ms: 1.03x slower                                                 |
| pickle                  | 7.14 us                                                               | 7.18 us: 1.01x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 19.2 us: 1.09x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.80 us: 1.03x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 200 us: 1.11x faster                                                  |
| pprint_safe_repr        | 488 ms                                                                | 460 ms: 1.06x faster                                                  |
| pprint_pformat          | 1.00 sec                                                              | 940 ms: 1.07x faster                                                  |
| pycparser               | 704 ms                                                                | 721 ms: 1.02x slower                                                  |
| pyflate                 | 318 ms                                                                | 317 ms: 1.00x faster                                                  |
| pylint                  | 264 ms                                                                | 271 ms: 1.03x slower                                                  |
| python_startup          | 9.25 ms                                                               | 9.13 ms: 1.01x faster                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.18 ms: 1.02x faster                                                 |
| raytrace                | 208 ms                                                                | 209 ms: 1.01x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 75.6 ms: 1.03x faster                                                 |
| regex_dna               | 149 ms                                                                | 169 ms: 1.13x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.20 ms: 1.09x faster                                                 |
| regex_v8                | 16.8 ms                                                               | 20.5 ms: 1.22x slower                                                 |
| richards                | 33.3 ms                                                               | 32.1 ms: 1.04x faster                                                 |
| scimark_fft             | 199 ms                                                                | 201 ms: 1.01x slower                                                  |
| scimark_lu              | 71.8 ms                                                               | 72.6 ms: 1.01x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 46.9 ms: 1.04x faster                                                 |
| scimark_sor             | 77.6 ms                                                               | 84.7 ms: 1.09x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.22 ms: 1.01x slower                                                 |
| spectral_norm           | 72.2 ms                                                               | 73.6 ms: 1.02x slower                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 63.2 ms: 1.02x slower                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.37 ms: 1.01x slower                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.17 ms: 1.02x faster                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.33 ms: 1.01x faster                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 31.9 ms: 1.02x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 172 ms: 1.02x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.29 us: 1.05x faster                                                 |
| sympy_expand            | 243 ms                                                                | 241 ms: 1.01x faster                                                  |
| sympy_integrate         | 11.6 ms                                                               | 11.2 ms: 1.03x faster                                                 |
| sympy_sum               | 82.4 ms                                                               | 81.7 ms: 1.01x faster                                                 |
| sympy_str               | 151 ms                                                                | 147 ms: 1.02x faster                                                  |
| telco                   | 3.42 ms                                                               | 3.39 ms: 1.01x faster                                                 |
| thrift                  | 435 us                                                                | 439 us: 1.01x slower                                                  |
| unpack_sequence         | 32.2 ns                                                               | 31.9 ns: 1.01x faster                                                 |
| unpickle                | 9.97 us                                                               | 9.82 us: 1.02x faster                                                 |
| unpickle_list           | 2.77 us                                                               | 2.62 us: 1.06x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 157 us: 1.11x faster                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 95.7 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 64.4 ms: 1.01x faster                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 47.9 ms: 1.00x faster                                                 |
| xml_etree_process       | 34.8 ms                                                               | 35.1 ms: 1.01x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (8): 2to3, aiohttp, async_tree_cpu_io_mixed, dulwich_log, gunicorn, pathlib, pidigits, tornado_http
