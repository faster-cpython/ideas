Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 184 ms: 1.01x slower                                                  |
| chameleon      | 4.73 ms                                                               | 4.75 ms: 1.00x slower                                                 |
| docutils       | 1.46 sec                                                              | 1.45 sec: 1.01x faster                                                |
| html5lib       | 35.8 ms                                                               | 33.2 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 51.4 ms: 1.08x faster                                                 |
| nbody          | 63.8 ms                                                               | 64.0 ms: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 78.4 ms: 1.01x slower                                                 |
| regex_dna      | 149 ms                                                                | 140 ms: 1.07x faster                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.03 ms: 1.18x faster                                                 |
| regex_v8       | 16.8 ms                                                               | 15.8 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 7.77 ms: 1.01x slower                                                 |
| pickle               | 7.14 us                                                               | 7.17 us: 1.01x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 17.1 us: 1.03x faster                                                 |
| pickle_list          | 2.73 us                                                               | 2.71 us: 1.01x faster                                                 |
| pickle_pure_python   | 222 us                                                                | 212 us: 1.05x faster                                                  |
| unpickle_list        | 2.77 us                                                               | 2.61 us: 1.06x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 181 us: 1.03x slower                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 99.3 ms: 1.00x slower                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 65.5 ms: 1.00x slower                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 49.0 ms: 1.02x slower                                                 |
| xml_etree_process    | 34.8 ms                                                               | 35.9 ms: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (2): json_loads, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.22 ms: 1.00x faster                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.24 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.5 ms: 1.02x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 15.4 ms: 1.01x faster                                                 |
| genshi_xml      | 31.3 ms                                                               | 31.6 ms: 1.01x slower                                                 |
| mako            | 8.44 ms                                                               | 8.40 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220506-darwin-arm64-python-8d32a5c8c4e9c90b0a21-3.11.0b1-8d32a5c |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 184 ms: 1.01x slower                                                  |
| async_generators        | 197 ms                                                                | 200 ms: 1.01x slower                                                  |
| chameleon               | 4.73 ms                                                               | 4.75 ms: 1.00x slower                                                 |
| chaos                   | 49.5 ms                                                               | 50.6 ms: 1.02x slower                                                 |
| bench_thread_pool       | 462 us                                                                | 482 us: 1.04x slower                                                  |
| coroutines              | 17.4 ms                                                               | 18.8 ms: 1.08x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 52.1 ms: 1.01x slower                                                 |
| deepcopy                | 237 us                                                                | 222 us: 1.07x faster                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 1.90 us: 1.07x faster                                                 |
| deepcopy_memo           | 28.7 us                                                               | 26.2 us: 1.09x faster                                                 |
| deltablue               | 2.83 ms                                                               | 2.74 ms: 1.03x faster                                                 |
| django_template         | 21.0 ms                                                               | 21.5 ms: 1.02x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.45 sec: 1.01x faster                                                |
| dulwich_log             | 29.4 ms                                                               | 29.5 ms: 1.00x slower                                                 |
| fannkuch                | 261 ms                                                                | 261 ms: 1.00x slower                                                  |
| float                   | 55.7 ms                                                               | 51.4 ms: 1.08x faster                                                 |
| generators              | 27.7 ms                                                               | 28.6 ms: 1.03x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.4 ms: 1.01x faster                                                 |
| genshi_xml              | 31.3 ms                                                               | 31.6 ms: 1.01x slower                                                 |
| go                      | 106 ms                                                                | 110 ms: 1.04x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.92 ms: 1.04x slower                                                 |
| html5lib                | 35.8 ms                                                               | 33.2 ms: 1.08x faster                                                 |
| json_dumps              | 7.69 ms                                                               | 7.77 ms: 1.01x slower                                                 |
| logging_format          | 3.74 us                                                               | 3.90 us: 1.04x slower                                                 |
| logging_silent          | 65.7 ns                                                               | 67.5 ns: 1.03x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.60 us: 1.05x slower                                                 |
| mako                    | 8.44 ms                                                               | 8.40 ms: 1.01x faster                                                 |
| mdp                     | 1.53 sec                                                              | 1.56 sec: 1.03x slower                                                |
| meteor_contest          | 77.8 ms                                                               | 76.8 ms: 1.01x faster                                                 |
| nbody                   | 63.8 ms                                                               | 64.0 ms: 1.00x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 60.4 ms: 1.03x slower                                                 |
| pickle                  | 7.14 us                                                               | 7.17 us: 1.01x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 17.1 us: 1.03x faster                                                 |
| pickle_list             | 2.73 us                                                               | 2.71 us: 1.01x faster                                                 |
| pickle_pure_python      | 222 us                                                                | 212 us: 1.05x faster                                                  |
| pprint_safe_repr        | 488 ms                                                                | 470 ms: 1.04x faster                                                  |
| pprint_pformat          | 1.00 sec                                                              | 966 ms: 1.04x faster                                                  |
| pyflate                 | 318 ms                                                                | 322 ms: 1.01x slower                                                  |
| python_startup          | 9.25 ms                                                               | 9.22 ms: 1.00x faster                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.24 ms: 1.01x faster                                                 |
| raytrace                | 208 ms                                                                | 207 ms: 1.01x faster                                                  |
| regex_compile           | 77.7 ms                                                               | 78.4 ms: 1.01x slower                                                 |
| regex_dna               | 149 ms                                                                | 140 ms: 1.07x faster                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.03 ms: 1.18x faster                                                 |
| regex_v8                | 16.8 ms                                                               | 15.8 ms: 1.06x faster                                                 |
| richards                | 33.3 ms                                                               | 33.8 ms: 1.02x slower                                                 |
| scimark_fft             | 199 ms                                                                | 201 ms: 1.01x slower                                                  |
| scimark_lu              | 71.8 ms                                                               | 73.7 ms: 1.03x slower                                                 |
| scimark_sor             | 77.6 ms                                                               | 79.2 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.23 ms: 1.01x slower                                                 |
| spectral_norm           | 72.2 ms                                                               | 71.7 ms: 1.01x faster                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 62.8 ms: 1.02x slower                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.44 ms: 1.02x slower                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.21 ms: 1.02x slower                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.38 ms: 1.02x slower                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 33.0 ms: 1.05x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 179 ms: 1.06x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.32 us: 1.02x faster                                                 |
| sympy_expand            | 243 ms                                                                | 249 ms: 1.02x slower                                                  |
| sympy_integrate         | 11.6 ms                                                               | 11.7 ms: 1.01x slower                                                 |
| sympy_sum               | 82.4 ms                                                               | 83.6 ms: 1.01x slower                                                 |
| sympy_str               | 151 ms                                                                | 153 ms: 1.01x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.41 ms: 1.00x faster                                                 |
| thrift                  | 435 us                                                                | 443 us: 1.02x slower                                                  |
| unpack_sequence         | 32.2 ns                                                               | 32.3 ns: 1.00x slower                                                 |
| unpickle_list           | 2.77 us                                                               | 2.61 us: 1.06x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 181 us: 1.03x slower                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 99.3 ms: 1.00x slower                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 65.5 ms: 1.00x slower                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 49.0 ms: 1.02x slower                                                 |
| xml_etree_process       | 34.8 ms                                                               | 35.9 ms: 1.03x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (18): aiohttp, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, bench_mp_pool, flaskblogging, gunicorn, json, json_loads, mypy, pathlib, pidigits, pycparser, pylint, scimark_monte_carlo, tornado_http, unpickle
