
# Results vs. 3.11.0

- fork: python
- ref: 385b5d6e091da454c3e0
- machine: windows-amd64
- commit hash: 385b5d6
- commit date: 2023-04-02
- overall geometric mean: 1.10x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.50 ms: 1.15x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 35.7 ms: 1.08x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 87.7 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 53.3 ms: 1.33x faster                                                       |
| float          | 53.3 ms                                                                  | 47.4 ms: 1.13x faster                                                       |
| pidigits       | 147 ms                                                                   | 145 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 79.5 ms: 1.13x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.55 ms: 1.05x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| regex_dna      | 115 ms                                                                   | 123 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.30 ms: 1.45x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 121 us: 1.24x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 171 us: 1.19x faster                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 34.7 ms: 1.05x faster                                                       |
| unpickle             | 8.01 us                                                                  | 7.73 us: 1.04x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 50.7 ms: 1.03x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 89.7 ms: 1.03x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 60.4 ms: 1.02x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.76 us: 1.02x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.9 us: 1.01x slower                                                       |
| pickle               | 6.47 us                                                                  | 7.09 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (2): json_loads, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 19.0 ms: 1.04x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 16.2 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.2 ms: 1.30x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 29.6 ms: 1.28x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.17 ms: 1.17x faster                                                       |
| django_template | 23.9 ms                                                                  | 20.7 ms: 1.15x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.22x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| generators              | 33.5 ms                                                                  | 20.2 ms: 1.66x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 27.4 ns: 1.57x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.30 ms: 1.45x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 481 ms: 1.40x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 1.95 ms: 1.37x faster                                                       |
| richards                | 32.1 ms                                                                  | 24.0 ms: 1.34x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 53.3 ms: 1.33x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 53.8 ns: 1.32x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 13.2 ms: 1.30x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 55.4 ms: 1.30x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 29.6 ms: 1.28x faster                                                       |
| mypy2                   | 276 ms                                                                   | 217 ms: 1.27x faster                                                        |
| deepcopy_memo           | 25.3 us                                                                  | 20.1 us: 1.26x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.09 ms: 1.26x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 50.6 ms: 1.24x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 121 us: 1.24x faster                                                        |
| raytrace                | 206 ms                                                                   | 169 ms: 1.22x faster                                                        |
| json                    | 3.20 ms                                                                  | 2.65 ms: 1.21x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 38.0 ms: 1.21x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.40 sec: 1.20x faster                                                      |
| pickle_pure_python      | 203 us                                                                   | 171 us: 1.19x faster                                                        |
| scimark_sor             | 77.7 ms                                                                  | 65.1 ms: 1.19x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 154 ms: 1.19x faster                                                        |
| go                      | 97.5 ms                                                                  | 82.4 ms: 1.18x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 3.78 ms: 1.18x faster                                                       |
| deepcopy                | 240 us                                                                   | 205 us: 1.17x faster                                                        |
| mako                    | 7.20 ms                                                                  | 6.17 ms: 1.17x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 906 ms: 1.16x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 40.9 ms: 1.16x faster                                                       |
| django_template         | 23.9 ms                                                                  | 20.7 ms: 1.15x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.50 ms: 1.15x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.80 us: 1.14x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 165 ms: 1.14x faster                                                        |
| fannkuch                | 255 ms                                                                   | 225 ms: 1.14x faster                                                        |
| nqueens                 | 65.1 ms                                                                  | 57.4 ms: 1.13x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.29 us: 1.13x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 453 ms: 1.13x faster                                                        |
| regex_compile           | 89.7 ms                                                                  | 79.5 ms: 1.13x faster                                                       |
| float                   | 53.3 ms                                                                  | 47.4 ms: 1.13x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 30.7 ms: 1.12x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 832 us: 1.12x faster                                                        |
| crypto_pyaes            | 48.3 ms                                                                  | 43.4 ms: 1.11x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.02 ms: 1.11x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.02 us: 1.10x faster                                                       |
| pyflate                 | 302 ms                                                                   | 278 ms: 1.09x faster                                                        |
| html5lib                | 38.5 ms                                                                  | 35.7 ms: 1.08x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 69.1 ms: 1.08x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 476 ms: 1.08x faster                                                        |
| sympy_expand            | 298 ms                                                                   | 278 ms: 1.07x faster                                                        |
| coroutines              | 14.8 ms                                                                  | 13.8 ms: 1.07x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.8 ms: 1.07x faster                                                       |
| coverage                | 55.3 ms                                                                  | 52.2 ms: 1.06x faster                                                       |
| thrift                  | 487 us                                                                   | 460 us: 1.06x faster                                                        |
| comprehensions          | 15.4 us                                                                  | 14.6 us: 1.06x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 34.7 ms: 1.05x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.55 ms: 1.05x faster                                                       |
| sympy_str               | 184 ms                                                                   | 175 ms: 1.05x faster                                                        |
| tornado_http            | 91.8 ms                                                                  | 87.7 ms: 1.05x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.6 ms: 1.04x faster                                                       |
| unpickle                | 8.01 us                                                                  | 7.73 us: 1.04x faster                                                       |
| async_tree_memoization  | 374 ms                                                                   | 362 ms: 1.03x faster                                                        |
| xml_etree_generate      | 52.3 ms                                                                  | 50.7 ms: 1.03x faster                                                       |
| pycparser               | 686 ms                                                                   | 665 ms: 1.03x faster                                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 89.7 ms: 1.03x faster                                                       |
| async_tree_none         | 313 ms                                                                   | 306 ms: 1.02x faster                                                        |
| xml_etree_iterparse     | 61.8 ms                                                                  | 60.4 ms: 1.02x faster                                                       |
| bench_thread_pool       | 856 us                                                                   | 836 us: 1.02x faster                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.76 us: 1.02x faster                                                       |
| 2to3                    | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                      |
| sympy_sum               | 98.9 ms                                                                  | 97.7 ms: 1.01x faster                                                       |
| pidigits                | 147 ms                                                                   | 145 ms: 1.01x faster                                                        |
| pickle_dict             | 18.6 us                                                                  | 18.9 us: 1.01x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 757 ms: 1.02x slower                                                        |
| regex_v8                | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 19.0 ms: 1.04x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 696 us: 1.05x slower                                                        |
| gc_traversal            | 1.40 ms                                                                  | 1.47 ms: 1.05x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 16.2 ms: 1.05x slower                                                       |
| regex_dna               | 115 ms                                                                   | 123 ms: 1.06x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.78 us: 1.07x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 66.4 ms: 1.09x slower                                                       |
| pickle                  | 6.47 us                                                                  | 7.09 us: 1.10x slower                                                       |
| async_generators        | 180 ms                                                                   | 206 ms: 1.14x slower                                                        |
| pathlib                 | 72.9 ms                                                                  | 83.9 ms: 1.15x slower                                                       |
| dask                    | 267 ms                                                                   | 355 ms: 1.33x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.10x faster                                                                |

Benchmark hidden because not significant (3): telco, json_loads, pickle_list
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
