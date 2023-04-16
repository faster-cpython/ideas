
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4fe1c4b
- commit date: 2023-04-15
- overall geometric mean: 1.05x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 249 ms: 1.03x faster                                   |
| chameleon      | 6.52 ms                                                             | 6.33 ms: 1.03x faster                                  |
| docutils       | 2.59 sec                                                            | 2.51 sec: 1.03x faster                                 |
| html5lib       | 64.0 ms                                                             | 60.7 ms: 1.05x faster                                  |
| tornado_http   | 96.7 ms                                                             | 92.4 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                               | 1.04x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 96.7 ms                                                             | 85.1 ms: 1.14x faster                                  |
| pidigits       | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| float          | 76.0 ms                                                             | 73.5 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                               | 1.07x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 137 ms                                                              | 132 ms: 1.03x faster                                   |
| regex_v8       | 22.0 ms                                                             | 21.3 ms: 1.03x faster                                  |
| regex_dna      | 196 ms                                                              | 202 ms: 1.03x slower                                   |
| Geometric mean | (ref)                                                               | 1.01x faster                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.46 ms: 1.32x faster                                  |
| unpickle_pure_python | 228 us                                                              | 203 us: 1.12x faster                                   |
| xml_etree_parse      | 162 ms                                                              | 148 ms: 1.09x faster                                   |
| json_loads           | 26.2 us                                                             | 24.1 us: 1.09x faster                                  |
| xml_etree_iterparse  | 108 ms                                                              | 99.3 ms: 1.09x faster                                  |
| pickle_pure_python   | 307 us                                                              | 285 us: 1.08x faster                                   |
| unpickle_list        | 4.96 us                                                             | 4.88 us: 1.02x faster                                  |
| xml_etree_process    | 54.1 ms                                                             | 55.0 ms: 1.02x slower                                  |
| xml_etree_generate   | 76.5 ms                                                             | 79.9 ms: 1.04x slower                                  |
| pickle_dict          | 30.9 us                                                             | 32.9 us: 1.06x slower                                  |
| pickle_list          | 4.03 us                                                             | 4.31 us: 1.07x slower                                  |
| unpickle             | 13.2 us                                                             | 14.6 us: 1.11x slower                                  |
| pickle               | 9.79 us                                                             | 10.9 us: 1.11x slower                                  |
| Geometric mean       | (ref)                                                               | 1.03x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.91 ms: 1.05x slower                                  |
| python_startup_no_site | 5.98 ms                                                             | 6.60 ms: 1.10x slower                                  |
| Geometric mean         | (ref)                                                               | 1.08x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 47.1 ms: 1.10x faster                                  |
| genshi_text     | 21.8 ms                                                             | 21.0 ms: 1.04x faster                                  |
| django_template | 32.9 ms                                                             | 32.4 ms: 1.01x faster                                  |
| mako            | 9.82 ms                                                             | 9.86 ms: 1.00x slower                                  |
| Geometric mean  | (ref)                                                               | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 73.4 ms                                                             | 28.0 ms: 2.62x faster                                  |
| asyncio_tcp             | 888 ms                                                              | 501 ms: 1.77x faster                                   |
| json_dumps              | 12.5 ms                                                             | 9.46 ms: 1.32x faster                                  |
| mypy2                   | 422 ms                                                              | 331 ms: 1.27x faster                                   |
| coroutines              | 26.3 ms                                                             | 21.5 ms: 1.22x faster                                  |
| unpack_sequence         | 49.5 ns                                                             | 42.5 ns: 1.16x faster                                  |
| deltablue               | 3.66 ms                                                             | 3.20 ms: 1.15x faster                                  |
| sqlglot_parse           | 1.36 ms                                                             | 1.19 ms: 1.14x faster                                  |
| nbody                   | 96.7 ms                                                             | 85.1 ms: 1.14x faster                                  |
| unpickle_pure_python    | 228 us                                                              | 203 us: 1.12x faster                                   |
| sqlglot_transpile       | 1.65 ms                                                             | 1.48 ms: 1.12x faster                                  |
| richards                | 45.7 ms                                                             | 40.9 ms: 1.12x faster                                  |
| genshi_xml              | 51.8 ms                                                             | 47.1 ms: 1.10x faster                                  |
| pylint                  | 476 ms                                                              | 435 ms: 1.09x faster                                   |
| xml_etree_parse         | 162 ms                                                              | 148 ms: 1.09x faster                                   |
| hexiom                  | 6.48 ms                                                             | 5.94 ms: 1.09x faster                                  |
| json_loads              | 26.2 us                                                             | 24.1 us: 1.09x faster                                  |
| spectral_norm           | 99.5 ms                                                             | 91.5 ms: 1.09x faster                                  |
| xml_etree_iterparse     | 108 ms                                                              | 99.3 ms: 1.09x faster                                  |
| pickle_pure_python      | 307 us                                                              | 285 us: 1.08x faster                                   |
| pathlib                 | 18.2 ms                                                             | 17.0 ms: 1.07x faster                                  |
| logging_format          | 6.64 us                                                             | 6.22 us: 1.07x faster                                  |
| logging_simple          | 6.09 us                                                             | 5.72 us: 1.06x faster                                  |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.20 ms: 1.06x faster                                  |
| nqueens                 | 84.0 ms                                                             | 79.1 ms: 1.06x faster                                  |
| deepcopy_memo           | 36.4 us                                                             | 34.3 us: 1.06x faster                                  |
| scimark_fft             | 328 ms                                                              | 309 ms: 1.06x faster                                   |
| mdp                     | 2.64 sec                                                            | 2.49 sec: 1.06x faster                                 |
| html5lib                | 64.0 ms                                                             | 60.7 ms: 1.05x faster                                  |
| coverage                | 101 ms                                                              | 96.0 ms: 1.05x faster                                  |
| scimark_sor             | 115 ms                                                              | 109 ms: 1.05x faster                                   |
| aiohttp                 | 1.05 ms                                                             | 1.00 ms: 1.05x faster                                  |
| sympy_expand            | 477 ms                                                              | 454 ms: 1.05x faster                                   |
| raytrace                | 292 ms                                                              | 279 ms: 1.05x faster                                   |
| bench_thread_pool       | 820 us                                                              | 781 us: 1.05x faster                                   |
| pidigits                | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| sympy_str               | 291 ms                                                              | 279 ms: 1.05x faster                                   |
| tornado_http            | 96.7 ms                                                             | 92.4 ms: 1.05x faster                                  |
| gunicorn                | 1.13 ms                                                             | 1.08 ms: 1.04x faster                                  |
| json                    | 4.86 ms                                                             | 4.65 ms: 1.04x faster                                  |
| pprint_pformat          | 1.45 sec                                                            | 1.39 sec: 1.04x faster                                 |
| pycparser               | 1.14 sec                                                            | 1.10 sec: 1.04x faster                                 |
| sqlglot_normalize       | 108 ms                                                              | 104 ms: 1.04x faster                                   |
| go                      | 138 ms                                                              | 133 ms: 1.04x faster                                   |
| genshi_text             | 21.8 ms                                                             | 21.0 ms: 1.04x faster                                  |
| pprint_safe_repr        | 701 ms                                                              | 675 ms: 1.04x faster                                   |
| sqlglot_optimize        | 53.4 ms                                                             | 51.4 ms: 1.04x faster                                  |
| sympy_integrate         | 21.0 ms                                                             | 20.3 ms: 1.04x faster                                  |
| chaos                   | 68.0 ms                                                             | 65.7 ms: 1.04x faster                                  |
| regex_compile           | 137 ms                                                              | 132 ms: 1.03x faster                                   |
| comprehensions          | 22.2 us                                                             | 21.5 us: 1.03x faster                                  |
| meteor_contest          | 106 ms                                                              | 103 ms: 1.03x faster                                   |
| sqlalchemy_imperative   | 18.0 ms                                                             | 17.4 ms: 1.03x faster                                  |
| docutils                | 2.59 sec                                                            | 2.51 sec: 1.03x faster                                 |
| float                   | 76.0 ms                                                             | 73.5 ms: 1.03x faster                                  |
| 2to3                    | 257 ms                                                              | 249 ms: 1.03x faster                                   |
| deepcopy                | 339 us                                                              | 328 us: 1.03x faster                                   |
| regex_v8                | 22.0 ms                                                             | 21.3 ms: 1.03x faster                                  |
| chameleon               | 6.52 ms                                                             | 6.33 ms: 1.03x faster                                  |
| dulwich_log             | 63.6 ms                                                             | 61.8 ms: 1.03x faster                                  |
| async_tree_cpu_io_mixed | 736 ms                                                              | 716 ms: 1.03x faster                                   |
| sympy_sum               | 167 ms                                                              | 163 ms: 1.03x faster                                   |
| sqlalchemy_declarative  | 138 ms                                                              | 135 ms: 1.03x faster                                   |
| logging_silent          | 98.7 ns                                                             | 97.0 ns: 1.02x faster                                  |
| unpickle_list           | 4.96 us                                                             | 4.88 us: 1.02x faster                                  |
| scimark_lu              | 108 ms                                                              | 107 ms: 1.02x faster                                   |
| fannkuch                | 384 ms                                                              | 378 ms: 1.02x faster                                   |
| async_tree_none         | 525 ms                                                              | 518 ms: 1.01x faster                                   |
| django_template         | 32.9 ms                                                             | 32.4 ms: 1.01x faster                                  |
| telco                   | 6.59 ms                                                             | 6.54 ms: 1.01x faster                                  |
| mako                    | 9.82 ms                                                             | 9.86 ms: 1.00x slower                                  |
| crypto_pyaes            | 73.8 ms                                                             | 74.6 ms: 1.01x slower                                  |
| xml_etree_process       | 54.1 ms                                                             | 55.0 ms: 1.02x slower                                  |
| create_gc_cycles        | 1.48 ms                                                             | 1.50 ms: 1.02x slower                                  |
| thrift                  | 766 us                                                              | 780 us: 1.02x slower                                   |
| regex_dna               | 196 ms                                                              | 202 ms: 1.03x slower                                   |
| sqlite_synth            | 2.51 us                                                             | 2.62 us: 1.04x slower                                  |
| xml_etree_generate      | 76.5 ms                                                             | 79.9 ms: 1.04x slower                                  |
| python_startup          | 8.49 ms                                                             | 8.91 ms: 1.05x slower                                  |
| pickle_dict             | 30.9 us                                                             | 32.9 us: 1.06x slower                                  |
| pickle_list             | 4.03 us                                                             | 4.31 us: 1.07x slower                                  |
| gc_traversal            | 3.63 ms                                                             | 3.98 ms: 1.10x slower                                  |
| python_startup_no_site  | 5.98 ms                                                             | 6.60 ms: 1.10x slower                                  |
| unpickle                | 13.2 us                                                             | 14.6 us: 1.11x slower                                  |
| pickle                  | 9.79 us                                                             | 10.9 us: 1.11x slower                                  |
| async_generators        | 361 ms                                                              | 430 ms: 1.19x slower                                   |
| dask                    | 368 ms                                                              | 492 ms: 1.34x slower                                   |
| Geometric mean          | (ref)                                                               | 1.05x faster                                           |

Benchmark hidden because not significant (8): async_tree_memoization, djangocms, scimark_monte_carlo, bench_mp_pool, async_tree_io, regex_effbot, pyflate, deepcopy_reduce
Ignored benchmarks (1) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging
