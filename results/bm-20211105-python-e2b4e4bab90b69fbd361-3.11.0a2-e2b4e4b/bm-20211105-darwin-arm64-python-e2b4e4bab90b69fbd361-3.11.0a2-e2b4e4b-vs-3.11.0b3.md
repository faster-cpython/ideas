Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 186 ms: 1.02x slower                                                  |
| chameleon      | 4.73 ms                                                               | 5.09 ms: 1.08x slower                                                 |
| docutils       | 1.46 sec                                                              | 1.53 sec: 1.05x slower                                                |
| html5lib       | 35.8 ms                                                               | 36.5 ms: 1.02x slower                                                 |
| tornado_http   | 69.7 ms                                                               | 75.9 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 51.6 ms: 1.08x faster                                                 |
| nbody          | 63.8 ms                                                               | 74.0 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 77.9 ms: 1.00x slower                                                 |
| regex_dna      | 149 ms                                                                | 164 ms: 1.10x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.47 ms: 1.03x slower                                                 |
| regex_v8       | 16.8 ms                                                               | 18.1 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 7.80 ms: 1.01x slower                                                 |
| json_loads           | 16.4 us                                                               | 16.8 us: 1.02x slower                                                 |
| pickle               | 7.14 us                                                               | 7.28 us: 1.02x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.84 us: 1.04x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 227 us: 1.02x slower                                                  |
| unpickle_list        | 2.77 us                                                               | 2.52 us: 1.10x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 174 us: 1.00x faster                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 95.7 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 66.5 ms: 1.02x slower                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 48.7 ms: 1.01x slower                                                 |
| xml_etree_process    | 34.8 ms                                                               | 36.8 ms: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (2): pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 9.25 ms                                                               | 13.6 ms: 1.47x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.21x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 22.7 ms: 1.08x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 15.7 ms: 1.01x slower                                                 |
| genshi_xml      | 31.3 ms                                                               | 31.1 ms: 1.01x faster                                                 |
| mako            | 8.44 ms                                                               | 8.49 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 186 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed | 533 ms                                                                | 579 ms: 1.09x slower                                                  |
| async_tree_io           | 702 ms                                                                | 779 ms: 1.11x slower                                                  |
| async_tree_memoization  | 346 ms                                                                | 360 ms: 1.04x slower                                                  |
| chameleon               | 4.73 ms                                                               | 5.09 ms: 1.08x slower                                                 |
| chaos                   | 49.5 ms                                                               | 49.0 ms: 1.01x faster                                                 |
| bench_mp_pool           | 41.0 ms                                                               | 39.9 ms: 1.03x faster                                                 |
| bench_thread_pool       | 462 us                                                                | 496 us: 1.07x slower                                                  |
| coroutines              | 17.4 ms                                                               | 19.2 ms: 1.10x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 58.1 ms: 1.12x slower                                                 |
| deepcopy_memo           | 28.7 us                                                               | 27.8 us: 1.03x faster                                                 |
| deltablue               | 2.83 ms                                                               | 3.19 ms: 1.13x slower                                                 |
| django_template         | 21.0 ms                                                               | 22.7 ms: 1.08x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.53 sec: 1.05x slower                                                |
| dulwich_log             | 29.4 ms                                                               | 30.0 ms: 1.02x slower                                                 |
| fannkuch                | 261 ms                                                                | 280 ms: 1.07x slower                                                  |
| flaskblogging           | 2.27 ms                                                               | 2.76 ms: 1.21x slower                                                 |
| float                   | 55.7 ms                                                               | 51.6 ms: 1.08x faster                                                 |
| generators              | 27.7 ms                                                               | 28.2 ms: 1.02x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.7 ms: 1.01x slower                                                 |
| genshi_xml              | 31.3 ms                                                               | 31.1 ms: 1.01x faster                                                 |
| go                      | 106 ms                                                                | 119 ms: 1.12x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.91 ms: 1.04x slower                                                 |
| html5lib                | 35.8 ms                                                               | 36.5 ms: 1.02x slower                                                 |
| json                    | 2.91 ms                                                               | 3.03 ms: 1.04x slower                                                 |
| json_dumps              | 7.69 ms                                                               | 7.80 ms: 1.01x slower                                                 |
| json_loads              | 16.4 us                                                               | 16.8 us: 1.02x slower                                                 |
| logging_format          | 3.74 us                                                               | 3.72 us: 1.01x faster                                                 |
| logging_silent          | 65.7 ns                                                               | 82.6 ns: 1.26x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.45 us: 1.00x slower                                                 |
| mako                    | 8.44 ms                                                               | 8.49 ms: 1.01x slower                                                 |
| mdp                     | 1.53 sec                                                              | 1.56 sec: 1.03x slower                                                |
| meteor_contest          | 77.8 ms                                                               | 74.3 ms: 1.05x faster                                                 |
| nbody                   | 63.8 ms                                                               | 74.0 ms: 1.16x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 61.3 ms: 1.04x slower                                                 |
| pathlib                 | 20.8 ms                                                               | 20.5 ms: 1.02x faster                                                 |
| pickle                  | 7.14 us                                                               | 7.28 us: 1.02x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.84 us: 1.04x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 227 us: 1.02x slower                                                  |
| pprint_safe_repr        | 488 ms                                                                | 500 ms: 1.03x slower                                                  |
| pprint_pformat          | 1.00 sec                                                              | 1.02 sec: 1.02x slower                                                |
| pycparser               | 704 ms                                                                | 766 ms: 1.09x slower                                                  |
| pyflate                 | 318 ms                                                                | 361 ms: 1.14x slower                                                  |
| pylint                  | 264 ms                                                                | 276 ms: 1.05x slower                                                  |
| python_startup          | 9.25 ms                                                               | 13.6 ms: 1.47x slower                                                 |
| raytrace                | 208 ms                                                                | 208 ms: 1.00x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 77.9 ms: 1.00x slower                                                 |
| regex_dna               | 149 ms                                                                | 164 ms: 1.10x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.47 ms: 1.03x slower                                                 |
| regex_v8                | 16.8 ms                                                               | 18.1 ms: 1.08x slower                                                 |
| richards                | 33.3 ms                                                               | 37.4 ms: 1.12x slower                                                 |
| scimark_fft             | 199 ms                                                                | 202 ms: 1.01x slower                                                  |
| scimark_lu              | 71.8 ms                                                               | 93.9 ms: 1.31x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 48.8 ms: 1.00x faster                                                 |
| scimark_sor             | 77.6 ms                                                               | 98.8 ms: 1.27x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.24 ms: 1.01x slower                                                 |
| spectral_norm           | 72.2 ms                                                               | 75.0 ms: 1.04x slower                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.23 ms: 1.03x slower                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.40 ms: 1.04x slower                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 33.5 ms: 1.07x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 174 ms: 1.03x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.39 us: 1.03x slower                                                 |
| sympy_expand            | 243 ms                                                                | 254 ms: 1.05x slower                                                  |
| sympy_integrate         | 11.6 ms                                                               | 12.1 ms: 1.05x slower                                                 |
| sympy_sum               | 82.4 ms                                                               | 86.0 ms: 1.04x slower                                                 |
| sympy_str               | 151 ms                                                                | 157 ms: 1.04x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.40 ms: 1.01x faster                                                 |
| thrift                  | 435 us                                                                | 465 us: 1.07x slower                                                  |
| tornado_http            | 69.7 ms                                                               | 75.9 ms: 1.09x slower                                                 |
| unpack_sequence         | 32.2 ns                                                               | 31.2 ns: 1.03x faster                                                 |
| unpickle_list           | 2.77 us                                                               | 2.52 us: 1.10x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 174 us: 1.00x faster                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 95.7 ms: 1.03x faster                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 66.5 ms: 1.02x slower                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 48.7 ms: 1.01x slower                                                 |
| xml_etree_process       | 34.8 ms                                                               | 36.8 ms: 1.06x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.05x slower                                                          |

Benchmark hidden because not significant (9): async_generators, async_tree_none, deepcopy, deepcopy_reduce, gunicorn, pickle_dict, pidigits, python_startup_no_site, unpickle
Ignored benchmarks (4) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, mypy, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of public/results/bm-20211105-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b/bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b.json: coverage
