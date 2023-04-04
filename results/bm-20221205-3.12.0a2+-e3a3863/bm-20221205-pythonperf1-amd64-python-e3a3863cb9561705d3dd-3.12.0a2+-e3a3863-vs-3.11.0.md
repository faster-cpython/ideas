
# Results vs. 3.11.0

- fork: python
- ref: e3a3863cb9561705d3dd
- machine: windows-amd64
- commit hash: e3a3863
- commit date: 2022-12-05
- overall geometric mean: 1.07x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 199 ms: 1.02x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.68 ms: 1.10x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 34.5 ms: 1.12x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 90.7 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 61.5 ms: 1.15x faster                                                       |
| float          | 53.3 ms                                                                  | 49.8 ms: 1.07x faster                                                       |
| pidigits       | 147 ms                                                                   | 147 ms: 1.00x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 81.9 ms: 1.10x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| regex_dna      | 115 ms                                                                   | 121 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.16 ms: 1.49x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 124 us: 1.21x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 172 us: 1.18x faster                                                        |
| unpickle_list        | 2.80 us                                                                  | 2.59 us: 1.08x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 34.3 ms: 1.07x faster                                                       |
| json_loads           | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 50.6 ms: 1.03x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 89.7 ms: 1.03x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.9 us: 1.02x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.3 ms: 1.02x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.84 us: 1.05x slower                                                       |
| pickle               | 6.47 us                                                                  | 7.11 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.9 ms: 1.04x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.4 ms: 1.20x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 32.1 ms: 1.18x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.20 ms: 1.16x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.8 ms: 1.09x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.16x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2+-e3a3863 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 26.3 ns: 1.64x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.16 ms: 1.49x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.07 ms: 1.29x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 55.3 ns: 1.28x faster                                                       |
| mypy2                   | 276 ms                                                                   | 218 ms: 1.27x faster                                                        |
| richards                | 32.1 ms                                                                  | 25.3 ms: 1.27x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 20.9 us: 1.21x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 124 us: 1.21x faster                                                        |
| genshi_text             | 17.3 ms                                                                  | 14.4 ms: 1.20x faster                                                       |
| fannkuch                | 255 ms                                                                   | 215 ms: 1.19x faster                                                        |
| go                      | 97.5 ms                                                                  | 82.2 ms: 1.19x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 60.5 ms: 1.19x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 32.1 ms: 1.18x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 172 us: 1.18x faster                                                        |
| json                    | 3.20 ms                                                                  | 2.72 ms: 1.18x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.20 ms: 1.16x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.5 ms: 1.16x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 61.5 ms: 1.15x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.29 ms: 1.15x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 67.8 ms: 1.15x faster                                                       |
| pyflate                 | 302 ms                                                                   | 267 ms: 1.13x faster                                                        |
| raytrace                | 206 ms                                                                   | 182 ms: 1.13x faster                                                        |
| deepcopy                | 240 us                                                                   | 213 us: 1.13x faster                                                        |
| pprint_pformat          | 1.05 sec                                                                 | 934 ms: 1.12x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 3.98 ms: 1.12x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 34.5 ms: 1.12x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 835 us: 1.11x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.85 us: 1.11x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.68 ms: 1.10x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 57.2 ms: 1.10x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 81.9 ms: 1.10x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 467 ms: 1.09x faster                                                        |
| django_template         | 23.9 ms                                                                  | 21.8 ms: 1.09x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 59.9 ms: 1.09x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.59 us: 1.08x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.12 us: 1.08x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.0 ms: 1.08x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 176 ms: 1.07x faster                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.05 ms: 1.07x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 278 ms: 1.07x faster                                                        |
| float                   | 53.3 ms                                                                  | 49.8 ms: 1.07x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.67 us: 1.07x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 34.3 ms: 1.07x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 171 ms: 1.06x faster                                                        |
| meteor_contest          | 74.4 ms                                                                  | 70.4 ms: 1.06x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.9 ms: 1.06x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 44.8 ms: 1.06x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 45.8 ms: 1.05x faster                                                       |
| json_loads              | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.59 sec: 1.05x faster                                                      |
| coverage                | 55.3 ms                                                                  | 52.8 ms: 1.05x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.75 ms: 1.05x faster                                                       |
| thrift                  | 487 us                                                                   | 465 us: 1.05x faster                                                        |
| pycparser               | 686 ms                                                                   | 662 ms: 1.04x faster                                                        |
| sympy_str               | 184 ms                                                                   | 178 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 495 ms: 1.03x faster                                                        |
| xml_etree_generate      | 52.3 ms                                                                  | 50.6 ms: 1.03x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 89.7 ms: 1.03x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| 2to3                    | 204 ms                                                                   | 199 ms: 1.02x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 42.4 ms: 1.02x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                       |
| tornado_http            | 91.8 ms                                                                  | 90.7 ms: 1.01x faster                                                       |
| comprehensions          | 15.4 us                                                                  | 15.3 us: 1.01x faster                                                       |
| pidigits                | 147 ms                                                                   | 147 ms: 1.00x slower                                                        |
| async_generators        | 180 ms                                                                   | 181 ms: 1.00x slower                                                        |
| sympy_sum               | 98.9 ms                                                                  | 99.6 ms: 1.01x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 15.0 ms: 1.01x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.9 us: 1.02x slower                                                       |
| async_tree_memoization  | 374 ms                                                                   | 381 ms: 1.02x slower                                                        |
| python_startup          | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.3 ms: 1.02x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 682 us: 1.02x slower                                                        |
| pathlib                 | 72.9 ms                                                                  | 75.1 ms: 1.03x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.9 ms: 1.04x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 63.8 ms: 1.04x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 327 ms: 1.04x slower                                                        |
| pickle_list             | 2.70 us                                                                  | 2.84 us: 1.05x slower                                                       |
| regex_dna               | 115 ms                                                                   | 121 ms: 1.05x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.78 us: 1.06x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.49 ms: 1.06x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 792 ms: 1.07x slower                                                        |
| generators              | 33.5 ms                                                                  | 36.3 ms: 1.08x slower                                                       |
| pickle                  | 6.47 us                                                                  | 7.11 us: 1.10x slower                                                       |
| asyncio_tcp             | 674 ms                                                                   | 758 ms: 1.12x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (3): bench_thread_pool, dask, unpickle
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
