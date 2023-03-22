
# Results vs. 3.11.0

- fork: python
- ref: 72f00f420afaba3bc873
- machine: darwin-arm64
- commit hash: 72f00f4
- commit date: 2022-05-30
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| chameleon      | 4.61 ms                                                             | 4.71 ms: 1.02x slower                                                 |
| docutils       | 1.46 sec                                                            | 1.46 sec: 1.00x faster                                                |
| html5lib       | 34.7 ms                                                             | 35.9 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 63.9 ms: 1.02x faster                                                 |
| pidigits       | 282 ms                                                              | 282 ms: 1.00x slower                                                  |
| float          | 51.7 ms                                                             | 55.0 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                               | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.63 ms                                                             | 2.39 ms: 1.10x faster                                                 |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| regex_v8       | 16.5 ms                                                             | 16.6 ms: 1.01x slower                                                 |
| regex_compile  | 76.3 ms                                                             | 77.4 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                               | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 2.86 us                                                             | 2.71 us: 1.06x faster                                                 |
| pickle_dict          | 17.9 us                                                             | 17.2 us: 1.04x faster                                                 |
| pickle               | 7.21 us                                                             | 7.12 us: 1.01x faster                                                 |
| xml_etree_process    | 35.1 ms                                                             | 34.7 ms: 1.01x faster                                                 |
| json_dumps           | 7.67 ms                                                             | 7.63 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 65.6 ms                                                             | 65.3 ms: 1.00x faster                                                 |
| xml_etree_generate   | 48.4 ms                                                             | 48.2 ms: 1.00x faster                                                 |
| json_loads           | 16.1 us                                                             | 16.3 us: 1.01x slower                                                 |
| unpickle_list        | 2.64 us                                                             | 2.71 us: 1.03x slower                                                 |
| unpickle             | 9.68 us                                                             | 9.96 us: 1.03x slower                                                 |
| unpickle_pure_python | 159 us                                                              | 175 us: 1.10x slower                                                  |
| pickle_pure_python   | 200 us                                                              | 223 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                             | 7.20 ms: 1.01x faster                                                 |
| python_startup         | 9.19 ms                                                             | 9.15 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                               | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.0 ms: 1.00x faster                                                 |
| genshi_text     | 15.3 ms                                                             | 15.4 ms: 1.01x slower                                                 |
| genshi_xml      | 30.5 ms                                                             | 31.3 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| scimark_sor             | 83.3 ms                                                             | 75.5 ms: 1.10x faster                                                 |
| regex_effbot            | 2.63 ms                                                             | 2.39 ms: 1.10x faster                                                 |
| pickle_list             | 2.86 us                                                             | 2.71 us: 1.06x faster                                                 |
| pickle_dict             | 17.9 us                                                             | 17.2 us: 1.04x faster                                                 |
| sympy_sum               | 85.5 ms                                                             | 82.2 ms: 1.04x faster                                                 |
| logging_silent          | 67.4 ns                                                             | 65.4 ns: 1.03x faster                                                 |
| unpack_sequence         | 33.1 ns                                                             | 32.2 ns: 1.03x faster                                                 |
| generators              | 28.4 ms                                                             | 27.6 ms: 1.03x faster                                                 |
| nbody                   | 65.2 ms                                                             | 63.9 ms: 1.02x faster                                                 |
| coroutines              | 17.8 ms                                                             | 17.4 ms: 1.02x faster                                                 |
| go                      | 109 ms                                                              | 108 ms: 1.02x faster                                                  |
| sqlalchemy_declarative  | 62.4 ms                                                             | 61.5 ms: 1.02x faster                                                 |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                  |
| nqueens                 | 59.5 ms                                                             | 58.7 ms: 1.01x faster                                                 |
| pickle                  | 7.21 us                                                             | 7.12 us: 1.01x faster                                                 |
| xml_etree_process       | 35.1 ms                                                             | 34.7 ms: 1.01x faster                                                 |
| scimark_lu              | 72.2 ms                                                             | 71.4 ms: 1.01x faster                                                 |
| mypy                    | 421 ms                                                              | 416 ms: 1.01x faster                                                  |
| sqlglot_normalize       | 171 ms                                                              | 170 ms: 1.01x faster                                                  |
| fannkuch                | 262 ms                                                              | 260 ms: 1.01x faster                                                  |
| hexiom                  | 4.73 ms                                                             | 4.70 ms: 1.01x faster                                                 |
| spectral_norm           | 72.7 ms                                                             | 72.2 ms: 1.01x faster                                                 |
| mdp                     | 1.54 sec                                                            | 1.53 sec: 1.01x faster                                                |
| python_startup_no_site  | 7.24 ms                                                             | 7.20 ms: 1.01x faster                                                 |
| json_dumps              | 7.67 ms                                                             | 7.63 ms: 1.01x faster                                                 |
| django_template         | 21.1 ms                                                             | 21.0 ms: 1.00x faster                                                 |
| sympy_str               | 151 ms                                                              | 150 ms: 1.00x faster                                                  |
| python_startup          | 9.19 ms                                                             | 9.15 ms: 1.00x faster                                                 |
| xml_etree_iterparse     | 65.6 ms                                                             | 65.3 ms: 1.00x faster                                                 |
| scimark_fft             | 201 ms                                                              | 200 ms: 1.00x faster                                                  |
| xml_etree_generate      | 48.4 ms                                                             | 48.2 ms: 1.00x faster                                                 |
| docutils                | 1.46 sec                                                            | 1.46 sec: 1.00x faster                                                |
| crypto_pyaes            | 51.7 ms                                                             | 51.6 ms: 1.00x faster                                                 |
| pidigits                | 282 ms                                                              | 282 ms: 1.00x slower                                                  |
| sympy_expand            | 242 ms                                                              | 243 ms: 1.00x slower                                                  |
| sympy_integrate         | 11.5 ms                                                             | 11.5 ms: 1.00x slower                                                 |
| sqlglot_optimize        | 31.3 ms                                                             | 31.4 ms: 1.00x slower                                                 |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.26 ms: 1.01x slower                                                 |
| genshi_text             | 15.3 ms                                                             | 15.4 ms: 1.01x slower                                                 |
| deltablue               | 2.82 ms                                                             | 2.84 ms: 1.01x slower                                                 |
| telco                   | 3.39 ms                                                             | 3.41 ms: 1.01x slower                                                 |
| async_tree_io           | 696 ms                                                              | 702 ms: 1.01x slower                                                  |
| json_loads              | 16.1 us                                                             | 16.3 us: 1.01x slower                                                 |
| regex_v8                | 16.5 ms                                                             | 16.6 ms: 1.01x slower                                                 |
| bench_thread_pool       | 457 us                                                              | 462 us: 1.01x slower                                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 534 ms: 1.01x slower                                                  |
| async_generators        | 195 ms                                                              | 198 ms: 1.01x slower                                                  |
| pyflate                 | 313 ms                                                              | 316 ms: 1.01x slower                                                  |
| raytrace                | 207 ms                                                              | 210 ms: 1.01x slower                                                  |
| dulwich_log             | 29.1 ms                                                             | 29.4 ms: 1.01x slower                                                 |
| regex_compile           | 76.3 ms                                                             | 77.4 ms: 1.01x slower                                                 |
| thrift                  | 429 us                                                              | 437 us: 1.02x slower                                                  |
| async_tree_none         | 281 ms                                                              | 287 ms: 1.02x slower                                                  |
| chameleon               | 4.61 ms                                                             | 4.71 ms: 1.02x slower                                                 |
| richards                | 32.7 ms                                                             | 33.5 ms: 1.02x slower                                                 |
| genshi_xml              | 30.5 ms                                                             | 31.3 ms: 1.03x slower                                                 |
| unpickle_list           | 2.64 us                                                             | 2.71 us: 1.03x slower                                                 |
| unpickle                | 9.68 us                                                             | 9.96 us: 1.03x slower                                                 |
| json                    | 2.83 ms                                                             | 2.92 ms: 1.03x slower                                                 |
| html5lib                | 34.7 ms                                                             | 35.9 ms: 1.03x slower                                                 |
| scimark_monte_carlo     | 46.9 ms                                                             | 48.7 ms: 1.04x slower                                                 |
| sqlite_synth            | 1.29 us                                                             | 1.35 us: 1.04x slower                                                 |
| meteor_contest          | 73.9 ms                                                             | 77.4 ms: 1.05x slower                                                 |
| pprint_safe_repr        | 467 ms                                                              | 490 ms: 1.05x slower                                                  |
| pprint_pformat          | 953 ms                                                              | 1.01 sec: 1.06x slower                                                |
| float                   | 51.7 ms                                                             | 55.0 ms: 1.06x slower                                                 |
| deepcopy                | 222 us                                                              | 239 us: 1.07x slower                                                  |
| deepcopy_reduce         | 1.90 us                                                             | 2.05 us: 1.08x slower                                                 |
| async_tree_memoization  | 317 ms                                                              | 344 ms: 1.08x slower                                                  |
| deepcopy_memo           | 26.2 us                                                             | 28.5 us: 1.09x slower                                                 |
| unpickle_pure_python    | 159 us                                                              | 175 us: 1.10x slower                                                  |
| pickle_pure_python      | 200 us                                                              | 223 us: 1.11x slower                                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.35 ms: 1.21x slower                                                 |
| sqlglot_parse           | 948 us                                                              | 1.19 ms: 1.25x slower                                                 |
| Geometric mean          | (ref)                                                               | 1.01x slower                                                          |

Benchmark hidden because not significant (14): tornado_http, aiohttp, bench_mp_pool, pylint, xml_etree_parse, mako, logging_simple, scimark_sparse_mat_mult, chaos, 2to3, pathlib, logging_format, gunicorn, pycparser
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: coverage, flaskblogging
