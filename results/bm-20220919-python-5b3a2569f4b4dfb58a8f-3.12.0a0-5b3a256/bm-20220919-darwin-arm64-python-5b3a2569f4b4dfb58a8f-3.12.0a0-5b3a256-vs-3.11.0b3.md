Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.73 ms                                                               | 4.69 ms: 1.01x faster                                                 |
| docutils       | 1.46 sec                                                              | 1.48 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 55.9 ms: 1.00x slower                                                 |
| nbody          | 63.8 ms                                                               | 65.4 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 75.6 ms: 1.03x faster                                                 |
| regex_dna      | 149 ms                                                                | 155 ms: 1.04x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.67 ms: 1.11x slower                                                 |
| regex_v8       | 16.8 ms                                                               | 16.7 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.09 ms: 1.26x faster                                                 |
| json_loads           | 16.4 us                                                               | 16.1 us: 1.02x faster                                                 |
| pickle               | 7.14 us                                                               | 7.52 us: 1.05x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 17.9 us: 1.01x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.83 us: 1.04x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 206 us: 1.08x faster                                                  |
| unpickle             | 9.97 us                                                               | 9.68 us: 1.03x faster                                                 |
| unpickle_list        | 2.77 us                                                               | 2.54 us: 1.09x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 161 us: 1.09x faster                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 96.1 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 64.8 ms: 1.01x faster                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 47.5 ms: 1.01x faster                                                 |
| xml_etree_process    | 34.8 ms                                                               | 34.9 ms: 1.00x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.22 ms: 1.00x faster                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.30 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.8 ms: 1.04x slower                                                 |
| genshi_text     | 15.5 ms                                                               | 15.3 ms: 1.01x faster                                                 |
| genshi_xml      | 31.3 ms                                                               | 30.1 ms: 1.04x faster                                                 |
| mako            | 8.44 ms                                                               | 8.14 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| async_generators        | 197 ms                                                                | 201 ms: 1.02x slower                                                  |
| async_tree_none         | 287 ms                                                                | 282 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed | 533 ms                                                                | 529 ms: 1.01x faster                                                  |
| async_tree_io           | 702 ms                                                                | 732 ms: 1.04x slower                                                  |
| async_tree_memoization  | 346 ms                                                                | 381 ms: 1.10x slower                                                  |
| chameleon               | 4.73 ms                                                               | 4.69 ms: 1.01x faster                                                 |
| chaos                   | 49.5 ms                                                               | 50.7 ms: 1.02x slower                                                 |
| bench_thread_pool       | 462 us                                                                | 455 us: 1.02x faster                                                  |
| coroutines              | 17.4 ms                                                               | 19.5 ms: 1.12x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 52.0 ms: 1.01x slower                                                 |
| deepcopy                | 237 us                                                                | 240 us: 1.01x slower                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 2.07 us: 1.01x slower                                                 |
| deepcopy_memo           | 28.7 us                                                               | 28.7 us: 1.00x faster                                                 |
| deltablue               | 2.83 ms                                                               | 2.83 ms: 1.00x slower                                                 |
| django_template         | 21.0 ms                                                               | 21.8 ms: 1.04x slower                                                 |
| docutils                | 1.46 sec                                                              | 1.48 sec: 1.01x slower                                                |
| dulwich_log             | 29.4 ms                                                               | 29.1 ms: 1.01x faster                                                 |
| fannkuch                | 261 ms                                                                | 272 ms: 1.04x slower                                                  |
| flaskblogging           | 2.27 ms                                                               | 2.24 ms: 1.02x faster                                                 |
| float                   | 55.7 ms                                                               | 55.9 ms: 1.00x slower                                                 |
| generators              | 27.7 ms                                                               | 29.2 ms: 1.05x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.3 ms: 1.01x faster                                                 |
| genshi_xml              | 31.3 ms                                                               | 30.1 ms: 1.04x faster                                                 |
| go                      | 106 ms                                                                | 118 ms: 1.11x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.92 ms: 1.04x slower                                                 |
| json                    | 2.91 ms                                                               | 2.84 ms: 1.02x faster                                                 |
| json_dumps              | 7.69 ms                                                               | 6.09 ms: 1.26x faster                                                 |
| json_loads              | 16.4 us                                                               | 16.1 us: 1.02x faster                                                 |
| logging_format          | 3.74 us                                                               | 3.94 us: 1.05x slower                                                 |
| logging_silent          | 65.7 ns                                                               | 66.5 ns: 1.01x slower                                                 |
| logging_simple          | 3.44 us                                                               | 3.65 us: 1.06x slower                                                 |
| mako                    | 8.44 ms                                                               | 8.14 ms: 1.04x faster                                                 |
| meteor_contest          | 77.8 ms                                                               | 77.9 ms: 1.00x slower                                                 |
| nbody                   | 63.8 ms                                                               | 65.4 ms: 1.03x slower                                                 |
| nqueens                 | 58.7 ms                                                               | 61.2 ms: 1.04x slower                                                 |
| pathlib                 | 20.8 ms                                                               | 20.6 ms: 1.01x faster                                                 |
| pickle                  | 7.14 us                                                               | 7.52 us: 1.05x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 17.9 us: 1.01x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.83 us: 1.04x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 206 us: 1.08x faster                                                  |
| pprint_safe_repr        | 488 ms                                                                | 496 ms: 1.02x slower                                                  |
| pprint_pformat          | 1.00 sec                                                              | 1.01 sec: 1.01x slower                                                |
| pycparser               | 704 ms                                                                | 713 ms: 1.01x slower                                                  |
| pyflate                 | 318 ms                                                                | 350 ms: 1.10x slower                                                  |
| python_startup          | 9.25 ms                                                               | 9.22 ms: 1.00x faster                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.30 ms: 1.00x faster                                                 |
| raytrace                | 208 ms                                                                | 215 ms: 1.03x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 75.6 ms: 1.03x faster                                                 |
| regex_dna               | 149 ms                                                                | 155 ms: 1.04x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.67 ms: 1.11x slower                                                 |
| regex_v8                | 16.8 ms                                                               | 16.7 ms: 1.00x faster                                                 |
| scimark_fft             | 199 ms                                                                | 199 ms: 1.00x faster                                                  |
| scimark_lu              | 71.8 ms                                                               | 72.4 ms: 1.01x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 54.4 ms: 1.11x slower                                                 |
| scimark_sor             | 77.6 ms                                                               | 101 ms: 1.31x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.83 ms: 1.13x faster                                                 |
| spectral_norm           | 72.2 ms                                                               | 72.9 ms: 1.01x slower                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 61.3 ms: 1.01x faster                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.07 ms: 1.03x faster                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.00 ms: 1.18x faster                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.17 ms: 1.16x faster                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 31.9 ms: 1.02x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 174 ms: 1.03x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.45 us: 1.08x slower                                                 |
| sympy_expand            | 243 ms                                                                | 248 ms: 1.02x slower                                                  |
| sympy_integrate         | 11.6 ms                                                               | 11.7 ms: 1.01x slower                                                 |
| sympy_sum               | 82.4 ms                                                               | 86.1 ms: 1.05x slower                                                 |
| sympy_str               | 151 ms                                                                | 154 ms: 1.02x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.36 ms: 1.02x faster                                                 |
| thrift                  | 435 us                                                                | 443 us: 1.02x slower                                                  |
| unpack_sequence         | 32.2 ns                                                               | 34.2 ns: 1.06x slower                                                 |
| unpickle                | 9.97 us                                                               | 9.68 us: 1.03x faster                                                 |
| unpickle_list           | 2.77 us                                                               | 2.54 us: 1.09x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 161 us: 1.09x faster                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 96.1 ms: 1.03x faster                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 64.8 ms: 1.01x faster                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 47.5 ms: 1.01x faster                                                 |
| xml_etree_process       | 34.8 ms                                                               | 34.9 ms: 1.00x slower                                                 |
| Geometric mean          | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (8): bench_mp_pool, html5lib, mdp, mypy, pidigits, pylint, richards, tornado_http
Ignored benchmarks (2) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, gunicorn
Ignored benchmarks (1) of public/results/bm-20220919-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256/bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256.json: coverage
