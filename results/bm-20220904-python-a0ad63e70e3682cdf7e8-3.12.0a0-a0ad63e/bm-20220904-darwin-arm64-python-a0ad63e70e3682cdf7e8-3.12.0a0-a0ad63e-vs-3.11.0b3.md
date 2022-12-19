Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| chameleon      | 4.73 ms                                                               | 4.59 ms: 1.03x faster                                                 |
| docutils       | 1.46 sec                                                              | 1.48 sec: 1.01x slower                                                |
| html5lib       | 35.8 ms                                                               | 36.4 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 51.3 ms: 1.09x faster                                                 |
| nbody          | 63.8 ms                                                               | 64.0 ms: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 75.3 ms: 1.03x faster                                                 |
| regex_dna      | 149 ms                                                                | 151 ms: 1.01x slower                                                  |
| regex_effbot   | 2.40 ms                                                               | 2.72 ms: 1.14x slower                                                 |
| regex_v8       | 16.8 ms                                                               | 16.4 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.10 ms: 1.26x faster                                                 |
| json_loads           | 16.4 us                                                               | 16.2 us: 1.01x faster                                                 |
| pickle               | 7.14 us                                                               | 7.59 us: 1.06x slower                                                 |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list          | 2.73 us                                                               | 2.85 us: 1.05x slower                                                 |
| pickle_pure_python   | 222 us                                                                | 198 us: 1.12x faster                                                  |
| unpickle             | 9.97 us                                                               | 9.64 us: 1.03x faster                                                 |
| unpickle_list        | 2.77 us                                                               | 2.58 us: 1.07x faster                                                 |
| unpickle_pure_python | 175 us                                                                | 160 us: 1.09x faster                                                  |
| xml_etree_parse      | 99.1 ms                                                               | 95.9 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 65.2 ms                                                               | 64.5 ms: 1.01x faster                                                 |
| xml_etree_generate   | 48.0 ms                                                               | 47.2 ms: 1.02x faster                                                 |
| xml_etree_process    | 34.8 ms                                                               | 34.5 ms: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                 | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.07 ms: 1.02x faster                                                 |
| python_startup_no_site | 7.30 ms                                                               | 7.16 ms: 1.02x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.02x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 20.9 ms: 1.00x faster                                                 |
| genshi_text     | 15.5 ms                                                               | 15.1 ms: 1.03x faster                                                 |
| genshi_xml      | 31.3 ms                                                               | 29.9 ms: 1.05x faster                                                 |
| mako            | 8.44 ms                                                               | 7.97 ms: 1.06x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 185 ms: 1.02x slower                                                  |
| async_generators        | 197 ms                                                                | 199 ms: 1.01x slower                                                  |
| async_tree_none         | 287 ms                                                                | 284 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed | 533 ms                                                                | 530 ms: 1.01x faster                                                  |
| async_tree_io           | 702 ms                                                                | 734 ms: 1.05x slower                                                  |
| async_tree_memoization  | 346 ms                                                                | 381 ms: 1.10x slower                                                  |
| chameleon               | 4.73 ms                                                               | 4.59 ms: 1.03x faster                                                 |
| bench_thread_pool       | 462 us                                                                | 449 us: 1.03x faster                                                  |
| coroutines              | 17.4 ms                                                               | 19.3 ms: 1.11x slower                                                 |
| crypto_pyaes            | 51.7 ms                                                               | 51.1 ms: 1.01x faster                                                 |
| deepcopy                | 237 us                                                                | 215 us: 1.10x faster                                                  |
| deepcopy_reduce         | 2.04 us                                                               | 1.85 us: 1.10x faster                                                 |
| deepcopy_memo           | 28.7 us                                                               | 24.8 us: 1.16x faster                                                 |
| deltablue               | 2.83 ms                                                               | 2.84 ms: 1.00x slower                                                 |
| django_template         | 21.0 ms                                                               | 20.9 ms: 1.00x faster                                                 |
| docutils                | 1.46 sec                                                              | 1.48 sec: 1.01x slower                                                |
| dulwich_log             | 29.4 ms                                                               | 29.5 ms: 1.00x slower                                                 |
| fannkuch                | 261 ms                                                                | 268 ms: 1.03x slower                                                  |
| flaskblogging           | 2.27 ms                                                               | 2.22 ms: 1.02x faster                                                 |
| float                   | 55.7 ms                                                               | 51.3 ms: 1.09x faster                                                 |
| generators              | 27.7 ms                                                               | 29.1 ms: 1.05x slower                                                 |
| genshi_text             | 15.5 ms                                                               | 15.1 ms: 1.03x faster                                                 |
| genshi_xml              | 31.3 ms                                                               | 29.9 ms: 1.05x faster                                                 |
| go                      | 106 ms                                                                | 117 ms: 1.10x slower                                                  |
| hexiom                  | 4.71 ms                                                               | 4.84 ms: 1.03x slower                                                 |
| html5lib                | 35.8 ms                                                               | 36.4 ms: 1.02x slower                                                 |
| json                    | 2.91 ms                                                               | 2.82 ms: 1.03x faster                                                 |
| json_dumps              | 7.69 ms                                                               | 6.10 ms: 1.26x faster                                                 |
| json_loads              | 16.4 us                                                               | 16.2 us: 1.01x faster                                                 |
| logging_format          | 3.74 us                                                               | 3.92 us: 1.05x slower                                                 |
| logging_silent          | 65.7 ns                                                               | 64.5 ns: 1.02x faster                                                 |
| logging_simple          | 3.44 us                                                               | 3.63 us: 1.05x slower                                                 |
| mako                    | 8.44 ms                                                               | 7.97 ms: 1.06x faster                                                 |
| mdp                     | 1.53 sec                                                              | 1.55 sec: 1.02x slower                                                |
| meteor_contest          | 77.8 ms                                                               | 77.0 ms: 1.01x faster                                                 |
| nbody                   | 63.8 ms                                                               | 64.0 ms: 1.00x slower                                                 |
| pickle                  | 7.14 us                                                               | 7.59 us: 1.06x slower                                                 |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                 |
| pickle_list             | 2.73 us                                                               | 2.85 us: 1.05x slower                                                 |
| pickle_pure_python      | 222 us                                                                | 198 us: 1.12x faster                                                  |
| pprint_safe_repr        | 488 ms                                                                | 468 ms: 1.04x faster                                                  |
| pprint_pformat          | 1.00 sec                                                              | 949 ms: 1.06x faster                                                  |
| pyflate                 | 318 ms                                                                | 345 ms: 1.09x slower                                                  |
| python_startup          | 9.25 ms                                                               | 9.07 ms: 1.02x faster                                                 |
| python_startup_no_site  | 7.30 ms                                                               | 7.16 ms: 1.02x faster                                                 |
| raytrace                | 208 ms                                                                | 211 ms: 1.02x slower                                                  |
| regex_compile           | 77.7 ms                                                               | 75.3 ms: 1.03x faster                                                 |
| regex_dna               | 149 ms                                                                | 151 ms: 1.01x slower                                                  |
| regex_effbot            | 2.40 ms                                                               | 2.72 ms: 1.14x slower                                                 |
| regex_v8                | 16.8 ms                                                               | 16.4 ms: 1.02x faster                                                 |
| richards                | 33.3 ms                                                               | 33.4 ms: 1.01x slower                                                 |
| scimark_fft             | 199 ms                                                                | 197 ms: 1.01x faster                                                  |
| scimark_lu              | 71.8 ms                                                               | 72.7 ms: 1.01x slower                                                 |
| scimark_monte_carlo     | 48.9 ms                                                               | 53.8 ms: 1.10x slower                                                 |
| scimark_sor             | 77.6 ms                                                               | 99.0 ms: 1.28x slower                                                 |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.80 ms: 1.15x faster                                                 |
| spectral_norm           | 72.2 ms                                                               | 71.7 ms: 1.01x faster                                                 |
| sqlalchemy_declarative  | 61.8 ms                                                               | 61.5 ms: 1.00x faster                                                 |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.12 ms: 1.02x faster                                                 |
| sqlglot_parse           | 1.19 ms                                                               | 1.00 ms: 1.18x faster                                                 |
| sqlglot_transpile       | 1.35 ms                                                               | 1.16 ms: 1.16x faster                                                 |
| sqlglot_optimize        | 31.4 ms                                                               | 31.7 ms: 1.01x slower                                                 |
| sqlglot_normalize       | 169 ms                                                                | 172 ms: 1.01x slower                                                  |
| sqlite_synth            | 1.35 us                                                               | 1.40 us: 1.03x slower                                                 |
| sympy_expand            | 243 ms                                                                | 247 ms: 1.01x slower                                                  |
| sympy_integrate         | 11.6 ms                                                               | 11.5 ms: 1.01x faster                                                 |
| sympy_sum               | 82.4 ms                                                               | 84.0 ms: 1.02x slower                                                 |
| sympy_str               | 151 ms                                                                | 152 ms: 1.01x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.34 ms: 1.03x faster                                                 |
| thrift                  | 435 us                                                                | 441 us: 1.01x slower                                                  |
| unpack_sequence         | 32.2 ns                                                               | 33.0 ns: 1.02x slower                                                 |
| unpickle                | 9.97 us                                                               | 9.64 us: 1.03x faster                                                 |
| unpickle_list           | 2.77 us                                                               | 2.58 us: 1.07x faster                                                 |
| unpickle_pure_python    | 175 us                                                                | 160 us: 1.09x faster                                                  |
| xml_etree_parse         | 99.1 ms                                                               | 95.9 ms: 1.03x faster                                                 |
| xml_etree_iterparse     | 65.2 ms                                                               | 64.5 ms: 1.01x faster                                                 |
| xml_etree_generate      | 48.0 ms                                                               | 47.2 ms: 1.02x faster                                                 |
| xml_etree_process       | 34.8 ms                                                               | 34.5 ms: 1.01x faster                                                 |
| Geometric mean          | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (9): chaos, bench_mp_pool, mypy, nqueens, pathlib, pidigits, pycparser, pylint, tornado_http
Ignored benchmarks (2) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, gunicorn
Ignored benchmarks (1) of public/results/bm-20220904-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e/bm-20220904-darwin-arm64-python-a0ad63e70e3682cdf7e8-3.12.0a0-a0ad63e.json: coverage
