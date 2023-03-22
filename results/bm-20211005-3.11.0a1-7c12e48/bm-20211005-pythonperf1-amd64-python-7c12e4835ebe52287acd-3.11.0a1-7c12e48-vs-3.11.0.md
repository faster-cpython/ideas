
# Results vs. 3.11.0

- fork: python
- ref: 7c12e4835ebe52287acd
- machine: windows-amd64
- commit hash: 7c12e48
- commit date: 2021-10-05
- overall geometric mean: 1.09x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 222 ms: 1.09x slower                                                       |
| chameleon      | 5.15 ms                                                                  | 5.68 ms: 1.10x slower                                                      |
| docutils       | 1.59 sec                                                                 | 1.73 sec: 1.08x slower                                                     |
| html5lib       | 38.5 ms                                                                  | 41.5 ms: 1.08x slower                                                      |
| tornado_http   | 91.8 ms                                                                  | 97.6 ms: 1.06x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.08x slower                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                   | 150 ms: 1.03x slower                                                       |
| float          | 53.3 ms                                                                  | 57.2 ms: 1.07x slower                                                      |
| nbody          | 70.9 ms                                                                  | 86.8 ms: 1.22x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.11x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.66 ms: 1.02x slower                                                      |
| regex_compile  | 89.7 ms                                                                  | 92.3 ms: 1.03x slower                                                      |
| regex_v8       | 13.5 ms                                                                  | 14.4 ms: 1.07x slower                                                      |
| regex_dna      | 115 ms                                                                   | 129 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.06x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 18.6 us                                                                  | 16.8 us: 1.11x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.56 us: 1.09x faster                                                      |
| pickle               | 6.47 us                                                                  | 6.58 us: 1.02x slower                                                      |
| json_dumps           | 7.71 ms                                                                  | 8.03 ms: 1.04x slower                                                      |
| xml_etree_generate   | 52.3 ms                                                                  | 54.8 ms: 1.05x slower                                                      |
| unpickle             | 8.01 us                                                                  | 8.48 us: 1.06x slower                                                      |
| xml_etree_iterparse  | 61.8 ms                                                                  | 65.6 ms: 1.06x slower                                                      |
| json_loads           | 13.5 us                                                                  | 14.4 us: 1.07x slower                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 98.4 ms: 1.07x slower                                                      |
| xml_etree_process    | 36.6 ms                                                                  | 40.3 ms: 1.10x slower                                                      |
| unpickle_pure_python | 150 us                                                                   | 172 us: 1.15x slower                                                       |
| pickle_pure_python   | 203 us                                                                   | 240 us: 1.18x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.04x slower                                                               |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.6 ms: 1.01x slower                                                      |
| python_startup         | 18.4 ms                                                                  | 20.7 ms: 1.13x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.07x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 37.8 ms: 1.01x faster                                                      |
| django_template | 23.9 ms                                                                  | 25.8 ms: 1.08x slower                                                      |
| mako            | 7.20 ms                                                                  | 8.12 ms: 1.13x slower                                                      |
| Geometric mean  | (ref)                                                                    | 1.05x slower                                                               |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| logging_format          | 7.13 us                                                                  | 5.64 us: 1.26x faster                                                      |
| logging_simple          | 6.60 us                                                                  | 5.24 us: 1.26x faster                                                      |
| generators              | 33.5 ms                                                                  | 28.9 ms: 1.16x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 16.8 us: 1.11x faster                                                      |
| unpickle_list           | 2.80 us                                                                  | 2.56 us: 1.09x faster                                                      |
| asyncio_tcp             | 674 ms                                                                   | 628 ms: 1.07x faster                                                       |
| json                    | 3.20 ms                                                                  | 3.01 ms: 1.06x faster                                                      |
| mdp                     | 1.67 sec                                                                 | 1.58 sec: 1.06x faster                                                     |
| async_tree_none         | 313 ms                                                                   | 296 ms: 1.06x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 41.7 ns: 1.03x faster                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.37 ms: 1.02x faster                                                      |
| genshi_xml              | 38.0 ms                                                                  | 37.8 ms: 1.01x faster                                                      |
| flaskblogging           | 2.04 sec                                                                 | 2.05 sec: 1.00x slower                                                     |
| meteor_contest          | 74.4 ms                                                                  | 75.3 ms: 1.01x slower                                                      |
| telco                   | 3.93 ms                                                                  | 3.98 ms: 1.01x slower                                                      |
| python_startup_no_site  | 15.4 ms                                                                  | 15.6 ms: 1.01x slower                                                      |
| sympy_sum               | 98.9 ms                                                                  | 100 ms: 1.01x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.58 us: 1.02x slower                                                      |
| regex_effbot            | 1.63 ms                                                                  | 1.66 ms: 1.02x slower                                                      |
| sympy_str               | 184 ms                                                                   | 188 ms: 1.02x slower                                                       |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 10.7 ms: 1.02x slower                                                      |
| async_tree_memoization  | 374 ms                                                                   | 384 ms: 1.03x slower                                                       |
| pidigits                | 147 ms                                                                   | 150 ms: 1.03x slower                                                       |
| regex_compile           | 89.7 ms                                                                  | 92.3 ms: 1.03x slower                                                      |
| bench_mp_pool           | 61.2 ms                                                                  | 63.0 ms: 1.03x slower                                                      |
| sympy_expand            | 298 ms                                                                   | 309 ms: 1.04x slower                                                       |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 86.3 ms: 1.04x slower                                                      |
| nqueens                 | 65.1 ms                                                                  | 67.7 ms: 1.04x slower                                                      |
| json_dumps              | 7.71 ms                                                                  | 8.03 ms: 1.04x slower                                                      |
| async_tree_io           | 744 ms                                                                   | 777 ms: 1.04x slower                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 54.8 ms: 1.05x slower                                                      |
| sympy_integrate         | 13.7 ms                                                                  | 14.4 ms: 1.05x slower                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 2.16 us: 1.05x slower                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 541 ms: 1.06x slower                                                       |
| unpickle                | 8.01 us                                                                  | 8.48 us: 1.06x slower                                                      |
| dulwich_log             | 43.4 ms                                                                  | 46.1 ms: 1.06x slower                                                      |
| xml_etree_iterparse     | 61.8 ms                                                                  | 65.6 ms: 1.06x slower                                                      |
| tornado_http            | 91.8 ms                                                                  | 97.6 ms: 1.06x slower                                                      |
| sqlglot_normalize       | 189 ms                                                                   | 201 ms: 1.06x slower                                                       |
| json_loads              | 13.5 us                                                                  | 14.4 us: 1.07x slower                                                      |
| regex_v8                | 13.5 ms                                                                  | 14.4 ms: 1.07x slower                                                      |
| xml_etree_parse         | 92.1 ms                                                                  | 98.4 ms: 1.07x slower                                                      |
| deepcopy                | 240 us                                                                   | 256 us: 1.07x slower                                                       |
| bench_thread_pool       | 856 us                                                                   | 915 us: 1.07x slower                                                       |
| float                   | 53.3 ms                                                                  | 57.2 ms: 1.07x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.80 us: 1.08x slower                                                      |
| html5lib                | 38.5 ms                                                                  | 41.5 ms: 1.08x slower                                                      |
| richards                | 32.1 ms                                                                  | 34.7 ms: 1.08x slower                                                      |
| django_template         | 23.9 ms                                                                  | 25.8 ms: 1.08x slower                                                      |
| docutils                | 1.59 sec                                                                 | 1.73 sec: 1.08x slower                                                     |
| 2to3                    | 204 ms                                                                   | 222 ms: 1.09x slower                                                       |
| raytrace                | 206 ms                                                                   | 224 ms: 1.09x slower                                                       |
| fannkuch                | 255 ms                                                                   | 279 ms: 1.09x slower                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 37.8 ms: 1.10x slower                                                      |
| thrift                  | 487 us                                                                   | 535 us: 1.10x slower                                                       |
| async_generators        | 180 ms                                                                   | 198 ms: 1.10x slower                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 40.3 ms: 1.10x slower                                                      |
| chameleon               | 5.15 ms                                                                  | 5.68 ms: 1.10x slower                                                      |
| dask                    | 267 ms                                                                   | 295 ms: 1.10x slower                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 1.16 sec: 1.11x slower                                                     |
| go                      | 97.5 ms                                                                  | 108 ms: 1.11x slower                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 570 ms: 1.11x slower                                                       |
| regex_dna               | 115 ms                                                                   | 129 ms: 1.12x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 20.7 ms: 1.13x slower                                                      |
| mako                    | 7.20 ms                                                                  | 8.12 ms: 1.13x slower                                                      |
| deepcopy_memo           | 25.3 us                                                                  | 28.6 us: 1.13x slower                                                      |
| pycparser               | 686 ms                                                                   | 777 ms: 1.13x slower                                                       |
| unpickle_pure_python    | 150 us                                                                   | 172 us: 1.15x slower                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 52.6 ms: 1.15x slower                                                      |
| hexiom                  | 4.46 ms                                                                  | 5.17 ms: 1.16x slower                                                      |
| chaos                   | 47.3 ms                                                                  | 55.0 ms: 1.16x slower                                                      |
| deltablue               | 2.68 ms                                                                  | 3.12 ms: 1.17x slower                                                      |
| logging_silent          | 71.0 ns                                                                  | 83.4 ns: 1.17x slower                                                      |
| spectral_norm           | 71.8 ms                                                                  | 84.7 ms: 1.18x slower                                                      |
| scimark_fft             | 183 ms                                                                   | 216 ms: 1.18x slower                                                       |
| pickle_pure_python      | 203 us                                                                   | 240 us: 1.18x slower                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 57.7 ms: 1.19x slower                                                      |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 3.18 ms: 1.21x slower                                                      |
| pyflate                 | 302 ms                                                                   | 365 ms: 1.21x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 17.9 ms: 1.21x slower                                                      |
| create_gc_cycles        | 666 us                                                                   | 807 us: 1.21x slower                                                       |
| nbody                   | 70.9 ms                                                                  | 86.8 ms: 1.22x slower                                                      |
| comprehensions          | 15.4 us                                                                  | 19.1 us: 1.25x slower                                                      |
| scimark_lu              | 62.8 ms                                                                  | 83.6 ms: 1.33x slower                                                      |
| scimark_sor             | 77.7 ms                                                                  | 105 ms: 1.35x slower                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.53 ms: 1.36x slower                                                      |
| sqlglot_parse           | 929 us                                                                   | 1.32 ms: 1.42x slower                                                      |
| coverage                | 55.3 ms                                                                  | 261 ms: 4.73x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.09x slower                                                               |

Benchmark hidden because not significant (4): pickle_list, pylint, genshi_text, pathlib
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, mypy2
