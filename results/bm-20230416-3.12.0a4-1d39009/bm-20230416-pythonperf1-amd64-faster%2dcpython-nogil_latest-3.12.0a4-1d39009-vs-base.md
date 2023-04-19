
# Results vs. base

- fork: faster-cpython
- ref: nogil_latest
- machine: windows-amd64
- commit hash: 1d39009
- commit date: 2023-04-16
- overall geometric mean: 1.17x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:--------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 190 ms                                                                     | 224 ms: 1.18x slower                                                         |
| chameleon      | 4.34 ms                                                                    | 5.66 ms: 1.31x slower                                                        |
| docutils       | 1.50 sec                                                                   | 1.89 sec: 1.26x slower                                                       |
| html5lib       | 35.3 ms                                                                    | 39.3 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                                      | 1.21x slower                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:--------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                     | 141 ms: 1.04x faster                                                         |
| float          | 46.3 ms                                                                    | 49.6 ms: 1.07x slower                                                        |
| nbody          | 56.6 ms                                                                    | 89.9 ms: 1.59x slower                                                        |
| Geometric mean | (ref)                                                                      | 1.18x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:--------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 1.73 ms                                                                    | 1.53 ms: 1.13x faster                                                        |
| regex_dna      | 121 ms                                                                     | 110 ms: 1.10x faster                                                         |
| regex_v8       | 13.7 ms                                                                    | 13.2 ms: 1.04x faster                                                        |
| regex_compile  | 78.9 ms                                                                    | 96.4 ms: 1.22x slower                                                        |
| Geometric mean | (ref)                                                                      | 1.01x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------------|:--------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse      | 87.1 ms                                                                    | 82.9 ms: 1.05x faster                                                        |
| pickle_list          | 2.74 us                                                                    | 2.81 us: 1.03x slower                                                        |
| pickle               | 6.79 us                                                                    | 7.14 us: 1.05x slower                                                        |
| unpickle             | 8.68 us                                                                    | 9.19 us: 1.06x slower                                                        |
| unpickle_list        | 2.62 us                                                                    | 2.86 us: 1.09x slower                                                        |
| json_loads           | 12.7 us                                                                    | 14.6 us: 1.15x slower                                                        |
| pickle_dict          | 18.4 us                                                                    | 21.8 us: 1.18x slower                                                        |
| xml_etree_generate   | 47.6 ms                                                                    | 57.5 ms: 1.21x slower                                                        |
| json_dumps           | 5.36 ms                                                                    | 6.50 ms: 1.21x slower                                                        |
| xml_etree_iterparse  | 61.1 ms                                                                    | 74.7 ms: 1.22x slower                                                        |
| xml_etree_process    | 33.0 ms                                                                    | 41.7 ms: 1.26x slower                                                        |
| pickle_pure_python   | 166 us                                                                     | 218 us: 1.31x slower                                                         |
| unpickle_pure_python | 118 us                                                                     | 159 us: 1.35x slower                                                         |
| Geometric mean       | (ref)                                                                      | 1.15x slower                                                                 |

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-----------------|:--------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 31.5 ms                                                                    | 35.3 ms: 1.12x slower                                                        |
| django_template | 20.9 ms                                                                    | 25.5 ms: 1.22x slower                                                        |
| genshi_text     | 13.3 ms                                                                    | 17.7 ms: 1.33x slower                                                        |
| mako            | 5.94 ms                                                                    | 8.95 ms: 1.51x slower                                                        |
| Geometric mean  | (ref)                                                                      | 1.29x slower                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-------------------------|:--------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io           | 768 ms                                                                     | 405 ms: 1.90x faster                                                         |
| async_tree_none         | 321 ms                                                                     | 189 ms: 1.70x faster                                                         |
| async_tree_memoization  | 377 ms                                                                     | 240 ms: 1.57x faster                                                         |
| async_tree_cpu_io_mixed | 494 ms                                                                     | 371 ms: 1.33x faster                                                         |
| sqlite_synth            | 1.70 us                                                                    | 1.35 us: 1.26x faster                                                        |
| regex_effbot            | 1.73 ms                                                                    | 1.53 ms: 1.13x faster                                                        |
| regex_dna               | 121 ms                                                                     | 110 ms: 1.10x faster                                                         |
| xml_etree_parse         | 87.1 ms                                                                    | 82.9 ms: 1.05x faster                                                        |
| pidigits                | 147 ms                                                                     | 141 ms: 1.04x faster                                                         |
| regex_v8                | 13.7 ms                                                                    | 13.2 ms: 1.04x faster                                                        |
| pickle_list             | 2.74 us                                                                    | 2.81 us: 1.03x slower                                                        |
| dulwich_log             | 42.3 ms                                                                    | 43.6 ms: 1.03x slower                                                        |
| asyncio_tcp             | 474 ms                                                                     | 489 ms: 1.03x slower                                                         |
| bench_mp_pool           | 60.9 ms                                                                    | 63.9 ms: 1.05x slower                                                        |
| pickle                  | 6.79 us                                                                    | 7.14 us: 1.05x slower                                                        |
| unpickle                | 8.68 us                                                                    | 9.19 us: 1.06x slower                                                        |
| float                   | 46.3 ms                                                                    | 49.6 ms: 1.07x slower                                                        |
| mdp                     | 1.51 sec                                                                   | 1.63 sec: 1.08x slower                                                       |
| gc_traversal            | 1.43 ms                                                                    | 1.56 ms: 1.09x slower                                                        |
| unpickle_list           | 2.62 us                                                                    | 2.86 us: 1.09x slower                                                        |
| json                    | 2.68 ms                                                                    | 2.94 ms: 1.10x slower                                                        |
| html5lib                | 35.3 ms                                                                    | 39.3 ms: 1.11x slower                                                        |
| genshi_xml              | 31.5 ms                                                                    | 35.3 ms: 1.12x slower                                                        |
| nqueens                 | 58.4 ms                                                                    | 65.6 ms: 1.12x slower                                                        |
| pycparser               | 634 ms                                                                     | 713 ms: 1.12x slower                                                         |
| create_gc_cycles        | 663 us                                                                     | 748 us: 1.13x slower                                                         |
| coroutines              | 14.7 ms                                                                    | 16.8 ms: 1.14x slower                                                        |
| coverage                | 52.4 ms                                                                    | 59.9 ms: 1.14x slower                                                        |
| json_loads              | 12.7 us                                                                    | 14.6 us: 1.15x slower                                                        |
| generators              | 32.6 ms                                                                    | 37.5 ms: 1.15x slower                                                        |
| pyflate                 | 262 ms                                                                     | 302 ms: 1.15x slower                                                         |
| sympy_sum               | 94.2 ms                                                                    | 109 ms: 1.16x slower                                                         |
| logging_simple          | 5.91 us                                                                    | 6.92 us: 1.17x slower                                                        |
| sympy_str               | 169 ms                                                                     | 198 ms: 1.18x slower                                                         |
| sympy_integrate         | 12.6 ms                                                                    | 14.8 ms: 1.18x slower                                                        |
| 2to3                    | 190 ms                                                                     | 224 ms: 1.18x slower                                                         |
| logging_format          | 6.29 us                                                                    | 7.40 us: 1.18x slower                                                        |
| crypto_pyaes            | 44.6 ms                                                                    | 52.7 ms: 1.18x slower                                                        |
| pickle_dict             | 18.4 us                                                                    | 21.8 us: 1.18x slower                                                        |
| sympy_expand            | 267 ms                                                                     | 320 ms: 1.20x slower                                                         |
| sqlglot_normalize       | 165 ms                                                                     | 199 ms: 1.20x slower                                                         |
| thrift                  | 450 us                                                                     | 542 us: 1.20x slower                                                         |
| fannkuch                | 237 ms                                                                     | 285 ms: 1.20x slower                                                         |
| xml_etree_generate      | 47.6 ms                                                                    | 57.5 ms: 1.21x slower                                                        |
| sqlglot_optimize        | 30.4 ms                                                                    | 36.8 ms: 1.21x slower                                                        |
| json_dumps              | 5.36 ms                                                                    | 6.50 ms: 1.21x slower                                                        |
| telco                   | 3.63 ms                                                                    | 4.41 ms: 1.21x slower                                                        |
| django_template         | 20.9 ms                                                                    | 25.5 ms: 1.22x slower                                                        |
| regex_compile           | 78.9 ms                                                                    | 96.4 ms: 1.22x slower                                                        |
| xml_etree_iterparse     | 61.1 ms                                                                    | 74.7 ms: 1.22x slower                                                        |
| async_generators        | 166 ms                                                                     | 205 ms: 1.23x slower                                                         |
| chaos                   | 42.7 ms                                                                    | 53.7 ms: 1.26x slower                                                        |
| bench_thread_pool       | 817 us                                                                     | 1.03 ms: 1.26x slower                                                        |
| docutils                | 1.50 sec                                                                   | 1.89 sec: 1.26x slower                                                       |
| xml_etree_process       | 33.0 ms                                                                    | 41.7 ms: 1.26x slower                                                        |
| go                      | 80.8 ms                                                                    | 103 ms: 1.27x slower                                                         |
| meteor_contest          | 67.6 ms                                                                    | 86.5 ms: 1.28x slower                                                        |
| sqlglot_transpile       | 1.02 ms                                                                    | 1.33 ms: 1.30x slower                                                        |
| chameleon               | 4.34 ms                                                                    | 5.66 ms: 1.31x slower                                                        |
| comprehensions          | 14.5 us                                                                    | 19.1 us: 1.31x slower                                                        |
| pickle_pure_python      | 166 us                                                                     | 218 us: 1.31x slower                                                         |
| spectral_norm           | 59.6 ms                                                                    | 78.8 ms: 1.32x slower                                                        |
| scimark_fft             | 166 ms                                                                     | 220 ms: 1.32x slower                                                         |
| hexiom                  | 3.75 ms                                                                    | 4.97 ms: 1.32x slower                                                        |
| pprint_safe_repr        | 441 ms                                                                     | 586 ms: 1.33x slower                                                         |
| genshi_text             | 13.3 ms                                                                    | 17.7 ms: 1.33x slower                                                        |
| scimark_lu              | 54.8 ms                                                                    | 73.1 ms: 1.33x slower                                                        |
| logging_silent          | 55.9 ns                                                                    | 75.0 ns: 1.34x slower                                                        |
| unpickle_pure_python    | 118 us                                                                     | 159 us: 1.35x slower                                                         |
| sqlglot_parse           | 829 us                                                                     | 1.12 ms: 1.35x slower                                                        |
| pprint_pformat          | 894 ms                                                                     | 1.21 sec: 1.35x slower                                                       |
| deepcopy_reduce         | 1.77 us                                                                    | 2.40 us: 1.36x slower                                                        |
| deepcopy                | 198 us                                                                     | 272 us: 1.37x slower                                                         |
| scimark_sparse_mat_mult | 2.17 ms                                                                    | 2.98 ms: 1.37x slower                                                        |
| richards                | 23.5 ms                                                                    | 32.3 ms: 1.37x slower                                                        |
| scimark_monte_carlo     | 37.1 ms                                                                    | 51.2 ms: 1.38x slower                                                        |
| mypy2                   | 208 ms                                                                     | 291 ms: 1.40x slower                                                         |
| deltablue               | 1.93 ms                                                                    | 2.71 ms: 1.40x slower                                                        |
| scimark_sor             | 62.4 ms                                                                    | 89.1 ms: 1.43x slower                                                        |
| raytrace                | 169 ms                                                                     | 241 ms: 1.43x slower                                                         |
| deepcopy_memo           | 19.9 us                                                                    | 29.5 us: 1.48x slower                                                        |
| mako                    | 5.94 ms                                                                    | 8.95 ms: 1.51x slower                                                        |
| nbody                   | 56.6 ms                                                                    | 89.9 ms: 1.59x slower                                                        |
| unpack_sequence         | 25.8 ns                                                                    | 55.2 ns: 2.14x slower                                                        |
| Geometric mean          | (ref)                                                                      | 1.17x slower                                                                 |

Benchmark hidden because not significant (3): pathlib, python_startup_no_site, python_startup
Ignored benchmarks (1) of public/results/bm-20230110-3.12.0a4-3d5d3f7/bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7.json: dask
