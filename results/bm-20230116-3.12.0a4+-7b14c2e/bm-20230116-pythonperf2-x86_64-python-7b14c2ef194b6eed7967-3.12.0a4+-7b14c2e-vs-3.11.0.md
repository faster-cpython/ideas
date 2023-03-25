
# Results vs. 3.11.0

- fork: python
- ref: 7b14c2ef194b6eed7967
- machine: linux-x86_64
- commit hash: 7b14c2e
- commit date: 2023-01-16
- overall geometric mean: 1.03x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 287 ms: 1.01x faster                                                         |
| chameleon      | 7.50 ms                                                                   | 7.60 ms: 1.01x slower                                                        |
| docutils       | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 66.6 ms: 1.05x faster                                                        |
| tornado_http   | 125 ms                                                                    | 120 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                   | 72.6 ms: 1.04x faster                                                        |
| nbody          | 92.1 ms                                                                   | 89.1 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                        |
| regex_compile  | 154 ms                                                                    | 151 ms: 1.02x faster                                                         |
| regex_dna      | 225 ms                                                                    | 226 ms: 1.00x slower                                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.34 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.1 ms: 1.32x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.3 us: 1.17x faster                                                        |
| unpickle_pure_python | 238 us                                                                    | 210 us: 1.13x faster                                                         |
| xml_etree_parse      | 161 ms                                                                    | 143 ms: 1.12x faster                                                         |
| pickle_pure_python   | 319 us                                                                    | 304 us: 1.05x faster                                                         |
| xml_etree_process    | 55.8 ms                                                                   | 54.8 ms: 1.02x faster                                                        |
| pickle               | 9.92 us                                                                   | 10.0 us: 1.01x slower                                                        |
| unpickle             | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                        |
| pickle_dict          | 31.1 us                                                                   | 32.2 us: 1.04x slower                                                        |
| pickle_list          | 3.78 us                                                                   | 4.12 us: 1.09x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.05x faster                                                                 |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 11.1 ms: 1.03x slower                                                        |
| python_startup_no_site | 7.73 ms                                                                   | 8.18 ms: 1.06x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.05x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| genshi_text    | 26.3 ms                                                                   | 25.5 ms: 1.03x faster                                                        |
| genshi_xml     | 57.8 ms                                                                   | 56.5 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| asyncio_tcp             | 752 ms                                                                    | 393 ms: 1.91x faster                                                         |
| json_dumps              | 13.4 ms                                                                   | 10.1 ms: 1.32x faster                                                        |
| gc_traversal            | 4.22 ms                                                                   | 3.52 ms: 1.20x faster                                                        |
| mypy2                   | 446 ms                                                                    | 379 ms: 1.18x faster                                                         |
| json_loads              | 28.4 us                                                                   | 24.3 us: 1.17x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 210 us: 1.13x faster                                                         |
| xml_etree_parse         | 161 ms                                                                    | 143 ms: 1.12x faster                                                         |
| fannkuch                | 449 ms                                                                    | 401 ms: 1.12x faster                                                         |
| deltablue               | 3.99 ms                                                                   | 3.58 ms: 1.12x faster                                                        |
| scimark_lu              | 114 ms                                                                    | 103 ms: 1.11x faster                                                         |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.66 ms: 1.11x faster                                                        |
| json                    | 5.59 ms                                                                   | 5.09 ms: 1.10x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 22.9 ms: 1.07x faster                                                        |
| richards                | 49.1 ms                                                                   | 46.0 ms: 1.07x faster                                                        |
| mako                    | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| chaos                   | 76.2 ms                                                                   | 72.1 ms: 1.06x faster                                                        |
| pycparser               | 1.30 sec                                                                  | 1.23 sec: 1.06x faster                                                       |
| html5lib                | 70.2 ms                                                                   | 66.6 ms: 1.05x faster                                                        |
| nqueens                 | 101 ms                                                                    | 95.8 ms: 1.05x faster                                                        |
| pickle_pure_python      | 319 us                                                                    | 304 us: 1.05x faster                                                         |
| async_tree_memoization  | 639 ms                                                                    | 609 ms: 1.05x faster                                                         |
| hexiom                  | 7.00 ms                                                                   | 6.69 ms: 1.05x faster                                                        |
| tornado_http            | 125 ms                                                                    | 120 ms: 1.04x faster                                                         |
| float                   | 75.7 ms                                                                   | 72.6 ms: 1.04x faster                                                        |
| coroutines              | 29.5 ms                                                                   | 28.3 ms: 1.04x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 510 ms: 1.04x faster                                                         |
| bench_thread_pool       | 990 us                                                                    | 955 us: 1.04x faster                                                         |
| dulwich_log             | 69.1 ms                                                                   | 66.9 ms: 1.03x faster                                                        |
| aiohttp                 | 959 us                                                                    | 927 us: 1.03x faster                                                         |
| nbody                   | 92.1 ms                                                                   | 89.1 ms: 1.03x faster                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.59 ms: 1.03x faster                                                        |
| logging_silent          | 103 ns                                                                    | 99.5 ns: 1.03x faster                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 65.8 ms: 1.03x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 25.5 ms: 1.03x faster                                                        |
| thrift                  | 942 us                                                                    | 916 us: 1.03x faster                                                         |
| docutils                | 2.86 sec                                                                  | 2.78 sec: 1.03x faster                                                       |
| unpack_sequence         | 45.9 ns                                                                   | 44.7 ns: 1.03x faster                                                        |
| gunicorn                | 936 us                                                                    | 914 us: 1.02x faster                                                         |
| genshi_xml              | 57.8 ms                                                                   | 56.5 ms: 1.02x faster                                                        |
| async_tree_io           | 1.18 sec                                                                  | 1.16 sec: 1.02x faster                                                       |
| regex_compile           | 154 ms                                                                    | 151 ms: 1.02x faster                                                         |
| sympy_expand            | 547 ms                                                                    | 536 ms: 1.02x faster                                                         |
| xml_etree_process       | 55.8 ms                                                                   | 54.8 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 741 ms: 1.02x faster                                                         |
| raytrace                | 303 ms                                                                    | 300 ms: 1.01x faster                                                         |
| 2to3                    | 289 ms                                                                    | 287 ms: 1.01x faster                                                         |
| crypto_pyaes            | 85.0 ms                                                                   | 84.3 ms: 1.01x faster                                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.59 sec: 1.01x faster                                                       |
| meteor_contest          | 129 ms                                                                    | 129 ms: 1.01x faster                                                         |
| regex_dna               | 225 ms                                                                    | 226 ms: 1.00x slower                                                         |
| deepcopy_memo           | 37.0 us                                                                   | 37.1 us: 1.00x slower                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.4 ms: 1.00x slower                                                        |
| pathlib                 | 19.2 ms                                                                   | 19.3 ms: 1.01x slower                                                        |
| logging_format          | 7.84 us                                                                   | 7.90 us: 1.01x slower                                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.34 ms: 1.01x slower                                                        |
| pickle                  | 9.92 us                                                                   | 10.0 us: 1.01x slower                                                        |
| telco                   | 6.70 ms                                                                   | 6.77 ms: 1.01x slower                                                        |
| go                      | 158 ms                                                                    | 160 ms: 1.01x slower                                                         |
| chameleon               | 7.50 ms                                                                   | 7.60 ms: 1.01x slower                                                        |
| sympy_sum               | 182 ms                                                                    | 185 ms: 1.01x slower                                                         |
| unpickle                | 13.0 us                                                                   | 13.3 us: 1.02x slower                                                        |
| mdp                     | 2.73 sec                                                                  | 2.77 sec: 1.02x slower                                                       |
| deepcopy_reduce         | 3.39 us                                                                   | 3.45 us: 1.02x slower                                                        |
| spectral_norm           | 95.1 ms                                                                   | 96.9 ms: 1.02x slower                                                        |
| logging_simple          | 6.95 us                                                                   | 7.12 us: 1.02x slower                                                        |
| sqlite_synth            | 2.49 us                                                                   | 2.57 us: 1.03x slower                                                        |
| deepcopy                | 384 us                                                                    | 397 us: 1.03x slower                                                         |
| python_startup          | 10.7 ms                                                                   | 11.1 ms: 1.03x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 32.2 us: 1.04x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 287 ms: 1.04x slower                                                         |
| sqlglot_parse           | 1.53 ms                                                                   | 1.59 ms: 1.04x slower                                                        |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.96 ms: 1.04x slower                                                        |
| async_generators        | 318 ms                                                                    | 333 ms: 1.04x slower                                                         |
| bench_mp_pool           | 4.54 ms                                                                   | 4.79 ms: 1.05x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 8.18 ms: 1.06x slower                                                        |
| generators              | 56.0 ms                                                                   | 60.7 ms: 1.08x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 4.12 us: 1.09x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 27.3 us: 1.10x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.03x faster                                                                 |

Benchmark hidden because not significant (13): dask, sqlglot_normalize, pyflate, pidigits, xml_etree_generate, sqlglot_optimize, scimark_sor, sympy_str, xml_etree_iterparse, unpickle_list, coverage, pprint_safe_repr, django_template
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
