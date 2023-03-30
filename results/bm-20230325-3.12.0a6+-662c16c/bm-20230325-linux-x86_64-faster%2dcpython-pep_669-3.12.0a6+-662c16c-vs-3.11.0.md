
# Results vs. 3.11.0

- fork: faster-cpython
- ref: pep_669
- machine: linux-x86_64
- commit hash: 662c16c
- commit date: 2023-03-25
- overall geometric mean: 1.05x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 257 ms                                                              | 247 ms: 1.04x faster                                                |
| chameleon      | 6.52 ms                                                             | 6.20 ms: 1.05x faster                                               |
| docutils       | 2.59 sec                                                            | 2.51 sec: 1.03x faster                                              |
| html5lib       | 64.0 ms                                                             | 60.5 ms: 1.06x faster                                               |
| tornado_http   | 96.7 ms                                                             | 90.0 ms: 1.07x faster                                               |
| Geometric mean | (ref)                                                               | 1.05x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 96.7 ms                                                             | 84.3 ms: 1.15x faster                                               |
| float          | 76.0 ms                                                             | 71.2 ms: 1.07x faster                                               |
| pidigits       | 197 ms                                                              | 188 ms: 1.05x faster                                                |
| Geometric mean | (ref)                                                               | 1.09x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                              | 129 ms: 1.06x faster                                                |
| regex_v8       | 22.0 ms                                                             | 22.2 ms: 1.01x slower                                               |
| regex_dna      | 196 ms                                                              | 203 ms: 1.03x slower                                                |
| regex_effbot   | 3.32 ms                                                             | 3.47 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                               | 1.01x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 12.5 ms                                                             | 9.53 ms: 1.31x faster                                               |
| unpickle_pure_python | 228 us                                                              | 197 us: 1.16x faster                                                |
| xml_etree_parse      | 162 ms                                                              | 148 ms: 1.10x faster                                                |
| pickle_pure_python   | 307 us                                                              | 282 us: 1.09x faster                                                |
| json_loads           | 26.2 us                                                             | 24.0 us: 1.09x faster                                               |
| xml_etree_iterparse  | 108 ms                                                              | 99.1 ms: 1.09x faster                                               |
| pickle_dict          | 30.9 us                                                             | 30.6 us: 1.01x faster                                               |
| xml_etree_process    | 54.1 ms                                                             | 54.8 ms: 1.01x slower                                               |
| xml_etree_generate   | 76.5 ms                                                             | 79.2 ms: 1.04x slower                                               |
| pickle_list          | 4.03 us                                                             | 4.22 us: 1.05x slower                                               |
| pickle               | 9.79 us                                                             | 10.3 us: 1.05x slower                                               |
| unpickle             | 13.2 us                                                             | 14.1 us: 1.07x slower                                               |
| Geometric mean       | (ref)                                                               | 1.04x faster                                                        |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 8.49 ms                                                             | 8.86 ms: 1.04x slower                                               |
| python_startup_no_site | 5.98 ms                                                             | 6.57 ms: 1.10x slower                                               |
| Geometric mean         | (ref)                                                               | 1.07x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                             | 46.0 ms: 1.13x faster                                               |
| genshi_text     | 21.8 ms                                                             | 20.4 ms: 1.07x faster                                               |
| django_template | 32.9 ms                                                             | 32.6 ms: 1.01x faster                                               |
| Geometric mean  | (ref)                                                               | 1.05x faster                                                        |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|-------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| generators              | 73.4 ms                                                             | 27.5 ms: 2.67x faster                                               |
| asyncio_tcp             | 888 ms                                                              | 501 ms: 1.77x faster                                                |
| json_dumps              | 12.5 ms                                                             | 9.53 ms: 1.31x faster                                               |
| mypy2                   | 422 ms                                                              | 326 ms: 1.29x faster                                                |
| coroutines              | 26.3 ms                                                             | 22.1 ms: 1.19x faster                                               |
| deltablue               | 3.66 ms                                                             | 3.15 ms: 1.16x faster                                               |
| unpickle_pure_python    | 228 us                                                              | 197 us: 1.16x faster                                                |
| unpack_sequence         | 49.5 ns                                                             | 43.1 ns: 1.15x faster                                               |
| nbody                   | 96.7 ms                                                             | 84.3 ms: 1.15x faster                                               |
| genshi_xml              | 51.8 ms                                                             | 46.0 ms: 1.13x faster                                               |
| spectral_norm           | 99.5 ms                                                             | 88.8 ms: 1.12x faster                                               |
| hexiom                  | 6.48 ms                                                             | 5.90 ms: 1.10x faster                                               |
| xml_etree_parse         | 162 ms                                                              | 148 ms: 1.10x faster                                                |
| deepcopy_memo           | 36.4 us                                                             | 33.3 us: 1.09x faster                                               |
| pickle_pure_python      | 307 us                                                              | 282 us: 1.09x faster                                                |
| json_loads              | 26.2 us                                                             | 24.0 us: 1.09x faster                                               |
| xml_etree_iterparse     | 108 ms                                                              | 99.1 ms: 1.09x faster                                               |
| richards                | 45.7 ms                                                             | 42.4 ms: 1.08x faster                                               |
| tornado_http            | 96.7 ms                                                             | 90.0 ms: 1.07x faster                                               |
| logging_simple          | 6.09 us                                                             | 5.68 us: 1.07x faster                                               |
| scimark_fft             | 328 ms                                                              | 306 ms: 1.07x faster                                                |
| genshi_text             | 21.8 ms                                                             | 20.4 ms: 1.07x faster                                               |
| logging_silent          | 98.7 ns                                                             | 92.5 ns: 1.07x faster                                               |
| float                   | 76.0 ms                                                             | 71.2 ms: 1.07x faster                                               |
| logging_format          | 6.64 us                                                             | 6.23 us: 1.07x faster                                               |
| aiohttp                 | 1.05 ms                                                             | 991 us: 1.06x faster                                                |
| mdp                     | 2.64 sec                                                            | 2.48 sec: 1.06x faster                                              |
| scimark_sor             | 115 ms                                                              | 108 ms: 1.06x faster                                                |
| deepcopy                | 339 us                                                              | 319 us: 1.06x faster                                                |
| sympy_expand            | 477 ms                                                              | 449 ms: 1.06x faster                                                |
| regex_compile           | 137 ms                                                              | 129 ms: 1.06x faster                                                |
| sqlglot_optimize        | 53.4 ms                                                             | 50.4 ms: 1.06x faster                                               |
| html5lib                | 64.0 ms                                                             | 60.5 ms: 1.06x faster                                               |
| gunicorn                | 1.13 ms                                                             | 1.07 ms: 1.06x faster                                               |
| scimark_sparse_mat_mult | 4.47 ms                                                             | 4.24 ms: 1.05x faster                                               |
| json                    | 4.86 ms                                                             | 4.61 ms: 1.05x faster                                               |
| pprint_pformat          | 1.45 sec                                                            | 1.38 sec: 1.05x faster                                              |
| bench_thread_pool       | 820 us                                                              | 779 us: 1.05x faster                                                |
| sympy_integrate         | 21.0 ms                                                             | 20.0 ms: 1.05x faster                                               |
| sympy_str               | 291 ms                                                              | 277 ms: 1.05x faster                                                |
| sqlalchemy_imperative   | 18.0 ms                                                             | 17.1 ms: 1.05x faster                                               |
| chameleon               | 6.52 ms                                                             | 6.20 ms: 1.05x faster                                               |
| raytrace                | 292 ms                                                              | 278 ms: 1.05x faster                                                |
| nqueens                 | 84.0 ms                                                             | 80.1 ms: 1.05x faster                                               |
| sqlglot_normalize       | 108 ms                                                              | 104 ms: 1.05x faster                                                |
| pidigits                | 197 ms                                                              | 188 ms: 1.05x faster                                                |
| coverage                | 101 ms                                                              | 96.7 ms: 1.05x faster                                               |
| pathlib                 | 18.2 ms                                                             | 17.4 ms: 1.04x faster                                               |
| pprint_safe_repr        | 701 ms                                                              | 673 ms: 1.04x faster                                                |
| 2to3                    | 257 ms                                                              | 247 ms: 1.04x faster                                                |
| scimark_monte_carlo     | 67.8 ms                                                             | 65.2 ms: 1.04x faster                                               |
| sqlalchemy_declarative  | 138 ms                                                              | 133 ms: 1.04x faster                                                |
| sympy_sum               | 167 ms                                                              | 162 ms: 1.03x faster                                                |
| docutils                | 2.59 sec                                                            | 2.51 sec: 1.03x faster                                              |
| meteor_contest          | 106 ms                                                              | 103 ms: 1.03x faster                                                |
| telco                   | 6.59 ms                                                             | 6.41 ms: 1.03x faster                                               |
| dulwich_log             | 63.6 ms                                                             | 62.1 ms: 1.03x faster                                               |
| chaos                   | 68.0 ms                                                             | 66.6 ms: 1.02x faster                                               |
| pyflate                 | 414 ms                                                              | 406 ms: 1.02x faster                                                |
| deepcopy_reduce         | 2.96 us                                                             | 2.90 us: 1.02x faster                                               |
| crypto_pyaes            | 73.8 ms                                                             | 72.7 ms: 1.01x faster                                               |
| pycparser               | 1.14 sec                                                            | 1.13 sec: 1.01x faster                                              |
| pickle_dict             | 30.9 us                                                             | 30.6 us: 1.01x faster                                               |
| async_tree_none         | 525 ms                                                              | 520 ms: 1.01x faster                                                |
| django_template         | 32.9 ms                                                             | 32.6 ms: 1.01x faster                                               |
| go                      | 138 ms                                                              | 137 ms: 1.01x faster                                                |
| create_gc_cycles        | 1.48 ms                                                             | 1.47 ms: 1.00x faster                                               |
| gc_traversal            | 3.63 ms                                                             | 3.64 ms: 1.00x slower                                               |
| regex_v8                | 22.0 ms                                                             | 22.2 ms: 1.01x slower                                               |
| xml_etree_process       | 54.1 ms                                                             | 54.8 ms: 1.01x slower                                               |
| sqlglot_transpile       | 1.65 ms                                                             | 1.68 ms: 1.02x slower                                               |
| thrift                  | 766 us                                                              | 784 us: 1.02x slower                                                |
| sqlglot_parse           | 1.36 ms                                                             | 1.40 ms: 1.02x slower                                               |
| regex_dna               | 196 ms                                                              | 203 ms: 1.03x slower                                                |
| xml_etree_generate      | 76.5 ms                                                             | 79.2 ms: 1.04x slower                                               |
| sqlite_synth            | 2.51 us                                                             | 2.62 us: 1.04x slower                                               |
| python_startup          | 8.49 ms                                                             | 8.86 ms: 1.04x slower                                               |
| regex_effbot            | 3.32 ms                                                             | 3.47 ms: 1.04x slower                                               |
| pickle_list             | 4.03 us                                                             | 4.22 us: 1.05x slower                                               |
| comprehensions          | 22.2 us                                                             | 23.3 us: 1.05x slower                                               |
| pickle                  | 9.79 us                                                             | 10.3 us: 1.05x slower                                               |
| unpickle                | 13.2 us                                                             | 14.1 us: 1.07x slower                                               |
| python_startup_no_site  | 5.98 ms                                                             | 6.57 ms: 1.10x slower                                               |
| async_generators        | 361 ms                                                              | 422 ms: 1.17x slower                                                |
| dask                    | 368 ms                                                              | 490 ms: 1.33x slower                                                |
| Geometric mean          | (ref)                                                               | 1.05x faster                                                        |

Benchmark hidden because not significant (9): scimark_lu, fannkuch, async_tree_cpu_io_mixed, djangocms, async_tree_io, unpickle_list, bench_mp_pool, async_tree_memoization, mako
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint
