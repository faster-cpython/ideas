Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221002-darwin-arm64-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.73 ms                                                               | 4.69 ms: 1.01x faster                                                 |
| docutils       | 1.46 sec                                                              | 1.47 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221002-darwin-arm64-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 56.1 ms: 1.01x slower                                                 |
| nbody          | 63.8 ms                                                               | 65.3 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221002-darwin-arm64-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 75.4 ms: 1.03x faster                                                 |
| regex_dna      | 149 ms                                                                | 150 ms: 1.00x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.59 ms: 1.08x slower                                                 |
| regex_v8       | 16.8 ms                                                               | 16.1 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221002-darwin-arm64-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.13 ms: 1.25x faster                                                 |
| json_loads           | 16.4 us                                                               | 16.2 us: 1.01x faster                                                 |
| pickle               | 7.14 us                                                               | 7.55 us: 1.06x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.85 us: 1.05x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 205 us: 1.08x faster                                                  |
| unpickle             | 9.97 us                                                               | 9.75 us: 1.02x faster                                                 |
| unpickle_list        | 2.77 us                                                               | 2.56 us: 1.08x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 162 us: 1.08x faster                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 96.1 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 64.9 ms: 1.01x faster                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 47.6 ms: 1.01x faster                                                 |
| xml_etree_process    | 34.8 ms                                                               | 34.9 ms: 1.00x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221002-darwin-arm64-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.06 ms: 1.02x faster                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.16 ms: 1.02x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.02x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221002-darwin-arm64-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.9 ms: 1.04x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 15.4 ms: 1.01x faster                                                 |
| genshi_xml      | 31.3 ms                                                               | 30.3 ms: 1.04x faster                                                 |
| mako            | 8.44 ms                                                               | 8.14 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221002-darwin-arm64-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68 |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| async_generators        | 197 ms                                                                | 201 ms: 1.02x slower                                                  |
| async_tree_none         | 287 ms                                                                | 283 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed | 533 ms                                                                | 530 ms: 1.01x faster                                                  |
| async_tree_io           | 702 ms                                                                | 732 ms: 1.04x slower                                                  |
| async_tree_memoization  | 346 ms                                                                | 383 ms: 1.11x slower                                                  |
| chameleon               | 4.73 ms                                                               | 4.69 ms: 1.01x faster                                                 |
| chaos                   | 49.5 ms                                                               | 50.9 ms: 1.03x slower                                                 |
| bench_thread_pool       | 462 us                                                                | 454 us: 1.02x faster                                                  |
| coroutines              | 17.4 ms                                                               | 19.5 ms: 1.12x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 52.2 ms: 1.01x slower                                                 |
| deepcopy                | 237 us                                                                | 240 us: 1.01x slower                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 2.06 us: 1.01x slower                                                 |
| deepcopy_memo           | 28.7 us                                                               | 28.5 us: 1.01x faster                                                 |
| django_template         | 21.0 ms                                                               | 21.9 ms: 1.04x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.47 sec: 1.01x slower                                                |
| dulwich_log             | 29.4 ms                                                               | 29.1 ms: 1.01x faster                                                 |
| fannkuch                | 261 ms                                                                | 270 ms: 1.03x slower                                                  |
| flaskblogging           | 2.27 ms                                                               | 2.23 ms: 1.02x faster                                                 |
| float                   | 55.7 ms                                                               | 56.1 ms: 1.01x slower                                                 |
| generators              | 27.7 ms                                                               | 29.2 ms: 1.06x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.4 ms: 1.01x faster                                                 |
| genshi_xml              | 31.3 ms                                                               | 30.3 ms: 1.04x faster                                                 |
| go                      | 106 ms                                                                | 118 ms: 1.11x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.93 ms: 1.05x slower                                                 |
| json                    | 2.91 ms                                                               | 2.83 ms: 1.03x faster                                                 |
| json_dumps              | 7.69 ms                                                               | 6.13 ms: 1.25x faster                                                 |
| json_loads              | 16.4 us                                                               | 16.2 us: 1.01x faster                                                 |
| logging_format          | 3.74 us                                                               | 3.97 us: 1.06x slower                                                 |
| logging_silent          | 65.7 ns                                                               | 71.7 ns: 1.09x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.68 us: 1.07x slower                                                 |
| mako                    | 8.44 ms                                                               | 8.14 ms: 1.04x faster                                                 |
| mdp                     | 1.53 sec                                                              | 1.53 sec: 1.00x slower                                                |
| meteor_contest          | 77.8 ms                                                               | 78.1 ms: 1.00x slower                                                 |
| nbody                   | 63.8 ms                                                               | 65.3 ms: 1.02x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 61.3 ms: 1.04x slower                                                 |
| pathlib                 | 20.8 ms                                                               | 20.6 ms: 1.01x faster                                                 |
| pickle                  | 7.14 us                                                               | 7.55 us: 1.06x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.85 us: 1.05x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 205 us: 1.08x faster                                                  |
| pprint_safe_repr        | 488 ms                                                                | 496 ms: 1.02x slower                                                  |
| pprint_pformat          | 1.00 sec                                                              | 1.01 sec: 1.00x slower                                                |
| pycparser               | 704 ms                                                                | 713 ms: 1.01x slower                                                  |
| pyflate                 | 318 ms                                                                | 353 ms: 1.11x slower                                                  |
| python_startup          | 9.25 ms                                                               | 9.06 ms: 1.02x faster                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.16 ms: 1.02x faster                                                 |
| raytrace                | 208 ms                                                                | 216 ms: 1.04x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 75.4 ms: 1.03x faster                                                 |
| regex_dna               | 149 ms                                                                | 150 ms: 1.00x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.59 ms: 1.08x slower                                                 |
| regex_v8                | 16.8 ms                                                               | 16.1 ms: 1.04x faster                                                 |
| scimark_fft             | 199 ms                                                                | 199 ms: 1.00x faster                                                  |
| scimark_lu              | 71.8 ms                                                               | 72.3 ms: 1.01x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 55.4 ms: 1.13x slower                                                 |
| scimark_sor             | 77.6 ms                                                               | 101 ms: 1.30x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.82 ms: 1.13x faster                                                 |
| spectral_norm           | 72.2 ms                                                               | 73.0 ms: 1.01x slower                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 61.2 ms: 1.01x faster                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.06 ms: 1.03x faster                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.00 ms: 1.18x faster                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.17 ms: 1.15x faster                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 31.9 ms: 1.02x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 174 ms: 1.03x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.46 us: 1.08x slower                                                 |
| sympy_expand            | 243 ms                                                                | 248 ms: 1.02x slower                                                  |
| sympy_integrate         | 11.6 ms                                                               | 11.6 ms: 1.01x slower                                                 |
| sympy_sum               | 82.4 ms                                                               | 85.9 ms: 1.04x slower                                                 |
| sympy_str               | 151 ms                                                                | 153 ms: 1.01x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.36 ms: 1.02x faster                                                 |
| thrift                  | 435 us                                                                | 446 us: 1.02x slower                                                  |
| unpack_sequence         | 32.2 ns                                                               | 34.1 ns: 1.06x slower                                                 |
| unpickle                | 9.97 us                                                               | 9.75 us: 1.02x faster                                                 |
| unpickle_list           | 2.77 us                                                               | 2.56 us: 1.08x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 162 us: 1.08x faster                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 96.1 ms: 1.03x faster                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 64.9 ms: 1.01x faster                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 47.6 ms: 1.01x faster                                                 |
| xml_etree_process       | 34.8 ms                                                               | 34.9 ms: 1.00x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (8): bench_mp_pool, deltablue, html5lib, mypy, pidigits, pylint, richards, tornado_http
Ignored benchmarks (2) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, gunicorn
Ignored benchmarks (1) of public/results/bm-20221002-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68/bm-20221002-darwin-arm64-python-14d4f68ebb495fe7ccba-3.12.0a0-14d4f68.json: coverage
