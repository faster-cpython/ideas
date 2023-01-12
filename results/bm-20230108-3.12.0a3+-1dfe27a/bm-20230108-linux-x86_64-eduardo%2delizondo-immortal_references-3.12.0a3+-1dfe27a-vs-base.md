
# Results vs. base

- fork: eduardo-elizondo
- ref: immortal_references
- machine: linux-x86_64
- commit hash: 1dfe27a
- commit date: 2023-01-08
- overall geometric mean: 1.06x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 274 ms: 1.08x slower                                                              |
| chameleon      | 6.36 ms                                                                | 6.83 ms: 1.07x slower                                                             |
| docutils       | 2.50 sec                                                               | 2.69 sec: 1.08x slower                                                            |
| html5lib       | 59.6 ms                                                                | 64.0 ms: 1.07x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 71.9 ms                                                                | 79.7 ms: 1.11x slower                                                             |
| nbody          | 94.5 ms                                                                | 96.7 ms: 1.02x slower                                                             |
| pidigits       | 190 ms                                                                 | 190 ms: 1.00x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                                 | 144 ms: 1.12x slower                                                              |
| regex_dna      | 207 ms                                                                 | 203 ms: 1.02x faster                                                              |
| regex_effbot   | 3.42 ms                                                                | 3.39 ms: 1.01x faster                                                             |
| regex_v8       | 20.7 ms                                                                | 21.1 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 9.56 ms                                                                | 9.78 ms: 1.02x slower                                                             |
| json_loads           | 24.2 us                                                                | 26.6 us: 1.10x slower                                                             |
| pickle               | 10.2 us                                                                | 10.5 us: 1.03x slower                                                             |
| pickle_dict          | 31.6 us                                                                | 30.5 us: 1.04x faster                                                             |
| pickle_list          | 4.12 us                                                                | 4.35 us: 1.05x slower                                                             |
| pickle_pure_python   | 285 us                                                                 | 309 us: 1.08x slower                                                              |
| unpickle             | 13.3 us                                                                | 13.7 us: 1.03x slower                                                             |
| unpickle_list        | 5.13 us                                                                | 4.79 us: 1.07x faster                                                             |
| unpickle_pure_python | 197 us                                                                 | 217 us: 1.10x slower                                                              |
| xml_etree_parse      | 148 ms                                                                 | 151 ms: 1.02x slower                                                              |
| xml_etree_iterparse  | 102 ms                                                                 | 106 ms: 1.03x slower                                                              |
| xml_etree_generate   | 76.9 ms                                                                | 79.5 ms: 1.03x slower                                                             |
| xml_etree_process    | 53.7 ms                                                                | 56.7 ms: 1.06x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.04x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 8.52 ms                                                                | 8.77 ms: 1.03x slower                                                             |
| python_startup_no_site | 6.07 ms                                                                | 6.21 ms: 1.02x slower                                                             |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| django_template | 32.9 ms                                                                | 34.8 ms: 1.06x slower                                                             |
| genshi_text     | 20.5 ms                                                                | 22.2 ms: 1.08x slower                                                             |
| genshi_xml      | 47.3 ms                                                                | 51.0 ms: 1.08x slower                                                             |
| mako            | 9.65 ms                                                                | 10.5 ms: 1.09x slower                                                             |
| Geometric mean  | (ref)                                                                  | 1.08x slower                                                                      |

All benchmarks:
===============

| Benchmark               | bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a3+-1dfe27a |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3                    | 253 ms                                                                 | 274 ms: 1.08x slower                                                              |
| async_generators        | 359 ms                                                                 | 375 ms: 1.04x slower                                                              |
| async_tree_none         | 523 ms                                                                 | 536 ms: 1.03x slower                                                              |
| async_tree_cpu_io_mixed | 757 ms                                                                 | 765 ms: 1.01x slower                                                              |
| async_tree_io           | 1.32 sec                                                               | 1.34 sec: 1.01x slower                                                            |
| async_tree_memoization  | 645 ms                                                                 | 688 ms: 1.07x slower                                                              |
| asyncio_tcp             | 506 ms                                                                 | 514 ms: 1.02x slower                                                              |
| chameleon               | 6.36 ms                                                                | 6.83 ms: 1.07x slower                                                             |
| chaos                   | 67.6 ms                                                                | 69.2 ms: 1.02x slower                                                             |
| bench_thread_pool       | 779 us                                                                 | 834 us: 1.07x slower                                                              |
| coroutines              | 24.5 ms                                                                | 26.6 ms: 1.08x slower                                                             |
| coverage                | 95.1 ms                                                                | 102 ms: 1.07x slower                                                              |
| crypto_pyaes            | 76.3 ms                                                                | 79.0 ms: 1.04x slower                                                             |
| dask                    | 499 ms                                                                 | 545 ms: 1.09x slower                                                              |
| deepcopy                | 334 us                                                                 | 366 us: 1.10x slower                                                              |
| deepcopy_reduce         | 2.97 us                                                                | 3.21 us: 1.08x slower                                                             |
| deepcopy_memo           | 34.0 us                                                                | 38.0 us: 1.12x slower                                                             |
| deltablue               | 3.24 ms                                                                | 3.68 ms: 1.14x slower                                                             |
| django_template         | 32.9 ms                                                                | 34.8 ms: 1.06x slower                                                             |
| djangocms               | 32.4 us                                                                | 33.6 us: 1.04x slower                                                             |
| docutils                | 2.50 sec                                                               | 2.69 sec: 1.08x slower                                                            |
| dulwich_log             | 62.2 ms                                                                | 68.7 ms: 1.10x slower                                                             |
| fannkuch                | 370 ms                                                                 | 387 ms: 1.05x slower                                                              |
| float                   | 71.9 ms                                                                | 79.7 ms: 1.11x slower                                                             |
| create_gc_cycles        | 1.43 ms                                                                | 1.46 ms: 1.02x slower                                                             |
| gc_traversal            | 3.63 ms                                                                | 3.90 ms: 1.08x slower                                                             |
| generators              | 73.6 ms                                                                | 80.5 ms: 1.09x slower                                                             |
| genshi_text             | 20.5 ms                                                                | 22.2 ms: 1.08x slower                                                             |
| genshi_xml              | 47.3 ms                                                                | 51.0 ms: 1.08x slower                                                             |
| go                      | 134 ms                                                                 | 134 ms: 1.00x slower                                                              |
| hexiom                  | 6.11 ms                                                                | 6.38 ms: 1.05x slower                                                             |
| html5lib                | 59.6 ms                                                                | 64.0 ms: 1.07x slower                                                             |
| json                    | 4.68 ms                                                                | 5.00 ms: 1.07x slower                                                             |
| json_dumps              | 9.56 ms                                                                | 9.78 ms: 1.02x slower                                                             |
| json_loads              | 24.2 us                                                                | 26.6 us: 1.10x slower                                                             |
| logging_format          | 6.37 us                                                                | 6.96 us: 1.09x slower                                                             |
| logging_silent          | 92.3 ns                                                                | 101 ns: 1.09x slower                                                              |
| logging_simple          | 5.76 us                                                                | 6.31 us: 1.09x slower                                                             |
| mako                    | 9.65 ms                                                                | 10.5 ms: 1.09x slower                                                             |
| mdp                     | 2.71 sec                                                               | 2.61 sec: 1.04x faster                                                            |
| meteor_contest          | 104 ms                                                                 | 116 ms: 1.11x slower                                                              |
| nbody                   | 94.5 ms                                                                | 96.7 ms: 1.02x slower                                                             |
| pathlib                 | 17.9 ms                                                                | 18.4 ms: 1.03x slower                                                             |
| pickle                  | 10.2 us                                                                | 10.5 us: 1.03x slower                                                             |
| pickle_dict             | 31.6 us                                                                | 30.5 us: 1.04x faster                                                             |
| pickle_list             | 4.12 us                                                                | 4.35 us: 1.05x slower                                                             |
| pickle_pure_python      | 285 us                                                                 | 309 us: 1.08x slower                                                              |
| pidigits                | 190 ms                                                                 | 190 ms: 1.00x slower                                                              |
| pprint_safe_repr        | 676 ms                                                                 | 729 ms: 1.08x slower                                                              |
| pprint_pformat          | 1.39 sec                                                               | 1.49 sec: 1.07x slower                                                            |
| pycparser               | 1.10 sec                                                               | 1.15 sec: 1.05x slower                                                            |
| pyflate                 | 407 ms                                                                 | 429 ms: 1.05x slower                                                              |
| python_startup          | 8.52 ms                                                                | 8.77 ms: 1.03x slower                                                             |
| python_startup_no_site  | 6.07 ms                                                                | 6.21 ms: 1.02x slower                                                             |
| raytrace                | 283 ms                                                                 | 309 ms: 1.09x slower                                                              |
| regex_compile           | 129 ms                                                                 | 144 ms: 1.12x slower                                                              |
| regex_dna               | 207 ms                                                                 | 203 ms: 1.02x faster                                                              |
| regex_effbot            | 3.42 ms                                                                | 3.39 ms: 1.01x faster                                                             |
| regex_v8                | 20.7 ms                                                                | 21.1 ms: 1.02x slower                                                             |
| richards                | 41.6 ms                                                                | 44.9 ms: 1.08x slower                                                             |
| scimark_fft             | 314 ms                                                                 | 359 ms: 1.14x slower                                                              |
| scimark_lu              | 111 ms                                                                 | 115 ms: 1.04x slower                                                              |
| scimark_monte_carlo     | 64.4 ms                                                                | 69.6 ms: 1.08x slower                                                             |
| scimark_sor             | 106 ms                                                                 | 121 ms: 1.13x slower                                                              |
| scimark_sparse_mat_mult | 4.08 ms                                                                | 4.34 ms: 1.07x slower                                                             |
| spectral_norm           | 95.4 ms                                                                | 106 ms: 1.11x slower                                                              |
| sqlglot_parse           | 1.40 ms                                                                | 1.55 ms: 1.11x slower                                                             |
| sqlglot_transpile       | 1.69 ms                                                                | 1.87 ms: 1.10x slower                                                             |
| sqlglot_optimize        | 51.3 ms                                                                | 55.2 ms: 1.08x slower                                                             |
| sqlglot_normalize       | 105 ms                                                                 | 114 ms: 1.09x slower                                                              |
| sqlite_synth            | 2.57 us                                                                | 2.65 us: 1.03x slower                                                             |
| sympy_expand            | 460 ms                                                                 | 501 ms: 1.09x slower                                                              |
| sympy_integrate         | 20.4 ms                                                                | 22.0 ms: 1.08x slower                                                             |
| sympy_sum               | 164 ms                                                                 | 182 ms: 1.11x slower                                                              |
| sympy_str               | 283 ms                                                                 | 311 ms: 1.10x slower                                                              |
| telco                   | 6.41 ms                                                                | 6.64 ms: 1.04x slower                                                             |
| thrift                  | 753 us                                                                 | 775 us: 1.03x slower                                                              |
| unpack_sequence         | 43.2 ns                                                                | 51.6 ns: 1.20x slower                                                             |
| unpickle                | 13.3 us                                                                | 13.7 us: 1.03x slower                                                             |
| unpickle_list           | 5.13 us                                                                | 4.79 us: 1.07x faster                                                             |
| unpickle_pure_python    | 197 us                                                                 | 217 us: 1.10x slower                                                              |
| xml_etree_parse         | 148 ms                                                                 | 151 ms: 1.02x slower                                                              |
| xml_etree_iterparse     | 102 ms                                                                 | 106 ms: 1.03x slower                                                              |
| xml_etree_generate      | 76.9 ms                                                                | 79.5 ms: 1.03x slower                                                             |
| xml_etree_process       | 53.7 ms                                                                | 56.7 ms: 1.06x slower                                                             |
| Geometric mean          | (ref)                                                                  | 1.06x slower                                                                      |

Benchmark hidden because not significant (3): bench_mp_pool, mypy, nqueens
