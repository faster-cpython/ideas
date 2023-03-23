
# Results vs. 3.11.0

- fork: python
- ref: 2cd268a3a9340346dd86
- machine: windows-amd64
- commit hash: 2cd268a
- commit date: 2021-12-06
- overall geometric mean: 1.12x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 232 ms: 1.14x slower                                                     |
| chameleon      | 5.15 ms                                                                  | 5.89 ms: 1.14x slower                                                    |
| docutils       | 1.59 sec                                                                 | 1.88 sec: 1.18x slower                                                   |
| html5lib       | 38.5 ms                                                                  | 48.7 ms: 1.26x slower                                                    |
| tornado_http   | 91.8 ms                                                                  | 109 ms: 1.19x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.18x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                   | 149 ms: 1.02x slower                                                     |
| nbody          | 70.9 ms                                                                  | 77.2 ms: 1.09x slower                                                    |
| float          | 53.3 ms                                                                  | 61.8 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.74 ms: 1.06x slower                                                    |
| regex_v8       | 13.5 ms                                                                  | 15.0 ms: 1.11x slower                                                    |
| regex_dna      | 115 ms                                                                   | 129 ms: 1.12x slower                                                     |
| regex_compile  | 89.7 ms                                                                  | 103 ms: 1.15x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_dict          | 18.6 us                                                                  | 17.0 us: 1.10x faster                                                    |
| unpickle_list        | 2.80 us                                                                  | 2.64 us: 1.06x faster                                                    |
| unpickle             | 8.01 us                                                                  | 8.17 us: 1.02x slower                                                    |
| xml_etree_iterparse  | 61.8 ms                                                                  | 64.6 ms: 1.04x slower                                                    |
| xml_etree_generate   | 52.3 ms                                                                  | 55.0 ms: 1.05x slower                                                    |
| pickle               | 6.47 us                                                                  | 6.84 us: 1.06x slower                                                    |
| xml_etree_parse      | 92.1 ms                                                                  | 98.0 ms: 1.06x slower                                                    |
| json_dumps           | 7.71 ms                                                                  | 8.45 ms: 1.10x slower                                                    |
| json_loads           | 13.5 us                                                                  | 15.0 us: 1.11x slower                                                    |
| unpickle_pure_python | 150 us                                                                   | 177 us: 1.18x slower                                                     |
| xml_etree_process    | 36.6 ms                                                                  | 44.0 ms: 1.20x slower                                                    |
| pickle_pure_python   | 203 us                                                                   | 267 us: 1.31x slower                                                     |
| Geometric mean       | (ref)                                                                    | 1.07x slower                                                             |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.1 ms: 1.02x faster                                                    |
| python_startup         | 18.4 ms                                                                  | 19.7 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 40.9 ms: 1.07x slower                                                    |
| genshi_text     | 17.3 ms                                                                  | 19.6 ms: 1.13x slower                                                    |
| mako            | 7.20 ms                                                                  | 8.56 ms: 1.19x slower                                                    |
| django_template | 23.9 ms                                                                  | 29.2 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|-------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coverage                | 55.3 ms                                                                  | 38.8 ms: 1.42x faster                                                    |
| pickle_dict             | 18.6 us                                                                  | 17.0 us: 1.10x faster                                                    |
| generators              | 33.5 ms                                                                  | 30.7 ms: 1.09x faster                                                    |
| unpack_sequence         | 43.1 ns                                                                  | 40.5 ns: 1.06x faster                                                    |
| unpickle_list           | 2.80 us                                                                  | 2.64 us: 1.06x faster                                                    |
| logging_format          | 7.13 us                                                                  | 6.72 us: 1.06x faster                                                    |
| logging_simple          | 6.60 us                                                                  | 6.24 us: 1.06x faster                                                    |
| gc_traversal            | 1.40 ms                                                                  | 1.37 ms: 1.02x faster                                                    |
| telco                   | 3.93 ms                                                                  | 3.86 ms: 1.02x faster                                                    |
| meteor_contest          | 74.4 ms                                                                  | 73.2 ms: 1.02x faster                                                    |
| python_startup_no_site  | 15.4 ms                                                                  | 15.1 ms: 1.02x faster                                                    |
| bench_mp_pool           | 61.2 ms                                                                  | 60.4 ms: 1.01x faster                                                    |
| pidigits                | 147 ms                                                                   | 149 ms: 1.02x slower                                                     |
| unpickle                | 8.01 us                                                                  | 8.17 us: 1.02x slower                                                    |
| mdp                     | 1.67 sec                                                                 | 1.72 sec: 1.03x slower                                                   |
| comprehensions          | 15.4 us                                                                  | 15.8 us: 1.03x slower                                                    |
| sympy_str               | 184 ms                                                                   | 191 ms: 1.04x slower                                                     |
| fannkuch                | 255 ms                                                                   | 266 ms: 1.04x slower                                                     |
| pathlib                 | 72.9 ms                                                                  | 75.9 ms: 1.04x slower                                                    |
| xml_etree_iterparse     | 61.8 ms                                                                  | 64.6 ms: 1.04x slower                                                    |
| deepcopy_reduce         | 2.06 us                                                                  | 2.15 us: 1.05x slower                                                    |
| xml_etree_generate      | 52.3 ms                                                                  | 55.0 ms: 1.05x slower                                                    |
| sympy_sum               | 98.9 ms                                                                  | 104 ms: 1.06x slower                                                     |
| sympy_expand            | 298 ms                                                                   | 316 ms: 1.06x slower                                                     |
| pickle                  | 6.47 us                                                                  | 6.84 us: 1.06x slower                                                    |
| asyncio_tcp             | 674 ms                                                                   | 713 ms: 1.06x slower                                                     |
| deepcopy                | 240 us                                                                   | 254 us: 1.06x slower                                                     |
| xml_etree_parse         | 92.1 ms                                                                  | 98.0 ms: 1.06x slower                                                    |
| regex_effbot            | 1.63 ms                                                                  | 1.74 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.80 ms: 1.07x slower                                                    |
| scimark_fft             | 183 ms                                                                   | 195 ms: 1.07x slower                                                     |
| python_startup          | 18.4 ms                                                                  | 19.7 ms: 1.07x slower                                                    |
| coroutines              | 14.8 ms                                                                  | 15.9 ms: 1.07x slower                                                    |
| genshi_xml              | 38.0 ms                                                                  | 40.9 ms: 1.07x slower                                                    |
| sqlglot_normalize       | 189 ms                                                                   | 203 ms: 1.07x slower                                                     |
| pylint                  | 319 ms                                                                   | 343 ms: 1.08x slower                                                     |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 11.4 ms: 1.09x slower                                                    |
| sympy_integrate         | 13.7 ms                                                                  | 14.9 ms: 1.09x slower                                                    |
| nbody                   | 70.9 ms                                                                  | 77.2 ms: 1.09x slower                                                    |
| json_dumps              | 7.71 ms                                                                  | 8.45 ms: 1.10x slower                                                    |
| spectral_norm           | 71.8 ms                                                                  | 79.4 ms: 1.11x slower                                                    |
| sqlite_synth            | 1.67 us                                                                  | 1.85 us: 1.11x slower                                                    |
| json_loads              | 13.5 us                                                                  | 15.0 us: 1.11x slower                                                    |
| regex_v8                | 13.5 ms                                                                  | 15.0 ms: 1.11x slower                                                    |
| dulwich_log             | 43.4 ms                                                                  | 48.7 ms: 1.12x slower                                                    |
| regex_dna               | 115 ms                                                                   | 129 ms: 1.12x slower                                                     |
| bench_thread_pool       | 856 us                                                                   | 965 us: 1.13x slower                                                     |
| genshi_text             | 17.3 ms                                                                  | 19.6 ms: 1.13x slower                                                    |
| deepcopy_memo           | 25.3 us                                                                  | 28.7 us: 1.13x slower                                                    |
| sqlglot_optimize        | 34.5 ms                                                                  | 39.2 ms: 1.14x slower                                                    |
| 2to3                    | 204 ms                                                                   | 232 ms: 1.14x slower                                                     |
| chameleon               | 5.15 ms                                                                  | 5.89 ms: 1.14x slower                                                    |
| aiohttp                 | 864 us                                                                   | 990 us: 1.15x slower                                                     |
| regex_compile           | 89.7 ms                                                                  | 103 ms: 1.15x slower                                                     |
| create_gc_cycles        | 666 us                                                                   | 770 us: 1.16x slower                                                     |
| float                   | 53.3 ms                                                                  | 61.8 ms: 1.16x slower                                                    |
| pprint_safe_repr        | 512 ms                                                                   | 601 ms: 1.17x slower                                                     |
| docutils                | 1.59 sec                                                                 | 1.88 sec: 1.18x slower                                                   |
| unpickle_pure_python    | 150 us                                                                   | 177 us: 1.18x slower                                                     |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 98.4 ms: 1.18x slower                                                    |
| pprint_pformat          | 1.05 sec                                                                 | 1.24 sec: 1.19x slower                                                   |
| mako                    | 7.20 ms                                                                  | 8.56 ms: 1.19x slower                                                    |
| tornado_http            | 91.8 ms                                                                  | 109 ms: 1.19x slower                                                     |
| dask                    | 267 ms                                                                   | 319 ms: 1.19x slower                                                     |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 615 ms: 1.20x slower                                                     |
| xml_etree_process       | 36.6 ms                                                                  | 44.0 ms: 1.20x slower                                                    |
| hexiom                  | 4.46 ms                                                                  | 5.42 ms: 1.22x slower                                                    |
| django_template         | 23.9 ms                                                                  | 29.2 ms: 1.22x slower                                                    |
| mypy2                   | 276 ms                                                                   | 340 ms: 1.23x slower                                                     |
| async_generators        | 180 ms                                                                   | 224 ms: 1.24x slower                                                     |
| scimark_monte_carlo     | 45.8 ms                                                                  | 56.9 ms: 1.24x slower                                                    |
| chaos                   | 47.3 ms                                                                  | 59.4 ms: 1.25x slower                                                    |
| pycparser               | 686 ms                                                                   | 861 ms: 1.26x slower                                                     |
| html5lib                | 38.5 ms                                                                  | 48.7 ms: 1.26x slower                                                    |
| richards                | 32.1 ms                                                                  | 40.9 ms: 1.27x slower                                                    |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.45 ms: 1.28x slower                                                    |
| thrift                  | 487 us                                                                   | 625 us: 1.28x slower                                                     |
| async_tree_memoization  | 374 ms                                                                   | 484 ms: 1.29x slower                                                     |
| sqlglot_parse           | 929 us                                                                   | 1.21 ms: 1.30x slower                                                    |
| pyflate                 | 302 ms                                                                   | 394 ms: 1.31x slower                                                     |
| pickle_pure_python      | 203 us                                                                   | 267 us: 1.31x slower                                                     |
| raytrace                | 206 ms                                                                   | 273 ms: 1.33x slower                                                     |
| scimark_lu              | 62.8 ms                                                                  | 83.4 ms: 1.33x slower                                                    |
| async_tree_none         | 313 ms                                                                   | 417 ms: 1.33x slower                                                     |
| crypto_pyaes            | 48.3 ms                                                                  | 65.5 ms: 1.36x slower                                                    |
| scimark_sor             | 77.7 ms                                                                  | 106 ms: 1.36x slower                                                     |
| logging_silent          | 71.0 ns                                                                  | 98.0 ns: 1.38x slower                                                    |
| async_tree_io           | 744 ms                                                                   | 1.03 sec: 1.38x slower                                                   |
| go                      | 97.5 ms                                                                  | 137 ms: 1.41x slower                                                     |
| deltablue               | 2.68 ms                                                                  | 4.13 ms: 1.54x slower                                                    |
| Geometric mean          | (ref)                                                                    | 1.12x slower                                                             |

Benchmark hidden because not significant (4): json, pickle_list, flaskblogging, nqueens
