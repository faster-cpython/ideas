
# Results vs. 3.11.0

- fork: python
- ref: 702a5bc4637c82dc011e
- machine: windows-amd64
- commit hash: 702a5bc
- commit date: 2022-12-19
- overall geometric mean: 1.06x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 5.15 ms                                                                  | 4.63 ms: 1.11x faster                                                       |
| html5lib       | 38.5 ms                                                                  | 35.6 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 63.8 ms: 1.11x faster                                                       |
| float          | 53.3 ms                                                                  | 50.3 ms: 1.06x faster                                                       |
| pidigits       | 147 ms                                                                   | 146 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.52 ms: 1.08x faster                                                       |
| regex_compile  | 89.7 ms                                                                  | 85.6 ms: 1.05x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.1 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.48 ms: 1.41x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 128 us: 1.17x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 183 us: 1.11x faster                                                        |
| unpickle_list        | 2.80 us                                                                  | 2.62 us: 1.07x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 50.0 ms: 1.05x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.5 ms: 1.03x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 90.6 ms: 1.02x faster                                                       |
| json_loads           | 13.5 us                                                                  | 13.4 us: 1.01x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.0 us: 1.02x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.79 us: 1.03x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 64.5 ms: 1.04x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.99 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                                       |
| python_startup         | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.3 ms: 1.20x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.31 ms: 1.14x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 34.2 ms: 1.11x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.8 ms: 1.10x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.14x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 29.5 ns: 1.46x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.48 ms: 1.41x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 486 ms: 1.39x faster                                                        |
| mypy2                   | 276 ms                                                                   | 223 ms: 1.24x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 2.18 ms: 1.23x faster                                                       |
| richards                | 32.1 ms                                                                  | 26.4 ms: 1.21x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 14.3 ms: 1.20x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 59.1 ns: 1.20x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 61.3 ms: 1.17x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 128 us: 1.17x faster                                                        |
| deepcopy_memo           | 25.3 us                                                                  | 21.7 us: 1.17x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.31 ms: 1.14x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.80 ms: 1.14x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 40.1 ms: 1.14x faster                                                       |
| deepcopy                | 240 us                                                                   | 215 us: 1.12x faster                                                        |
| chameleon               | 5.15 ms                                                                  | 4.63 ms: 1.11x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 69.9 ms: 1.11x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 34.2 ms: 1.11x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.37 ms: 1.11x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 63.8 ms: 1.11x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 183 us: 1.11x faster                                                        |
| pprint_pformat          | 1.05 sec                                                                 | 953 ms: 1.10x faster                                                        |
| go                      | 97.5 ms                                                                  | 88.8 ms: 1.10x faster                                                       |
| django_template         | 23.9 ms                                                                  | 21.8 ms: 1.10x faster                                                       |
| fannkuch                | 255 ms                                                                   | 233 ms: 1.09x faster                                                        |
| pprint_safe_repr        | 512 ms                                                                   | 469 ms: 1.09x faster                                                        |
| scimark_lu              | 62.8 ms                                                                  | 57.7 ms: 1.09x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 60.1 ms: 1.08x faster                                                       |
| raytrace                | 206 ms                                                                   | 190 ms: 1.08x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.55 sec: 1.08x faster                                                      |
| html5lib                | 38.5 ms                                                                  | 35.6 ms: 1.08x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 4.13 ms: 1.08x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.52 ms: 1.08x faster                                                       |
| pyflate                 | 302 ms                                                                   | 281 ms: 1.07x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.92 us: 1.07x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.62 us: 1.07x faster                                                       |
| float                   | 53.3 ms                                                                  | 50.3 ms: 1.06x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.23 us: 1.06x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 85.6 ms: 1.05x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 50.0 ms: 1.05x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.82 us: 1.05x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 286 ms: 1.04x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 182 ms: 1.04x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 42.0 ms: 1.04x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 900 us: 1.03x faster                                                        |
| regex_v8                | 13.5 ms                                                                  | 13.1 ms: 1.03x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 46.8 ms: 1.03x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 35.5 ms: 1.03x faster                                                       |
| thrift                  | 487 us                                                                   | 473 us: 1.03x faster                                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 33.5 ms: 1.03x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.3 ms: 1.03x faster                                                       |
| sympy_str               | 184 ms                                                                   | 179 ms: 1.03x faster                                                        |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 499 ms: 1.03x faster                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.10 ms: 1.03x faster                                                       |
| coverage                | 55.3 ms                                                                  | 54.0 ms: 1.02x faster                                                       |
| dask                    | 267 ms                                                                   | 261 ms: 1.02x faster                                                        |
| scimark_fft             | 183 ms                                                                   | 179 ms: 1.02x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 46.5 ms: 1.02x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.86 ms: 1.02x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 73.1 ms: 1.02x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 90.6 ms: 1.02x faster                                                       |
| pycparser               | 686 ms                                                                   | 675 ms: 1.02x faster                                                        |
| json_loads              | 13.5 us                                                                  | 13.4 us: 1.01x faster                                                       |
| pidigits                | 147 ms                                                                   | 146 ms: 1.00x faster                                                        |
| async_generators        | 180 ms                                                                   | 181 ms: 1.01x slower                                                        |
| sympy_sum               | 98.9 ms                                                                  | 99.7 ms: 1.01x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 677 us: 1.02x slower                                                        |
| pickle_dict             | 18.6 us                                                                  | 19.0 us: 1.02x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 15.1 ms: 1.02x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                       |
| async_tree_memoization  | 374 ms                                                                   | 386 ms: 1.03x slower                                                        |
| pickle_list             | 2.70 us                                                                  | 2.79 us: 1.03x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 63.2 ms: 1.03x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 75.7 ms: 1.04x slower                                                       |
| comprehensions          | 15.4 us                                                                  | 16.0 us: 1.04x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 64.5 ms: 1.04x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.48 ms: 1.05x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.78 us: 1.06x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 334 ms: 1.07x slower                                                        |
| pickle                  | 6.47 us                                                                  | 6.99 us: 1.08x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 807 ms: 1.08x slower                                                        |
| generators              | 33.5 ms                                                                  | 38.7 ms: 1.15x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (5): docutils, bench_thread_pool, unpickle, 2to3, regex_dna
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
