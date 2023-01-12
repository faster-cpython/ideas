
# Results vs. 3.11.0

- fork: eduardo-elizondo
- ref: immortal_references
- machine: linux-x86_64
- commit hash: 1dfe27a
- commit date: 2023-01-08
- overall geometric mean: 1.03x slower \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 274 ms: 1.06x slower                                                              |
| chameleon      | 6.41 ms                                                | 6.83 ms: 1.07x slower                                                             |
| docutils       | 2.60 sec                                               | 2.69 sec: 1.04x slower                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                      |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 79.7 ms: 1.04x slower                                                             |
| nbody          | 95.0 ms                                                | 96.7 ms: 1.02x slower                                                             |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                                              |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 144 ms: 1.06x slower                                                              |
| regex_dna      | 203 ms                                                 | 203 ms: 1.00x faster                                                              |
| regex_effbot   | 3.36 ms                                                | 3.39 ms: 1.01x slower                                                             |
| regex_v8       | 22.3 ms                                                | 21.1 ms: 1.06x faster                                                             |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.78 ms: 1.29x faster                                                             |
| json_loads           | 26.2 us                                                | 26.6 us: 1.02x slower                                                             |
| pickle               | 9.79 us                                                | 10.5 us: 1.07x slower                                                             |
| pickle_dict          | 31.4 us                                                | 30.5 us: 1.03x faster                                                             |
| pickle_list          | 4.17 us                                                | 4.35 us: 1.04x slower                                                             |
| pickle_pure_python   | 304 us                                                 | 309 us: 1.02x slower                                                              |
| unpickle             | 13.3 us                                                | 13.7 us: 1.03x slower                                                             |
| unpickle_list        | 4.95 us                                                | 4.79 us: 1.03x faster                                                             |
| unpickle_pure_python | 225 us                                                 | 217 us: 1.04x faster                                                              |
| xml_etree_parse      | 158 ms                                                 | 151 ms: 1.05x faster                                                              |
| xml_etree_iterparse  | 103 ms                                                 | 106 ms: 1.03x slower                                                              |
| xml_etree_generate   | 76.2 ms                                                | 79.5 ms: 1.04x slower                                                             |
| xml_etree_process    | 53.8 ms                                                | 56.7 ms: 1.05x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.77 ms: 1.05x slower                                                             |
| python_startup_no_site | 5.96 ms                                                | 6.21 ms: 1.04x slower                                                             |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| django_template | 32.5 ms                                                | 34.8 ms: 1.07x slower                                                             |
| genshi_xml      | 52.1 ms                                                | 51.0 ms: 1.02x faster                                                             |
| mako            | 9.85 ms                                                | 10.5 ms: 1.06x slower                                                             |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 274 ms: 1.06x slower                                                              |
| async_generators        | 359 ms                                                 | 375 ms: 1.04x slower                                                              |
| async_tree_none         | 529 ms                                                 | 536 ms: 1.01x slower                                                              |
| async_tree_cpu_io_mixed | 752 ms                                                 | 765 ms: 1.02x slower                                                              |
| async_tree_io           | 1.31 sec                                               | 1.34 sec: 1.02x slower                                                            |
| async_tree_memoization  | 625 ms                                                 | 688 ms: 1.10x slower                                                              |
| chameleon               | 6.41 ms                                                | 6.83 ms: 1.07x slower                                                             |
| chaos                   | 68.6 ms                                                | 69.2 ms: 1.01x slower                                                             |
| bench_thread_pool       | 810 us                                                 | 834 us: 1.03x slower                                                              |
| coroutines              | 26.1 ms                                                | 26.6 ms: 1.02x slower                                                             |
| coverage                | 101 ms                                                 | 102 ms: 1.02x slower                                                              |
| crypto_pyaes            | 73.9 ms                                                | 79.0 ms: 1.07x slower                                                             |
| deepcopy                | 344 us                                                 | 366 us: 1.06x slower                                                              |
| deepcopy_reduce         | 2.97 us                                                | 3.21 us: 1.08x slower                                                             |
| deepcopy_memo           | 36.4 us                                                | 38.0 us: 1.04x slower                                                             |
| deltablue               | 3.64 ms                                                | 3.68 ms: 1.01x slower                                                             |
| django_template         | 32.5 ms                                                | 34.8 ms: 1.07x slower                                                             |
| docutils                | 2.60 sec                                               | 2.69 sec: 1.04x slower                                                            |
| dulwich_log             | 63.9 ms                                                | 68.7 ms: 1.07x slower                                                             |
| float                   | 76.3 ms                                                | 79.7 ms: 1.04x slower                                                             |
| generators              | 72.2 ms                                                | 80.5 ms: 1.12x slower                                                             |
| genshi_xml              | 52.1 ms                                                | 51.0 ms: 1.02x faster                                                             |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                                              |
| hexiom                  | 6.35 ms                                                | 6.38 ms: 1.01x slower                                                             |
| json                    | 4.95 ms                                                | 5.00 ms: 1.01x slower                                                             |
| json_dumps              | 12.7 ms                                                | 9.78 ms: 1.29x faster                                                             |
| json_loads              | 26.2 us                                                | 26.6 us: 1.02x slower                                                             |
| logging_format          | 6.62 us                                                | 6.96 us: 1.05x slower                                                             |
| logging_silent          | 98.5 ns                                                | 101 ns: 1.02x slower                                                              |
| logging_simple          | 6.06 us                                                | 6.31 us: 1.04x slower                                                             |
| mako                    | 9.85 ms                                                | 10.5 ms: 1.06x slower                                                             |
| mdp                     | 2.62 sec                                               | 2.61 sec: 1.00x faster                                                            |
| meteor_contest          | 105 ms                                                 | 116 ms: 1.11x slower                                                              |
| mypy                    | 669 ms                                                 | 876 ms: 1.31x slower                                                              |
| nbody                   | 95.0 ms                                                | 96.7 ms: 1.02x slower                                                             |
| nqueens                 | 85.0 ms                                                | 80.1 ms: 1.06x faster                                                             |
| pathlib                 | 18.2 ms                                                | 18.4 ms: 1.01x slower                                                             |
| pickle                  | 9.79 us                                                | 10.5 us: 1.07x slower                                                             |
| pickle_dict             | 31.4 us                                                | 30.5 us: 1.03x faster                                                             |
| pickle_list             | 4.17 us                                                | 4.35 us: 1.04x slower                                                             |
| pickle_pure_python      | 304 us                                                 | 309 us: 1.02x slower                                                              |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                                              |
| pprint_safe_repr        | 691 ms                                                 | 729 ms: 1.06x slower                                                              |
| pprint_pformat          | 1.44 sec                                               | 1.49 sec: 1.03x slower                                                            |
| pycparser               | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                            |
| pyflate                 | 417 ms                                                 | 429 ms: 1.03x slower                                                              |
| python_startup          | 8.36 ms                                                | 8.77 ms: 1.05x slower                                                             |
| python_startup_no_site  | 5.96 ms                                                | 6.21 ms: 1.04x slower                                                             |
| raytrace                | 290 ms                                                 | 309 ms: 1.06x slower                                                              |
| regex_compile           | 136 ms                                                 | 144 ms: 1.06x slower                                                              |
| regex_dna               | 203 ms                                                 | 203 ms: 1.00x faster                                                              |
| regex_effbot            | 3.36 ms                                                | 3.39 ms: 1.01x slower                                                             |
| regex_v8                | 22.3 ms                                                | 21.1 ms: 1.06x faster                                                             |
| richards                | 46.2 ms                                                | 44.9 ms: 1.03x faster                                                             |
| scimark_fft             | 329 ms                                                 | 359 ms: 1.09x slower                                                              |
| scimark_lu              | 107 ms                                                 | 115 ms: 1.07x slower                                                              |
| scimark_monte_carlo     | 68.3 ms                                                | 69.6 ms: 1.02x slower                                                             |
| scimark_sor             | 115 ms                                                 | 121 ms: 1.05x slower                                                              |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.34 ms: 1.01x faster                                                             |
| spectral_norm           | 99.9 ms                                                | 106 ms: 1.06x slower                                                              |
| sqlglot_parse           | 1.37 ms                                                | 1.55 ms: 1.13x slower                                                             |
| sqlglot_transpile       | 1.66 ms                                                | 1.87 ms: 1.13x slower                                                             |
| sqlglot_optimize        | 53.0 ms                                                | 55.2 ms: 1.04x slower                                                             |
| sqlglot_normalize       | 108 ms                                                 | 114 ms: 1.05x slower                                                              |
| sqlite_synth            | 2.49 us                                                | 2.65 us: 1.06x slower                                                             |
| sympy_expand            | 472 ms                                                 | 501 ms: 1.06x slower                                                              |
| sympy_integrate         | 20.9 ms                                                | 22.0 ms: 1.06x slower                                                             |
| sympy_sum               | 166 ms                                                 | 182 ms: 1.09x slower                                                              |
| sympy_str               | 287 ms                                                 | 311 ms: 1.08x slower                                                              |
| thrift                  | 752 us                                                 | 775 us: 1.03x slower                                                              |
| unpack_sequence         | 43.4 ns                                                | 51.6 ns: 1.19x slower                                                             |
| unpickle                | 13.3 us                                                | 13.7 us: 1.03x slower                                                             |
| unpickle_list           | 4.95 us                                                | 4.79 us: 1.03x faster                                                             |
| unpickle_pure_python    | 225 us                                                 | 217 us: 1.04x faster                                                              |
| xml_etree_parse         | 158 ms                                                 | 151 ms: 1.05x faster                                                              |
| xml_etree_iterparse     | 103 ms                                                 | 106 ms: 1.03x slower                                                              |
| xml_etree_generate      | 76.2 ms                                                | 79.5 ms: 1.04x slower                                                             |
| xml_etree_process       | 53.8 ms                                                | 56.7 ms: 1.05x slower                                                             |
| Geometric mean          | (ref)                                                  | 1.03x slower                                                                      |

Benchmark hidden because not significant (5): bench_mp_pool, fannkuch, genshi_text, html5lib, telco
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (5) of public/results/bm-20230108-3.12.0a3+-1dfe27a/bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
