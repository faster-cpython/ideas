Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 185 ms: 1.02x slower                                                   |
| chameleon      | 4.73 ms                                                               | 4.50 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                           |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 57.0 ms: 1.02x slower                                                  |
| nbody          | 63.8 ms                                                               | 64.4 ms: 1.01x slower                                                  |
| pidigits       | 282 ms                                                                | 283 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 75.7 ms: 1.03x faster                                                  |
| regex_dna      | 149 ms                                                                | 149 ms: 1.00x faster                                                   |
| regex_effbot   | 2.40 ms                                                               | 2.60 ms: 1.09x slower                                                  |
| regex_v8       | 16.8 ms                                                               | 16.1 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.07 ms: 1.27x faster                                                  |
| json_loads           | 16.4 us                                                               | 16.4 us: 1.00x faster                                                  |
| pickle               | 7.14 us                                                               | 7.61 us: 1.07x slower                                                  |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list          | 2.73 us                                                               | 2.86 us: 1.05x slower                                                  |
| pickle_pure_python   | 222 us                                                                | 209 us: 1.06x faster                                                   |
| unpickle             | 9.97 us                                                               | 9.79 us: 1.02x faster                                                  |
| unpickle_list        | 2.77 us                                                               | 2.62 us: 1.06x faster                                                  |
| unpickle_pure_python | 175 us                                                                | 161 us: 1.09x faster                                                   |
| xml_etree_parse      | 99.1 ms                                                               | 92.9 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 65.2 ms                                                               | 66.3 ms: 1.02x slower                                                  |
| xml_etree_generate   | 48.0 ms                                                               | 48.4 ms: 1.01x slower                                                  |
| xml_etree_process    | 34.8 ms                                                               | 35.1 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.49 ms: 1.03x slower                                                  |
| python_startup_no_site | 7.30 ms                                                               | 7.54 ms: 1.03x slower                                                  |
| Geometric mean         | (ref)                                                                 | 1.03x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.4 ms: 1.02x slower                                                  |
| genshi_text     | 15.5 ms                                                               | 14.6 ms: 1.07x faster                                                  |
| genshi_xml      | 31.3 ms                                                               | 29.5 ms: 1.06x faster                                                  |
| mako            | 8.44 ms                                                               | 7.29 ms: 1.16x faster                                                  |
| Geometric mean  | (ref)                                                                 | 1.07x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 185 ms: 1.02x slower                                                   |
| async_generators        | 197 ms                                                                | 204 ms: 1.04x slower                                                   |
| async_tree_none         | 287 ms                                                                | 285 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed | 533 ms                                                                | 543 ms: 1.02x slower                                                   |
| async_tree_io           | 702 ms                                                                | 733 ms: 1.04x slower                                                   |
| async_tree_memoization  | 346 ms                                                                | 322 ms: 1.08x faster                                                   |
| chameleon               | 4.73 ms                                                               | 4.50 ms: 1.05x faster                                                  |
| chaos                   | 49.5 ms                                                               | 50.5 ms: 1.02x slower                                                  |
| bench_mp_pool           | 41.0 ms                                                               | 42.2 ms: 1.03x slower                                                  |
| bench_thread_pool       | 462 us                                                                | 454 us: 1.02x faster                                                   |
| coroutines              | 17.4 ms                                                               | 19.9 ms: 1.14x slower                                                  |
| crypto_pyaes            | 51.7 ms                                                               | 53.3 ms: 1.03x slower                                                  |
| deepcopy                | 237 us                                                                | 243 us: 1.02x slower                                                   |
| deepcopy_reduce         | 2.04 us                                                               | 2.07 us: 1.02x slower                                                  |
| deepcopy_memo           | 28.7 us                                                               | 30.1 us: 1.05x slower                                                  |
| deltablue               | 2.83 ms                                                               | 2.79 ms: 1.01x faster                                                  |
| django_template         | 21.0 ms                                                               | 21.4 ms: 1.02x slower                                                  |
| dulwich_log             | 29.4 ms                                                               | 29.2 ms: 1.01x faster                                                  |
| fannkuch                | 261 ms                                                                | 270 ms: 1.04x slower                                                   |
| float                   | 55.7 ms                                                               | 57.0 ms: 1.02x slower                                                  |
| generators              | 27.7 ms                                                               | 33.8 ms: 1.22x slower                                                  |
| genshi_text             | 15.5 ms                                                               | 14.6 ms: 1.07x faster                                                  |
| genshi_xml              | 31.3 ms                                                               | 29.5 ms: 1.06x faster                                                  |
| go                      | 106 ms                                                                | 118 ms: 1.11x slower                                                   |
| hexiom                  | 4.71 ms                                                               | 4.92 ms: 1.05x slower                                                  |
| json                    | 2.91 ms                                                               | 2.88 ms: 1.01x faster                                                  |
| json_dumps              | 7.69 ms                                                               | 6.07 ms: 1.27x faster                                                  |
| json_loads              | 16.4 us                                                               | 16.4 us: 1.00x faster                                                  |
| logging_format          | 3.74 us                                                               | 3.93 us: 1.05x slower                                                  |
| logging_silent          | 65.7 ns                                                               | 64.2 ns: 1.02x faster                                                  |
| logging_simple          | 3.44 us                                                               | 3.64 us: 1.06x slower                                                  |
| mako                    | 8.44 ms                                                               | 7.29 ms: 1.16x faster                                                  |
| mdp                     | 1.53 sec                                                              | 1.54 sec: 1.01x slower                                                 |
| meteor_contest          | 77.8 ms                                                               | 77.6 ms: 1.00x faster                                                  |
| nbody                   | 63.8 ms                                                               | 64.4 ms: 1.01x slower                                                  |
| nqueens                 | 58.7 ms                                                               | 61.7 ms: 1.05x slower                                                  |
| pathlib                 | 20.8 ms                                                               | 20.4 ms: 1.02x faster                                                  |
| pickle                  | 7.14 us                                                               | 7.61 us: 1.07x slower                                                  |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list             | 2.73 us                                                               | 2.86 us: 1.05x slower                                                  |
| pickle_pure_python      | 222 us                                                                | 209 us: 1.06x faster                                                   |
| pidigits                | 282 ms                                                                | 283 ms: 1.00x slower                                                   |
| pprint_safe_repr        | 488 ms                                                                | 496 ms: 1.02x slower                                                   |
| pprint_pformat          | 1.00 sec                                                              | 1.01 sec: 1.01x slower                                                 |
| pyflate                 | 318 ms                                                                | 351 ms: 1.10x slower                                                   |
| python_startup          | 9.25 ms                                                               | 9.49 ms: 1.03x slower                                                  |
| python_startup_no_site  | 7.30 ms                                                               | 7.54 ms: 1.03x slower                                                  |
| raytrace                | 208 ms                                                                | 219 ms: 1.05x slower                                                   |
| regex_compile           | 77.7 ms                                                               | 75.7 ms: 1.03x faster                                                  |
| regex_dna               | 149 ms                                                                | 149 ms: 1.00x faster                                                   |
| regex_effbot            | 2.40 ms                                                               | 2.60 ms: 1.09x slower                                                  |
| regex_v8                | 16.8 ms                                                               | 16.1 ms: 1.05x faster                                                  |
| richards                | 33.3 ms                                                               | 31.0 ms: 1.07x faster                                                  |
| scimark_fft             | 199 ms                                                                | 197 ms: 1.01x faster                                                   |
| scimark_lu              | 71.8 ms                                                               | 71.2 ms: 1.01x faster                                                  |
| scimark_monte_carlo     | 48.9 ms                                                               | 55.5 ms: 1.14x slower                                                  |
| scimark_sor             | 77.6 ms                                                               | 98.4 ms: 1.27x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.80 ms: 1.14x faster                                                  |
| spectral_norm           | 72.2 ms                                                               | 72.9 ms: 1.01x slower                                                  |
| sqlglot_parse           | 1.19 ms                                                               | 995 us: 1.19x faster                                                   |
| sqlglot_transpile       | 1.35 ms                                                               | 1.16 ms: 1.17x faster                                                  |
| sqlglot_optimize        | 31.4 ms                                                               | 31.6 ms: 1.01x slower                                                  |
| sqlglot_normalize       | 169 ms                                                                | 174 ms: 1.03x slower                                                   |
| sqlite_synth            | 1.35 us                                                               | 1.41 us: 1.04x slower                                                  |
| sympy_expand            | 243 ms                                                                | 248 ms: 1.02x slower                                                   |
| sympy_integrate         | 11.6 ms                                                               | 11.7 ms: 1.01x slower                                                  |
| sympy_sum               | 82.4 ms                                                               | 87.1 ms: 1.06x slower                                                  |
| sympy_str               | 151 ms                                                                | 154 ms: 1.02x slower                                                   |
| thrift                  | 435 us                                                                | 438 us: 1.01x slower                                                   |
| unpack_sequence         | 32.2 ns                                                               | 61.5 ns: 1.91x slower                                                  |
| unpickle                | 9.97 us                                                               | 9.79 us: 1.02x faster                                                  |
| unpickle_list           | 2.77 us                                                               | 2.62 us: 1.06x faster                                                  |
| unpickle_pure_python    | 175 us                                                                | 161 us: 1.09x faster                                                   |
| xml_etree_parse         | 99.1 ms                                                               | 92.9 ms: 1.07x faster                                                  |
| xml_etree_iterparse     | 65.2 ms                                                               | 66.3 ms: 1.02x slower                                                  |
| xml_etree_generate      | 48.0 ms                                                               | 48.4 ms: 1.01x slower                                                  |
| xml_etree_process       | 34.8 ms                                                               | 35.1 ms: 1.01x slower                                                  |
| Geometric mean          | (ref)                                                                 | 1.01x slower                                                           |

Benchmark hidden because not significant (6): docutils, html5lib, mypy, pycparser, telco, tornado_http
Ignored benchmarks (6) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of public/results/bm-20221121-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d/bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d.json: coverage
