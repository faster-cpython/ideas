
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 30a306c
- commit date: 2023-03-25
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 198 ms: 1.03x faster                                        |
| chameleon      | 5.15 ms                                                                  | 4.57 ms: 1.13x faster                                       |
| docutils       | 1.59 sec                                                                 | 1.52 sec: 1.05x faster                                      |
| html5lib       | 38.5 ms                                                                  | 35.5 ms: 1.08x faster                                       |
| tornado_http   | 91.8 ms                                                                  | 87.7 ms: 1.05x faster                                       |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 56.6 ms: 1.25x faster                                       |
| float          | 53.3 ms                                                                  | 48.6 ms: 1.10x faster                                       |
| pidigits       | 147 ms                                                                   | 145 ms: 1.01x faster                                        |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 82.3 ms: 1.09x faster                                       |
| regex_v8       | 13.5 ms                                                                  | 13.6 ms: 1.01x slower                                       |
| regex_dna      | 115 ms                                                                   | 119 ms: 1.04x slower                                        |
| regex_effbot   | 1.63 ms                                                                  | 1.77 ms: 1.08x slower                                       |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.58 ms: 1.38x faster                                       |
| unpickle_pure_python | 150 us                                                                   | 122 us: 1.22x faster                                        |
| pickle_pure_python   | 203 us                                                                   | 176 us: 1.16x faster                                        |
| unpickle_list        | 2.80 us                                                                  | 2.66 us: 1.05x faster                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.3 ms: 1.04x faster                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 89.5 ms: 1.03x faster                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 60.4 ms: 1.02x faster                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.7 ms: 1.01x faster                                       |
| json_loads           | 13.5 us                                                                  | 13.4 us: 1.01x faster                                       |
| pickle_dict          | 18.6 us                                                                  | 18.7 us: 1.01x slower                                       |
| pickle_list          | 2.70 us                                                                  | 2.91 us: 1.08x slower                                       |
| pickle               | 6.47 us                                                                  | 7.04 us: 1.09x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.6 ms: 1.26x faster                                       |
| genshi_xml      | 38.0 ms                                                                  | 30.3 ms: 1.25x faster                                       |
| django_template | 23.9 ms                                                                  | 20.6 ms: 1.16x faster                                       |
| mako            | 7.20 ms                                                                  | 6.32 ms: 1.14x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.20x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| generators              | 33.5 ms                                                                  | 21.0 ms: 1.60x faster                                       |
| unpack_sequence         | 43.1 ns                                                                  | 27.2 ns: 1.59x faster                                       |
| asyncio_tcp             | 674 ms                                                                   | 467 ms: 1.44x faster                                        |
| json_dumps              | 7.71 ms                                                                  | 5.58 ms: 1.38x faster                                       |
| deltablue               | 2.68 ms                                                                  | 1.94 ms: 1.38x faster                                       |
| logging_silent          | 71.0 ns                                                                  | 54.4 ns: 1.31x faster                                       |
| mypy2                   | 276 ms                                                                   | 212 ms: 1.31x faster                                        |
| richards                | 32.1 ms                                                                  | 25.1 ms: 1.28x faster                                       |
| genshi_text             | 17.3 ms                                                                  | 13.6 ms: 1.26x faster                                       |
| genshi_xml              | 38.0 ms                                                                  | 30.3 ms: 1.25x faster                                       |
| nbody                   | 70.9 ms                                                                  | 56.6 ms: 1.25x faster                                       |
| mdp                     | 1.67 sec                                                                 | 1.37 sec: 1.23x faster                                      |
| unpickle_pure_python    | 150 us                                                                   | 122 us: 1.22x faster                                        |
| raytrace                | 206 ms                                                                   | 171 ms: 1.21x faster                                        |
| scimark_lu              | 62.8 ms                                                                  | 52.6 ms: 1.20x faster                                       |
| go                      | 97.5 ms                                                                  | 82.6 ms: 1.18x faster                                       |
| deepcopy_memo           | 25.3 us                                                                  | 21.5 us: 1.18x faster                                       |
| chaos                   | 47.3 ms                                                                  | 40.2 ms: 1.18x faster                                       |
| hexiom                  | 4.46 ms                                                                  | 3.80 ms: 1.17x faster                                       |
| json                    | 3.20 ms                                                                  | 2.75 ms: 1.17x faster                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.25 ms: 1.17x faster                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.5 ms: 1.16x faster                                       |
| django_template         | 23.9 ms                                                                  | 20.6 ms: 1.16x faster                                       |
| pickle_pure_python      | 203 us                                                                   | 176 us: 1.16x faster                                        |
| nqueens                 | 65.1 ms                                                                  | 56.7 ms: 1.15x faster                                       |
| mako                    | 7.20 ms                                                                  | 6.32 ms: 1.14x faster                                       |
| deepcopy                | 240 us                                                                   | 212 us: 1.13x faster                                        |
| chameleon               | 5.15 ms                                                                  | 4.57 ms: 1.13x faster                                       |
| fannkuch                | 255 ms                                                                   | 227 ms: 1.13x faster                                        |
| logging_format          | 7.13 us                                                                  | 6.35 us: 1.12x faster                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.83 us: 1.12x faster                                       |
| pprint_safe_repr        | 512 ms                                                                   | 458 ms: 1.12x faster                                        |
| pprint_pformat          | 1.05 sec                                                                 | 941 ms: 1.12x faster                                        |
| scimark_fft             | 183 ms                                                                   | 165 ms: 1.11x faster                                        |
| sqlglot_normalize       | 189 ms                                                                   | 171 ms: 1.11x faster                                        |
| logging_simple          | 6.60 us                                                                  | 5.99 us: 1.10x faster                                       |
| spectral_norm           | 71.8 ms                                                                  | 65.4 ms: 1.10x faster                                       |
| float                   | 53.3 ms                                                                  | 48.6 ms: 1.10x faster                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.5 ms: 1.09x faster                                       |
| regex_compile           | 89.7 ms                                                                  | 82.3 ms: 1.09x faster                                       |
| html5lib                | 38.5 ms                                                                  | 35.5 ms: 1.08x faster                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 475 ms: 1.08x faster                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.05 ms: 1.08x faster                                       |
| sqlglot_parse           | 929 us                                                                   | 864 us: 1.08x faster                                        |
| pyflate                 | 302 ms                                                                   | 281 ms: 1.07x faster                                        |
| crypto_pyaes            | 48.3 ms                                                                  | 45.0 ms: 1.07x faster                                       |
| coverage                | 55.3 ms                                                                  | 51.5 ms: 1.07x faster                                       |
| sympy_expand            | 298 ms                                                                   | 278 ms: 1.07x faster                                        |
| pycparser               | 686 ms                                                                   | 641 ms: 1.07x faster                                        |
| sympy_integrate         | 13.7 ms                                                                  | 12.8 ms: 1.06x faster                                       |
| async_tree_none         | 313 ms                                                                   | 295 ms: 1.06x faster                                        |
| sympy_str               | 184 ms                                                                   | 174 ms: 1.06x faster                                        |
| thrift                  | 487 us                                                                   | 461 us: 1.06x faster                                        |
| async_tree_memoization  | 374 ms                                                                   | 355 ms: 1.05x faster                                        |
| docutils                | 1.59 sec                                                                 | 1.52 sec: 1.05x faster                                      |
| unpickle_list           | 2.80 us                                                                  | 2.66 us: 1.05x faster                                       |
| meteor_contest          | 74.4 ms                                                                  | 70.9 ms: 1.05x faster                                       |
| tornado_http            | 91.8 ms                                                                  | 87.7 ms: 1.05x faster                                       |
| xml_etree_process       | 36.6 ms                                                                  | 35.3 ms: 1.04x faster                                       |
| coroutines              | 14.8 ms                                                                  | 14.4 ms: 1.03x faster                                       |
| 2to3                    | 204 ms                                                                   | 198 ms: 1.03x faster                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 89.5 ms: 1.03x faster                                       |
| bench_thread_pool       | 856 us                                                                   | 833 us: 1.03x faster                                        |
| telco                   | 3.93 ms                                                                  | 3.83 ms: 1.03x faster                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 60.4 ms: 1.02x faster                                       |
| sympy_sum               | 98.9 ms                                                                  | 96.8 ms: 1.02x faster                                       |
| comprehensions          | 15.4 us                                                                  | 15.0 us: 1.02x faster                                       |
| async_tree_io           | 744 ms                                                                   | 731 ms: 1.02x faster                                        |
| scimark_sor             | 77.7 ms                                                                  | 76.4 ms: 1.02x faster                                       |
| pidigits                | 147 ms                                                                   | 145 ms: 1.01x faster                                        |
| dulwich_log             | 43.4 ms                                                                  | 43.0 ms: 1.01x faster                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 51.7 ms: 1.01x faster                                       |
| json_loads              | 13.5 us                                                                  | 13.4 us: 1.01x faster                                       |
| pickle_dict             | 18.6 us                                                                  | 18.7 us: 1.01x slower                                       |
| create_gc_cycles        | 666 us                                                                   | 671 us: 1.01x slower                                        |
| regex_v8                | 13.5 ms                                                                  | 13.6 ms: 1.01x slower                                       |
| python_startup          | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.7 ms: 1.02x slower                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.45 ms: 1.03x slower                                       |
| regex_dna               | 115 ms                                                                   | 119 ms: 1.04x slower                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 64.8 ms: 1.06x slower                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.78 us: 1.07x slower                                       |
| pickle_list             | 2.70 us                                                                  | 2.91 us: 1.08x slower                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.77 ms: 1.08x slower                                       |
| pickle                  | 6.47 us                                                                  | 7.04 us: 1.09x slower                                       |
| pathlib                 | 72.9 ms                                                                  | 84.2 ms: 1.15x slower                                       |
| async_generators        | 180 ms                                                                   | 213 ms: 1.18x slower                                        |
| dask                    | 267 ms                                                                   | 354 ms: 1.33x slower                                        |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
