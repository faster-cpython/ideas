Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.73 ms                                                               | 5.14 ms: 1.09x slower                                                 |
| docutils       | 1.46 sec                                                              | 1.56 sec: 1.07x slower                                                |
| html5lib       | 35.8 ms                                                               | 36.9 ms: 1.03x slower                                                 |
| tornado_http   | 69.7 ms                                                               | 79.7 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.07x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 56.5 ms: 1.01x slower                                                 |
| nbody          | 63.8 ms                                                               | 65.2 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 78.4 ms: 1.01x slower                                                 |
| regex_dna      | 149 ms                                                                | 163 ms: 1.09x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.50 ms: 1.04x slower                                                 |
| regex_v8       | 16.8 ms                                                               | 18.0 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 7.91 ms: 1.03x slower                                                 |
| json_loads           | 16.4 us                                                               | 16.8 us: 1.02x slower                                                 |
| pickle               | 7.14 us                                                               | 7.42 us: 1.04x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.85 us: 1.04x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 224 us: 1.01x slower                                                  |
| unpickle             | 9.97 us                                                               | 10.1 us: 1.02x slower                                                 |
| unpickle_list        | 2.77 us                                                               | 2.50 us: 1.11x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 177 us: 1.01x slower                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 96.5 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 67.2 ms: 1.03x slower                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 49.9 ms: 1.04x slower                                                 |
| xml_etree_process    | 34.8 ms                                                               | 37.5 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.02x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 12.7 ms: 1.37x slower                                                 |
| python_startup_no_site | 7.30 ms                                                               | 6.93 ms: 1.05x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 23.1 ms: 1.10x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 16.1 ms: 1.04x slower                                                 |
| genshi_xml      | 31.3 ms                                                               | 32.4 ms: 1.03x slower                                                 |
| mako            | 8.44 ms                                                               | 8.53 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.05x slower                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| async_tree_none         | 287 ms                                                                | 301 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed | 533 ms                                                                | 580 ms: 1.09x slower                                                  |
| async_tree_io           | 702 ms                                                                | 833 ms: 1.19x slower                                                  |
| async_tree_memoization  | 346 ms                                                                | 391 ms: 1.13x slower                                                  |
| chameleon               | 4.73 ms                                                               | 5.14 ms: 1.09x slower                                                 |
| chaos                   | 49.5 ms                                                               | 49.8 ms: 1.01x slower                                                 |
| bench_mp_pool           | 41.0 ms                                                               | 42.1 ms: 1.02x slower                                                 |
| bench_thread_pool       | 462 us                                                                | 501 us: 1.08x slower                                                  |
| coroutines              | 17.4 ms                                                               | 18.5 ms: 1.06x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 59.6 ms: 1.15x slower                                                 |
| deepcopy                | 237 us                                                                | 240 us: 1.01x slower                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 2.06 us: 1.01x slower                                                 |
| deepcopy_memo           | 28.7 us                                                               | 27.9 us: 1.03x faster                                                 |
| deltablue               | 2.83 ms                                                               | 3.12 ms: 1.10x slower                                                 |
| django_template         | 21.0 ms                                                               | 23.1 ms: 1.10x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.56 sec: 1.07x slower                                                |
| dulwich_log             | 29.4 ms                                                               | 30.8 ms: 1.05x slower                                                 |
| fannkuch                | 261 ms                                                                | 269 ms: 1.03x slower                                                  |
| flaskblogging           | 2.27 ms                                                               | 2.79 ms: 1.23x slower                                                 |
| float                   | 55.7 ms                                                               | 56.5 ms: 1.01x slower                                                 |
| generators              | 27.7 ms                                                               | 27.3 ms: 1.02x faster                                                 |
| genshi_text             | 15.5 ms                                                               | 16.1 ms: 1.04x slower                                                 |
| genshi_xml              | 31.3 ms                                                               | 32.4 ms: 1.03x slower                                                 |
| go                      | 106 ms                                                                | 119 ms: 1.12x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.74 ms: 1.01x slower                                                 |
| html5lib                | 35.8 ms                                                               | 36.9 ms: 1.03x slower                                                 |
| json                    | 2.91 ms                                                               | 3.04 ms: 1.05x slower                                                 |
| json_dumps              | 7.69 ms                                                               | 7.91 ms: 1.03x slower                                                 |
| json_loads              | 16.4 us                                                               | 16.8 us: 1.02x slower                                                 |
| logging_format          | 3.74 us                                                               | 3.83 us: 1.02x slower                                                 |
| logging_silent          | 65.7 ns                                                               | 81.8 ns: 1.25x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.51 us: 1.02x slower                                                 |
| mako                    | 8.44 ms                                                               | 8.53 ms: 1.01x slower                                                 |
| mdp                     | 1.53 sec                                                              | 1.58 sec: 1.03x slower                                                |
| meteor_contest          | 77.8 ms                                                               | 73.8 ms: 1.05x faster                                                 |
| nbody                   | 63.8 ms                                                               | 65.2 ms: 1.02x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 60.7 ms: 1.04x slower                                                 |
| pathlib                 | 20.8 ms                                                               | 21.1 ms: 1.01x slower                                                 |
| pickle                  | 7.14 us                                                               | 7.42 us: 1.04x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.85 us: 1.04x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 224 us: 1.01x slower                                                  |
| pprint_safe_repr        | 488 ms                                                                | 503 ms: 1.03x slower                                                  |
| pprint_pformat          | 1.00 sec                                                              | 1.03 sec: 1.03x slower                                                |
| pycparser               | 704 ms                                                                | 762 ms: 1.08x slower                                                  |
| pyflate                 | 318 ms                                                                | 347 ms: 1.09x slower                                                  |
| pylint                  | 264 ms                                                                | 280 ms: 1.06x slower                                                  |
| python_startup          | 9.25 ms                                                               | 12.7 ms: 1.37x slower                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 6.93 ms: 1.05x faster                                                 |
| raytrace                | 208 ms                                                                | 228 ms: 1.10x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 78.4 ms: 1.01x slower                                                 |
| regex_dna               | 149 ms                                                                | 163 ms: 1.09x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.50 ms: 1.04x slower                                                 |
| regex_v8                | 16.8 ms                                                               | 18.0 ms: 1.07x slower                                                 |
| richards                | 33.3 ms                                                               | 36.4 ms: 1.09x slower                                                 |
| scimark_fft             | 199 ms                                                                | 202 ms: 1.02x slower                                                  |
| scimark_lu              | 71.8 ms                                                               | 78.9 ms: 1.10x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 51.6 ms: 1.06x slower                                                 |
| scimark_sor             | 77.6 ms                                                               | 86.7 ms: 1.12x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.25 ms: 1.01x slower                                                 |
| spectral_norm           | 72.2 ms                                                               | 76.7 ms: 1.06x slower                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.30 ms: 1.10x slower                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.48 ms: 1.10x slower                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 34.5 ms: 1.10x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 180 ms: 1.06x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.39 us: 1.03x slower                                                 |
| sympy_expand            | 243 ms                                                                | 262 ms: 1.08x slower                                                  |
| sympy_integrate         | 11.6 ms                                                               | 12.1 ms: 1.04x slower                                                 |
| sympy_sum               | 82.4 ms                                                               | 88.7 ms: 1.08x slower                                                 |
| sympy_str               | 151 ms                                                                | 161 ms: 1.07x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.56 ms: 1.04x slower                                                 |
| thrift                  | 435 us                                                                | 474 us: 1.09x slower                                                  |
| tornado_http            | 69.7 ms                                                               | 79.7 ms: 1.14x slower                                                 |
| unpack_sequence         | 32.2 ns                                                               | 32.2 ns: 1.00x faster                                                 |
| unpickle                | 9.97 us                                                               | 10.1 us: 1.02x slower                                                 |
| unpickle_list           | 2.77 us                                                               | 2.50 us: 1.11x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 177 us: 1.01x slower                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 96.5 ms: 1.03x faster                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 67.2 ms: 1.03x slower                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 49.9 ms: 1.04x slower                                                 |
| xml_etree_process       | 34.8 ms                                                               | 37.5 ms: 1.08x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.05x slower                                                          |

Benchmark hidden because not significant (2): async_generators, pidigits
Ignored benchmarks (5) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, gunicorn, mypy, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of public/results/bm-20211208-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba/bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba.json: coverage
