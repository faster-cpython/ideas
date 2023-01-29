
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 666c084
- commit date: 2023-01-28
- overall geometric mean: 1.00x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 185 ms: 1.02x slower                                   |
| chameleon      | 4.61 ms                                                             | 4.58 ms: 1.01x faster                                  |
| docutils       | 1.46 sec                                                            | 1.45 sec: 1.01x faster                                 |
| html5lib       | 34.7 ms                                                             | 35.2 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                               | 1.00x slower                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 64.2 ms: 1.02x faster                                  |
| pidigits       | 282 ms                                                              | 283 ms: 1.00x slower                                   |
| Geometric mean | (ref)                                                               | 1.00x faster                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 73.6 ms: 1.04x faster                                  |
| regex_dna      | 151 ms                                                              | 150 ms: 1.01x faster                                   |
| regex_effbot   | 2.63 ms                                                             | 2.65 ms: 1.01x slower                                  |
| regex_v8       | 16.5 ms                                                             | 16.1 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.13 ms: 1.25x faster                                  |
| json_loads           | 16.1 us                                                             | 16.4 us: 1.01x slower                                  |
| pickle               | 7.21 us                                                             | 7.52 us: 1.04x slower                                  |
| pickle_dict          | 17.9 us                                                             | 17.9 us: 1.00x faster                                  |
| pickle_pure_python   | 200 us                                                              | 192 us: 1.04x faster                                   |
| unpickle             | 9.68 us                                                             | 10.1 us: 1.05x slower                                  |
| unpickle_list        | 2.64 us                                                             | 2.73 us: 1.04x slower                                  |
| unpickle_pure_python | 159 us                                                              | 148 us: 1.08x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 93.9 ms: 1.06x faster                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 67.9 ms: 1.03x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 49.4 ms: 1.02x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 35.8 ms: 1.02x slower                                  |
| Geometric mean       | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.40 ms: 1.02x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.39 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                               | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.3 ms: 1.01x slower                                  |
| genshi_text     | 15.3 ms                                                             | 14.7 ms: 1.04x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 29.0 ms: 1.05x faster                                  |
| mako            | 8.40 ms                                                             | 7.25 ms: 1.16x faster                                  |
| Geometric mean  | (ref)                                                               | 1.06x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 185 ms: 1.02x slower                                   |
| async_generators        | 195 ms                                                              | 200 ms: 1.02x slower                                   |
| async_tree_none         | 281 ms                                                              | 288 ms: 1.02x slower                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 544 ms: 1.03x slower                                   |
| async_tree_io           | 696 ms                                                              | 740 ms: 1.06x slower                                   |
| async_tree_memoization  | 317 ms                                                              | 323 ms: 1.02x slower                                   |
| chameleon               | 4.61 ms                                                             | 4.58 ms: 1.01x faster                                  |
| chaos                   | 49.3 ms                                                             | 47.7 ms: 1.03x faster                                  |
| bench_mp_pool           | 41.4 ms                                                             | 42.6 ms: 1.03x slower                                  |
| bench_thread_pool       | 457 us                                                              | 450 us: 1.02x faster                                   |
| coroutines              | 17.8 ms                                                             | 18.8 ms: 1.06x slower                                  |
| coverage                | 58.4 ms                                                             | 57.1 ms: 1.02x faster                                  |
| crypto_pyaes            | 51.7 ms                                                             | 51.9 ms: 1.00x slower                                  |
| deepcopy                | 222 us                                                              | 219 us: 1.02x faster                                   |
| deepcopy_reduce         | 1.90 us                                                             | 1.88 us: 1.01x faster                                  |
| deepcopy_memo           | 26.2 us                                                             | 26.0 us: 1.01x faster                                  |
| deltablue               | 2.82 ms                                                             | 2.50 ms: 1.13x faster                                  |
| django_template         | 21.1 ms                                                             | 21.3 ms: 1.01x slower                                  |
| docutils                | 1.46 sec                                                            | 1.45 sec: 1.01x faster                                 |
| dulwich_log             | 29.1 ms                                                             | 28.5 ms: 1.02x faster                                  |
| fannkuch                | 262 ms                                                              | 258 ms: 1.02x faster                                   |
| generators              | 28.4 ms                                                             | 34.7 ms: 1.22x slower                                  |
| genshi_text             | 15.3 ms                                                             | 14.7 ms: 1.04x faster                                  |
| genshi_xml              | 30.5 ms                                                             | 29.0 ms: 1.05x faster                                  |
| go                      | 109 ms                                                              | 111 ms: 1.01x slower                                   |
| hexiom                  | 4.73 ms                                                             | 4.70 ms: 1.01x faster                                  |
| html5lib                | 34.7 ms                                                             | 35.2 ms: 1.02x slower                                  |
| json                    | 2.83 ms                                                             | 2.86 ms: 1.01x slower                                  |
| json_dumps              | 7.67 ms                                                             | 6.13 ms: 1.25x faster                                  |
| json_loads              | 16.1 us                                                             | 16.4 us: 1.01x slower                                  |
| logging_format          | 3.73 us                                                             | 3.79 us: 1.02x slower                                  |
| logging_silent          | 67.4 ns                                                             | 66.4 ns: 1.02x faster                                  |
| logging_simple          | 3.47 us                                                             | 3.51 us: 1.01x slower                                  |
| mako                    | 8.40 ms                                                             | 7.25 ms: 1.16x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.51 sec: 1.02x faster                                 |
| meteor_contest          | 73.9 ms                                                             | 73.8 ms: 1.00x faster                                  |
| mypy                    | 421 ms                                                              | 413 ms: 1.02x faster                                   |
| nbody                   | 65.2 ms                                                             | 64.2 ms: 1.02x faster                                  |
| nqueens                 | 59.5 ms                                                             | 59.9 ms: 1.01x slower                                  |
| pickle                  | 7.21 us                                                             | 7.52 us: 1.04x slower                                  |
| pickle_dict             | 17.9 us                                                             | 17.9 us: 1.00x faster                                  |
| pickle_pure_python      | 200 us                                                              | 192 us: 1.04x faster                                   |
| pidigits                | 282 ms                                                              | 283 ms: 1.00x slower                                   |
| pprint_safe_repr        | 467 ms                                                              | 468 ms: 1.00x slower                                   |
| pprint_pformat          | 953 ms                                                              | 950 ms: 1.00x faster                                   |
| pycparser               | 694 ms                                                              | 680 ms: 1.02x faster                                   |
| pyflate                 | 313 ms                                                              | 324 ms: 1.04x slower                                   |
| python_startup          | 9.19 ms                                                             | 9.40 ms: 1.02x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.39 ms: 1.02x slower                                  |
| raytrace                | 207 ms                                                              | 208 ms: 1.00x slower                                   |
| regex_compile           | 76.3 ms                                                             | 73.6 ms: 1.04x faster                                  |
| regex_dna               | 151 ms                                                              | 150 ms: 1.01x faster                                   |
| regex_effbot            | 2.63 ms                                                             | 2.65 ms: 1.01x slower                                  |
| regex_v8                | 16.5 ms                                                             | 16.1 ms: 1.02x faster                                  |
| richards                | 32.7 ms                                                             | 31.0 ms: 1.05x faster                                  |
| scimark_fft             | 201 ms                                                              | 192 ms: 1.04x faster                                   |
| scimark_lu              | 72.2 ms                                                             | 70.7 ms: 1.02x faster                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 48.9 ms: 1.04x slower                                  |
| scimark_sor             | 83.3 ms                                                             | 77.8 ms: 1.07x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.79 ms: 1.15x faster                                  |
| spectral_norm           | 72.7 ms                                                             | 72.3 ms: 1.01x faster                                  |
| sqlglot_parse           | 948 us                                                              | 1.02 ms: 1.07x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.18 ms: 1.06x slower                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 31.4 ms: 1.01x slower                                  |
| sqlglot_normalize       | 171 ms                                                              | 172 ms: 1.01x slower                                   |
| sqlite_synth            | 1.29 us                                                             | 1.36 us: 1.05x slower                                  |
| sympy_expand            | 242 ms                                                              | 240 ms: 1.01x faster                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.1 ms: 1.03x faster                                  |
| sympy_sum               | 85.5 ms                                                             | 81.9 ms: 1.04x faster                                  |
| sympy_str               | 151 ms                                                              | 145 ms: 1.04x faster                                   |
| telco                   | 3.39 ms                                                             | 3.43 ms: 1.01x slower                                  |
| thrift                  | 429 us                                                              | 449 us: 1.04x slower                                   |
| unpack_sequence         | 33.1 ns                                                             | 32.8 ns: 1.01x faster                                  |
| unpickle                | 9.68 us                                                             | 10.1 us: 1.05x slower                                  |
| unpickle_list           | 2.64 us                                                             | 2.73 us: 1.04x slower                                  |
| unpickle_pure_python    | 159 us                                                              | 148 us: 1.08x faster                                   |
| xml_etree_parse         | 99.6 ms                                                             | 93.9 ms: 1.06x faster                                  |
| xml_etree_iterparse     | 65.6 ms                                                             | 67.9 ms: 1.03x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 49.4 ms: 1.02x slower                                  |
| xml_etree_process       | 35.1 ms                                                             | 35.8 ms: 1.02x slower                                  |
| Geometric mean          | (ref)                                                               | 1.00x faster                                           |

Benchmark hidden because not significant (4): float, pathlib, pickle_list, tornado_http
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of public/results/bm-20230128-3.12.0a4+-666c084/bm-20230128-darwin-arm64-python-main-3.12.0a4+-666c084.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
