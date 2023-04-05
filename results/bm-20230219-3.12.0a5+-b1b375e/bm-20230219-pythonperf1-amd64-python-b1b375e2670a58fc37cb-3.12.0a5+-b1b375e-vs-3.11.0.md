
# Results vs. 3.11.0

- fork: python
- ref: b1b375e2670a58fc37cb
- machine: windows-amd64
- commit hash: b1b375e
- commit date: 2023-02-19
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 199 ms: 1.03x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.63 ms: 1.11x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 35.0 ms: 1.10x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 61.9 ms: 1.14x faster                                                       |
| float          | 53.3 ms                                                                  | 48.6 ms: 1.10x faster                                                       |
| pidigits       | 147 ms                                                                   | 150 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 79.1 ms: 1.13x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.58 ms: 1.04x faster                                                       |
| regex_dna      | 115 ms                                                                   | 120 ms: 1.04x slower                                                        |
| regex_v8       | 13.5 ms                                                                  | 14.2 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.37 ms: 1.44x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 122 us: 1.22x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 173 us: 1.18x faster                                                        |
| json_loads           | 13.5 us                                                                  | 12.8 us: 1.06x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.1 ms: 1.02x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.8 ms: 1.02x faster                                                       |
| unpickle             | 8.01 us                                                                  | 7.87 us: 1.02x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.75 us: 1.02x faster                                                       |
| pickle               | 6.47 us                                                                  | 7.13 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (4): xml_etree_iterparse, pickle_list, pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.0 ms: 1.24x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 32.0 ms: 1.19x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.19 ms: 1.16x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.3 ms: 1.12x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.18x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230219-pythonperf1-amd64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 25.9 ns: 1.67x faster                                                       |
| generators              | 33.5 ms                                                                  | 21.6 ms: 1.55x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.37 ms: 1.44x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 483 ms: 1.39x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 1.96 ms: 1.37x faster                                                       |
| richards                | 32.1 ms                                                                  | 23.9 ms: 1.34x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 54.2 ns: 1.31x faster                                                       |
| comprehensions          | 15.4 us                                                                  | 11.9 us: 1.29x faster                                                       |
| mypy2                   | 276 ms                                                                   | 217 ms: 1.27x faster                                                        |
| genshi_text             | 17.3 ms                                                                  | 14.0 ms: 1.24x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 122 us: 1.22x faster                                                        |
| scimark_sor             | 77.7 ms                                                                  | 63.5 ms: 1.22x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.17 ms: 1.21x faster                                                       |
| fannkuch                | 255 ms                                                                   | 212 ms: 1.20x faster                                                        |
| genshi_xml              | 38.0 ms                                                                  | 32.0 ms: 1.19x faster                                                       |
| pyflate                 | 302 ms                                                                   | 256 ms: 1.18x faster                                                        |
| pickle_pure_python      | 203 us                                                                   | 173 us: 1.18x faster                                                        |
| raytrace                | 206 ms                                                                   | 176 ms: 1.17x faster                                                        |
| spectral_norm           | 71.8 ms                                                                  | 61.5 ms: 1.17x faster                                                       |
| go                      | 97.5 ms                                                                  | 83.6 ms: 1.17x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.19 ms: 1.16x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 3.84 ms: 1.16x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 21.8 us: 1.16x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.7 ms: 1.15x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 61.9 ms: 1.14x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 57.1 ms: 1.14x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 41.6 ms: 1.14x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 79.1 ms: 1.13x faster                                                       |
| deepcopy                | 240 us                                                                   | 213 us: 1.13x faster                                                        |
| django_template         | 23.9 ms                                                                  | 21.3 ms: 1.12x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 56.1 ms: 1.12x faster                                                       |
| sympy_str               | 184 ms                                                                   | 164 ms: 1.12x faster                                                        |
| chameleon               | 5.15 ms                                                                  | 4.63 ms: 1.11x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.41 us: 1.11x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.89 ms: 1.11x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.3 ms: 1.10x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.87 us: 1.10x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 35.0 ms: 1.10x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 272 ms: 1.10x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.53 sec: 1.10x faster                                                      |
| float                   | 53.3 ms                                                                  | 48.6 ms: 1.10x faster                                                       |
| coverage                | 55.3 ms                                                                  | 50.6 ms: 1.09x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 167 ms: 1.09x faster                                                        |
| pprint_pformat          | 1.05 sec                                                                 | 961 ms: 1.09x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 174 ms: 1.08x faster                                                        |
| crypto_pyaes            | 48.3 ms                                                                  | 44.6 ms: 1.08x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 476 ms: 1.07x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 40.5 ms: 1.07x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 479 ms: 1.07x faster                                                        |
| logging_simple          | 6.60 us                                                                  | 6.19 us: 1.07x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 92.8 ms: 1.07x faster                                                       |
| json_loads              | 13.5 us                                                                  | 12.8 us: 1.06x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.9 ms: 1.06x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.72 ms: 1.05x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.1 ms: 1.05x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 888 us: 1.05x faster                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.09 ms: 1.04x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.58 ms: 1.04x faster                                                       |
| thrift                  | 487 us                                                                   | 470 us: 1.04x faster                                                        |
| meteor_contest          | 74.4 ms                                                                  | 71.8 ms: 1.04x faster                                                       |
| 2to3                    | 204 ms                                                                   | 199 ms: 1.03x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| xml_etree_generate      | 52.3 ms                                                                  | 51.1 ms: 1.02x faster                                                       |
| async_tree_memoization  | 374 ms                                                                   | 366 ms: 1.02x faster                                                        |
| xml_etree_process       | 36.6 ms                                                                  | 35.8 ms: 1.02x faster                                                       |
| pycparser               | 686 ms                                                                   | 672 ms: 1.02x faster                                                        |
| unpickle                | 8.01 us                                                                  | 7.87 us: 1.02x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.75 us: 1.02x faster                                                       |
| bench_thread_pool       | 856 us                                                                   | 846 us: 1.01x faster                                                        |
| python_startup          | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| pidigits                | 147 ms                                                                   | 150 ms: 1.03x slower                                                        |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 75.8 ms: 1.04x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 775 ms: 1.04x slower                                                        |
| regex_dna               | 115 ms                                                                   | 120 ms: 1.04x slower                                                        |
| regex_v8                | 13.5 ms                                                                  | 14.2 ms: 1.05x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.48 ms: 1.06x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 64.9 ms: 1.06x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 708 us: 1.06x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.81 us: 1.08x slower                                                       |
| pickle                  | 6.47 us                                                                  | 7.13 us: 1.10x slower                                                       |
| async_generators        | 180 ms                                                                   | 220 ms: 1.22x slower                                                        |
| dask                    | 267 ms                                                                   | 350 ms: 1.31x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (6): tornado_http, xml_etree_iterparse, pickle_list, pickle_dict, xml_etree_parse, async_tree_none
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
