Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 182 ms                                                                | 181 ms: 1.00x faster                                                   |
| chameleon      | 4.73 ms                                                               | 4.63 ms: 1.02x faster                                                  |
| html5lib       | 35.8 ms                                                               | 34.7 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                           |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.7 ms                                                               | 52.9 ms: 1.05x faster                                                  |
| nbody          | 63.8 ms                                                               | 65.5 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 77.7 ms                                                               | 76.4 ms: 1.02x faster                                                  |
| regex_dna      | 149 ms                                                                | 152 ms: 1.01x slower                                                   |
| regex_effbot   | 2.40 ms                                                               | 2.63 ms: 1.10x slower                                                  |
| regex_v8       | 16.8 ms                                                               | 16.4 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.69 ms                                                               | 7.58 ms: 1.01x faster                                                  |
| json_loads           | 16.4 us                                                               | 16.2 us: 1.02x faster                                                  |
| pickle               | 7.14 us                                                               | 7.22 us: 1.01x slower                                                  |
| pickle_dict          | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list          | 2.73 us                                                               | 2.85 us: 1.05x slower                                                  |
| pickle_pure_python   | 222 us                                                                | 199 us: 1.11x faster                                                   |
| unpickle             | 9.97 us                                                               | 9.74 us: 1.02x faster                                                  |
| unpickle_list        | 2.77 us                                                               | 2.64 us: 1.05x faster                                                  |
| unpickle_pure_python | 175 us                                                                | 159 us: 1.10x faster                                                   |
| xml_etree_parse      | 99.1 ms                                                               | 99.5 ms: 1.00x slower                                                  |
| xml_etree_iterparse  | 65.2 ms                                                               | 65.7 ms: 1.01x slower                                                  |
| xml_etree_generate   | 48.0 ms                                                               | 48.3 ms: 1.01x slower                                                  |
| xml_etree_process    | 34.8 ms                                                               | 35.1 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.25 ms                                                               | 9.21 ms: 1.00x faster                                                  |
| python_startup_no_site | 7.30 ms                                                               | 7.27 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 21.0 ms                                                               | 21.1 ms: 1.00x slower                                                  |
| genshi_text     | 15.5 ms                                                               | 15.2 ms: 1.02x faster                                                  |
| genshi_xml      | 31.3 ms                                                               | 30.1 ms: 1.04x faster                                                  |
| mako            | 8.44 ms                                                               | 8.39 ms: 1.01x faster                                                  |
| Geometric mean  | (ref)                                                                 | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220601-darwin-arm64-python-eb0004c27163ec089201-3.11.0b3-eb0004c | bm-20220911-darwin-arm64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 182 ms                                                                | 181 ms: 1.00x faster                                                   |
| async_generators        | 197 ms                                                                | 195 ms: 1.01x faster                                                   |
| async_tree_none         | 287 ms                                                                | 281 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed | 533 ms                                                                | 529 ms: 1.01x faster                                                   |
| async_tree_io           | 702 ms                                                                | 698 ms: 1.01x faster                                                   |
| async_tree_memoization  | 346 ms                                                                | 317 ms: 1.09x faster                                                   |
| chameleon               | 4.73 ms                                                               | 4.63 ms: 1.02x faster                                                  |
| chaos                   | 49.5 ms                                                               | 49.3 ms: 1.00x faster                                                  |
| bench_thread_pool       | 462 us                                                                | 458 us: 1.01x faster                                                   |
| coroutines              | 17.4 ms                                                               | 17.6 ms: 1.01x slower                                                  |
| crypto_pyaes            | 51.7 ms                                                               | 51.8 ms: 1.00x slower                                                  |
| deepcopy                | 237 us                                                                | 222 us: 1.07x faster                                                   |
| deepcopy_reduce         | 2.04 us                                                               | 1.90 us: 1.07x faster                                                  |
| deepcopy_memo           | 28.7 us                                                               | 26.3 us: 1.09x faster                                                  |
| django_template         | 21.0 ms                                                               | 21.1 ms: 1.00x slower                                                  |
| dulwich_log             | 29.4 ms                                                               | 29.0 ms: 1.02x faster                                                  |
| fannkuch                | 261 ms                                                                | 263 ms: 1.01x slower                                                   |
| float                   | 55.7 ms                                                               | 52.9 ms: 1.05x faster                                                  |
| generators              | 27.7 ms                                                               | 28.4 ms: 1.03x slower                                                  |
| genshi_text             | 15.5 ms                                                               | 15.2 ms: 1.02x faster                                                  |
| genshi_xml              | 31.3 ms                                                               | 30.1 ms: 1.04x faster                                                  |
| go                      | 106 ms                                                                | 109 ms: 1.03x slower                                                   |
| hexiom                  | 4.71 ms                                                               | 4.72 ms: 1.00x slower                                                  |
| html5lib                | 35.8 ms                                                               | 34.7 ms: 1.03x faster                                                  |
| json                    | 2.91 ms                                                               | 2.83 ms: 1.03x faster                                                  |
| json_dumps              | 7.69 ms                                                               | 7.58 ms: 1.01x faster                                                  |
| json_loads              | 16.4 us                                                               | 16.2 us: 1.02x faster                                                  |
| logging_format          | 3.74 us                                                               | 3.73 us: 1.00x faster                                                  |
| logging_silent          | 65.7 ns                                                               | 67.5 ns: 1.03x slower                                                  |
| logging_simple          | 3.44 us                                                               | 3.45 us: 1.00x slower                                                  |
| mako                    | 8.44 ms                                                               | 8.39 ms: 1.01x faster                                                  |
| mdp                     | 1.53 sec                                                              | 1.54 sec: 1.01x slower                                                 |
| meteor_contest          | 77.8 ms                                                               | 74.0 ms: 1.05x faster                                                  |
| nbody                   | 63.8 ms                                                               | 65.5 ms: 1.03x slower                                                  |
| nqueens                 | 58.7 ms                                                               | 59.5 ms: 1.01x slower                                                  |
| pickle                  | 7.14 us                                                               | 7.22 us: 1.01x slower                                                  |
| pickle_dict             | 17.6 us                                                               | 18.0 us: 1.02x slower                                                  |
| pickle_list             | 2.73 us                                                               | 2.85 us: 1.05x slower                                                  |
| pickle_pure_python      | 222 us                                                                | 199 us: 1.11x faster                                                   |
| pprint_safe_repr        | 488 ms                                                                | 467 ms: 1.04x faster                                                   |
| pprint_pformat          | 1.00 sec                                                              | 954 ms: 1.05x faster                                                   |
| pyflate                 | 318 ms                                                                | 313 ms: 1.02x faster                                                   |
| python_startup          | 9.25 ms                                                               | 9.21 ms: 1.00x faster                                                  |
| python_startup_no_site  | 7.30 ms                                                               | 7.27 ms: 1.00x faster                                                  |
| raytrace                | 208 ms                                                                | 207 ms: 1.01x faster                                                   |
| regex_compile           | 77.7 ms                                                               | 76.4 ms: 1.02x faster                                                  |
| regex_dna               | 149 ms                                                                | 152 ms: 1.01x slower                                                   |
| regex_effbot            | 2.40 ms                                                               | 2.63 ms: 1.10x slower                                                  |
| regex_v8                | 16.8 ms                                                               | 16.4 ms: 1.02x faster                                                  |
| richards                | 33.3 ms                                                               | 32.8 ms: 1.01x faster                                                  |
| scimark_fft             | 199 ms                                                                | 201 ms: 1.01x slower                                                   |
| scimark_lu              | 71.8 ms                                                               | 72.3 ms: 1.01x slower                                                  |
| scimark_monte_carlo     | 48.9 ms                                                               | 46.8 ms: 1.04x faster                                                  |
| scimark_sor             | 77.6 ms                                                               | 83.0 ms: 1.07x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                               | 3.24 ms: 1.01x slower                                                  |
| spectral_norm           | 72.2 ms                                                               | 72.7 ms: 1.01x slower                                                  |
| sqlalchemy_declarative  | 61.8 ms                                                               | 62.4 ms: 1.01x slower                                                  |
| sqlalchemy_imperative   | 7.29 ms                                                               | 7.24 ms: 1.01x faster                                                  |
| sqlglot_parse           | 1.19 ms                                                               | 953 us: 1.25x faster                                                   |
| sqlglot_transpile       | 1.35 ms                                                               | 1.11 ms: 1.21x faster                                                  |
| sqlglot_optimize        | 31.4 ms                                                               | 31.2 ms: 1.00x faster                                                  |
| sqlglot_normalize       | 169 ms                                                                | 171 ms: 1.01x slower                                                   |
| sqlite_synth            | 1.35 us                                                               | 1.29 us: 1.04x faster                                                  |
| sympy_expand            | 243 ms                                                                | 242 ms: 1.00x faster                                                   |
| sympy_integrate         | 11.6 ms                                                               | 11.5 ms: 1.01x faster                                                  |
| sympy_sum               | 82.4 ms                                                               | 85.5 ms: 1.04x slower                                                  |
| telco                   | 3.42 ms                                                               | 3.40 ms: 1.01x faster                                                  |
| thrift                  | 435 us                                                                | 429 us: 1.01x faster                                                   |
| unpack_sequence         | 32.2 ns                                                               | 33.1 ns: 1.03x slower                                                  |
| unpickle                | 9.97 us                                                               | 9.74 us: 1.02x faster                                                  |
| unpickle_list           | 2.77 us                                                               | 2.64 us: 1.05x faster                                                  |
| unpickle_pure_python    | 175 us                                                                | 159 us: 1.10x faster                                                   |
| xml_etree_parse         | 99.1 ms                                                               | 99.5 ms: 1.00x slower                                                  |
| xml_etree_iterparse     | 65.2 ms                                                               | 65.7 ms: 1.01x slower                                                  |
| xml_etree_generate      | 48.0 ms                                                               | 48.3 ms: 1.01x slower                                                  |
| xml_etree_process       | 34.8 ms                                                               | 35.1 ms: 1.01x slower                                                  |
| Geometric mean          | (ref)                                                                 | 1.01x faster                                                           |

Benchmark hidden because not significant (13): aiohttp, bench_mp_pool, deltablue, docutils, flaskblogging, gunicorn, mypy, pathlib, pidigits, pycparser, pylint, sympy_str, tornado_http
