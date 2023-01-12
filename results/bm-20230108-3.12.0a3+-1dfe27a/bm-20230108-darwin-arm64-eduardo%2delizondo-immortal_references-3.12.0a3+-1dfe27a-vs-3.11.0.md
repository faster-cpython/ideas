
# Results vs. 3.11.0

- fork: eduardo-elizondo
- ref: immortal_references
- machine: darwin-arm64
- commit hash: 1dfe27a
- commit date: 2023-01-08
- overall geometric mean: 1.02x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 178 ms: 1.02x faster                                                              |
| chameleon      | 4.61 ms                                                             | 4.51 ms: 1.02x faster                                                             |
| docutils       | 1.46 sec                                                            | 1.45 sec: 1.01x faster                                                            |
| html5lib       | 34.7 ms                                                             | 33.6 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                               | 1.02x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 51.7 ms                                                             | 52.0 ms: 1.01x slower                                                             |
| nbody          | 65.2 ms                                                             | 66.3 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                               | 1.01x slower                                                                      |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 69.8 ms: 1.09x faster                                                             |
| regex_dna      | 151 ms                                                              | 149 ms: 1.01x faster                                                              |
| regex_v8       | 16.5 ms                                                             | 16.1 ms: 1.02x faster                                                             |
| Geometric mean | (ref)                                                               | 1.03x faster                                                                      |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 5.95 ms: 1.29x faster                                                             |
| json_loads           | 16.1 us                                                             | 16.3 us: 1.01x slower                                                             |
| pickle               | 7.21 us                                                             | 7.69 us: 1.07x slower                                                             |
| pickle_dict          | 17.9 us                                                             | 18.1 us: 1.01x slower                                                             |
| pickle_pure_python   | 200 us                                                              | 187 us: 1.07x faster                                                              |
| unpickle             | 9.68 us                                                             | 10.2 us: 1.05x slower                                                             |
| unpickle_list        | 2.64 us                                                             | 2.66 us: 1.01x slower                                                             |
| unpickle_pure_python | 159 us                                                              | 143 us: 1.12x faster                                                              |
| xml_etree_parse      | 99.6 ms                                                             | 94.7 ms: 1.05x faster                                                             |
| xml_etree_iterparse  | 65.6 ms                                                             | 66.3 ms: 1.01x slower                                                             |
| xml_etree_generate   | 48.4 ms                                                             | 49.3 ms: 1.02x slower                                                             |
| xml_etree_process    | 35.1 ms                                                             | 35.0 ms: 1.00x faster                                                             |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                                      |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.33 ms: 1.02x slower                                                             |
| python_startup_no_site | 7.24 ms                                                             | 7.31 ms: 1.01x slower                                                             |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 20.9 ms: 1.01x faster                                                             |
| genshi_text     | 15.3 ms                                                             | 14.4 ms: 1.07x faster                                                             |
| genshi_xml      | 30.5 ms                                                             | 28.5 ms: 1.07x faster                                                             |
| mako            | 8.40 ms                                                             | 8.51 ms: 1.01x slower                                                             |
| Geometric mean  | (ref)                                                               | 1.03x faster                                                                      |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 178 ms: 1.02x faster                                                              |
| async_generators        | 195 ms                                                              | 197 ms: 1.01x slower                                                              |
| async_tree_none         | 281 ms                                                              | 276 ms: 1.02x faster                                                              |
| async_tree_io           | 696 ms                                                              | 720 ms: 1.03x slower                                                              |
| chameleon               | 4.61 ms                                                             | 4.51 ms: 1.02x faster                                                             |
| chaos                   | 49.3 ms                                                             | 46.1 ms: 1.07x faster                                                             |
| bench_mp_pool           | 41.4 ms                                                             | 42.9 ms: 1.04x slower                                                             |
| bench_thread_pool       | 457 us                                                              | 443 us: 1.03x faster                                                              |
| coroutines              | 17.8 ms                                                             | 16.8 ms: 1.06x faster                                                             |
| coverage                | 58.4 ms                                                             | 56.2 ms: 1.04x faster                                                             |
| crypto_pyaes            | 51.7 ms                                                             | 52.0 ms: 1.01x slower                                                             |
| deepcopy                | 222 us                                                              | 215 us: 1.03x faster                                                              |
| deepcopy_reduce         | 1.90 us                                                             | 1.85 us: 1.02x faster                                                             |
| deepcopy_memo           | 26.2 us                                                             | 25.6 us: 1.02x faster                                                             |
| deltablue               | 2.82 ms                                                             | 2.56 ms: 1.10x faster                                                             |
| django_template         | 21.1 ms                                                             | 20.9 ms: 1.01x faster                                                             |
| docutils                | 1.46 sec                                                            | 1.45 sec: 1.01x faster                                                            |
| dulwich_log             | 29.1 ms                                                             | 27.9 ms: 1.04x faster                                                             |
| fannkuch                | 262 ms                                                              | 232 ms: 1.13x faster                                                              |
| float                   | 51.7 ms                                                             | 52.0 ms: 1.01x slower                                                             |
| generators              | 28.4 ms                                                             | 33.7 ms: 1.19x slower                                                             |
| genshi_text             | 15.3 ms                                                             | 14.4 ms: 1.07x faster                                                             |
| genshi_xml              | 30.5 ms                                                             | 28.5 ms: 1.07x faster                                                             |
| go                      | 109 ms                                                              | 103 ms: 1.06x faster                                                              |
| hexiom                  | 4.73 ms                                                             | 4.44 ms: 1.07x faster                                                             |
| html5lib                | 34.7 ms                                                             | 33.6 ms: 1.03x faster                                                             |
| json_dumps              | 7.67 ms                                                             | 5.95 ms: 1.29x faster                                                             |
| json_loads              | 16.1 us                                                             | 16.3 us: 1.01x slower                                                             |
| logging_format          | 3.73 us                                                             | 3.59 us: 1.04x faster                                                             |
| logging_silent          | 67.4 ns                                                             | 63.7 ns: 1.06x faster                                                             |
| logging_simple          | 3.47 us                                                             | 3.30 us: 1.05x faster                                                             |
| mako                    | 8.40 ms                                                             | 8.51 ms: 1.01x slower                                                             |
| mdp                     | 1.54 sec                                                            | 1.50 sec: 1.03x faster                                                            |
| meteor_contest          | 73.9 ms                                                             | 74.3 ms: 1.01x slower                                                             |
| mypy                    | 421 ms                                                              | 415 ms: 1.01x faster                                                              |
| nbody                   | 65.2 ms                                                             | 66.3 ms: 1.02x slower                                                             |
| nqueens                 | 59.5 ms                                                             | 55.9 ms: 1.06x faster                                                             |
| pathlib                 | 20.6 ms                                                             | 20.8 ms: 1.01x slower                                                             |
| pickle                  | 7.21 us                                                             | 7.69 us: 1.07x slower                                                             |
| pickle_dict             | 17.9 us                                                             | 18.1 us: 1.01x slower                                                             |
| pickle_pure_python      | 200 us                                                              | 187 us: 1.07x faster                                                              |
| pprint_safe_repr        | 467 ms                                                              | 448 ms: 1.04x faster                                                              |
| pprint_pformat          | 953 ms                                                              | 910 ms: 1.05x faster                                                              |
| pycparser               | 694 ms                                                              | 667 ms: 1.04x faster                                                              |
| pyflate                 | 313 ms                                                              | 319 ms: 1.02x slower                                                              |
| python_startup          | 9.19 ms                                                             | 9.33 ms: 1.02x slower                                                             |
| python_startup_no_site  | 7.24 ms                                                             | 7.31 ms: 1.01x slower                                                             |
| raytrace                | 207 ms                                                              | 222 ms: 1.07x slower                                                              |
| regex_compile           | 76.3 ms                                                             | 69.8 ms: 1.09x faster                                                             |
| regex_dna               | 151 ms                                                              | 149 ms: 1.01x faster                                                              |
| regex_v8                | 16.5 ms                                                             | 16.1 ms: 1.02x faster                                                             |
| richards                | 32.7 ms                                                             | 28.9 ms: 1.13x faster                                                             |
| scimark_fft             | 201 ms                                                              | 199 ms: 1.01x faster                                                              |
| scimark_lu              | 72.2 ms                                                             | 75.7 ms: 1.05x slower                                                             |
| scimark_monte_carlo     | 46.9 ms                                                             | 46.2 ms: 1.02x faster                                                             |
| scimark_sor             | 83.3 ms                                                             | 84.0 ms: 1.01x slower                                                             |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.90 ms: 1.11x faster                                                             |
| spectral_norm           | 72.7 ms                                                             | 73.0 ms: 1.00x slower                                                             |
| sqlglot_parse           | 948 us                                                              | 991 us: 1.05x slower                                                              |
| sqlglot_transpile       | 1.11 ms                                                             | 1.15 ms: 1.04x slower                                                             |
| sqlglot_optimize        | 31.3 ms                                                             | 31.1 ms: 1.01x faster                                                             |
| sqlglot_normalize       | 171 ms                                                              | 170 ms: 1.01x faster                                                              |
| sqlite_synth            | 1.29 us                                                             | 1.40 us: 1.08x slower                                                             |
| sympy_expand            | 242 ms                                                              | 232 ms: 1.04x faster                                                              |
| sympy_integrate         | 11.5 ms                                                             | 11.2 ms: 1.02x faster                                                             |
| sympy_sum               | 85.5 ms                                                             | 83.2 ms: 1.03x faster                                                             |
| sympy_str               | 151 ms                                                              | 145 ms: 1.04x faster                                                              |
| telco                   | 3.39 ms                                                             | 3.45 ms: 1.02x slower                                                             |
| thrift                  | 429 us                                                              | 431 us: 1.00x slower                                                              |
| unpack_sequence         | 33.1 ns                                                             | 28.8 ns: 1.15x faster                                                             |
| unpickle                | 9.68 us                                                             | 10.2 us: 1.05x slower                                                             |
| unpickle_list           | 2.64 us                                                             | 2.66 us: 1.01x slower                                                             |
| unpickle_pure_python    | 159 us                                                              | 143 us: 1.12x faster                                                              |
| xml_etree_parse         | 99.6 ms                                                             | 94.7 ms: 1.05x faster                                                             |
| xml_etree_iterparse     | 65.6 ms                                                             | 66.3 ms: 1.01x slower                                                             |
| xml_etree_generate      | 48.4 ms                                                             | 49.3 ms: 1.02x slower                                                             |
| xml_etree_process       | 35.1 ms                                                             | 35.0 ms: 1.00x faster                                                             |
| Geometric mean          | (ref)                                                               | 1.02x faster                                                                      |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_memoization, json, pickle_list, pidigits, regex_effbot
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (4) of public/results/bm-20230108-3.12.0a3+-1dfe27a/bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
