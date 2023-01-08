
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 951303f
- commit date: 2023-01-07
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 182 ms: 1.00x slower                                   |
| chameleon      | 4.61 ms                                                             | 4.48 ms: 1.03x faster                                  |
| docutils       | 1.46 sec                                                            | 1.43 sec: 1.02x faster                                 |
| Geometric mean | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 65.2 ms                                                             | 63.8 ms: 1.02x faster                                  |
| pidigits       | 282 ms                                                              | 277 ms: 1.02x faster                                   |
| Geometric mean | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 75.2 ms: 1.02x faster                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                   |
| regex_effbot   | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                  |
| regex_v8       | 16.5 ms                                                             | 16.1 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                               | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.10 ms: 1.26x faster                                  |
| json_loads           | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| pickle               | 7.21 us                                                             | 7.52 us: 1.04x slower                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| pickle_pure_python   | 200 us                                                              | 192 us: 1.04x faster                                   |
| unpickle             | 9.68 us                                                             | 9.05 us: 1.07x faster                                  |
| unpickle_pure_python | 159 us                                                              | 142 us: 1.12x faster                                   |
| xml_etree_parse      | 99.6 ms                                                             | 92.8 ms: 1.07x faster                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 66.2 ms: 1.01x slower                                  |
| xml_etree_generate   | 48.4 ms                                                             | 48.5 ms: 1.00x slower                                  |
| xml_etree_process    | 35.1 ms                                                             | 34.7 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                               | 1.04x faster                                           |

Benchmark hidden because not significant (2): pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.28 ms: 1.01x slower                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.32 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                               | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.3 ms: 1.01x slower                                  |
| genshi_text     | 15.3 ms                                                             | 14.3 ms: 1.08x faster                                  |
| genshi_xml      | 30.5 ms                                                             | 28.2 ms: 1.08x faster                                  |
| mako            | 8.40 ms                                                             | 7.10 ms: 1.18x faster                                  |
| Geometric mean  | (ref)                                                               | 1.08x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 182 ms: 1.00x slower                                   |
| async_generators        | 195 ms                                                              | 200 ms: 1.03x slower                                   |
| async_tree_none         | 281 ms                                                              | 287 ms: 1.02x slower                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 541 ms: 1.02x slower                                   |
| async_tree_io           | 696 ms                                                              | 736 ms: 1.06x slower                                   |
| async_tree_memoization  | 317 ms                                                              | 328 ms: 1.04x slower                                   |
| chameleon               | 4.61 ms                                                             | 4.48 ms: 1.03x faster                                  |
| chaos                   | 49.3 ms                                                             | 50.3 ms: 1.02x slower                                  |
| bench_thread_pool       | 457 us                                                              | 450 us: 1.02x faster                                   |
| coroutines              | 17.8 ms                                                             | 18.8 ms: 1.06x slower                                  |
| coverage                | 58.4 ms                                                             | 57.3 ms: 1.02x faster                                  |
| crypto_pyaes            | 51.7 ms                                                             | 53.7 ms: 1.04x slower                                  |
| deepcopy                | 222 us                                                              | 219 us: 1.02x faster                                   |
| deepcopy_reduce         | 1.90 us                                                             | 1.91 us: 1.01x slower                                  |
| deepcopy_memo           | 26.2 us                                                             | 25.6 us: 1.02x faster                                  |
| deltablue               | 2.82 ms                                                             | 2.56 ms: 1.10x faster                                  |
| django_template         | 21.1 ms                                                             | 21.3 ms: 1.01x slower                                  |
| docutils                | 1.46 sec                                                            | 1.43 sec: 1.02x faster                                 |
| dulwich_log             | 29.1 ms                                                             | 28.7 ms: 1.01x faster                                  |
| fannkuch                | 262 ms                                                              | 258 ms: 1.02x faster                                   |
| generators              | 28.4 ms                                                             | 33.7 ms: 1.19x slower                                  |
| genshi_text             | 15.3 ms                                                             | 14.3 ms: 1.08x faster                                  |
| genshi_xml              | 30.5 ms                                                             | 28.2 ms: 1.08x faster                                  |
| go                      | 109 ms                                                              | 108 ms: 1.02x faster                                   |
| hexiom                  | 4.73 ms                                                             | 4.78 ms: 1.01x slower                                  |
| json_dumps              | 7.67 ms                                                             | 6.10 ms: 1.26x faster                                  |
| json_loads              | 16.1 us                                                             | 16.3 us: 1.01x slower                                  |
| logging_format          | 3.73 us                                                             | 3.81 us: 1.02x slower                                  |
| logging_silent          | 67.4 ns                                                             | 64.9 ns: 1.04x faster                                  |
| logging_simple          | 3.47 us                                                             | 3.52 us: 1.01x slower                                  |
| mako                    | 8.40 ms                                                             | 7.10 ms: 1.18x faster                                  |
| mdp                     | 1.54 sec                                                            | 1.53 sec: 1.00x faster                                 |
| meteor_contest          | 73.9 ms                                                             | 76.3 ms: 1.03x slower                                  |
| mypy                    | 421 ms                                                              | 413 ms: 1.02x faster                                   |
| nbody                   | 65.2 ms                                                             | 63.8 ms: 1.02x faster                                  |
| nqueens                 | 59.5 ms                                                             | 60.2 ms: 1.01x slower                                  |
| pickle                  | 7.21 us                                                             | 7.52 us: 1.04x slower                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.00x slower                                  |
| pickle_pure_python      | 200 us                                                              | 192 us: 1.04x faster                                   |
| pidigits                | 282 ms                                                              | 277 ms: 1.02x faster                                   |
| pprint_safe_repr        | 467 ms                                                              | 455 ms: 1.03x faster                                   |
| pprint_pformat          | 953 ms                                                              | 925 ms: 1.03x faster                                   |
| pycparser               | 694 ms                                                              | 685 ms: 1.01x faster                                   |
| pyflate                 | 313 ms                                                              | 322 ms: 1.03x slower                                   |
| python_startup          | 9.19 ms                                                             | 9.28 ms: 1.01x slower                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.32 ms: 1.01x slower                                  |
| raytrace                | 207 ms                                                              | 221 ms: 1.07x slower                                   |
| regex_compile           | 76.3 ms                                                             | 75.2 ms: 1.02x faster                                  |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                   |
| regex_effbot            | 2.63 ms                                                             | 2.61 ms: 1.01x faster                                  |
| regex_v8                | 16.5 ms                                                             | 16.1 ms: 1.03x faster                                  |
| richards                | 32.7 ms                                                             | 30.4 ms: 1.08x faster                                  |
| scimark_fft             | 201 ms                                                              | 195 ms: 1.03x faster                                   |
| scimark_lu              | 72.2 ms                                                             | 71.9 ms: 1.00x faster                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 51.0 ms: 1.09x slower                                  |
| scimark_sor             | 83.3 ms                                                             | 82.4 ms: 1.01x faster                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.82 ms: 1.14x faster                                  |
| sqlglot_parse           | 948 us                                                              | 1.04 ms: 1.09x slower                                  |
| sqlglot_transpile       | 1.11 ms                                                             | 1.20 ms: 1.08x slower                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 31.0 ms: 1.01x faster                                  |
| sqlglot_normalize       | 171 ms                                                              | 170 ms: 1.01x faster                                   |
| sqlite_synth            | 1.29 us                                                             | 1.35 us: 1.04x slower                                  |
| sympy_expand            | 242 ms                                                              | 241 ms: 1.01x faster                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.4 ms: 1.01x faster                                  |
| sympy_sum               | 85.5 ms                                                             | 85.9 ms: 1.00x slower                                  |
| sympy_str               | 151 ms                                                              | 151 ms: 1.00x slower                                   |
| telco                   | 3.39 ms                                                             | 3.47 ms: 1.02x slower                                  |
| thrift                  | 429 us                                                              | 439 us: 1.02x slower                                   |
| unpack_sequence         | 33.1 ns                                                             | 32.5 ns: 1.02x faster                                  |
| unpickle                | 9.68 us                                                             | 9.05 us: 1.07x faster                                  |
| unpickle_pure_python    | 159 us                                                              | 142 us: 1.12x faster                                   |
| xml_etree_parse         | 99.6 ms                                                             | 92.8 ms: 1.07x faster                                  |
| xml_etree_iterparse     | 65.6 ms                                                             | 66.2 ms: 1.01x slower                                  |
| xml_etree_generate      | 48.4 ms                                                             | 48.5 ms: 1.00x slower                                  |
| xml_etree_process       | 35.1 ms                                                             | 34.7 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (8): bench_mp_pool, float, html5lib, json, pathlib, pickle_list, spectral_norm, unpickle_list
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
