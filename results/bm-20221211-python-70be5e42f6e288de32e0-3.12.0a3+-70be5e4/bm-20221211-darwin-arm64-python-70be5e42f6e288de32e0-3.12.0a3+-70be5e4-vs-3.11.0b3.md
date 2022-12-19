Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 179 ms: 1.01x faster                                                   |
| chameleon      | 4.73 ms                                                               | 4.28 ms: 1.11x faster                                                  |
| docutils       | 1.46 sec                                                              | 1.44 sec: 1.02x faster                                                 |
| html5lib       | 35.8 ms                                                               | 34.3 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.05x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 51.9 ms: 1.07x faster                                                  |
| nbody          | 63.8 ms                                                               | 62.8 ms: 1.02x faster                                                  |
| pidigits       | 282 ms                                                                | 283 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 72.7 ms: 1.07x faster                                                  |
| regex_dna      | 149 ms                                                                | 149 ms: 1.00x faster                                                   |
| regex_effbot   | 2.40 ms                                                               | 2.60 ms: 1.09x slower                                                  |
| regex_v8       | 16.8 ms                                                               | 16.1 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 6.17 ms: 1.25x faster                                                  |
| json_loads           | 16.4 us                                                               | 16.3 us: 1.01x faster                                                  |
| pickle               | 7.14 us                                                               | 7.63 us: 1.07x slower                                                  |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list          | 2.73 us                                                               | 2.86 us: 1.05x slower                                                  |
| pickle_pure_python   | 222 us                                                                | 196 us: 1.13x faster                                                   |
| unpickle             | 9.97 us                                                               | 9.68 us: 1.03x faster                                                  |
| unpickle_list        | 2.77 us                                                               | 2.58 us: 1.07x faster                                                  |
| unpickle_pure_python | 175 us                                                                | 152 us: 1.15x faster                                                   |
| xml_etree_parse      | 99.1 ms                                                               | 93.1 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 65.2 ms                                                               | 65.6 ms: 1.01x slower                                                  |
| xml_etree_generate   | 48.0 ms                                                               | 47.1 ms: 1.02x faster                                                  |
| xml_etree_process    | 34.8 ms                                                               | 34.4 ms: 1.01x faster                                                  |
| Geometric mean       | (ref)                                                                 | 1.04x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.29 ms: 1.00x slower                                                  |
| python_startup_no_site | 7.30 ms                                                               | 7.34 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 20.2 ms: 1.04x faster                                                  |
| genshi_text     | 15.5 ms                                                               | 14.0 ms: 1.11x faster                                                  |
| genshi_xml      | 31.3 ms                                                               | 28.3 ms: 1.11x faster                                                  |
| mako            | 8.44 ms                                                               | 6.88 ms: 1.23x faster                                                  |
| Geometric mean  | (ref)                                                                 | 1.12x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 179 ms: 1.01x faster                                                   |
| async_generators        | 197 ms                                                                | 198 ms: 1.00x slower                                                   |
| async_tree_none         | 287 ms                                                                | 285 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed | 533 ms                                                                | 541 ms: 1.02x slower                                                   |
| async_tree_io           | 702 ms                                                                | 726 ms: 1.03x slower                                                   |
| async_tree_memoization  | 346 ms                                                                | 329 ms: 1.05x faster                                                   |
| chameleon               | 4.73 ms                                                               | 4.28 ms: 1.11x faster                                                  |
| chaos                   | 49.5 ms                                                               | 49.2 ms: 1.01x faster                                                  |
| bench_mp_pool           | 41.0 ms                                                               | 42.5 ms: 1.03x slower                                                  |
| bench_thread_pool       | 462 us                                                                | 442 us: 1.04x faster                                                   |
| coroutines              | 17.4 ms                                                               | 17.5 ms: 1.01x slower                                                  |
| crypto_pyaes            | 51.7 ms                                                               | 52.9 ms: 1.02x slower                                                  |
| deepcopy                | 237 us                                                                | 228 us: 1.04x faster                                                   |
| deepcopy_reduce         | 2.04 us                                                               | 1.94 us: 1.05x faster                                                  |
| deepcopy_memo           | 28.7 us                                                               | 27.2 us: 1.05x faster                                                  |
| deltablue               | 2.83 ms                                                               | 2.48 ms: 1.14x faster                                                  |
| django_template         | 21.0 ms                                                               | 20.2 ms: 1.04x faster                                                  |
| docutils                | 1.46 sec                                                              | 1.44 sec: 1.02x faster                                                 |
| dulwich_log             | 29.4 ms                                                               | 28.4 ms: 1.04x faster                                                  |
| fannkuch                | 261 ms                                                                | 256 ms: 1.02x faster                                                   |
| float                   | 55.7 ms                                                               | 51.9 ms: 1.07x faster                                                  |
| generators              | 27.7 ms                                                               | 32.0 ms: 1.16x slower                                                  |
| genshi_text             | 15.5 ms                                                               | 14.0 ms: 1.11x faster                                                  |
| genshi_xml              | 31.3 ms                                                               | 28.3 ms: 1.11x faster                                                  |
| hexiom                  | 4.71 ms                                                               | 4.59 ms: 1.02x faster                                                  |
| html5lib                | 35.8 ms                                                               | 34.3 ms: 1.05x faster                                                  |
| json                    | 2.91 ms                                                               | 2.84 ms: 1.02x faster                                                  |
| json_dumps              | 7.69 ms                                                               | 6.17 ms: 1.25x faster                                                  |
| json_loads              | 16.4 us                                                               | 16.3 us: 1.01x faster                                                  |
| logging_format          | 3.74 us                                                               | 3.71 us: 1.01x faster                                                  |
| logging_silent          | 65.7 ns                                                               | 62.3 ns: 1.05x faster                                                  |
| logging_simple          | 3.44 us                                                               | 3.40 us: 1.01x faster                                                  |
| mako                    | 8.44 ms                                                               | 6.88 ms: 1.23x faster                                                  |
| mdp                     | 1.53 sec                                                              | 1.50 sec: 1.02x faster                                                 |
| meteor_contest          | 77.8 ms                                                               | 76.3 ms: 1.02x faster                                                  |
| mypy                    | 418 ms                                                                | 410 ms: 1.02x faster                                                   |
| nbody                   | 63.8 ms                                                               | 62.8 ms: 1.02x faster                                                  |
| nqueens                 | 58.7 ms                                                               | 59.0 ms: 1.01x slower                                                  |
| pathlib                 | 20.8 ms                                                               | 20.3 ms: 1.03x faster                                                  |
| pickle                  | 7.14 us                                                               | 7.63 us: 1.07x slower                                                  |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list             | 2.73 us                                                               | 2.86 us: 1.05x slower                                                  |
| pickle_pure_python      | 222 us                                                                | 196 us: 1.13x faster                                                   |
| pidigits                | 282 ms                                                                | 283 ms: 1.00x slower                                                   |
| pprint_safe_repr        | 488 ms                                                                | 471 ms: 1.03x faster                                                   |
| pprint_pformat          | 1.00 sec                                                              | 960 ms: 1.05x faster                                                   |
| pycparser               | 704 ms                                                                | 670 ms: 1.05x faster                                                   |
| pyflate                 | 318 ms                                                                | 323 ms: 1.02x slower                                                   |
| python_startup          | 9.25 ms                                                               | 9.29 ms: 1.00x slower                                                  |
| python_startup_no_site  | 7.30 ms                                                               | 7.34 ms: 1.00x slower                                                  |
| raytrace                | 208 ms                                                                | 211 ms: 1.02x slower                                                   |
| regex_compile           | 77.7 ms                                                               | 72.7 ms: 1.07x faster                                                  |
| regex_dna               | 149 ms                                                                | 149 ms: 1.00x faster                                                   |
| regex_effbot            | 2.40 ms                                                               | 2.60 ms: 1.09x slower                                                  |
| regex_v8                | 16.8 ms                                                               | 16.1 ms: 1.05x faster                                                  |
| richards                | 33.3 ms                                                               | 28.9 ms: 1.15x faster                                                  |
| scimark_fft             | 199 ms                                                                | 194 ms: 1.03x faster                                                   |
| scimark_lu              | 71.8 ms                                                               | 69.2 ms: 1.04x faster                                                  |
| scimark_monte_carlo     | 48.9 ms                                                               | 48.3 ms: 1.01x faster                                                  |
| scimark_sor             | 77.6 ms                                                               | 77.5 ms: 1.00x faster                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 2.78 ms: 1.15x faster                                                  |
| spectral_norm           | 72.2 ms                                                               | 71.8 ms: 1.01x faster                                                  |
| sqlglot_parse           | 1.19 ms                                                               | 948 us: 1.25x faster                                                   |
| sqlglot_transpile       | 1.35 ms                                                               | 1.11 ms: 1.22x faster                                                  |
| sqlglot_optimize        | 31.4 ms                                                               | 31.0 ms: 1.01x faster                                                  |
| sqlglot_normalize       | 169 ms                                                                | 168 ms: 1.01x faster                                                   |
| sqlite_synth            | 1.35 us                                                               | 1.44 us: 1.07x slower                                                  |
| sympy_expand            | 243 ms                                                                | 241 ms: 1.01x faster                                                   |
| sympy_integrate         | 11.6 ms                                                               | 11.3 ms: 1.02x faster                                                  |
| sympy_sum               | 82.4 ms                                                               | 85.2 ms: 1.03x slower                                                  |
| sympy_str               | 151 ms                                                                | 150 ms: 1.00x faster                                                   |
| telco                   | 3.42 ms                                                               | 3.35 ms: 1.02x faster                                                  |
| thrift                  | 435 us                                                                | 429 us: 1.01x faster                                                   |
| unpack_sequence         | 32.2 ns                                                               | 30.1 ns: 1.07x faster                                                  |
| unpickle                | 9.97 us                                                               | 9.68 us: 1.03x faster                                                  |
| unpickle_list           | 2.77 us                                                               | 2.58 us: 1.07x faster                                                  |
| unpickle_pure_python    | 175 us                                                                | 152 us: 1.15x faster                                                   |
| xml_etree_parse         | 99.1 ms                                                               | 93.1 ms: 1.06x faster                                                  |
| xml_etree_iterparse     | 65.2 ms                                                               | 65.6 ms: 1.01x slower                                                  |
| xml_etree_generate      | 48.0 ms                                                               | 47.1 ms: 1.02x faster                                                  |
| xml_etree_process       | 34.8 ms                                                               | 34.4 ms: 1.01x faster                                                  |
| Geometric mean          | (ref)                                                                 | 1.03x faster                                                           |

Benchmark hidden because not significant (1): go
Ignored benchmarks (7) of public/results/bm-20220601-python-eb0004c27163ec089201-3.11.0b3-eb0004c/bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (1) of public/results/bm-20221211-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4/bm-20221211-darwin-arm64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4.json: coverage
