
# Results vs. 3.11.0

- fork: python
- ref: aad5f6a89125ad4529ab
- machine: windows-amd64
- commit hash: aad5f6a
- commit date: 2023-02-07
- overall geometric mean: 1.12x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 231 ms: 1.13x slower                                                      |
| chameleon      | 5.15 ms                                                                  | 5.49 ms: 1.06x slower                                                     |
| docutils       | 1.59 sec                                                                 | 1.84 sec: 1.16x slower                                                    |
| html5lib       | 38.5 ms                                                                  | 48.2 ms: 1.25x slower                                                     |
| tornado_http   | 91.8 ms                                                                  | 109 ms: 1.19x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.16x slower                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                   | 148 ms: 1.01x slower                                                      |
| nbody          | 70.9 ms                                                                  | 71.9 ms: 1.01x slower                                                     |
| float          | 53.3 ms                                                                  | 60.6 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.05x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.81 ms: 1.11x slower                                                     |
| regex_v8       | 13.5 ms                                                                  | 15.0 ms: 1.11x slower                                                     |
| regex_dna      | 115 ms                                                                   | 132 ms: 1.15x slower                                                      |
| regex_compile  | 89.7 ms                                                                  | 103 ms: 1.15x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.13x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_list        | 2.80 us                                                                  | 2.73 us: 1.03x faster                                                     |
| xml_etree_generate   | 52.3 ms                                                                  | 53.3 ms: 1.02x slower                                                     |
| pickle_dict          | 18.6 us                                                                  | 19.1 us: 1.03x slower                                                     |
| xml_etree_iterparse  | 61.8 ms                                                                  | 64.4 ms: 1.04x slower                                                     |
| json_loads           | 13.5 us                                                                  | 14.2 us: 1.05x slower                                                     |
| xml_etree_parse      | 92.1 ms                                                                  | 96.6 ms: 1.05x slower                                                     |
| pickle_list          | 2.70 us                                                                  | 2.91 us: 1.08x slower                                                     |
| pickle               | 6.47 us                                                                  | 7.00 us: 1.08x slower                                                     |
| unpickle             | 8.01 us                                                                  | 9.05 us: 1.13x slower                                                     |
| json_dumps           | 7.71 ms                                                                  | 8.93 ms: 1.16x slower                                                     |
| xml_etree_process    | 36.6 ms                                                                  | 42.7 ms: 1.17x slower                                                     |
| unpickle_pure_python | 150 us                                                                   | 180 us: 1.21x slower                                                      |
| pickle_pure_python   | 203 us                                                                   | 267 us: 1.31x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.10x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.0 ms: 1.02x faster                                                     |
| python_startup         | 18.4 ms                                                                  | 19.8 ms: 1.08x slower                                                     |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|-----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 39.0 ms: 1.03x slower                                                     |
| genshi_text     | 17.3 ms                                                                  | 18.3 ms: 1.06x slower                                                     |
| django_template | 23.9 ms                                                                  | 29.2 ms: 1.22x slower                                                     |
| mako            | 7.20 ms                                                                  | 8.84 ms: 1.23x slower                                                     |
| Geometric mean  | (ref)                                                                    | 1.13x slower                                                              |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|-------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coverage                | 55.3 ms                                                                  | 40.0 ms: 1.38x faster                                                     |
| unpack_sequence         | 43.1 ns                                                                  | 40.8 ns: 1.06x faster                                                     |
| logging_format          | 7.13 us                                                                  | 6.81 us: 1.05x faster                                                     |
| generators              | 33.5 ms                                                                  | 32.5 ms: 1.03x faster                                                     |
| unpickle_list           | 2.80 us                                                                  | 2.73 us: 1.03x faster                                                     |
| logging_simple          | 6.60 us                                                                  | 6.45 us: 1.02x faster                                                     |
| python_startup_no_site  | 15.4 ms                                                                  | 15.0 ms: 1.02x faster                                                     |
| meteor_contest          | 74.4 ms                                                                  | 72.9 ms: 1.02x faster                                                     |
| bench_mp_pool           | 61.2 ms                                                                  | 60.0 ms: 1.02x faster                                                     |
| telco                   | 3.93 ms                                                                  | 3.88 ms: 1.01x faster                                                     |
| gc_traversal            | 1.40 ms                                                                  | 1.40 ms: 1.01x faster                                                     |
| pidigits                | 147 ms                                                                   | 148 ms: 1.01x slower                                                      |
| nbody                   | 70.9 ms                                                                  | 71.9 ms: 1.01x slower                                                     |
| fannkuch                | 255 ms                                                                   | 259 ms: 1.01x slower                                                      |
| comprehensions          | 15.4 us                                                                  | 15.7 us: 1.02x slower                                                     |
| xml_etree_generate      | 52.3 ms                                                                  | 53.3 ms: 1.02x slower                                                     |
| mdp                     | 1.67 sec                                                                 | 1.71 sec: 1.02x slower                                                    |
| genshi_xml              | 38.0 ms                                                                  | 39.0 ms: 1.03x slower                                                     |
| pickle_dict             | 18.6 us                                                                  | 19.1 us: 1.03x slower                                                     |
| pathlib                 | 72.9 ms                                                                  | 75.0 ms: 1.03x slower                                                     |
| sympy_str               | 184 ms                                                                   | 191 ms: 1.04x slower                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 2.14 us: 1.04x slower                                                     |
| xml_etree_iterparse     | 61.8 ms                                                                  | 64.4 ms: 1.04x slower                                                     |
| json_loads              | 13.5 us                                                                  | 14.2 us: 1.05x slower                                                     |
| xml_etree_parse         | 92.1 ms                                                                  | 96.6 ms: 1.05x slower                                                     |
| sympy_expand            | 298 ms                                                                   | 314 ms: 1.05x slower                                                      |
| genshi_text             | 17.3 ms                                                                  | 18.3 ms: 1.06x slower                                                     |
| scimark_fft             | 183 ms                                                                   | 194 ms: 1.06x slower                                                      |
| chameleon               | 5.15 ms                                                                  | 5.49 ms: 1.06x slower                                                     |
| pylint                  | 319 ms                                                                   | 340 ms: 1.07x slower                                                      |
| sqlglot_normalize       | 189 ms                                                                   | 202 ms: 1.07x slower                                                      |
| sympy_integrate         | 13.7 ms                                                                  | 14.6 ms: 1.07x slower                                                     |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.82 ms: 1.07x slower                                                     |
| coroutines              | 14.8 ms                                                                  | 15.9 ms: 1.07x slower                                                     |
| sympy_sum               | 98.9 ms                                                                  | 106 ms: 1.08x slower                                                      |
| pickle_list             | 2.70 us                                                                  | 2.91 us: 1.08x slower                                                     |
| python_startup          | 18.4 ms                                                                  | 19.8 ms: 1.08x slower                                                     |
| deepcopy                | 240 us                                                                   | 258 us: 1.08x slower                                                      |
| pickle                  | 6.47 us                                                                  | 7.00 us: 1.08x slower                                                     |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 11.5 ms: 1.10x slower                                                     |
| bench_thread_pool       | 856 us                                                                   | 944 us: 1.10x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.86 us: 1.11x slower                                                     |
| regex_effbot            | 1.63 ms                                                                  | 1.81 ms: 1.11x slower                                                     |
| regex_v8                | 13.5 ms                                                                  | 15.0 ms: 1.11x slower                                                     |
| sqlglot_optimize        | 34.5 ms                                                                  | 38.5 ms: 1.12x slower                                                     |
| pprint_pformat          | 1.05 sec                                                                 | 1.18 sec: 1.12x slower                                                    |
| pprint_safe_repr        | 512 ms                                                                   | 576 ms: 1.13x slower                                                      |
| dulwich_log             | 43.4 ms                                                                  | 49.0 ms: 1.13x slower                                                     |
| unpickle                | 8.01 us                                                                  | 9.05 us: 1.13x slower                                                     |
| 2to3                    | 204 ms                                                                   | 231 ms: 1.13x slower                                                      |
| aiohttp                 | 864 us                                                                   | 980 us: 1.13x slower                                                      |
| float                   | 53.3 ms                                                                  | 60.6 ms: 1.14x slower                                                     |
| regex_dna               | 115 ms                                                                   | 132 ms: 1.15x slower                                                      |
| deepcopy_memo           | 25.3 us                                                                  | 29.1 us: 1.15x slower                                                     |
| spectral_norm           | 71.8 ms                                                                  | 82.5 ms: 1.15x slower                                                     |
| regex_compile           | 89.7 ms                                                                  | 103 ms: 1.15x slower                                                      |
| docutils                | 1.59 sec                                                                 | 1.84 sec: 1.16x slower                                                    |
| json_dumps              | 7.71 ms                                                                  | 8.93 ms: 1.16x slower                                                     |
| create_gc_cycles        | 666 us                                                                   | 776 us: 1.17x slower                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 42.7 ms: 1.17x slower                                                     |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 97.2 ms: 1.17x slower                                                     |
| dask                    | 267 ms                                                                   | 314 ms: 1.18x slower                                                      |
| tornado_http            | 91.8 ms                                                                  | 109 ms: 1.19x slower                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 615 ms: 1.20x slower                                                      |
| scimark_monte_carlo     | 45.8 ms                                                                  | 55.2 ms: 1.20x slower                                                     |
| unpickle_pure_python    | 150 us                                                                   | 180 us: 1.21x slower                                                      |
| hexiom                  | 4.46 ms                                                                  | 5.38 ms: 1.21x slower                                                     |
| mypy2                   | 276 ms                                                                   | 338 ms: 1.22x slower                                                      |
| django_template         | 23.9 ms                                                                  | 29.2 ms: 1.22x slower                                                     |
| mako                    | 7.20 ms                                                                  | 8.84 ms: 1.23x slower                                                     |
| chaos                   | 47.3 ms                                                                  | 58.2 ms: 1.23x slower                                                     |
| thrift                  | 487 us                                                                   | 605 us: 1.24x slower                                                      |
| pycparser               | 686 ms                                                                   | 855 ms: 1.25x slower                                                      |
| html5lib                | 38.5 ms                                                                  | 48.2 ms: 1.25x slower                                                     |
| async_generators        | 180 ms                                                                   | 227 ms: 1.26x slower                                                      |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.45 ms: 1.28x slower                                                     |
| raytrace                | 206 ms                                                                   | 266 ms: 1.29x slower                                                      |
| pyflate                 | 302 ms                                                                   | 393 ms: 1.30x slower                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 63.1 ms: 1.31x slower                                                     |
| async_tree_memoization  | 374 ms                                                                   | 490 ms: 1.31x slower                                                      |
| pickle_pure_python      | 203 us                                                                   | 267 us: 1.31x slower                                                      |
| richards                | 32.1 ms                                                                  | 42.3 ms: 1.32x slower                                                     |
| sqlglot_parse           | 929 us                                                                   | 1.23 ms: 1.32x slower                                                     |
| scimark_lu              | 62.8 ms                                                                  | 83.2 ms: 1.32x slower                                                     |
| async_tree_none         | 313 ms                                                                   | 417 ms: 1.33x slower                                                      |
| scimark_sor             | 77.7 ms                                                                  | 104 ms: 1.34x slower                                                      |
| logging_silent          | 71.0 ns                                                                  | 99.1 ns: 1.40x slower                                                     |
| async_tree_io           | 744 ms                                                                   | 1.05 sec: 1.41x slower                                                    |
| go                      | 97.5 ms                                                                  | 138 ms: 1.42x slower                                                      |
| deltablue               | 2.68 ms                                                                  | 4.16 ms: 1.56x slower                                                     |
| Geometric mean          | (ref)                                                                    | 1.12x slower                                                              |

Benchmark hidden because not significant (4): json, flaskblogging, nqueens, asyncio_tcp
