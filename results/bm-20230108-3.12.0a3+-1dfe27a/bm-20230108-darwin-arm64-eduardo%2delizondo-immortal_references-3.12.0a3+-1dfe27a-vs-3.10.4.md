
# Results vs. 3.10.4

- fork: eduardo-elizondo
- ref: immortal_references
- machine: darwin-arm64
- commit hash: 1dfe27a
- commit date: 2023-01-08
- overall geometric mean: 1.24x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 178 ms: 1.25x faster                                                              |
| chameleon      | 5.86 ms                                                | 4.51 ms: 1.30x faster                                                             |
| docutils       | 1.76 sec                                               | 1.45 sec: 1.22x faster                                                            |
| html5lib       | 44.0 ms                                                | 33.6 ms: 1.31x faster                                                             |
| Geometric mean | (ref)                                                  | 1.27x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 52.0 ms: 1.38x faster                                                             |
| nbody          | 94.6 ms                                                | 66.3 ms: 1.43x faster                                                             |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                                              |
| Geometric mean | (ref)                                                  | 1.26x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 69.8 ms: 1.38x faster                                                             |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                              |
| regex_effbot   | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                             |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                                             |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 5.95 ms: 1.40x faster                                                             |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                                             |
| pickle               | 7.50 us                                                | 7.69 us: 1.02x slower                                                             |
| pickle_dict          | 18.0 us                                                | 18.1 us: 1.01x slower                                                             |
| pickle_list          | 2.83 us                                                | 2.86 us: 1.01x slower                                                             |
| pickle_pure_python   | 284 us                                                 | 187 us: 1.52x faster                                                              |
| unpickle             | 10.0 us                                                | 10.2 us: 1.02x slower                                                             |
| unpickle_pure_python | 204 us                                                 | 143 us: 1.43x faster                                                              |
| xml_etree_parse      | 100 ms                                                 | 94.7 ms: 1.06x faster                                                             |
| xml_etree_iterparse  | 69.0 ms                                                | 66.3 ms: 1.04x faster                                                             |
| xml_etree_generate   | 54.5 ms                                                | 49.3 ms: 1.11x faster                                                             |
| xml_etree_process    | 45.1 ms                                                | 35.0 ms: 1.29x faster                                                             |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                                      |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.33 ms: 1.03x faster                                                             |
| python_startup_no_site | 7.00 ms                                                | 7.31 ms: 1.04x slower                                                             |
| Geometric mean         | (ref)                                                  | 1.01x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 20.9 ms: 1.30x faster                                                             |
| genshi_text     | 18.2 ms                                                | 14.4 ms: 1.27x faster                                                             |
| genshi_xml      | 37.7 ms                                                | 28.5 ms: 1.32x faster                                                             |
| mako            | 10.6 ms                                                | 8.51 ms: 1.25x faster                                                             |
| Geometric mean  | (ref)                                                  | 1.28x faster                                                                      |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 178 ms: 1.25x faster                                                              |
| async_generators        | 231 ms                                                 | 197 ms: 1.17x faster                                                              |
| async_tree_none         | 396 ms                                                 | 276 ms: 1.43x faster                                                              |
| async_tree_cpu_io_mixed | 665 ms                                                 | 530 ms: 1.25x faster                                                              |
| async_tree_io           | 1.01 sec                                               | 720 ms: 1.40x faster                                                              |
| async_tree_memoization  | 485 ms                                                 | 317 ms: 1.53x faster                                                              |
| chameleon               | 5.86 ms                                                | 4.51 ms: 1.30x faster                                                             |
| chaos                   | 66.5 ms                                                | 46.1 ms: 1.44x faster                                                             |
| bench_mp_pool           | 40.8 ms                                                | 42.9 ms: 1.05x slower                                                             |
| bench_thread_pool       | 531 us                                                 | 443 us: 1.20x faster                                                              |
| coroutines              | 20.1 ms                                                | 16.8 ms: 1.20x faster                                                             |
| coverage                | 40.8 ms                                                | 56.2 ms: 1.38x slower                                                             |
| crypto_pyaes            | 77.9 ms                                                | 52.0 ms: 1.50x faster                                                             |
| deepcopy                | 278 us                                                 | 215 us: 1.29x faster                                                              |
| deepcopy_reduce         | 2.36 us                                                | 1.85 us: 1.28x faster                                                             |
| deepcopy_memo           | 34.4 us                                                | 25.6 us: 1.34x faster                                                             |
| deltablue               | 5.37 ms                                                | 2.56 ms: 2.10x faster                                                             |
| django_template         | 27.2 ms                                                | 20.9 ms: 1.30x faster                                                             |
| docutils                | 1.76 sec                                               | 1.45 sec: 1.22x faster                                                            |
| dulwich_log             | 36.4 ms                                                | 27.9 ms: 1.30x faster                                                             |
| fannkuch                | 318 ms                                                 | 232 ms: 1.37x faster                                                              |
| float                   | 72.1 ms                                                | 52.0 ms: 1.38x faster                                                             |
| generators              | 32.5 ms                                                | 33.7 ms: 1.04x slower                                                             |
| genshi_text             | 18.2 ms                                                | 14.4 ms: 1.27x faster                                                             |
| genshi_xml              | 37.7 ms                                                | 28.5 ms: 1.32x faster                                                             |
| go                      | 165 ms                                                 | 103 ms: 1.60x faster                                                              |
| hexiom                  | 6.31 ms                                                | 4.44 ms: 1.42x faster                                                             |
| html5lib                | 44.0 ms                                                | 33.6 ms: 1.31x faster                                                             |
| json                    | 3.13 ms                                                | 2.83 ms: 1.10x faster                                                             |
| json_dumps              | 8.34 ms                                                | 5.95 ms: 1.40x faster                                                             |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                                             |
| logging_format          | 4.95 us                                                | 3.59 us: 1.38x faster                                                             |
| logging_silent          | 119 ns                                                 | 63.7 ns: 1.87x faster                                                             |
| logging_simple          | 4.61 us                                                | 3.30 us: 1.39x faster                                                             |
| mako                    | 10.6 ms                                                | 8.51 ms: 1.25x faster                                                             |
| mdp                     | 1.66 sec                                               | 1.50 sec: 1.11x faster                                                            |
| meteor_contest          | 77.7 ms                                                | 74.3 ms: 1.05x faster                                                             |
| mypy                    | 521 ms                                                 | 415 ms: 1.26x faster                                                              |
| nbody                   | 94.6 ms                                                | 66.3 ms: 1.43x faster                                                             |
| nqueens                 | 68.6 ms                                                | 55.9 ms: 1.23x faster                                                             |
| pathlib                 | 22.2 ms                                                | 20.8 ms: 1.07x faster                                                             |
| pickle                  | 7.50 us                                                | 7.69 us: 1.02x slower                                                             |
| pickle_dict             | 18.0 us                                                | 18.1 us: 1.01x slower                                                             |
| pickle_list             | 2.83 us                                                | 2.86 us: 1.01x slower                                                             |
| pickle_pure_python      | 284 us                                                 | 187 us: 1.52x faster                                                              |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                                              |
| pprint_safe_repr        | 608 ms                                                 | 448 ms: 1.35x faster                                                              |
| pprint_pformat          | 1.24 sec                                               | 910 ms: 1.36x faster                                                              |
| pycparser               | 915 ms                                                 | 667 ms: 1.37x faster                                                              |
| pyflate                 | 454 ms                                                 | 319 ms: 1.42x faster                                                              |
| python_startup          | 9.59 ms                                                | 9.33 ms: 1.03x faster                                                             |
| python_startup_no_site  | 7.00 ms                                                | 7.31 ms: 1.04x slower                                                             |
| raytrace                | 329 ms                                                 | 222 ms: 1.48x faster                                                              |
| regex_compile           | 96.2 ms                                                | 69.8 ms: 1.38x faster                                                             |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                              |
| regex_effbot            | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                             |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                                             |
| richards                | 51.4 ms                                                | 28.9 ms: 1.78x faster                                                             |
| scimark_fft             | 231 ms                                                 | 199 ms: 1.16x faster                                                              |
| scimark_lu              | 110 ms                                                 | 75.7 ms: 1.45x faster                                                             |
| scimark_monte_carlo     | 72.3 ms                                                | 46.2 ms: 1.56x faster                                                             |
| scimark_sor             | 126 ms                                                 | 84.0 ms: 1.50x faster                                                             |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.90 ms: 1.20x faster                                                             |
| spectral_norm           | 95.8 ms                                                | 73.0 ms: 1.31x faster                                                             |
| sqlglot_parse           | 1.33 ms                                                | 991 us: 1.34x faster                                                              |
| sqlglot_transpile       | 1.54 ms                                                | 1.15 ms: 1.34x faster                                                             |
| sqlglot_optimize        | 38.1 ms                                                | 31.1 ms: 1.23x faster                                                             |
| sqlglot_normalize       | 198 ms                                                 | 170 ms: 1.17x faster                                                              |
| sqlite_synth            | 1.50 us                                                | 1.40 us: 1.07x faster                                                             |
| sympy_expand            | 275 ms                                                 | 232 ms: 1.19x faster                                                              |
| sympy_integrate         | 13.3 ms                                                | 11.2 ms: 1.18x faster                                                             |
| sympy_sum               | 93.5 ms                                                | 83.2 ms: 1.12x faster                                                             |
| sympy_str               | 169 ms                                                 | 145 ms: 1.17x faster                                                              |
| telco                   | 3.63 ms                                                | 3.45 ms: 1.05x faster                                                             |
| thrift                  | 577 us                                                 | 431 us: 1.34x faster                                                              |
| unpack_sequence         | 38.2 ns                                                | 28.8 ns: 1.33x faster                                                             |
| unpickle                | 10.0 us                                                | 10.2 us: 1.02x slower                                                             |
| unpickle_pure_python    | 204 us                                                 | 143 us: 1.43x faster                                                              |
| xml_etree_parse         | 100 ms                                                 | 94.7 ms: 1.06x faster                                                             |
| xml_etree_iterparse     | 69.0 ms                                                | 66.3 ms: 1.04x faster                                                             |
| xml_etree_generate      | 54.5 ms                                                | 49.3 ms: 1.11x faster                                                             |
| xml_etree_process       | 45.1 ms                                                | 35.0 ms: 1.29x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.24x faster                                                                      |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (4) of public/results/bm-20230108-3.12.0a3+-1dfe27a/bm-20230108-darwin-arm64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a.json: asyncio_tcp, create_gc_cycles, dask, gc_traversal
