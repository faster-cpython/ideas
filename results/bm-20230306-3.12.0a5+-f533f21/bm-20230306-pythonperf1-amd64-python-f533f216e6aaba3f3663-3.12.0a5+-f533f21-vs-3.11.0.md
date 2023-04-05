
# Results vs. 3.11.0

- fork: python
- ref: f533f216e6aaba3f3663
- machine: windows-amd64
- commit hash: f533f21
- commit date: 2023-03-06
- overall geometric mean: 1.06x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 5.15 ms                                                                  | 4.82 ms: 1.07x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 36.7 ms: 1.05x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 90.7 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 64.6 ms: 1.10x faster                                                       |
| float          | 53.3 ms                                                                  | 50.4 ms: 1.06x faster                                                       |
| pidigits       | 147 ms                                                                   | 150 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 82.1 ms: 1.09x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.65 ms: 1.01x slower                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.3 ms: 1.06x slower                                                       |
| regex_dna      | 115 ms                                                                   | 123 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.40 ms: 1.43x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 126 us: 1.18x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 176 us: 1.16x faster                                                        |
| json_loads           | 13.5 us                                                                  | 12.7 us: 1.06x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.74 us: 1.02x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 62.4 ms: 1.01x slower                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 37.7 ms: 1.03x slower                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 53.9 ms: 1.03x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.80 us: 1.04x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.91 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (3): xml_etree_parse, unpickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 16.0 ms: 1.04x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.2 ms: 1.22x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 32.1 ms: 1.19x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.36 ms: 1.13x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.9 ms: 1.09x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.16x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230306-pythonperf1-amd64-python-f533f216e6aaba3f3663-3.12.0a5+-f533f21 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| generators              | 33.5 ms                                                                  | 21.8 ms: 1.54x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 28.6 ns: 1.51x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.40 ms: 1.43x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 476 ms: 1.42x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 1.99 ms: 1.35x faster                                                       |
| mypy2                   | 276 ms                                                                   | 216 ms: 1.28x faster                                                        |
| logging_silent          | 71.0 ns                                                                  | 56.1 ns: 1.27x faster                                                       |
| richards                | 32.1 ms                                                                  | 25.4 ms: 1.26x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 14.2 ms: 1.22x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 32.1 ms: 1.19x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 126 us: 1.18x faster                                                        |
| pickle_pure_python      | 203 us                                                                   | 176 us: 1.16x faster                                                        |
| fannkuch                | 255 ms                                                                   | 221 ms: 1.15x faster                                                        |
| json                    | 3.20 ms                                                                  | 2.80 ms: 1.14x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.36 ms: 1.13x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 22.4 us: 1.13x faster                                                       |
| coverage                | 55.3 ms                                                                  | 49.1 ms: 1.13x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.49 sec: 1.12x faster                                                      |
| go                      | 97.5 ms                                                                  | 87.4 ms: 1.11x faster                                                       |
| raytrace                | 206 ms                                                                   | 185 ms: 1.11x faster                                                        |
| nqueens                 | 65.1 ms                                                                  | 58.5 ms: 1.11x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 42.5 ms: 1.11x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 4.02 ms: 1.11x faster                                                       |
| pyflate                 | 302 ms                                                                   | 272 ms: 1.11x faster                                                        |
| pprint_pformat          | 1.05 sec                                                                 | 951 ms: 1.10x faster                                                        |
| deepcopy                | 240 us                                                                   | 218 us: 1.10x faster                                                        |
| nbody                   | 70.9 ms                                                                  | 64.6 ms: 1.10x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 173 ms: 1.09x faster                                                        |
| regex_compile           | 89.7 ms                                                                  | 82.1 ms: 1.09x faster                                                       |
| django_template         | 23.9 ms                                                                  | 21.9 ms: 1.09x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.55 us: 1.09x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 71.7 ms: 1.08x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 42.3 ms: 1.08x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.13 us: 1.08x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 277 ms: 1.08x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.91 us: 1.08x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.82 ms: 1.07x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 45.3 ms: 1.07x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 67.4 ms: 1.06x faster                                                       |
| json_loads              | 13.5 us                                                                  | 12.7 us: 1.06x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.5 ms: 1.06x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 483 ms: 1.06x faster                                                        |
| float                   | 53.3 ms                                                                  | 50.4 ms: 1.06x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 59.5 ms: 1.06x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.2 ms: 1.05x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 36.7 ms: 1.05x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.2 ms: 1.04x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.1 ms: 1.04x faster                                                       |
| sympy_str               | 184 ms                                                                   | 177 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 493 ms: 1.04x faster                                                        |
| telco                   | 3.93 ms                                                                  | 3.81 ms: 1.03x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 72.4 ms: 1.03x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.10 ms: 1.03x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 908 us: 1.02x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| unpickle_list           | 2.80 us                                                                  | 2.74 us: 1.02x faster                                                       |
| async_tree_none         | 313 ms                                                                   | 306 ms: 1.02x faster                                                        |
| thrift                  | 487 us                                                                   | 478 us: 1.02x faster                                                        |
| tornado_http            | 91.8 ms                                                                  | 90.7 ms: 1.01x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.64 ms: 1.01x slower                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.65 ms: 1.01x slower                                                       |
| sympy_sum               | 98.9 ms                                                                  | 99.8 ms: 1.01x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 62.4 ms: 1.01x slower                                                       |
| pidigits                | 147 ms                                                                   | 150 ms: 1.02x slower                                                        |
| python_startup          | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 75.0 ms: 1.03x slower                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 37.7 ms: 1.03x slower                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 53.9 ms: 1.03x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.80 us: 1.04x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 16.0 ms: 1.04x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 778 ms: 1.05x slower                                                        |
| create_gc_cycles        | 666 us                                                                   | 701 us: 1.05x slower                                                        |
| regex_v8                | 13.5 ms                                                                  | 14.3 ms: 1.06x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.91 us: 1.07x slower                                                       |
| regex_dna               | 115 ms                                                                   | 123 ms: 1.07x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 65.7 ms: 1.07x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.51 ms: 1.08x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.82 us: 1.09x slower                                                       |
| async_generators        | 180 ms                                                                   | 224 ms: 1.24x slower                                                        |
| dask                    | 267 ms                                                                   | 356 ms: 1.34x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (9): async_tree_memoization, scimark_fft, bench_thread_pool, 2to3, xml_etree_parse, pycparser, comprehensions, unpickle, pickle_dict
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
