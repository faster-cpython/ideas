
# Results vs. 3.11.0

- fork: python
- ref: 7d4cc5aa854fdea4d01a
- machine: windows-amd64
- commit hash: 7d4cc5a
- commit date: 2023-04-04
- overall geometric mean: 1.12x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 233 ms: 1.14x slower                                                      |
| chameleon      | 5.15 ms                                                                  | 5.67 ms: 1.10x slower                                                     |
| docutils       | 1.59 sec                                                                 | 1.82 sec: 1.14x slower                                                    |
| html5lib       | 38.5 ms                                                                  | 45.8 ms: 1.19x slower                                                     |
| tornado_http   | 91.8 ms                                                                  | 108 ms: 1.18x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.15x slower                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 75.5 ms: 1.07x slower                                                     |
| float          | 53.3 ms                                                                  | 60.7 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.07x slower                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                     |
| regex_v8       | 13.5 ms                                                                  | 14.6 ms: 1.09x slower                                                     |
| regex_dna      | 115 ms                                                                   | 129 ms: 1.12x slower                                                      |
| regex_compile  | 89.7 ms                                                                  | 102 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.08x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_list        | 2.80 us                                                                  | 2.66 us: 1.05x faster                                                     |
| pickle_dict          | 18.6 us                                                                  | 18.7 us: 1.00x slower                                                     |
| json_loads           | 13.5 us                                                                  | 13.7 us: 1.01x slower                                                     |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.4 ms: 1.03x slower                                                     |
| xml_etree_generate   | 52.3 ms                                                                  | 54.3 ms: 1.04x slower                                                     |
| xml_etree_parse      | 92.1 ms                                                                  | 96.4 ms: 1.05x slower                                                     |
| pickle_list          | 2.70 us                                                                  | 2.86 us: 1.06x slower                                                     |
| pickle               | 6.47 us                                                                  | 7.34 us: 1.14x slower                                                     |
| json_dumps           | 7.71 ms                                                                  | 8.90 ms: 1.15x slower                                                     |
| unpickle             | 8.01 us                                                                  | 9.30 us: 1.16x slower                                                     |
| unpickle_pure_python | 150 us                                                                   | 177 us: 1.18x slower                                                      |
| xml_etree_process    | 36.6 ms                                                                  | 43.5 ms: 1.19x slower                                                     |
| pickle_pure_python   | 203 us                                                                   | 266 us: 1.31x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.09x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.6 ms: 1.02x slower                                                     |
| python_startup         | 18.4 ms                                                                  | 21.1 ms: 1.14x slower                                                     |
| Geometric mean         | (ref)                                                                    | 1.08x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 39.1 ms: 1.03x slower                                                     |
| genshi_text     | 17.3 ms                                                                  | 18.8 ms: 1.09x slower                                                     |
| django_template | 23.9 ms                                                                  | 28.9 ms: 1.21x slower                                                     |
| mako            | 7.20 ms                                                                  | 8.76 ms: 1.22x slower                                                     |
| Geometric mean  | (ref)                                                                    | 1.13x slower                                                              |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coverage                | 55.3 ms                                                                  | 39.2 ms: 1.41x faster                                                     |
| json                    | 3.20 ms                                                                  | 3.02 ms: 1.06x faster                                                     |
| logging_format          | 7.13 us                                                                  | 6.76 us: 1.05x faster                                                     |
| unpickle_list           | 2.80 us                                                                  | 2.66 us: 1.05x faster                                                     |
| logging_simple          | 6.60 us                                                                  | 6.28 us: 1.05x faster                                                     |
| generators              | 33.5 ms                                                                  | 32.1 ms: 1.05x faster                                                     |
| meteor_contest          | 74.4 ms                                                                  | 72.1 ms: 1.03x faster                                                     |
| unpack_sequence         | 43.1 ns                                                                  | 42.1 ns: 1.02x faster                                                     |
| regex_effbot            | 1.63 ms                                                                  | 1.60 ms: 1.02x faster                                                     |
| bench_mp_pool           | 61.2 ms                                                                  | 60.4 ms: 1.01x faster                                                     |
| flaskblogging           | 2.04 sec                                                                 | 2.05 sec: 1.00x slower                                                    |
| pickle_dict             | 18.6 us                                                                  | 18.7 us: 1.00x slower                                                     |
| gc_traversal            | 1.40 ms                                                                  | 1.42 ms: 1.01x slower                                                     |
| json_loads              | 13.5 us                                                                  | 13.7 us: 1.01x slower                                                     |
| comprehensions          | 15.4 us                                                                  | 15.6 us: 1.01x slower                                                     |
| python_startup_no_site  | 15.4 ms                                                                  | 15.6 ms: 1.02x slower                                                     |
| pathlib                 | 72.9 ms                                                                  | 74.4 ms: 1.02x slower                                                     |
| mdp                     | 1.67 sec                                                                 | 1.71 sec: 1.02x slower                                                    |
| sympy_str               | 184 ms                                                                   | 188 ms: 1.02x slower                                                      |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.4 ms: 1.03x slower                                                     |
| genshi_xml              | 38.0 ms                                                                  | 39.1 ms: 1.03x slower                                                     |
| nqueens                 | 65.1 ms                                                                  | 67.5 ms: 1.04x slower                                                     |
| deepcopy_reduce         | 2.06 us                                                                  | 2.13 us: 1.04x slower                                                     |
| xml_etree_generate      | 52.3 ms                                                                  | 54.3 ms: 1.04x slower                                                     |
| xml_etree_parse         | 92.1 ms                                                                  | 96.4 ms: 1.05x slower                                                     |
| sympy_expand            | 298 ms                                                                   | 312 ms: 1.05x slower                                                      |
| sympy_sum               | 98.9 ms                                                                  | 105 ms: 1.06x slower                                                      |
| pickle_list             | 2.70 us                                                                  | 2.86 us: 1.06x slower                                                     |
| coroutines              | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                     |
| nbody                   | 70.9 ms                                                                  | 75.5 ms: 1.07x slower                                                     |
| sqlglot_normalize       | 189 ms                                                                   | 202 ms: 1.07x slower                                                      |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 11.1 ms: 1.07x slower                                                     |
| pylint                  | 319 ms                                                                   | 341 ms: 1.07x slower                                                      |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.83 ms: 1.08x slower                                                     |
| sympy_integrate         | 13.7 ms                                                                  | 14.8 ms: 1.08x slower                                                     |
| fannkuch                | 255 ms                                                                   | 276 ms: 1.08x slower                                                      |
| bench_thread_pool       | 856 us                                                                   | 928 us: 1.08x slower                                                      |
| regex_v8                | 13.5 ms                                                                  | 14.6 ms: 1.09x slower                                                     |
| deepcopy                | 240 us                                                                   | 260 us: 1.09x slower                                                      |
| genshi_text             | 17.3 ms                                                                  | 18.8 ms: 1.09x slower                                                     |
| dulwich_log             | 43.4 ms                                                                  | 47.6 ms: 1.09x slower                                                     |
| chameleon               | 5.15 ms                                                                  | 5.67 ms: 1.10x slower                                                     |
| sqlite_synth            | 1.67 us                                                                  | 1.84 us: 1.10x slower                                                     |
| scimark_fft             | 183 ms                                                                   | 203 ms: 1.11x slower                                                      |
| aiohttp                 | 864 us                                                                   | 962 us: 1.11x slower                                                      |
| sqlglot_optimize        | 34.5 ms                                                                  | 38.5 ms: 1.12x slower                                                     |
| regex_dna               | 115 ms                                                                   | 129 ms: 1.12x slower                                                      |
| asyncio_tcp             | 674 ms                                                                   | 755 ms: 1.12x slower                                                      |
| deepcopy_memo           | 25.3 us                                                                  | 28.6 us: 1.13x slower                                                     |
| spectral_norm           | 71.8 ms                                                                  | 81.4 ms: 1.13x slower                                                     |
| dask                    | 267 ms                                                                   | 303 ms: 1.14x slower                                                      |
| pickle                  | 6.47 us                                                                  | 7.34 us: 1.14x slower                                                     |
| pprint_pformat          | 1.05 sec                                                                 | 1.19 sec: 1.14x slower                                                    |
| float                   | 53.3 ms                                                                  | 60.7 ms: 1.14x slower                                                     |
| regex_compile           | 89.7 ms                                                                  | 102 ms: 1.14x slower                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 584 ms: 1.14x slower                                                      |
| 2to3                    | 204 ms                                                                   | 233 ms: 1.14x slower                                                      |
| docutils                | 1.59 sec                                                                 | 1.82 sec: 1.14x slower                                                    |
| python_startup          | 18.4 ms                                                                  | 21.1 ms: 1.14x slower                                                     |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 95.8 ms: 1.15x slower                                                     |
| json_dumps              | 7.71 ms                                                                  | 8.90 ms: 1.15x slower                                                     |
| unpickle                | 8.01 us                                                                  | 9.30 us: 1.16x slower                                                     |
| create_gc_cycles        | 666 us                                                                   | 777 us: 1.17x slower                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 598 ms: 1.17x slower                                                      |
| tornado_http            | 91.8 ms                                                                  | 108 ms: 1.18x slower                                                      |
| unpickle_pure_python    | 150 us                                                                   | 177 us: 1.18x slower                                                      |
| html5lib                | 38.5 ms                                                                  | 45.8 ms: 1.19x slower                                                     |
| xml_etree_process       | 36.6 ms                                                                  | 43.5 ms: 1.19x slower                                                     |
| async_generators        | 180 ms                                                                   | 218 ms: 1.21x slower                                                      |
| hexiom                  | 4.46 ms                                                                  | 5.40 ms: 1.21x slower                                                     |
| django_template         | 23.9 ms                                                                  | 28.9 ms: 1.21x slower                                                     |
| mako                    | 7.20 ms                                                                  | 8.76 ms: 1.22x slower                                                     |
| pycparser               | 686 ms                                                                   | 839 ms: 1.22x slower                                                      |
| mypy2                   | 276 ms                                                                   | 343 ms: 1.24x slower                                                      |
| chaos                   | 47.3 ms                                                                  | 59.2 ms: 1.25x slower                                                     |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.42 ms: 1.26x slower                                                     |
| richards                | 32.1 ms                                                                  | 40.9 ms: 1.27x slower                                                     |
| sqlglot_parse           | 929 us                                                                   | 1.19 ms: 1.28x slower                                                     |
| async_tree_memoization  | 374 ms                                                                   | 481 ms: 1.29x slower                                                      |
| scimark_monte_carlo     | 45.8 ms                                                                  | 58.9 ms: 1.29x slower                                                     |
| thrift                  | 487 us                                                                   | 629 us: 1.29x slower                                                      |
| pyflate                 | 302 ms                                                                   | 391 ms: 1.29x slower                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 63.2 ms: 1.31x slower                                                     |
| pickle_pure_python      | 203 us                                                                   | 266 us: 1.31x slower                                                      |
| raytrace                | 206 ms                                                                   | 271 ms: 1.31x slower                                                      |
| async_tree_none         | 313 ms                                                                   | 414 ms: 1.32x slower                                                      |
| scimark_lu              | 62.8 ms                                                                  | 84.5 ms: 1.34x slower                                                     |
| logging_silent          | 71.0 ns                                                                  | 97.2 ns: 1.37x slower                                                     |
| scimark_sor             | 77.7 ms                                                                  | 107 ms: 1.38x slower                                                      |
| async_tree_io           | 744 ms                                                                   | 1.04 sec: 1.39x slower                                                    |
| go                      | 97.5 ms                                                                  | 137 ms: 1.40x slower                                                      |
| deltablue               | 2.68 ms                                                                  | 4.11 ms: 1.53x slower                                                     |
| Geometric mean          | (ref)                                                                    | 1.12x slower                                                              |

Benchmark hidden because not significant (2): pidigits, telco
