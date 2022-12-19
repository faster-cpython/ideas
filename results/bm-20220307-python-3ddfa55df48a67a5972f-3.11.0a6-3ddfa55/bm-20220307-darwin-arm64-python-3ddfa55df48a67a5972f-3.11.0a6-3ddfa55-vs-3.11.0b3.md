Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.73 ms                                                               | 4.64 ms: 1.02x faster                                                 |
| docutils       | 1.46 sec                                                              | 1.48 sec: 1.01x slower                                                |
| html5lib       | 35.8 ms                                                               | 33.3 ms: 1.08x faster                                                 |
| tornado_http   | 69.7 ms                                                               | 73.9 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 53.8 ms: 1.03x faster                                                 |
| nbody          | 63.8 ms                                                               | 66.0 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 76.1 ms: 1.02x faster                                                 |
| regex_dna      | 149 ms                                                                | 162 ms: 1.08x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.45 ms: 1.02x slower                                                 |
| regex_v8       | 16.8 ms                                                               | 18.2 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 7.68 ms: 1.00x faster                                                 |
| json_loads           | 16.4 us                                                               | 16.1 us: 1.02x faster                                                 |
| pickle               | 7.14 us                                                               | 7.24 us: 1.01x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 18.2 us: 1.03x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.83 us: 1.04x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 205 us: 1.08x faster                                                  |
| unpickle_list        | 2.77 us                                                               | 2.63 us: 1.05x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 169 us: 1.04x faster                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 95.4 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 64.8 ms: 1.01x faster                                                 |
| xml_etree_process    | 34.8 ms                                                               | 35.7 ms: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (2): unpickle, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 12.9 ms: 1.40x slower                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.12 ms: 1.03x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 22.2 ms: 1.06x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 15.0 ms: 1.03x faster                                                 |
| genshi_xml      | 31.3 ms                                                               | 31.6 ms: 1.01x slower                                                 |
| mako            | 8.44 ms                                                               | 7.66 ms: 1.10x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| aiohttp                 | 1.05 ms                                                               | 1.01 ms: 1.04x faster                                                 |
| async_generators        | 197 ms                                                                | 195 ms: 1.01x faster                                                  |
| async_tree_none         | 287 ms                                                                | 284 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed | 533 ms                                                                | 538 ms: 1.01x slower                                                  |
| async_tree_memoization  | 346 ms                                                                | 376 ms: 1.09x slower                                                  |
| chameleon               | 4.73 ms                                                               | 4.64 ms: 1.02x faster                                                 |
| chaos                   | 49.5 ms                                                               | 48.2 ms: 1.03x faster                                                 |
| bench_mp_pool           | 41.0 ms                                                               | 44.8 ms: 1.09x slower                                                 |
| bench_thread_pool       | 462 us                                                                | 495 us: 1.07x slower                                                  |
| coroutines              | 17.4 ms                                                               | 18.7 ms: 1.08x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 57.2 ms: 1.11x slower                                                 |
| deepcopy                | 237 us                                                                | 232 us: 1.02x faster                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 2.01 us: 1.01x faster                                                 |
| deepcopy_memo           | 28.7 us                                                               | 27.4 us: 1.05x faster                                                 |
| deltablue               | 2.83 ms                                                               | 2.97 ms: 1.05x slower                                                 |
| django_template         | 21.0 ms                                                               | 22.2 ms: 1.06x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.48 sec: 1.01x slower                                                |
| dulwich_log             | 29.4 ms                                                               | 30.0 ms: 1.02x slower                                                 |
| fannkuch                | 261 ms                                                                | 266 ms: 1.02x slower                                                  |
| flaskblogging           | 2.27 ms                                                               | 2.31 ms: 1.02x slower                                                 |
| float                   | 55.7 ms                                                               | 53.8 ms: 1.03x faster                                                 |
| generators              | 27.7 ms                                                               | 29.0 ms: 1.05x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.0 ms: 1.03x faster                                                 |
| genshi_xml              | 31.3 ms                                                               | 31.6 ms: 1.01x slower                                                 |
| go                      | 106 ms                                                                | 109 ms: 1.02x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.66 ms: 1.01x faster                                                 |
| html5lib                | 35.8 ms                                                               | 33.3 ms: 1.08x faster                                                 |
| json                    | 2.91 ms                                                               | 2.83 ms: 1.03x faster                                                 |
| json_dumps              | 7.69 ms                                                               | 7.68 ms: 1.00x faster                                                 |
| json_loads              | 16.4 us                                                               | 16.1 us: 1.02x faster                                                 |
| logging_format          | 3.74 us                                                               | 3.31 us: 1.13x faster                                                 |
| logging_silent          | 65.7 ns                                                               | 73.9 ns: 1.13x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.03 us: 1.14x faster                                                 |
| mako                    | 8.44 ms                                                               | 7.66 ms: 1.10x faster                                                 |
| mdp                     | 1.53 sec                                                              | 1.58 sec: 1.03x slower                                                |
| meteor_contest          | 77.8 ms                                                               | 74.3 ms: 1.05x faster                                                 |
| nbody                   | 63.8 ms                                                               | 66.0 ms: 1.03x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 61.2 ms: 1.04x slower                                                 |
| pickle                  | 7.14 us                                                               | 7.24 us: 1.01x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 18.2 us: 1.03x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.83 us: 1.04x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 205 us: 1.08x faster                                                  |
| pprint_safe_repr        | 488 ms                                                                | 490 ms: 1.01x slower                                                  |
| pprint_pformat          | 1.00 sec                                                              | 998 ms: 1.01x faster                                                  |
| pycparser               | 704 ms                                                                | 739 ms: 1.05x slower                                                  |
| pyflate                 | 318 ms                                                                | 325 ms: 1.02x slower                                                  |
| pylint                  | 264 ms                                                                | 276 ms: 1.04x slower                                                  |
| python_startup          | 9.25 ms                                                               | 12.9 ms: 1.40x slower                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.12 ms: 1.03x faster                                                 |
| raytrace                | 208 ms                                                                | 216 ms: 1.04x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 76.1 ms: 1.02x faster                                                 |
| regex_dna               | 149 ms                                                                | 162 ms: 1.08x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.45 ms: 1.02x slower                                                 |
| regex_v8                | 16.8 ms                                                               | 18.2 ms: 1.08x slower                                                 |
| scimark_fft             | 199 ms                                                                | 203 ms: 1.02x slower                                                  |
| scimark_lu              | 71.8 ms                                                               | 74.7 ms: 1.04x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 51.3 ms: 1.05x slower                                                 |
| scimark_sor             | 77.6 ms                                                               | 80.0 ms: 1.03x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.25 ms: 1.01x slower                                                 |
| spectral_norm           | 72.2 ms                                                               | 76.6 ms: 1.06x slower                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 64.4 ms: 1.04x slower                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.49 ms: 1.03x slower                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.18 ms: 1.01x faster                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 32.9 ms: 1.05x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 175 ms: 1.03x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.30 us: 1.04x faster                                                 |
| sympy_expand            | 243 ms                                                                | 250 ms: 1.03x slower                                                  |
| sympy_sum               | 82.4 ms                                                               | 84.9 ms: 1.03x slower                                                 |
| sympy_str               | 151 ms                                                                | 152 ms: 1.01x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.51 ms: 1.02x slower                                                 |
| thrift                  | 435 us                                                                | 446 us: 1.03x slower                                                  |
| tornado_http            | 69.7 ms                                                               | 73.9 ms: 1.06x slower                                                 |
| unpack_sequence         | 32.2 ns                                                               | 90.4 ns: 2.81x slower                                                 |
| unpickle_list           | 2.77 us                                                               | 2.63 us: 1.05x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 169 us: 1.04x faster                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 95.4 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 64.8 ms: 1.01x faster                                                 |
| xml_etree_process       | 34.8 ms                                                               | 35.7 ms: 1.03x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.03x slower                                                          |

Benchmark hidden because not significant (9): async_tree_io, gunicorn, pathlib, pidigits, richards, sqlglot_transpile, sympy_integrate, unpickle, xml_etree_generate
Ignored benchmarks (1) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: mypy
Ignored benchmarks (1) of public/results/bm-20220307-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55/bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55.json: coverage
