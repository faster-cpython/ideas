
# Results vs. 3.11.0

- fork: python
- ref: c03e05c2e72f3ea5e797
- machine: windows-amd64
- commit hash: c03e05c
- commit date: 2022-11-09
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 209 ms: 1.03x slower                                                        |
| chameleon      | 5.15 ms                                                                  | 5.20 ms: 1.01x slower                                                       |
| docutils       | 1.59 sec                                                                 | 1.63 sec: 1.02x slower                                                      |
| html5lib       | 38.5 ms                                                                  | 39.9 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| float          | 53.3 ms                                                                  | 55.8 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.56 ms: 1.05x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.1 ms: 1.03x faster                                                       |
| regex_dna      | 115 ms                                                                   | 118 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.54 ms: 1.39x faster                                                       |
| json_loads           | 13.5 us                                                                  | 13.0 us: 1.04x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 89.7 ms: 1.03x faster                                                       |
| unpickle             | 8.01 us                                                                  | 8.17 us: 1.02x slower                                                       |
| pickle_pure_python   | 203 us                                                                   | 208 us: 1.02x slower                                                        |
| pickle_list          | 2.70 us                                                                  | 2.76 us: 1.02x slower                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.1 us: 1.03x slower                                                       |
| unpickle_pure_python | 150 us                                                                   | 154 us: 1.03x slower                                                        |
| xml_etree_generate   | 52.3 ms                                                                  | 53.9 ms: 1.03x slower                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 37.8 ms: 1.03x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 65.2 ms: 1.06x slower                                                       |
| pickle               | 6.47 us                                                                  | 7.06 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 19.3 ms: 1.05x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 16.4 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 16.9 ms: 1.02x faster                                                       |
| django_template | 23.9 ms                                                                  | 24.4 ms: 1.02x slower                                                       |
| Geometric mean  | (ref)                                                                    | 1.01x slower                                                                |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 7.71 ms                                                                  | 5.54 ms: 1.39x faster                                                       |
| mypy2                   | 276 ms                                                                   | 224 ms: 1.23x faster                                                        |
| json                    | 3.20 ms                                                                  | 2.74 ms: 1.17x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 39.2 ns: 1.10x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.43 ms: 1.08x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.56 ms: 1.05x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.6 ms: 1.04x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.0 us: 1.04x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.59 ms: 1.04x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 72.0 ms: 1.03x faster                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.1 ms: 1.03x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 89.7 ms: 1.03x faster                                                       |
| richards                | 32.1 ms                                                                  | 31.5 ms: 1.02x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 16.9 ms: 1.02x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 70.5 ms: 1.02x faster                                                       |
| raytrace                | 206 ms                                                                   | 203 ms: 1.02x faster                                                        |
| pprint_safe_repr        | 512 ms                                                                   | 506 ms: 1.01x faster                                                        |
| coverage                | 55.3 ms                                                                  | 55.0 ms: 1.01x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.95 ms: 1.01x slower                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 48.6 ms: 1.01x slower                                                       |
| chameleon               | 5.15 ms                                                                  | 5.20 ms: 1.01x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 672 us: 1.01x slower                                                        |
| deepcopy_memo           | 25.3 us                                                                  | 25.7 us: 1.01x slower                                                       |
| logging_silent          | 71.0 ns                                                                  | 72.0 ns: 1.01x slower                                                       |
| bench_thread_pool       | 856 us                                                                   | 868 us: 1.01x slower                                                        |
| pathlib                 | 72.9 ms                                                                  | 74.2 ms: 1.02x slower                                                       |
| mdp                     | 1.67 sec                                                                 | 1.70 sec: 1.02x slower                                                      |
| sympy_str               | 184 ms                                                                   | 188 ms: 1.02x slower                                                        |
| unpickle                | 8.01 us                                                                  | 8.17 us: 1.02x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 15.1 ms: 1.02x slower                                                       |
| pickle_pure_python      | 203 us                                                                   | 208 us: 1.02x slower                                                        |
| thrift                  | 487 us                                                                   | 497 us: 1.02x slower                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.16 ms: 1.02x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.76 us: 1.02x slower                                                       |
| django_template         | 23.9 ms                                                                  | 24.4 ms: 1.02x slower                                                       |
| regex_dna               | 115 ms                                                                   | 118 ms: 1.02x slower                                                        |
| docutils                | 1.59 sec                                                                 | 1.63 sec: 1.02x slower                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 2.11 us: 1.03x slower                                                       |
| sympy_sum               | 98.9 ms                                                                  | 101 ms: 1.03x slower                                                        |
| 2to3                    | 204 ms                                                                   | 209 ms: 1.03x slower                                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 35.4 ms: 1.03x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 19.1 us: 1.03x slower                                                       |
| unpickle_pure_python    | 150 us                                                                   | 154 us: 1.03x slower                                                        |
| generators              | 33.5 ms                                                                  | 34.5 ms: 1.03x slower                                                       |
| sqlglot_parse           | 929 us                                                                   | 956 us: 1.03x slower                                                        |
| pyflate                 | 302 ms                                                                   | 311 ms: 1.03x slower                                                        |
| nqueens                 | 65.1 ms                                                                  | 67.1 ms: 1.03x slower                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 53.9 ms: 1.03x slower                                                       |
| pidigits                | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| scimark_sor             | 77.7 ms                                                                  | 80.1 ms: 1.03x slower                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 37.8 ms: 1.03x slower                                                       |
| scimark_fft             | 183 ms                                                                   | 189 ms: 1.04x slower                                                        |
| gc_traversal            | 1.40 ms                                                                  | 1.45 ms: 1.04x slower                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 196 ms: 1.04x slower                                                        |
| pycparser               | 686 ms                                                                   | 711 ms: 1.04x slower                                                        |
| scimark_monte_carlo     | 45.8 ms                                                                  | 47.5 ms: 1.04x slower                                                       |
| html5lib                | 38.5 ms                                                                  | 39.9 ms: 1.04x slower                                                       |
| chaos                   | 47.3 ms                                                                  | 49.1 ms: 1.04x slower                                                       |
| logging_format          | 7.13 us                                                                  | 7.41 us: 1.04x slower                                                       |
| async_generators        | 180 ms                                                                   | 188 ms: 1.04x slower                                                        |
| float                   | 53.3 ms                                                                  | 55.8 ms: 1.05x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 19.3 ms: 1.05x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 65.2 ms: 1.06x slower                                                       |
| fannkuch                | 255 ms                                                                   | 270 ms: 1.06x slower                                                        |
| deepcopy                | 240 us                                                                   | 255 us: 1.07x slower                                                        |
| logging_simple          | 6.60 us                                                                  | 7.05 us: 1.07x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 16.4 ms: 1.07x slower                                                       |
| async_tree_memoization  | 374 ms                                                                   | 402 ms: 1.07x slower                                                        |
| go                      | 97.5 ms                                                                  | 105 ms: 1.07x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.80 us: 1.08x slower                                                       |
| scimark_lu              | 62.8 ms                                                                  | 67.9 ms: 1.08x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 338 ms: 1.08x slower                                                        |
| pickle                  | 6.47 us                                                                  | 7.06 us: 1.09x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 67.3 ms: 1.10x slower                                                       |
| hexiom                  | 4.46 ms                                                                  | 4.95 ms: 1.11x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 827 ms: 1.11x slower                                                        |
| comprehensions          | 15.4 us                                                                  | 17.1 us: 1.11x slower                                                       |
| asyncio_tcp             | 674 ms                                                                   | 753 ms: 1.12x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.01x slower                                                                |

Benchmark hidden because not significant (11): unpickle_list, sympy_expand, mako, sympy_integrate, regex_compile, pprint_pformat, nbody, tornado_http, async_tree_cpu_io_mixed, dask, genshi_xml
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
