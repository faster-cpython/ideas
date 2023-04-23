
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 0fd3891
- commit date: 2023-04-22
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 268 ms: 1.04x slower                                   |
| chameleon      | 6.52 ms                                                             | 6.93 ms: 1.06x slower                                  |
| docutils       | 2.59 sec                                                            | 2.70 sec: 1.04x slower                                 |
| html5lib       | 64.0 ms                                                             | 65.0 ms: 1.02x slower                                  |
| tornado_http   | 96.7 ms                                                             | 104 ms: 1.08x slower                                   |
| Geometric mean | (ref)                                                               | 1.05x slower                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 96.7 ms                                                             | 88.4 ms: 1.09x faster                                  |
| pidigits       | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| float          | 76.0 ms                                                             | 80.4 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                               | 1.03x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 3.32 ms                                                             | 3.26 ms: 1.02x faster                                  |
| regex_v8       | 22.0 ms                                                             | 22.3 ms: 1.01x slower                                  |
| regex_dna      | 196 ms                                                              | 205 ms: 1.04x slower                                   |
| regex_compile  | 137 ms                                                              | 144 ms: 1.05x slower                                   |
| Geometric mean | (ref)                                                               | 1.02x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.75 ms: 1.29x faster                                  |
| xml_etree_parse      | 162 ms                                                              | 152 ms: 1.07x faster                                   |
| json_loads           | 26.2 us                                                             | 24.8 us: 1.06x faster                                  |
| xml_etree_iterparse  | 108 ms                                                              | 103 ms: 1.04x faster                                   |
| unpickle_pure_python | 228 us                                                              | 219 us: 1.04x faster                                   |
| pickle_dict          | 30.9 us                                                             | 30.7 us: 1.01x faster                                  |
| pickle_pure_python   | 307 us                                                              | 311 us: 1.01x slower                                   |
| unpickle_list        | 4.96 us                                                             | 5.24 us: 1.06x slower                                  |
| pickle               | 9.79 us                                                             | 10.5 us: 1.08x slower                                  |
| xml_etree_process    | 54.1 ms                                                             | 58.6 ms: 1.08x slower                                  |
| xml_etree_generate   | 76.5 ms                                                             | 83.2 ms: 1.09x slower                                  |
| pickle_list          | 4.03 us                                                             | 4.39 us: 1.09x slower                                  |
| unpickle             | 13.2 us                                                             | 14.9 us: 1.13x slower                                  |
| Geometric mean       | (ref)                                                               | 1.00x slower                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 9.05 ms: 1.07x slower                                  |
| python_startup_no_site | 5.98 ms                                                             | 6.65 ms: 1.11x slower                                  |
| Geometric mean         | (ref)                                                               | 1.09x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 50.7 ms: 1.02x faster                                  |
| genshi_text     | 21.8 ms                                                             | 22.7 ms: 1.04x slower                                  |
| django_template | 32.9 ms                                                             | 34.7 ms: 1.05x slower                                  |
| mako            | 9.82 ms                                                             | 10.5 ms: 1.07x slower                                  |
| Geometric mean  | (ref)                                                               | 1.04x slower                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-linux-x86_64-python-main-3.12.0a7+-0fd3891 |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 73.4 ms                                                             | 31.2 ms: 2.36x faster                                  |
| asyncio_tcp             | 888 ms                                                              | 511 ms: 1.74x faster                                   |
| json_dumps              | 12.5 ms                                                             | 9.75 ms: 1.29x faster                                  |
| coroutines              | 26.3 ms                                                             | 22.3 ms: 1.18x faster                                  |
| mypy2                   | 422 ms                                                              | 360 ms: 1.17x faster                                   |
| nbody                   | 96.7 ms                                                             | 88.4 ms: 1.09x faster                                  |
| xml_etree_parse         | 162 ms                                                              | 152 ms: 1.07x faster                                   |
| json_loads              | 26.2 us                                                             | 24.8 us: 1.06x faster                                  |
| pidigits                | 197 ms                                                              | 188 ms: 1.05x faster                                   |
| xml_etree_iterparse     | 108 ms                                                              | 103 ms: 1.04x faster                                   |
| unpickle_pure_python    | 228 us                                                              | 219 us: 1.04x faster                                   |
| unpack_sequence         | 49.5 ns                                                             | 47.4 ns: 1.04x faster                                  |
| richards                | 45.7 ms                                                             | 44.0 ms: 1.04x faster                                  |
| sqlglot_parse           | 1.36 ms                                                             | 1.31 ms: 1.04x faster                                  |
| nqueens                 | 84.0 ms                                                             | 81.2 ms: 1.03x faster                                  |
| pathlib                 | 18.2 ms                                                             | 17.7 ms: 1.03x faster                                  |
| json                    | 4.86 ms                                                             | 4.75 ms: 1.02x faster                                  |
| hexiom                  | 6.48 ms                                                             | 6.34 ms: 1.02x faster                                  |
| genshi_xml              | 51.8 ms                                                             | 50.7 ms: 1.02x faster                                  |
| mdp                     | 2.64 sec                                                            | 2.59 sec: 1.02x faster                                 |
| regex_effbot            | 3.32 ms                                                             | 3.26 ms: 1.02x faster                                  |
| sqlglot_transpile       | 1.65 ms                                                             | 1.63 ms: 1.01x faster                                  |
| pickle_dict             | 30.9 us                                                             | 30.7 us: 1.01x faster                                  |
| deltablue               | 3.66 ms                                                             | 3.64 ms: 1.01x faster                                  |
| async_tree_io           | 1.28 sec                                                            | 1.30 sec: 1.01x slower                                 |
| create_gc_cycles        | 1.48 ms                                                             | 1.50 ms: 1.01x slower                                  |
| pickle_pure_python      | 307 us                                                              | 311 us: 1.01x slower                                   |
| logging_simple          | 6.09 us                                                             | 6.17 us: 1.01x slower                                  |
| scimark_lu              | 108 ms                                                              | 110 ms: 1.01x slower                                   |
| regex_v8                | 22.0 ms                                                             | 22.3 ms: 1.01x slower                                  |
| html5lib                | 64.0 ms                                                             | 65.0 ms: 1.02x slower                                  |
| chaos                   | 68.0 ms                                                             | 69.3 ms: 1.02x slower                                  |
| bench_thread_pool       | 820 us                                                              | 836 us: 1.02x slower                                   |
| sqlglot_normalize       | 108 ms                                                              | 111 ms: 1.02x slower                                   |
| sqlglot_optimize        | 53.4 ms                                                             | 54.5 ms: 1.02x slower                                  |
| pprint_pformat          | 1.45 sec                                                            | 1.48 sec: 1.02x slower                                 |
| raytrace                | 292 ms                                                              | 300 ms: 1.03x slower                                   |
| logging_silent          | 98.7 ns                                                             | 101 ns: 1.03x slower                                   |
| telco                   | 6.59 ms                                                             | 6.83 ms: 1.04x slower                                  |
| genshi_text             | 21.8 ms                                                             | 22.7 ms: 1.04x slower                                  |
| sympy_integrate         | 21.0 ms                                                             | 21.9 ms: 1.04x slower                                  |
| thrift                  | 766 us                                                              | 796 us: 1.04x slower                                   |
| async_tree_memoization  | 621 ms                                                              | 646 ms: 1.04x slower                                   |
| sympy_expand            | 477 ms                                                              | 496 ms: 1.04x slower                                   |
| 2to3                    | 257 ms                                                              | 268 ms: 1.04x slower                                   |
| logging_format          | 6.64 us                                                             | 6.91 us: 1.04x slower                                  |
| djangocms               | 32.3 us                                                             | 33.6 us: 1.04x slower                                  |
| docutils                | 2.59 sec                                                            | 2.70 sec: 1.04x slower                                 |
| regex_dna               | 196 ms                                                              | 205 ms: 1.04x slower                                   |
| deepcopy_memo           | 36.4 us                                                             | 38.0 us: 1.05x slower                                  |
| comprehensions          | 22.2 us                                                             | 23.3 us: 1.05x slower                                  |
| meteor_contest          | 106 ms                                                              | 111 ms: 1.05x slower                                   |
| pprint_safe_repr        | 701 ms                                                              | 737 ms: 1.05x slower                                   |
| regex_compile           | 137 ms                                                              | 144 ms: 1.05x slower                                   |
| spectral_norm           | 99.5 ms                                                             | 105 ms: 1.05x slower                                   |
| django_template         | 32.9 ms                                                             | 34.7 ms: 1.05x slower                                  |
| unpickle_list           | 4.96 us                                                             | 5.24 us: 1.06x slower                                  |
| sqlite_synth            | 2.51 us                                                             | 2.66 us: 1.06x slower                                  |
| float                   | 76.0 ms                                                             | 80.4 ms: 1.06x slower                                  |
| sqlalchemy_declarative  | 138 ms                                                              | 147 ms: 1.06x slower                                   |
| deepcopy                | 339 us                                                              | 360 us: 1.06x slower                                   |
| chameleon               | 6.52 ms                                                             | 6.93 ms: 1.06x slower                                  |
| sqlalchemy_imperative   | 18.0 ms                                                             | 19.2 ms: 1.06x slower                                  |
| dulwich_log             | 63.6 ms                                                             | 67.8 ms: 1.06x slower                                  |
| python_startup          | 8.49 ms                                                             | 9.05 ms: 1.07x slower                                  |
| sympy_str               | 291 ms                                                              | 311 ms: 1.07x slower                                   |
| crypto_pyaes            | 73.8 ms                                                             | 78.9 ms: 1.07x slower                                  |
| mako                    | 9.82 ms                                                             | 10.5 ms: 1.07x slower                                  |
| deepcopy_reduce         | 2.96 us                                                             | 3.18 us: 1.08x slower                                  |
| pickle                  | 9.79 us                                                             | 10.5 us: 1.08x slower                                  |
| scimark_fft             | 328 ms                                                              | 353 ms: 1.08x slower                                   |
| tornado_http            | 96.7 ms                                                             | 104 ms: 1.08x slower                                   |
| scimark_sor             | 115 ms                                                              | 124 ms: 1.08x slower                                   |
| scimark_monte_carlo     | 67.8 ms                                                             | 73.3 ms: 1.08x slower                                  |
| sympy_sum               | 167 ms                                                              | 181 ms: 1.08x slower                                   |
| gc_traversal            | 3.63 ms                                                             | 3.93 ms: 1.08x slower                                  |
| xml_etree_process       | 54.1 ms                                                             | 58.6 ms: 1.08x slower                                  |
| xml_etree_generate      | 76.5 ms                                                             | 83.2 ms: 1.09x slower                                  |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.86 ms: 1.09x slower                                  |
| pickle_list             | 4.03 us                                                             | 4.39 us: 1.09x slower                                  |
| pyflate                 | 414 ms                                                              | 459 ms: 1.11x slower                                   |
| python_startup_no_site  | 5.98 ms                                                             | 6.65 ms: 1.11x slower                                  |
| unpickle                | 13.2 us                                                             | 14.9 us: 1.13x slower                                  |
| async_generators        | 361 ms                                                              | 445 ms: 1.23x slower                                   |
| dask                    | 368 ms                                                              | 539 ms: 1.46x slower                                   |
| Geometric mean          | (ref)                                                               | 1.01x slower                                           |

Benchmark hidden because not significant (8): pylint, go, async_tree_none, fannkuch, bench_mp_pool, coverage, pycparser, async_tree_cpu_io_mixed
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn
