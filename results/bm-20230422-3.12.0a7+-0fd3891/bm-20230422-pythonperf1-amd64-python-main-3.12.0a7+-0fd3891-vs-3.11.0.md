
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 0fd3891
- commit date: 2023-04-22
- overall geometric mean: 1.06x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 207 ms: 1.02x slower                                        |
| chameleon      | 5.15 ms                                                                  | 4.93 ms: 1.04x faster                                       |
| docutils       | 1.59 sec                                                                 | 1.54 sec: 1.03x faster                                      |
| html5lib       | 38.5 ms                                                                  | 36.6 ms: 1.05x faster                                       |
| tornado_http   | 91.8 ms                                                                  | 90.0 ms: 1.02x faster                                       |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 53.3 ms                                                                  | 51.4 ms: 1.04x faster                                       |
| pidigits       | 147 ms                                                                   | 148 ms: 1.01x slower                                        |
| nbody          | 70.9 ms                                                                  | 73.1 ms: 1.03x slower                                       |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.51 ms: 1.08x faster                                       |
| regex_compile  | 89.7 ms                                                                  | 83.8 ms: 1.07x faster                                       |
| regex_v8       | 13.5 ms                                                                  | 13.0 ms: 1.03x faster                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.41 ms: 1.43x faster                                       |
| unpickle_pure_python | 150 us                                                                   | 135 us: 1.11x faster                                        |
| pickle_pure_python   | 203 us                                                                   | 189 us: 1.08x faster                                        |
| unpickle_list        | 2.80 us                                                                  | 2.63 us: 1.07x faster                                       |
| json_loads           | 13.5 us                                                                  | 12.8 us: 1.06x faster                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 87.5 ms: 1.05x faster                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 60.0 ms: 1.03x faster                                       |
| pickle_dict          | 18.6 us                                                                  | 18.2 us: 1.03x faster                                       |
| xml_etree_process    | 36.6 ms                                                                  | 37.4 ms: 1.02x slower                                       |
| pickle_list          | 2.70 us                                                                  | 2.81 us: 1.04x slower                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 54.4 ms: 1.04x slower                                       |
| pickle               | 6.47 us                                                                  | 6.77 us: 1.05x slower                                       |
| unpickle             | 8.01 us                                                                  | 8.46 us: 1.06x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.04x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                       |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 32.5 ms: 1.17x faster                                       |
| genshi_text     | 17.3 ms                                                                  | 15.1 ms: 1.14x faster                                       |
| django_template | 23.9 ms                                                                  | 21.8 ms: 1.09x faster                                       |
| mako            | 7.20 ms                                                                  | 6.66 ms: 1.08x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.12x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| generators              | 33.5 ms                                                                  | 21.7 ms: 1.55x faster                                       |
| asyncio_tcp             | 674 ms                                                                   | 470 ms: 1.43x faster                                        |
| json_dumps              | 7.71 ms                                                                  | 5.41 ms: 1.43x faster                                       |
| mypy2                   | 276 ms                                                                   | 215 ms: 1.28x faster                                        |
| deltablue               | 2.68 ms                                                                  | 2.16 ms: 1.24x faster                                       |
| logging_silent          | 71.0 ns                                                                  | 59.5 ns: 1.19x faster                                       |
| richards                | 32.1 ms                                                                  | 27.1 ms: 1.18x faster                                       |
| sqlglot_parse           | 929 us                                                                   | 789 us: 1.18x faster                                        |
| genshi_xml              | 38.0 ms                                                                  | 32.5 ms: 1.17x faster                                       |
| spectral_norm           | 71.8 ms                                                                  | 61.6 ms: 1.17x faster                                       |
| mdp                     | 1.67 sec                                                                 | 1.44 sec: 1.16x faster                                      |
| scimark_lu              | 62.8 ms                                                                  | 54.2 ms: 1.16x faster                                       |
| unpack_sequence         | 43.1 ns                                                                  | 37.4 ns: 1.15x faster                                       |
| pylint                  | 319 ms                                                                   | 276 ms: 1.15x faster                                        |
| genshi_text             | 17.3 ms                                                                  | 15.1 ms: 1.14x faster                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 991 us: 1.14x faster                                        |
| nqueens                 | 65.1 ms                                                                  | 57.3 ms: 1.14x faster                                       |
| json                    | 3.20 ms                                                                  | 2.82 ms: 1.14x faster                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.33 ms: 1.13x faster                                       |
| go                      | 97.5 ms                                                                  | 87.4 ms: 1.12x faster                                       |
| raytrace                | 206 ms                                                                   | 185 ms: 1.11x faster                                        |
| unpickle_pure_python    | 150 us                                                                   | 135 us: 1.11x faster                                        |
| deepcopy_memo           | 25.3 us                                                                  | 23.0 us: 1.10x faster                                       |
| coverage                | 55.3 ms                                                                  | 50.5 ms: 1.09x faster                                       |
| chaos                   | 47.3 ms                                                                  | 43.3 ms: 1.09x faster                                       |
| django_template         | 23.9 ms                                                                  | 21.8 ms: 1.09x faster                                       |
| hexiom                  | 4.46 ms                                                                  | 4.10 ms: 1.09x faster                                       |
| mako                    | 7.20 ms                                                                  | 6.66 ms: 1.08x faster                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.51 ms: 1.08x faster                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 474 ms: 1.08x faster                                        |
| sympy_str               | 184 ms                                                                   | 171 ms: 1.08x faster                                        |
| coroutines              | 14.8 ms                                                                  | 13.8 ms: 1.08x faster                                       |
| pickle_pure_python      | 203 us                                                                   | 189 us: 1.08x faster                                        |
| sqlglot_normalize       | 189 ms                                                                   | 176 ms: 1.07x faster                                        |
| sympy_expand            | 298 ms                                                                   | 278 ms: 1.07x faster                                        |
| scimark_monte_carlo     | 45.8 ms                                                                  | 42.7 ms: 1.07x faster                                       |
| regex_compile           | 89.7 ms                                                                  | 83.8 ms: 1.07x faster                                       |
| logging_format          | 7.13 us                                                                  | 6.67 us: 1.07x faster                                       |
| unpickle_list           | 2.80 us                                                                  | 2.63 us: 1.07x faster                                       |
| json_loads              | 13.5 us                                                                  | 12.8 us: 1.06x faster                                       |
| scimark_fft             | 183 ms                                                                   | 172 ms: 1.06x faster                                        |
| pyflate                 | 302 ms                                                                   | 286 ms: 1.06x faster                                        |
| logging_simple          | 6.60 us                                                                  | 6.25 us: 1.06x faster                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.6 ms: 1.06x faster                                       |
| pprint_pformat          | 1.05 sec                                                                 | 995 ms: 1.05x faster                                        |
| deepcopy                | 240 us                                                                   | 227 us: 1.05x faster                                        |
| bench_thread_pool       | 856 us                                                                   | 813 us: 1.05x faster                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 87.5 ms: 1.05x faster                                       |
| fannkuch                | 255 ms                                                                   | 243 ms: 1.05x faster                                        |
| async_tree_none         | 313 ms                                                                   | 298 ms: 1.05x faster                                        |
| dulwich_log             | 43.4 ms                                                                  | 41.3 ms: 1.05x faster                                       |
| html5lib                | 38.5 ms                                                                  | 36.6 ms: 1.05x faster                                       |
| async_tree_memoization  | 374 ms                                                                   | 357 ms: 1.05x faster                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.97 us: 1.05x faster                                       |
| chameleon               | 5.15 ms                                                                  | 4.93 ms: 1.04x faster                                       |
| pycparser               | 686 ms                                                                   | 658 ms: 1.04x faster                                        |
| pprint_safe_repr        | 512 ms                                                                   | 491 ms: 1.04x faster                                        |
| crypto_pyaes            | 48.3 ms                                                                  | 46.4 ms: 1.04x faster                                       |
| float                   | 53.3 ms                                                                  | 51.4 ms: 1.04x faster                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.2 ms: 1.03x faster                                       |
| regex_v8                | 13.5 ms                                                                  | 13.0 ms: 1.03x faster                                       |
| telco                   | 3.93 ms                                                                  | 3.80 ms: 1.03x faster                                       |
| docutils                | 1.59 sec                                                                 | 1.54 sec: 1.03x faster                                      |
| xml_etree_iterparse     | 61.8 ms                                                                  | 60.0 ms: 1.03x faster                                       |
| sympy_sum               | 98.9 ms                                                                  | 96.1 ms: 1.03x faster                                       |
| thrift                  | 487 us                                                                   | 474 us: 1.03x faster                                        |
| pickle_dict             | 18.6 us                                                                  | 18.2 us: 1.03x faster                                       |
| comprehensions          | 15.4 us                                                                  | 15.0 us: 1.02x faster                                       |
| tornado_http            | 91.8 ms                                                                  | 90.0 ms: 1.02x faster                                       |
| python_startup          | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                       |
| pidigits                | 147 ms                                                                   | 148 ms: 1.01x slower                                        |
| 2to3                    | 204 ms                                                                   | 207 ms: 1.02x slower                                        |
| create_gc_cycles        | 666 us                                                                   | 677 us: 1.02x slower                                        |
| xml_etree_process       | 36.6 ms                                                                  | 37.4 ms: 1.02x slower                                       |
| nbody                   | 70.9 ms                                                                  | 73.1 ms: 1.03x slower                                       |
| pickle_list             | 2.70 us                                                                  | 2.81 us: 1.04x slower                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 54.4 ms: 1.04x slower                                       |
| scimark_sor             | 77.7 ms                                                                  | 80.8 ms: 1.04x slower                                       |
| meteor_contest          | 74.4 ms                                                                  | 77.8 ms: 1.05x slower                                       |
| pickle                  | 6.47 us                                                                  | 6.77 us: 1.05x slower                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.47 ms: 1.05x slower                                       |
| unpickle                | 8.01 us                                                                  | 8.46 us: 1.06x slower                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.81 us: 1.08x slower                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 66.7 ms: 1.09x slower                                       |
| pathlib                 | 72.9 ms                                                                  | 82.4 ms: 1.13x slower                                       |
| async_generators        | 180 ms                                                                   | 216 ms: 1.20x slower                                        |
| dask                    | 267 ms                                                                   | 357 ms: 1.34x slower                                        |
| Geometric mean          | (ref)                                                                    | 1.06x faster                                                |

Benchmark hidden because not significant (3): regex_dna, python_startup_no_site, async_tree_io
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
