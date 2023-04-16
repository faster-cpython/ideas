
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 4fe1c4b
- commit date: 2023-04-15
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 198 ms: 1.03x faster                                        |
| chameleon      | 5.15 ms                                                                  | 4.67 ms: 1.10x faster                                       |
| docutils       | 1.59 sec                                                                 | 1.49 sec: 1.07x faster                                      |
| html5lib       | 38.5 ms                                                                  | 35.4 ms: 1.09x faster                                       |
| tornado_http   | 91.8 ms                                                                  | 85.4 ms: 1.08x faster                                       |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 57.8 ms: 1.23x faster                                       |
| float          | 53.3 ms                                                                  | 48.3 ms: 1.10x faster                                       |
| pidigits       | 147 ms                                                                   | 146 ms: 1.01x faster                                        |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 80.9 ms: 1.11x faster                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.56 ms: 1.05x faster                                       |
| regex_dna      | 115 ms                                                                   | 119 ms: 1.04x slower                                        |
| regex_v8       | 13.5 ms                                                                  | 14.0 ms: 1.04x slower                                       |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.35 ms: 1.44x faster                                       |
| unpickle_pure_python | 150 us                                                                   | 127 us: 1.18x faster                                        |
| pickle_pure_python   | 203 us                                                                   | 183 us: 1.11x faster                                        |
| json_loads           | 13.5 us                                                                  | 12.7 us: 1.07x faster                                       |
| unpickle_list        | 2.80 us                                                                  | 2.68 us: 1.04x faster                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 89.2 ms: 1.03x faster                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 60.1 ms: 1.03x faster                                       |
| xml_etree_process    | 36.6 ms                                                                  | 36.1 ms: 1.01x faster                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 52.7 ms: 1.01x slower                                       |
| pickle               | 6.47 us                                                                  | 6.68 us: 1.03x slower                                       |
| pickle_list          | 2.70 us                                                                  | 2.82 us: 1.04x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                |

Benchmark hidden because not significant (2): pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.1 ms: 1.01x faster                                       |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 31.5 ms: 1.21x faster                                       |
| genshi_text     | 17.3 ms                                                                  | 14.3 ms: 1.21x faster                                       |
| mako            | 7.20 ms                                                                  | 6.53 ms: 1.10x faster                                       |
| django_template | 23.9 ms                                                                  | 21.7 ms: 1.10x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.15x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230415-pythonperf1-amd64-python-main-3.12.0a7+-4fe1c4b |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| generators              | 33.5 ms                                                                  | 20.0 ms: 1.68x faster                                       |
| json_dumps              | 7.71 ms                                                                  | 5.35 ms: 1.44x faster                                       |
| asyncio_tcp             | 674 ms                                                                   | 471 ms: 1.43x faster                                        |
| mypy2                   | 276 ms                                                                   | 206 ms: 1.34x faster                                        |
| unpack_sequence         | 43.1 ns                                                                  | 32.8 ns: 1.31x faster                                       |
| deltablue               | 2.68 ms                                                                  | 2.15 ms: 1.24x faster                                       |
| richards                | 32.1 ms                                                                  | 25.9 ms: 1.24x faster                                       |
| sqlglot_parse           | 929 us                                                                   | 755 us: 1.23x faster                                        |
| mdp                     | 1.67 sec                                                                 | 1.37 sec: 1.23x faster                                      |
| nbody                   | 70.9 ms                                                                  | 57.8 ms: 1.23x faster                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 930 us: 1.22x faster                                        |
| genshi_xml              | 38.0 ms                                                                  | 31.5 ms: 1.21x faster                                       |
| genshi_text             | 17.3 ms                                                                  | 14.3 ms: 1.21x faster                                       |
| json                    | 3.20 ms                                                                  | 2.68 ms: 1.19x faster                                       |
| raytrace                | 206 ms                                                                   | 173 ms: 1.19x faster                                        |
| logging_silent          | 71.0 ns                                                                  | 59.7 ns: 1.19x faster                                       |
| spectral_norm           | 71.8 ms                                                                  | 60.7 ms: 1.18x faster                                       |
| unpickle_pure_python    | 150 us                                                                   | 127 us: 1.18x faster                                        |
| pylint                  | 319 ms                                                                   | 270 ms: 1.18x faster                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.24 ms: 1.18x faster                                       |
| scimark_fft             | 183 ms                                                                   | 157 ms: 1.16x faster                                        |
| deepcopy_memo           | 25.3 us                                                                  | 22.0 us: 1.15x faster                                       |
| scimark_lu              | 62.8 ms                                                                  | 54.8 ms: 1.15x faster                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 40.1 ms: 1.14x faster                                       |
| hexiom                  | 4.46 ms                                                                  | 3.97 ms: 1.12x faster                                       |
| nqueens                 | 65.1 ms                                                                  | 58.4 ms: 1.11x faster                                       |
| pickle_pure_python      | 203 us                                                                   | 183 us: 1.11x faster                                        |
| regex_compile           | 89.7 ms                                                                  | 80.9 ms: 1.11x faster                                       |
| sympy_expand            | 298 ms                                                                   | 269 ms: 1.11x faster                                        |
| chaos                   | 47.3 ms                                                                  | 42.8 ms: 1.10x faster                                       |
| chameleon               | 5.15 ms                                                                  | 4.67 ms: 1.10x faster                                       |
| float                   | 53.3 ms                                                                  | 48.3 ms: 1.10x faster                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.3 ms: 1.10x faster                                       |
| mako                    | 7.20 ms                                                                  | 6.53 ms: 1.10x faster                                       |
| django_template         | 23.9 ms                                                                  | 21.7 ms: 1.10x faster                                       |
| go                      | 97.5 ms                                                                  | 88.8 ms: 1.10x faster                                       |
| sqlglot_normalize       | 189 ms                                                                   | 172 ms: 1.10x faster                                        |
| deepcopy                | 240 us                                                                   | 219 us: 1.10x faster                                        |
| html5lib                | 38.5 ms                                                                  | 35.4 ms: 1.09x faster                                       |
| bench_thread_pool       | 856 us                                                                   | 789 us: 1.08x faster                                        |
| sympy_str               | 184 ms                                                                   | 170 ms: 1.08x faster                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.91 us: 1.08x faster                                       |
| dulwich_log             | 43.4 ms                                                                  | 40.3 ms: 1.08x faster                                       |
| tornado_http            | 91.8 ms                                                                  | 85.4 ms: 1.08x faster                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.7 ms: 1.07x faster                                       |
| pycparser               | 686 ms                                                                   | 639 ms: 1.07x faster                                        |
| docutils                | 1.59 sec                                                                 | 1.49 sec: 1.07x faster                                      |
| scimark_sor             | 77.7 ms                                                                  | 72.5 ms: 1.07x faster                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 478 ms: 1.07x faster                                        |
| json_loads              | 13.5 us                                                                  | 12.7 us: 1.07x faster                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 45.3 ms: 1.07x faster                                       |
| pprint_pformat          | 1.05 sec                                                                 | 985 ms: 1.07x faster                                        |
| pprint_safe_repr        | 512 ms                                                                   | 480 ms: 1.07x faster                                        |
| coroutines              | 14.8 ms                                                                  | 13.9 ms: 1.06x faster                                       |
| comprehensions          | 15.4 us                                                                  | 14.5 us: 1.06x faster                                       |
| coverage                | 55.3 ms                                                                  | 52.1 ms: 1.06x faster                                       |
| sympy_sum               | 98.9 ms                                                                  | 93.7 ms: 1.06x faster                                       |
| logging_simple          | 6.60 us                                                                  | 6.27 us: 1.05x faster                                       |
| logging_format          | 7.13 us                                                                  | 6.78 us: 1.05x faster                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.56 ms: 1.05x faster                                       |
| pyflate                 | 302 ms                                                                   | 289 ms: 1.05x faster                                        |
| meteor_contest          | 74.4 ms                                                                  | 71.2 ms: 1.05x faster                                       |
| fannkuch                | 255 ms                                                                   | 245 ms: 1.04x faster                                        |
| telco                   | 3.93 ms                                                                  | 3.76 ms: 1.04x faster                                       |
| unpickle_list           | 2.80 us                                                                  | 2.68 us: 1.04x faster                                       |
| async_tree_memoization  | 374 ms                                                                   | 360 ms: 1.04x faster                                        |
| thrift                  | 487 us                                                                   | 471 us: 1.03x faster                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 89.2 ms: 1.03x faster                                       |
| async_tree_none         | 313 ms                                                                   | 303 ms: 1.03x faster                                        |
| 2to3                    | 204 ms                                                                   | 198 ms: 1.03x faster                                        |
| xml_etree_iterparse     | 61.8 ms                                                                  | 60.1 ms: 1.03x faster                                       |
| python_startup          | 18.4 ms                                                                  | 18.1 ms: 1.01x faster                                       |
| xml_etree_process       | 36.6 ms                                                                  | 36.1 ms: 1.01x faster                                       |
| pidigits                | 147 ms                                                                   | 146 ms: 1.01x faster                                        |
| xml_etree_generate      | 52.3 ms                                                                  | 52.7 ms: 1.01x slower                                       |
| create_gc_cycles        | 666 us                                                                   | 677 us: 1.02x slower                                        |
| pickle                  | 6.47 us                                                                  | 6.68 us: 1.03x slower                                       |
| regex_dna               | 115 ms                                                                   | 119 ms: 1.04x slower                                        |
| regex_v8                | 13.5 ms                                                                  | 14.0 ms: 1.04x slower                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.46 ms: 1.04x slower                                       |
| pickle_list             | 2.70 us                                                                  | 2.82 us: 1.04x slower                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 64.4 ms: 1.05x slower                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.80 us: 1.07x slower                                       |
| pathlib                 | 72.9 ms                                                                  | 82.3 ms: 1.13x slower                                       |
| async_generators        | 180 ms                                                                   | 211 ms: 1.17x slower                                        |
| dask                    | 267 ms                                                                   | 352 ms: 1.32x slower                                        |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                |

Benchmark hidden because not significant (4): pickle_dict, python_startup_no_site, async_tree_io, unpickle
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
