Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 186 ms: 1.02x slower                                                   |
| chameleon      | 4.73 ms                                                               | 4.64 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                           |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 56.4 ms: 1.01x slower                                                  |
| nbody          | 63.8 ms                                                               | 65.0 ms: 1.02x slower                                                  |
| pidigits       | 282 ms                                                                | 283 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 75.9 ms: 1.02x faster                                                  |
| regex_dna      | 149 ms                                                                | 149 ms: 1.00x faster                                                   |
| regex_effbot   | 2.40 ms                                                               | 2.61 ms: 1.09x slower                                                  |
| regex_v8       | 16.8 ms                                                               | 16.0 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.07 ms: 1.27x faster                                                  |
| json_loads           | 16.4 us                                                               | 16.4 us: 1.00x faster                                                  |
| pickle               | 7.14 us                                                               | 7.54 us: 1.06x slower                                                  |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list          | 2.73 us                                                               | 2.85 us: 1.04x slower                                                  |
| pickle_pure_python   | 222 us                                                                | 210 us: 1.06x faster                                                   |
| unpickle             | 9.97 us                                                               | 9.84 us: 1.01x faster                                                  |
| unpickle_list        | 2.77 us                                                               | 2.59 us: 1.07x faster                                                  |
| unpickle_pure_python | 175 us                                                                | 161 us: 1.09x faster                                                   |
| xml_etree_parse      | 99.1 ms                                                               | 93.2 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 65.2 ms                                                               | 66.4 ms: 1.02x slower                                                  |
| xml_etree_generate   | 48.0 ms                                                               | 48.7 ms: 1.01x slower                                                  |
| xml_etree_process    | 34.8 ms                                                               | 35.2 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.29 ms: 1.00x slower                                                  |
| python_startup_no_site | 7.30 ms                                                               | 7.33 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.6 ms: 1.03x slower                                                  |
| genshi_text     | 15.5 ms                                                               | 15.2 ms: 1.02x faster                                                  |
| genshi_xml      | 31.3 ms                                                               | 29.6 ms: 1.06x faster                                                  |
| mako            | 8.44 ms                                                               | 8.24 ms: 1.02x faster                                                  |
| Geometric mean  | (ref)                                                                 | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 186 ms: 1.02x slower                                                   |
| async_generators        | 197 ms                                                                | 204 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed | 533 ms                                                                | 539 ms: 1.01x slower                                                   |
| async_tree_io           | 702 ms                                                                | 733 ms: 1.04x slower                                                   |
| async_tree_memoization  | 346 ms                                                                | 323 ms: 1.07x faster                                                   |
| chameleon               | 4.73 ms                                                               | 4.64 ms: 1.02x faster                                                  |
| chaos                   | 49.5 ms                                                               | 51.1 ms: 1.03x slower                                                  |
| bench_mp_pool           | 41.0 ms                                                               | 42.1 ms: 1.03x slower                                                  |
| bench_thread_pool       | 462 us                                                                | 456 us: 1.01x faster                                                   |
| coroutines              | 17.4 ms                                                               | 20.0 ms: 1.15x slower                                                  |
| crypto_pyaes            | 51.7 ms                                                               | 53.4 ms: 1.03x slower                                                  |
| deepcopy                | 237 us                                                                | 240 us: 1.01x slower                                                   |
| deepcopy_memo           | 28.7 us                                                               | 29.5 us: 1.03x slower                                                  |
| deltablue               | 2.83 ms                                                               | 2.81 ms: 1.01x faster                                                  |
| django_template         | 21.0 ms                                                               | 21.6 ms: 1.03x slower                                                  |
| dulwich_log             | 29.4 ms                                                               | 29.3 ms: 1.00x faster                                                  |
| fannkuch                | 261 ms                                                                | 276 ms: 1.06x slower                                                   |
| float                   | 55.7 ms                                                               | 56.4 ms: 1.01x slower                                                  |
| generators              | 27.7 ms                                                               | 34.1 ms: 1.23x slower                                                  |
| genshi_text             | 15.5 ms                                                               | 15.2 ms: 1.02x faster                                                  |
| genshi_xml              | 31.3 ms                                                               | 29.6 ms: 1.06x faster                                                  |
| go                      | 106 ms                                                                | 118 ms: 1.11x slower                                                   |
| hexiom                  | 4.71 ms                                                               | 4.93 ms: 1.05x slower                                                  |
| json                    | 2.91 ms                                                               | 2.86 ms: 1.02x faster                                                  |
| json_dumps              | 7.69 ms                                                               | 6.07 ms: 1.27x faster                                                  |
| json_loads              | 16.4 us                                                               | 16.4 us: 1.00x faster                                                  |
| logging_format          | 3.74 us                                                               | 3.91 us: 1.04x slower                                                  |
| logging_silent          | 65.7 ns                                                               | 64.4 ns: 1.02x faster                                                  |
| logging_simple          | 3.44 us                                                               | 3.62 us: 1.05x slower                                                  |
| mako                    | 8.44 ms                                                               | 8.24 ms: 1.02x faster                                                  |
| mdp                     | 1.53 sec                                                              | 1.54 sec: 1.01x slower                                                 |
| meteor_contest          | 77.8 ms                                                               | 77.2 ms: 1.01x faster                                                  |
| nbody                   | 63.8 ms                                                               | 65.0 ms: 1.02x slower                                                  |
| nqueens                 | 58.7 ms                                                               | 61.9 ms: 1.06x slower                                                  |
| pathlib                 | 20.8 ms                                                               | 20.6 ms: 1.01x faster                                                  |
| pickle                  | 7.14 us                                                               | 7.54 us: 1.06x slower                                                  |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list             | 2.73 us                                                               | 2.85 us: 1.04x slower                                                  |
| pickle_pure_python      | 222 us                                                                | 210 us: 1.06x faster                                                   |
| pidigits                | 282 ms                                                                | 283 ms: 1.00x slower                                                   |
| pprint_safe_repr        | 488 ms                                                                | 491 ms: 1.01x slower                                                   |
| pyflate                 | 318 ms                                                                | 356 ms: 1.12x slower                                                   |
| python_startup          | 9.25 ms                                                               | 9.29 ms: 1.00x slower                                                  |
| python_startup_no_site  | 7.30 ms                                                               | 7.33 ms: 1.00x slower                                                  |
| raytrace                | 208 ms                                                                | 220 ms: 1.06x slower                                                   |
| regex_compile           | 77.7 ms                                                               | 75.9 ms: 1.02x faster                                                  |
| regex_dna               | 149 ms                                                                | 149 ms: 1.00x faster                                                   |
| regex_effbot            | 2.40 ms                                                               | 2.61 ms: 1.09x slower                                                  |
| regex_v8                | 16.8 ms                                                               | 16.0 ms: 1.05x faster                                                  |
| richards                | 33.3 ms                                                               | 31.3 ms: 1.06x faster                                                  |
| scimark_fft             | 199 ms                                                                | 198 ms: 1.00x faster                                                   |
| scimark_lu              | 71.8 ms                                                               | 71.0 ms: 1.01x faster                                                  |
| scimark_monte_carlo     | 48.9 ms                                                               | 56.3 ms: 1.15x slower                                                  |
| scimark_sor             | 77.6 ms                                                               | 99.3 ms: 1.28x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.83 ms: 1.13x faster                                                  |
| spectral_norm           | 72.2 ms                                                               | 73.7 ms: 1.02x slower                                                  |
| sqlglot_parse           | 1.19 ms                                                               | 996 us: 1.19x faster                                                   |
| sqlglot_transpile       | 1.35 ms                                                               | 1.17 ms: 1.16x faster                                                  |
| sqlglot_optimize        | 31.4 ms                                                               | 31.6 ms: 1.01x slower                                                  |
| sqlglot_normalize       | 169 ms                                                                | 173 ms: 1.02x slower                                                   |
| sqlite_synth            | 1.35 us                                                               | 1.43 us: 1.06x slower                                                  |
| sympy_expand            | 243 ms                                                                | 247 ms: 1.02x slower                                                   |
| sympy_integrate         | 11.6 ms                                                               | 11.8 ms: 1.02x slower                                                  |
| sympy_sum               | 82.4 ms                                                               | 86.6 ms: 1.05x slower                                                  |
| sympy_str               | 151 ms                                                                | 155 ms: 1.03x slower                                                   |
| thrift                  | 435 us                                                                | 438 us: 1.01x slower                                                   |
| unpack_sequence         | 32.2 ns                                                               | 62.7 ns: 1.95x slower                                                  |
| unpickle                | 9.97 us                                                               | 9.84 us: 1.01x faster                                                  |
| unpickle_list           | 2.77 us                                                               | 2.59 us: 1.07x faster                                                  |
| unpickle_pure_python    | 175 us                                                                | 161 us: 1.09x faster                                                   |
| xml_etree_parse         | 99.1 ms                                                               | 93.2 ms: 1.06x faster                                                  |
| xml_etree_iterparse     | 65.2 ms                                                               | 66.4 ms: 1.02x slower                                                  |
| xml_etree_generate      | 48.0 ms                                                               | 48.7 ms: 1.01x slower                                                  |
| xml_etree_process       | 34.8 ms                                                               | 35.2 ms: 1.01x slower                                                  |
| Geometric mean          | (ref)                                                                 | 1.02x slower                                                           |

Benchmark hidden because not significant (9): async_tree_none, deepcopy_reduce, docutils, html5lib, mypy, pprint_pformat, pycparser, telco, tornado_http
Ignored benchmarks (6) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of public/results/bm-20221128-python-594de165bf2f21d6b28e-3.12.0a2+-594de16/bm-20221128-darwin-arm64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16.json: coverage
