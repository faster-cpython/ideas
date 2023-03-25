
# Results vs. 3.11.0

- fork: python
- ref: 594de165bf2f21d6b28e
- machine: linux-x86_64
- commit hash: 594de16
- commit date: 2022-11-28
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf2-x86_64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 280 ms: 1.03x faster                                                         |
| chameleon      | 7.50 ms                                                                   | 7.65 ms: 1.02x slower                                                        |
| docutils       | 2.86 sec                                                                  | 2.77 sec: 1.03x faster                                                       |
| html5lib       | 70.2 ms                                                                   | 66.5 ms: 1.06x faster                                                        |
| tornado_http   | 125 ms                                                                    | 119 ms: 1.05x faster                                                         |
| Geometric mean | (ref)                                                                     | 1.03x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf2-x86_64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.1 ms                                                                   | 89.6 ms: 1.03x faster                                                        |
| float          | 75.7 ms                                                                   | 73.9 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf2-x86_64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                   | 23.2 ms: 1.05x faster                                                        |
| regex_compile  | 154 ms                                                                    | 149 ms: 1.03x faster                                                         |
| regex_effbot   | 3.31 ms                                                                   | 3.36 ms: 1.02x slower                                                        |
| regex_dna      | 225 ms                                                                    | 229 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf2-x86_64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.4 ms                                                                   | 10.5 ms: 1.28x faster                                                        |
| json_loads           | 28.4 us                                                                   | 24.2 us: 1.18x faster                                                        |
| xml_etree_parse      | 161 ms                                                                    | 141 ms: 1.14x faster                                                         |
| unpickle_pure_python | 238 us                                                                    | 219 us: 1.09x faster                                                         |
| pickle               | 9.92 us                                                                   | 9.77 us: 1.02x faster                                                        |
| xml_etree_iterparse  | 106 ms                                                                    | 104 ms: 1.01x faster                                                         |
| xml_etree_generate   | 79.1 ms                                                                   | 79.8 ms: 1.01x slower                                                        |
| pickle_list          | 3.78 us                                                                   | 3.84 us: 1.02x slower                                                        |
| pickle_dict          | 31.1 us                                                                   | 31.7 us: 1.02x slower                                                        |
| unpickle             | 13.0 us                                                                   | 13.5 us: 1.04x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.04x faster                                                                 |

Benchmark hidden because not significant (3): xml_etree_process, pickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf2-x86_64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.8 ms: 1.01x slower                                                        |
| python_startup_no_site | 7.73 ms                                                                   | 7.85 ms: 1.02x slower                                                        |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf2-x86_64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-----------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 57.8 ms                                                                   | 52.3 ms: 1.11x faster                                                        |
| genshi_text     | 26.3 ms                                                                   | 24.5 ms: 1.07x faster                                                        |
| mako            | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| django_template | 39.6 ms                                                                   | 40.1 ms: 1.01x slower                                                        |
| Geometric mean  | (ref)                                                                     | 1.06x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf2-x86_64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-------------------------|:-------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps              | 13.4 ms                                                                   | 10.5 ms: 1.28x faster                                                        |
| mypy2                   | 446 ms                                                                    | 372 ms: 1.20x faster                                                         |
| gc_traversal            | 4.22 ms                                                                   | 3.56 ms: 1.18x faster                                                        |
| json_loads              | 28.4 us                                                                   | 24.2 us: 1.18x faster                                                        |
| xml_etree_parse         | 161 ms                                                                    | 141 ms: 1.14x faster                                                         |
| fannkuch                | 449 ms                                                                    | 399 ms: 1.13x faster                                                         |
| scimark_lu              | 114 ms                                                                    | 103 ms: 1.11x faster                                                         |
| genshi_xml              | 57.8 ms                                                                   | 52.3 ms: 1.11x faster                                                        |
| json                    | 5.59 ms                                                                   | 5.08 ms: 1.10x faster                                                        |
| unpickle_pure_python    | 238 us                                                                    | 219 us: 1.09x faster                                                         |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 3.77 ms: 1.08x faster                                                        |
| deltablue               | 3.99 ms                                                                   | 3.71 ms: 1.08x faster                                                        |
| genshi_text             | 26.3 ms                                                                   | 24.5 ms: 1.07x faster                                                        |
| mako                    | 10.9 ms                                                                   | 10.2 ms: 1.07x faster                                                        |
| aiohttp                 | 959 us                                                                    | 904 us: 1.06x faster                                                         |
| html5lib                | 70.2 ms                                                                   | 66.5 ms: 1.06x faster                                                        |
| create_gc_cycles        | 1.65 ms                                                                   | 1.56 ms: 1.05x faster                                                        |
| regex_v8                | 24.4 ms                                                                   | 23.2 ms: 1.05x faster                                                        |
| tornado_http            | 125 ms                                                                    | 119 ms: 1.05x faster                                                         |
| coroutines              | 29.5 ms                                                                   | 28.2 ms: 1.05x faster                                                        |
| gunicorn                | 936 us                                                                    | 895 us: 1.05x faster                                                         |
| chaos                   | 76.2 ms                                                                   | 73.0 ms: 1.04x faster                                                        |
| async_tree_memoization  | 639 ms                                                                    | 616 ms: 1.04x faster                                                         |
| 2to3                    | 289 ms                                                                    | 280 ms: 1.03x faster                                                         |
| hexiom                  | 7.00 ms                                                                   | 6.78 ms: 1.03x faster                                                        |
| docutils                | 2.86 sec                                                                  | 2.77 sec: 1.03x faster                                                       |
| dulwich_log             | 69.1 ms                                                                   | 67.1 ms: 1.03x faster                                                        |
| regex_compile           | 154 ms                                                                    | 149 ms: 1.03x faster                                                         |
| nbody                   | 92.1 ms                                                                   | 89.6 ms: 1.03x faster                                                        |
| float                   | 75.7 ms                                                                   | 73.9 ms: 1.03x faster                                                        |
| async_tree_none         | 529 ms                                                                    | 517 ms: 1.02x faster                                                         |
| pycparser               | 1.30 sec                                                                  | 1.27 sec: 1.02x faster                                                       |
| async_tree_io           | 1.18 sec                                                                  | 1.16 sec: 1.02x faster                                                       |
| sqlglot_normalize       | 122 ms                                                                    | 120 ms: 1.02x faster                                                         |
| pathlib                 | 19.2 ms                                                                   | 18.8 ms: 1.02x faster                                                        |
| logging_silent          | 103 ns                                                                    | 101 ns: 1.02x faster                                                         |
| pickle                  | 9.92 us                                                                   | 9.77 us: 1.02x faster                                                        |
| crypto_pyaes            | 85.0 ms                                                                   | 83.7 ms: 1.01x faster                                                        |
| xml_etree_iterparse     | 106 ms                                                                    | 104 ms: 1.01x faster                                                         |
| pprint_pformat          | 1.60 sec                                                                  | 1.58 sec: 1.01x faster                                                       |
| sqlglot_optimize        | 58.6 ms                                                                   | 57.9 ms: 1.01x faster                                                        |
| asyncio_tcp             | 752 ms                                                                    | 745 ms: 1.01x faster                                                         |
| meteor_contest          | 129 ms                                                                    | 128 ms: 1.01x faster                                                         |
| sympy_expand            | 547 ms                                                                    | 543 ms: 1.01x faster                                                         |
| coverage                | 86.0 ms                                                                   | 85.4 ms: 1.01x faster                                                        |
| mdp                     | 2.73 sec                                                                  | 2.73 sec: 1.00x slower                                                       |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 758 ms: 1.01x slower                                                         |
| raytrace                | 303 ms                                                                    | 305 ms: 1.01x slower                                                         |
| python_startup          | 10.7 ms                                                                   | 10.8 ms: 1.01x slower                                                        |
| xml_etree_generate      | 79.1 ms                                                                   | 79.8 ms: 1.01x slower                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.5 ms: 1.01x slower                                                        |
| django_template         | 39.6 ms                                                                   | 40.1 ms: 1.01x slower                                                        |
| sympy_sum               | 182 ms                                                                    | 185 ms: 1.01x slower                                                         |
| sqlglot_parse           | 1.53 ms                                                                   | 1.55 ms: 1.01x slower                                                        |
| python_startup_no_site  | 7.73 ms                                                                   | 7.85 ms: 1.02x slower                                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.36 ms: 1.02x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 3.84 us: 1.02x slower                                                        |
| regex_dna               | 225 ms                                                                    | 229 ms: 1.02x slower                                                         |
| pickle_dict             | 31.1 us                                                                   | 31.7 us: 1.02x slower                                                        |
| chameleon               | 7.50 ms                                                                   | 7.65 ms: 1.02x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 282 ms: 1.02x slower                                                         |
| go                      | 158 ms                                                                    | 162 ms: 1.02x slower                                                         |
| sqlglot_transpile       | 1.88 ms                                                                   | 1.92 ms: 1.02x slower                                                        |
| pyflate                 | 438 ms                                                                    | 447 ms: 1.02x slower                                                         |
| scimark_sor             | 109 ms                                                                    | 112 ms: 1.02x slower                                                         |
| sqlite_synth            | 2.49 us                                                                   | 2.56 us: 1.03x slower                                                        |
| unpickle                | 13.0 us                                                                   | 13.5 us: 1.04x slower                                                        |
| spectral_norm           | 95.1 ms                                                                   | 98.7 ms: 1.04x slower                                                        |
| logging_simple          | 6.95 us                                                                   | 7.24 us: 1.04x slower                                                        |
| async_generators        | 318 ms                                                                    | 332 ms: 1.04x slower                                                         |
| deepcopy_memo           | 37.0 us                                                                   | 38.8 us: 1.05x slower                                                        |
| deepcopy_reduce         | 3.39 us                                                                   | 3.59 us: 1.06x slower                                                        |
| scimark_monte_carlo     | 67.8 ms                                                                   | 72.0 ms: 1.06x slower                                                        |
| deepcopy                | 384 us                                                                    | 415 us: 1.08x slower                                                         |
| comprehensions          | 24.7 us                                                                   | 26.8 us: 1.09x slower                                                        |
| generators              | 56.0 ms                                                                   | 61.1 ms: 1.09x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.02x faster                                                                 |

Benchmark hidden because not significant (15): bench_thread_pool, nqueens, unpack_sequence, dask, thrift, richards, telco, logging_format, pprint_safe_repr, xml_etree_process, pidigits, pickle_pure_python, sympy_str, unpickle_list, bench_mp_pool
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
