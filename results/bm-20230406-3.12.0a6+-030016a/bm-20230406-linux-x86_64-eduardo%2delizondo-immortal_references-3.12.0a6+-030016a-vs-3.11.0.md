
# Results vs. 3.11.0

- fork: eduardo-elizondo
- ref: immortal_references
- machine: linux-x86_64
- commit hash: 030016a
- commit date: 2023-04-06
- overall geometric mean: 1.03x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 271 ms: 1.06x slower                                                              |
| chameleon      | 6.52 ms                                                             | 6.94 ms: 1.07x slower                                                             |
| docutils       | 2.59 sec                                                            | 2.80 sec: 1.08x slower                                                            |
| html5lib       | 64.0 ms                                                             | 66.6 ms: 1.04x slower                                                             |
| tornado_http   | 96.7 ms                                                             | 104 ms: 1.07x slower                                                              |
| Geometric mean | (ref)                                                               | 1.06x slower                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| nbody          | 96.7 ms                                                             | 91.1 ms: 1.06x faster                                                             |
| pidigits       | 197 ms                                                              | 197 ms: 1.00x slower                                                              |
| float          | 76.0 ms                                                             | 81.0 ms: 1.07x slower                                                             |
| Geometric mean | (ref)                                                               | 1.00x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                             | 21.9 ms: 1.00x faster                                                             |
| regex_dna      | 196 ms                                                              | 203 ms: 1.03x slower                                                              |
| regex_compile  | 137 ms                                                              | 148 ms: 1.09x slower                                                              |
| regex_effbot   | 3.32 ms                                                             | 3.61 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.96 ms: 1.26x faster                                                             |
| xml_etree_parse      | 162 ms                                                              | 151 ms: 1.07x faster                                                              |
| xml_etree_iterparse  | 108 ms                                                              | 102 ms: 1.05x faster                                                              |
| unpickle_pure_python | 228 us                                                              | 219 us: 1.04x faster                                                              |
| json_loads           | 26.2 us                                                             | 25.8 us: 1.02x faster                                                             |
| unpickle             | 13.2 us                                                             | 13.5 us: 1.02x slower                                                             |
| pickle_pure_python   | 307 us                                                              | 316 us: 1.03x slower                                                              |
| unpickle_list        | 4.96 us                                                             | 5.14 us: 1.04x slower                                                             |
| xml_etree_process    | 54.1 ms                                                             | 59.0 ms: 1.09x slower                                                             |
| pickle               | 9.79 us                                                             | 10.7 us: 1.09x slower                                                             |
| xml_etree_generate   | 76.5 ms                                                             | 84.1 ms: 1.10x slower                                                             |
| pickle_list          | 4.03 us                                                             | 4.45 us: 1.10x slower                                                             |
| Geometric mean       | (ref)                                                               | 1.00x slower                                                                      |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 9.02 ms: 1.06x slower                                                             |
| python_startup_no_site | 5.98 ms                                                             | 6.59 ms: 1.10x slower                                                             |
| Geometric mean         | (ref)                                                               | 1.08x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 50.5 ms: 1.02x faster                                                             |
| genshi_text     | 21.8 ms                                                             | 22.9 ms: 1.05x slower                                                             |
| django_template | 32.9 ms                                                             | 35.6 ms: 1.08x slower                                                             |
| mako            | 9.82 ms                                                             | 11.0 ms: 1.12x slower                                                             |
| Geometric mean  | (ref)                                                               | 1.05x slower                                                                      |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| generators              | 73.4 ms                                                             | 31.8 ms: 2.31x faster                                                             |
| asyncio_tcp             | 888 ms                                                              | 517 ms: 1.72x faster                                                              |
| json_dumps              | 12.5 ms                                                             | 9.96 ms: 1.26x faster                                                             |
| coroutines              | 26.3 ms                                                             | 22.8 ms: 1.15x faster                                                             |
| mypy2                   | 422 ms                                                              | 366 ms: 1.15x faster                                                              |
| xml_etree_parse         | 162 ms                                                              | 151 ms: 1.07x faster                                                              |
| nbody                   | 96.7 ms                                                             | 91.1 ms: 1.06x faster                                                             |
| xml_etree_iterparse     | 108 ms                                                              | 102 ms: 1.05x faster                                                              |
| unpickle_pure_python    | 228 us                                                              | 219 us: 1.04x faster                                                              |
| coverage                | 101 ms                                                              | 98.5 ms: 1.03x faster                                                             |
| nqueens                 | 84.0 ms                                                             | 81.9 ms: 1.03x faster                                                             |
| genshi_xml              | 51.8 ms                                                             | 50.5 ms: 1.02x faster                                                             |
| hexiom                  | 6.48 ms                                                             | 6.33 ms: 1.02x faster                                                             |
| deltablue               | 3.66 ms                                                             | 3.59 ms: 1.02x faster                                                             |
| json_loads              | 26.2 us                                                             | 25.8 us: 1.02x faster                                                             |
| regex_v8                | 22.0 ms                                                             | 21.9 ms: 1.00x faster                                                             |
| pidigits                | 197 ms                                                              | 197 ms: 1.00x slower                                                              |
| gc_traversal            | 3.63 ms                                                             | 3.66 ms: 1.01x slower                                                             |
| go                      | 138 ms                                                              | 140 ms: 1.01x slower                                                              |
| pycparser               | 1.14 sec                                                            | 1.16 sec: 1.02x slower                                                            |
| pathlib                 | 18.2 ms                                                             | 18.5 ms: 1.02x slower                                                             |
| mdp                     | 2.64 sec                                                            | 2.68 sec: 1.02x slower                                                            |
| unpickle                | 13.2 us                                                             | 13.5 us: 1.02x slower                                                             |
| fannkuch                | 384 ms                                                              | 391 ms: 1.02x slower                                                              |
| raytrace                | 292 ms                                                              | 298 ms: 1.02x slower                                                              |
| telco                   | 6.59 ms                                                             | 6.73 ms: 1.02x slower                                                             |
| bench_thread_pool       | 820 us                                                              | 838 us: 1.02x slower                                                              |
| async_tree_io           | 1.28 sec                                                            | 1.31 sec: 1.02x slower                                                            |
| async_tree_none         | 525 ms                                                              | 539 ms: 1.03x slower                                                              |
| pickle_pure_python      | 307 us                                                              | 316 us: 1.03x slower                                                              |
| pprint_pformat          | 1.45 sec                                                            | 1.50 sec: 1.03x slower                                                            |
| regex_dna               | 196 ms                                                              | 203 ms: 1.03x slower                                                              |
| async_tree_cpu_io_mixed | 736 ms                                                              | 761 ms: 1.03x slower                                                              |
| unpickle_list           | 4.96 us                                                             | 5.14 us: 1.04x slower                                                             |
| chaos                   | 68.0 ms                                                             | 70.5 ms: 1.04x slower                                                             |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.64 ms: 1.04x slower                                                             |
| logging_silent          | 98.7 ns                                                             | 103 ns: 1.04x slower                                                              |
| html5lib                | 64.0 ms                                                             | 66.6 ms: 1.04x slower                                                             |
| sqlglot_optimize        | 53.4 ms                                                             | 55.6 ms: 1.04x slower                                                             |
| logging_simple          | 6.09 us                                                             | 6.35 us: 1.04x slower                                                             |
| thrift                  | 766 us                                                              | 802 us: 1.05x slower                                                              |
| scimark_lu              | 108 ms                                                              | 114 ms: 1.05x slower                                                              |
| genshi_text             | 21.8 ms                                                             | 22.9 ms: 1.05x slower                                                             |
| pprint_safe_repr        | 701 ms                                                              | 737 ms: 1.05x slower                                                              |
| sympy_integrate         | 21.0 ms                                                             | 22.2 ms: 1.05x slower                                                             |
| logging_format          | 6.64 us                                                             | 7.00 us: 1.05x slower                                                             |
| 2to3                    | 257 ms                                                              | 271 ms: 1.06x slower                                                              |
| djangocms               | 32.3 us                                                             | 34.1 us: 1.06x slower                                                             |
| sqlglot_normalize       | 108 ms                                                              | 115 ms: 1.06x slower                                                              |
| deepcopy_memo           | 36.4 us                                                             | 38.5 us: 1.06x slower                                                             |
| json                    | 4.86 ms                                                             | 5.15 ms: 1.06x slower                                                             |
| scimark_monte_carlo     | 67.8 ms                                                             | 71.9 ms: 1.06x slower                                                             |
| python_startup          | 8.49 ms                                                             | 9.02 ms: 1.06x slower                                                             |
| sympy_expand            | 477 ms                                                              | 506 ms: 1.06x slower                                                              |
| chameleon               | 6.52 ms                                                             | 6.94 ms: 1.07x slower                                                             |
| float                   | 76.0 ms                                                             | 81.0 ms: 1.07x slower                                                             |
| meteor_contest          | 106 ms                                                              | 113 ms: 1.07x slower                                                              |
| tornado_http            | 96.7 ms                                                             | 104 ms: 1.07x slower                                                              |
| unpack_sequence         | 49.5 ns                                                             | 53.0 ns: 1.07x slower                                                             |
| spectral_norm           | 99.5 ms                                                             | 107 ms: 1.07x slower                                                              |
| sqlite_synth            | 2.51 us                                                             | 2.70 us: 1.07x slower                                                             |
| scimark_fft             | 328 ms                                                              | 352 ms: 1.07x slower                                                              |
| sqlalchemy_declarative  | 138 ms                                                              | 149 ms: 1.07x slower                                                              |
| docutils                | 2.59 sec                                                            | 2.80 sec: 1.08x slower                                                            |
| django_template         | 32.9 ms                                                             | 35.6 ms: 1.08x slower                                                             |
| crypto_pyaes            | 73.8 ms                                                             | 80.0 ms: 1.08x slower                                                             |
| deepcopy                | 339 us                                                              | 367 us: 1.08x slower                                                              |
| regex_compile           | 137 ms                                                              | 148 ms: 1.09x slower                                                              |
| regex_effbot            | 3.32 ms                                                             | 3.61 ms: 1.09x slower                                                             |
| xml_etree_process       | 54.1 ms                                                             | 59.0 ms: 1.09x slower                                                             |
| pickle                  | 9.79 us                                                             | 10.7 us: 1.09x slower                                                             |
| sympy_str               | 291 ms                                                              | 319 ms: 1.09x slower                                                              |
| async_tree_memoization  | 621 ms                                                              | 680 ms: 1.09x slower                                                              |
| sympy_sum               | 167 ms                                                              | 183 ms: 1.10x slower                                                              |
| sqlalchemy_imperative   | 18.0 ms                                                             | 19.8 ms: 1.10x slower                                                             |
| dulwich_log             | 63.6 ms                                                             | 69.8 ms: 1.10x slower                                                             |
| xml_etree_generate      | 76.5 ms                                                             | 84.1 ms: 1.10x slower                                                             |
| python_startup_no_site  | 5.98 ms                                                             | 6.59 ms: 1.10x slower                                                             |
| pickle_list             | 4.03 us                                                             | 4.45 us: 1.10x slower                                                             |
| deepcopy_reduce         | 2.96 us                                                             | 3.26 us: 1.10x slower                                                             |
| mako                    | 9.82 ms                                                             | 11.0 ms: 1.12x slower                                                             |
| pyflate                 | 414 ms                                                              | 464 ms: 1.12x slower                                                              |
| comprehensions          | 22.2 us                                                             | 25.1 us: 1.13x slower                                                             |
| sqlglot_transpile       | 1.65 ms                                                             | 1.90 ms: 1.15x slower                                                             |
| sqlglot_parse           | 1.36 ms                                                             | 1.57 ms: 1.15x slower                                                             |
| async_generators        | 361 ms                                                              | 429 ms: 1.19x slower                                                              |
| scimark_sor             | 115 ms                                                              | 137 ms: 1.19x slower                                                              |
| dask                    | 368 ms                                                              | 555 ms: 1.51x slower                                                              |
| Geometric mean          | (ref)                                                               | 1.03x slower                                                                      |

Benchmark hidden because not significant (4): create_gc_cycles, bench_mp_pool, pickle_dict, richards
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint
