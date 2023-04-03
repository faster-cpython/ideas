
# Results vs. 3.11.0

- fork: python
- ref: 010576c6ea7e687cf2cb
- machine: windows-amd64
- commit hash: 010576c
- commit date: 2023-01-13
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.60 ms: 1.12x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.52 sec: 1.05x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 33.5 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 61.2 ms: 1.16x faster                                                       |
| float          | 53.3 ms                                                                  | 49.3 ms: 1.08x faster                                                       |
| pidigits       | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 80.4 ms: 1.12x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.0 ms: 1.04x slower                                                       |
| regex_dna      | 115 ms                                                                   | 122 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.26 ms: 1.47x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 122 us: 1.23x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 176 us: 1.16x faster                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 34.1 ms: 1.07x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 49.5 ms: 1.06x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.65 us: 1.06x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 90.3 ms: 1.02x faster                                                       |
| pickle_list          | 2.70 us                                                                  | 2.79 us: 1.03x slower                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.3 us: 1.03x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 64.0 ms: 1.04x slower                                                       |
| unpickle             | 8.01 us                                                                  | 8.48 us: 1.06x slower                                                       |
| json_loads           | 13.5 us                                                                  | 14.4 us: 1.06x slower                                                       |
| pickle               | 6.47 us                                                                  | 7.18 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.8 ms: 1.25x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 30.8 ms: 1.24x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.07 ms: 1.19x faster                                                       |
| django_template | 23.9 ms                                                                  | 20.7 ms: 1.15x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.20x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4+-010576c |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 26.4 ns: 1.63x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.26 ms: 1.47x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 484 ms: 1.39x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 1.96 ms: 1.37x faster                                                       |
| richards                | 32.1 ms                                                                  | 24.1 ms: 1.33x faster                                                       |
| mypy2                   | 276 ms                                                                   | 219 ms: 1.26x faster                                                        |
| logging_silent          | 71.0 ns                                                                  | 56.7 ns: 1.25x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 13.8 ms: 1.25x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 30.8 ms: 1.24x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 122 us: 1.23x faster                                                        |
| deepcopy_memo           | 25.3 us                                                                  | 20.7 us: 1.23x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 3.73 ms: 1.19x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.07 ms: 1.19x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 66.0 ms: 1.18x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.0 ms: 1.17x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 61.2 ms: 1.17x faster                                                       |
| deepcopy                | 240 us                                                                   | 206 us: 1.17x faster                                                        |
| go                      | 97.5 ms                                                                  | 83.6 ms: 1.17x faster                                                       |
| raytrace                | 206 ms                                                                   | 177 ms: 1.16x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.26 ms: 1.16x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 61.2 ms: 1.16x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 176 us: 1.16x faster                                                        |
| django_template         | 23.9 ms                                                                  | 20.7 ms: 1.15x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 56.6 ms: 1.15x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 33.5 ms: 1.15x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.81 ms: 1.14x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.60 ms: 1.12x faster                                                       |
| fannkuch                | 255 ms                                                                   | 228 ms: 1.12x faster                                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 30.9 ms: 1.12x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.38 us: 1.12x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 80.4 ms: 1.12x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 459 ms: 1.11x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.86 us: 1.11x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 952 ms: 1.10x faster                                                        |
| scimark_lu              | 62.8 ms                                                                  | 57.3 ms: 1.10x faster                                                       |
| pyflate                 | 302 ms                                                                   | 276 ms: 1.09x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 173 ms: 1.09x faster                                                        |
| scimark_fft             | 183 ms                                                                   | 169 ms: 1.08x faster                                                        |
| sympy_expand            | 298 ms                                                                   | 276 ms: 1.08x faster                                                        |
| float                   | 53.3 ms                                                                  | 49.3 ms: 1.08x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 43.8 ms: 1.08x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.12 us: 1.08x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.56 sec: 1.07x faster                                                      |
| pycparser               | 686 ms                                                                   | 640 ms: 1.07x faster                                                        |
| xml_etree_process       | 36.6 ms                                                                  | 34.1 ms: 1.07x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.06 ms: 1.07x faster                                                       |
| sympy_str               | 184 ms                                                                   | 173 ms: 1.07x faster                                                        |
| sqlglot_parse           | 929 us                                                                   | 874 us: 1.06x faster                                                        |
| telco                   | 3.93 ms                                                                  | 3.69 ms: 1.06x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 49.5 ms: 1.06x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.65 us: 1.06x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.9 ms: 1.06x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 46.0 ms: 1.05x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 487 ms: 1.05x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.52 sec: 1.05x faster                                                      |
| sympy_sum               | 98.9 ms                                                                  | 94.9 ms: 1.04x faster                                                       |
| coverage                | 55.3 ms                                                                  | 53.2 ms: 1.04x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.9 ms: 1.04x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 71.9 ms: 1.03x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.3 ms: 1.03x faster                                                       |
| async_tree_memoization  | 374 ms                                                                   | 363 ms: 1.03x faster                                                        |
| async_generators        | 180 ms                                                                   | 175 ms: 1.03x faster                                                        |
| dask                    | 267 ms                                                                   | 260 ms: 1.03x faster                                                        |
| thrift                  | 487 us                                                                   | 475 us: 1.02x faster                                                        |
| regex_effbot            | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 90.3 ms: 1.02x faster                                                       |
| bench_thread_pool       | 856 us                                                                   | 841 us: 1.02x faster                                                        |
| 2to3                    | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| python_startup          | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 320 ms: 1.02x slower                                                        |
| python_startup_no_site  | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 62.7 ms: 1.02x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 75.0 ms: 1.03x slower                                                       |
| pidigits                | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| generators              | 33.5 ms                                                                  | 34.6 ms: 1.03x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.79 us: 1.03x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 19.3 us: 1.03x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 64.0 ms: 1.04x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 14.0 ms: 1.04x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 781 ms: 1.05x slower                                                        |
| regex_dna               | 115 ms                                                                   | 122 ms: 1.06x slower                                                        |
| unpickle                | 8.01 us                                                                  | 8.48 us: 1.06x slower                                                       |
| json_loads              | 13.5 us                                                                  | 14.4 us: 1.06x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.51 ms: 1.07x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.80 us: 1.07x slower                                                       |
| pickle                  | 6.47 us                                                                  | 7.18 us: 1.11x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (3): tornado_http, comprehensions, create_gc_cycles
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
