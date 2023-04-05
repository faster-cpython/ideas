
# Results vs. 3.11.0

- fork: python
- ref: a1f08f5f19753c7c9295
- machine: windows-amd64
- commit hash: a1f08f5
- commit date: 2023-02-13
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 201 ms: 1.02x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.43 ms: 1.16x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.57 sec: 1.01x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 34.9 ms: 1.10x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 90.3 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 62.7 ms: 1.13x faster                                                       |
| float          | 53.3 ms                                                                  | 49.6 ms: 1.07x faster                                                       |
| pidigits       | 147 ms                                                                   | 150 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 78.6 ms: 1.14x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.4 ms: 1.07x slower                                                       |
| regex_dna      | 115 ms                                                                   | 124 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.27 ms: 1.46x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 119 us: 1.26x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 169 us: 1.20x faster                                                        |
| json_loads           | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.71 us: 1.03x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.9 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.6 ms: 1.01x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.3 us: 1.04x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 65.5 ms: 1.06x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.93 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (3): xml_etree_parse, unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.7 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.5 ms: 1.28x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 30.5 ms: 1.25x faster                                                       |
| mako            | 7.20 ms                                                                  | 5.99 ms: 1.20x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.0 ms: 1.14x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.22x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230213-pythonperf1-amd64-python-a1f08f5f19753c7c9295-3.12.0a5+-a1f08f5 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 25.6 ns: 1.68x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.27 ms: 1.46x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 485 ms: 1.39x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 1.96 ms: 1.37x faster                                                       |
| richards                | 32.1 ms                                                                  | 23.9 ms: 1.34x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 54.7 ns: 1.30x faster                                                       |
| comprehensions          | 15.4 us                                                                  | 12.0 us: 1.28x faster                                                       |
| mypy2                   | 276 ms                                                                   | 216 ms: 1.28x faster                                                        |
| genshi_text             | 17.3 ms                                                                  | 13.5 ms: 1.28x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 119 us: 1.26x faster                                                        |
| genshi_xml              | 38.0 ms                                                                  | 30.5 ms: 1.25x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 20.9 us: 1.21x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 169 us: 1.20x faster                                                        |
| mako                    | 7.20 ms                                                                  | 5.99 ms: 1.20x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 3.73 ms: 1.19x faster                                                       |
| go                      | 97.5 ms                                                                  | 82.0 ms: 1.19x faster                                                       |
| raytrace                | 206 ms                                                                   | 174 ms: 1.18x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.24 ms: 1.18x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 66.1 ms: 1.17x faster                                                       |
| deepcopy                | 240 us                                                                   | 205 us: 1.17x faster                                                        |
| chameleon               | 5.15 ms                                                                  | 4.43 ms: 1.16x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.4 ms: 1.16x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 56.2 ms: 1.16x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 62.0 ms: 1.16x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.78 ms: 1.15x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 78.6 ms: 1.14x faster                                                       |
| django_template         | 23.9 ms                                                                  | 21.0 ms: 1.14x faster                                                       |
| pyflate                 | 302 ms                                                                   | 265 ms: 1.14x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 41.6 ms: 1.14x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 925 ms: 1.14x faster                                                        |
| nbody                   | 70.9 ms                                                                  | 62.7 ms: 1.13x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.31 us: 1.13x faster                                                       |
| fannkuch                | 255 ms                                                                   | 226 ms: 1.13x faster                                                        |
| scimark_lu              | 62.8 ms                                                                  | 56.4 ms: 1.11x faster                                                       |
| sympy_str               | 184 ms                                                                   | 165 ms: 1.11x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.85 us: 1.11x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 270 ms: 1.11x faster                                                        |
| pprint_safe_repr        | 512 ms                                                                   | 463 ms: 1.10x faster                                                        |
| html5lib                | 38.5 ms                                                                  | 34.9 ms: 1.10x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 43.9 ms: 1.10x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.04 us: 1.09x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.6 ms: 1.09x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 168 ms: 1.08x faster                                                        |
| float                   | 53.3 ms                                                                  | 49.6 ms: 1.07x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 867 us: 1.07x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 176 ms: 1.07x faster                                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.3 ms: 1.07x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.07 ms: 1.06x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.58 sec: 1.06x faster                                                      |
| sympy_sum               | 98.9 ms                                                                  | 93.3 ms: 1.06x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 488 ms: 1.05x faster                                                        |
| coverage                | 55.3 ms                                                                  | 52.7 ms: 1.05x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 70.9 ms: 1.05x faster                                                       |
| json_loads              | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.2 ms: 1.04x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.8 ms: 1.04x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.71 us: 1.03x faster                                                       |
| pycparser               | 686 ms                                                                   | 666 ms: 1.03x faster                                                        |
| telco                   | 3.93 ms                                                                  | 3.82 ms: 1.03x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 35.9 ms: 1.02x faster                                                       |
| tornado_http            | 91.8 ms                                                                  | 90.3 ms: 1.02x faster                                                       |
| 2to3                    | 204 ms                                                                   | 201 ms: 1.02x faster                                                        |
| bench_thread_pool       | 856 us                                                                   | 843 us: 1.02x faster                                                        |
| thrift                  | 487 us                                                                   | 480 us: 1.01x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.57 sec: 1.01x faster                                                      |
| xml_etree_generate      | 52.3 ms                                                                  | 51.6 ms: 1.01x faster                                                       |
| pathlib                 | 72.9 ms                                                                  | 74.3 ms: 1.02x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                                       |
| pidigits                | 147 ms                                                                   | 150 ms: 1.02x slower                                                        |
| python_startup_no_site  | 15.4 ms                                                                  | 15.7 ms: 1.03x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 769 ms: 1.03x slower                                                        |
| pickle_dict             | 18.6 us                                                                  | 19.3 us: 1.04x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 693 us: 1.04x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 64.0 ms: 1.05x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 65.5 ms: 1.06x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.49 ms: 1.06x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 14.4 ms: 1.07x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.79 us: 1.07x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.93 us: 1.07x slower                                                       |
| regex_dna               | 115 ms                                                                   | 124 ms: 1.08x slower                                                        |
| async_generators        | 180 ms                                                                   | 216 ms: 1.20x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (6): async_tree_memoization, xml_etree_parse, async_tree_none, generators, unpickle, pickle_list
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, dask, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
