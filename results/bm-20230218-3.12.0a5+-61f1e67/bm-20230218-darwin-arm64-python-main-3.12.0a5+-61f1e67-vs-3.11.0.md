
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 61f1e67
- commit date: 2023-02-18
- overall geometric mean: 1.01x slower \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 161 ms: 1.12x faster                                   |
| chameleon      | 4.61 ms                                                             | 4.45 ms: 1.04x faster                                  |
| docutils       | 1.46 sec                                                            | 1.48 sec: 1.01x slower                                 |
| html5lib       | 34.7 ms                                                             | 35.5 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                               | 1.03x faster                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 64.1 ms: 1.02x faster                                  |
| pidigits       | 282 ms                                                              | 281 ms: 1.01x faster                                   |
| float          | 51.7 ms                                                             | 52.4 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                               | 1.00x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 16.5 ms                                                             | 15.7 ms: 1.05x faster                                  |
| regex_compile  | 76.3 ms                                                             | 72.9 ms: 1.05x faster                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.02x faster                                   |
| regex_effbot   | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                               | 1.03x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.16 ms: 1.24x faster                                  |
| unpickle_pure_python | 159 us                                                              | 142 us: 1.12x faster                                   |
| pickle_pure_python   | 200 us                                                              | 193 us: 1.04x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 96.6 ms: 1.03x faster                                  |
| unpickle_list        | 2.64 us                                                             | 2.56 us: 1.03x faster                                  |
| pickle_list          | 2.86 us                                                             | 2.80 us: 1.02x faster                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 35.9 ms: 1.02x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 50.2 ms: 1.04x slower                                  |
| pickle               | 7.21 us                                                             | 7.50 us: 1.04x slower                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 69.8 ms: 1.06x slower                                  |
| Geometric mean       | (ref)                                                               | 1.02x faster                                           |

Benchmark hidden because not significant (2): json_loads, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 11.4 ms: 1.24x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 9.34 ms: 1.29x slower                                  |
| Geometric mean         | (ref)                                                               | 1.26x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 8.40 ms                                                             | 7.35 ms: 1.14x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 28.2 ms: 1.08x faster                                  |
| genshi_text     | 15.3 ms                                                             | 14.3 ms: 1.07x faster                                  |
| django_template | 21.1 ms                                                             | 21.3 ms: 1.01x slower                                  |
| Geometric mean  | (ref)                                                               | 1.07x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps              | 7.67 ms                                                             | 6.16 ms: 1.24x faster                                  |
| mako                    | 8.40 ms                                                             | 7.35 ms: 1.14x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.81 ms: 1.14x faster                                  |
| 2to3                    | 181 ms                                                              | 161 ms: 1.12x faster                                   |
| unpickle_pure_python    | 159 us                                                              | 142 us: 1.12x faster                                   |
| generators              | 28.4 ms                                                             | 25.5 ms: 1.11x faster                                  |
| deltablue               | 2.82 ms                                                             | 2.56 ms: 1.10x faster                                  |
| hexiom                  | 4.73 ms                                                             | 4.30 ms: 1.10x faster                                  |
| richards                | 32.7 ms                                                             | 29.9 ms: 1.10x faster                                  |
| genshi_xml              | 30.5 ms                                                             | 28.2 ms: 1.08x faster                                  |
| genshi_text             | 15.3 ms                                                             | 14.3 ms: 1.07x faster                                  |
| chaos                   | 49.3 ms                                                             | 46.5 ms: 1.06x faster                                  |
| regex_v8                | 16.5 ms                                                             | 15.7 ms: 1.05x faster                                  |
| pycparser               | 694 ms                                                              | 662 ms: 1.05x faster                                   |
| regex_compile           | 76.3 ms                                                             | 72.9 ms: 1.05x faster                                  |
| scimark_fft             | 201 ms                                                              | 193 ms: 1.04x faster                                   |
| chameleon               | 4.61 ms                                                             | 4.45 ms: 1.04x faster                                  |
| pickle_pure_python      | 200 us                                                              | 193 us: 1.04x faster                                   |
| deepcopy_memo           | 26.2 us                                                             | 25.3 us: 1.03x faster                                  |
| xml_etree_parse         | 99.6 ms                                                             | 96.6 ms: 1.03x faster                                  |
| unpickle_list           | 2.64 us                                                             | 2.56 us: 1.03x faster                                  |
| fannkuch                | 262 ms                                                              | 255 ms: 1.03x faster                                   |
| sympy_str               | 151 ms                                                              | 147 ms: 1.03x faster                                   |
| sympy_sum               | 85.5 ms                                                             | 83.5 ms: 1.02x faster                                  |
| logging_silent          | 67.4 ns                                                             | 66.0 ns: 1.02x faster                                  |
| pickle_list             | 2.86 us                                                             | 2.80 us: 1.02x faster                                  |
| json                    | 2.83 ms                                                             | 2.77 ms: 1.02x faster                                  |
| nbody                   | 65.2 ms                                                             | 64.1 ms: 1.02x faster                                  |
| regex_dna               | 151 ms                                                              | 149 ms: 1.02x faster                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.3 ms: 1.01x faster                                  |
| unpack_sequence         | 33.1 ns                                                             | 32.7 ns: 1.01x faster                                  |
| go                      | 109 ms                                                              | 108 ms: 1.01x faster                                   |
| deepcopy                | 222 us                                                              | 220 us: 1.01x faster                                   |
| regex_effbot            | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                  |
| pidigits                | 282 ms                                                              | 281 ms: 1.01x faster                                   |
| mdp                     | 1.54 sec                                                            | 1.53 sec: 1.00x faster                                 |
| coroutines              | 17.8 ms                                                             | 17.7 ms: 1.00x faster                                  |
| sympy_expand            | 242 ms                                                              | 243 ms: 1.00x slower                                   |
| sqlalchemy_imperative   | 7.22 ms                                                             | 7.24 ms: 1.00x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| pprint_safe_repr        | 467 ms                                                              | 470 ms: 1.01x slower                                   |
| pprint_pformat          | 953 ms                                                              | 959 ms: 1.01x slower                                   |
| async_tree_none         | 281 ms                                                              | 283 ms: 1.01x slower                                   |
| scimark_lu              | 72.2 ms                                                             | 72.7 ms: 1.01x slower                                  |
| docutils                | 1.46 sec                                                            | 1.48 sec: 1.01x slower                                 |
| django_template         | 21.1 ms                                                             | 21.3 ms: 1.01x slower                                  |
| float                   | 51.7 ms                                                             | 52.4 ms: 1.01x slower                                  |
| bench_thread_pool       | 457 us                                                              | 463 us: 1.01x slower                                   |
| sqlglot_normalize       | 171 ms                                                              | 173 ms: 1.01x slower                                   |
| sqlglot_optimize        | 31.3 ms                                                             | 31.8 ms: 1.02x slower                                  |
| dulwich_log             | 29.1 ms                                                             | 29.5 ms: 1.02x slower                                  |
| sqlalchemy_declarative  | 62.4 ms                                                             | 63.4 ms: 1.02x slower                                  |
| deepcopy_reduce         | 1.90 us                                                             | 1.93 us: 1.02x slower                                  |
| async_tree_cpu_io_mixed | 528 ms                                                              | 541 ms: 1.02x slower                                   |
| xml_etree_process       | 35.1 ms                                                             | 35.9 ms: 1.02x slower                                  |
| html5lib                | 34.7 ms                                                             | 35.5 ms: 1.02x slower                                  |
| telco                   | 3.39 ms                                                             | 3.47 ms: 1.02x slower                                  |
| meteor_contest          | 73.9 ms                                                             | 75.8 ms: 1.02x slower                                  |
| nqueens                 | 59.5 ms                                                             | 61.1 ms: 1.03x slower                                  |
| async_tree_memoization  | 317 ms                                                              | 325 ms: 1.03x slower                                   |
| scimark_sor             | 83.3 ms                                                             | 85.9 ms: 1.03x slower                                  |
| spectral_norm           | 72.7 ms                                                             | 75.2 ms: 1.03x slower                                  |
| crypto_pyaes            | 51.7 ms                                                             | 53.5 ms: 1.04x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 50.2 ms: 1.04x slower                                  |
| pyflate                 | 313 ms                                                              | 325 ms: 1.04x slower                                   |
| pickle                  | 7.21 us                                                             | 7.50 us: 1.04x slower                                  |
| logging_format          | 3.73 us                                                             | 3.89 us: 1.04x slower                                  |
| logging_simple          | 3.47 us                                                             | 3.61 us: 1.04x slower                                  |
| coverage                | 58.4 ms                                                             | 61.0 ms: 1.04x slower                                  |
| sqlite_synth            | 1.29 us                                                             | 1.36 us: 1.05x slower                                  |
| async_tree_io           | 696 ms                                                              | 736 ms: 1.06x slower                                   |
| xml_etree_iterparse     | 65.6 ms                                                             | 69.8 ms: 1.06x slower                                  |
| thrift                  | 429 us                                                              | 458 us: 1.07x slower                                   |
| raytrace                | 207 ms                                                              | 223 ms: 1.07x slower                                   |
| bench_mp_pool           | 41.4 ms                                                             | 45.0 ms: 1.09x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.22 ms: 1.10x slower                                  |
| sqlglot_parse           | 948 us                                                              | 1.05 ms: 1.11x slower                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 52.4 ms: 1.12x slower                                  |
| python_startup          | 9.19 ms                                                             | 11.4 ms: 1.24x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 9.34 ms: 1.29x slower                                  |
| pathlib                 | 20.6 ms                                                             | 27.4 ms: 1.33x slower                                  |
| async_generators        | 195 ms                                                              | 263 ms: 1.35x slower                                   |
| Geometric mean          | (ref)                                                               | 1.01x slower                                           |

Benchmark hidden because not significant (3): tornado_http, json_loads, unpickle
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230218-3.12.0a5+-61f1e67/bm-20230218-darwin-arm64-python-main-3.12.0a5+-61f1e67.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal, mypy2
