
# Results vs. 3.11.0

- fork: python
- ref: d717be04dc7876696cb2
- machine: windows-amd64
- commit hash: d717be0
- commit date: 2023-01-22
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.37 ms: 1.18x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 35.7 ms: 1.08x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 88.8 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 59.7 ms: 1.19x faster                                                       |
| float          | 53.3 ms                                                                  | 47.2 ms: 1.13x faster                                                       |
| pidigits       | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 78.1 ms: 1.15x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.54 ms: 1.06x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.6 ms: 1.01x slower                                                       |
| regex_dna      | 115 ms                                                                   | 117 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.43 ms: 1.42x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 121 us: 1.24x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 171 us: 1.19x faster                                                        |
| json_loads           | 13.5 us                                                                  | 12.8 us: 1.06x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 49.7 ms: 1.05x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.0 ms: 1.04x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.76 us: 1.02x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.3 ms: 1.02x slower                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 94.7 ms: 1.03x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.94 us: 1.07x slower                                                       |
| unpickle             | 8.01 us                                                                  | 9.15 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 19.2 ms: 1.04x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 16.5 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.4 ms: 1.29x faster                                                       |
| django_template | 23.9 ms                                                                  | 20.4 ms: 1.17x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.21 ms: 1.16x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 33.0 ms: 1.15x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.19x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 25.7 ns: 1.68x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.43 ms: 1.42x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 483 ms: 1.40x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 2.02 ms: 1.33x faster                                                       |
| richards                | 32.1 ms                                                                  | 24.2 ms: 1.33x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 13.4 ms: 1.29x faster                                                       |
| mypy2                   | 276 ms                                                                   | 216 ms: 1.28x faster                                                        |
| logging_silent          | 71.0 ns                                                                  | 56.5 ns: 1.26x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 20.2 us: 1.25x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 121 us: 1.24x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.16 ms: 1.22x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 64.2 ms: 1.21x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 3.73 ms: 1.20x faster                                                       |
| raytrace                | 206 ms                                                                   | 173 ms: 1.19x faster                                                        |
| deepcopy                | 240 us                                                                   | 201 us: 1.19x faster                                                        |
| nbody                   | 70.9 ms                                                                  | 59.7 ms: 1.19x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 60.5 ms: 1.19x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 171 us: 1.19x faster                                                        |
| chameleon               | 5.15 ms                                                                  | 4.37 ms: 1.18x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 40.1 ms: 1.18x faster                                                       |
| pyflate                 | 302 ms                                                                   | 258 ms: 1.17x faster                                                        |
| fannkuch                | 255 ms                                                                   | 218 ms: 1.17x faster                                                        |
| django_template         | 23.9 ms                                                                  | 20.4 ms: 1.17x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.75 ms: 1.17x faster                                                       |
| go                      | 97.5 ms                                                                  | 83.7 ms: 1.17x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 55.9 ms: 1.17x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.21 ms: 1.16x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 33.0 ms: 1.15x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 78.1 ms: 1.15x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.80 us: 1.15x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 40.2 ms: 1.14x faster                                                       |
| float                   | 53.3 ms                                                                  | 47.2 ms: 1.13x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.38 us: 1.12x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 945 ms: 1.11x faster                                                        |
| sympy_expand            | 298 ms                                                                   | 271 ms: 1.10x faster                                                        |
| scimark_fft             | 183 ms                                                                   | 167 ms: 1.09x faster                                                        |
| scimark_lu              | 62.8 ms                                                                  | 57.6 ms: 1.09x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 469 ms: 1.09x faster                                                        |
| sympy_str               | 184 ms                                                                   | 169 ms: 1.09x faster                                                        |
| telco                   | 3.93 ms                                                                  | 3.61 ms: 1.09x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 174 ms: 1.09x faster                                                        |
| html5lib                | 38.5 ms                                                                  | 35.7 ms: 1.08x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 863 us: 1.08x faster                                                        |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.06 ms: 1.07x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 45.2 ms: 1.07x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.8 ms: 1.07x faster                                                       |
| thrift                  | 487 us                                                                   | 456 us: 1.07x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.57 sec: 1.06x faster                                                      |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.5 ms: 1.06x faster                                                       |
| json_loads              | 13.5 us                                                                  | 12.8 us: 1.06x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.23 us: 1.06x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.54 ms: 1.06x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 70.3 ms: 1.06x faster                                                       |
| async_generators        | 180 ms                                                                   | 171 ms: 1.05x faster                                                        |
| coverage                | 55.3 ms                                                                  | 52.6 ms: 1.05x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 49.7 ms: 1.05x faster                                                       |
| pycparser               | 686 ms                                                                   | 653 ms: 1.05x faster                                                        |
| xml_etree_process       | 36.6 ms                                                                  | 35.0 ms: 1.04x faster                                                       |
| dask                    | 267 ms                                                                   | 257 ms: 1.04x faster                                                        |
| tornado_http            | 91.8 ms                                                                  | 88.8 ms: 1.03x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 95.6 ms: 1.03x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| comprehensions          | 15.4 us                                                                  | 15.0 us: 1.03x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 42.5 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 502 ms: 1.02x faster                                                        |
| async_tree_none         | 313 ms                                                                   | 308 ms: 1.02x faster                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.76 us: 1.02x faster                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.6 ms: 1.01x faster                                                       |
| 2to3                    | 204 ms                                                                   | 202 ms: 1.01x faster                                                        |
| regex_v8                | 13.5 ms                                                                  | 13.6 ms: 1.01x slower                                                       |
| generators              | 33.5 ms                                                                  | 33.9 ms: 1.01x slower                                                       |
| regex_dna               | 115 ms                                                                   | 117 ms: 1.02x slower                                                        |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.3 ms: 1.02x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 74.8 ms: 1.03x slower                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 94.7 ms: 1.03x slower                                                       |
| pidigits                | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 63.3 ms: 1.03x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 770 ms: 1.04x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.74 us: 1.04x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 19.2 ms: 1.04x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 702 us: 1.05x slower                                                        |
| pickle                  | 6.47 us                                                                  | 6.94 us: 1.07x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 16.5 ms: 1.07x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.51 ms: 1.08x slower                                                       |
| unpickle                | 8.01 us                                                                  | 9.15 us: 1.14x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (3): bench_thread_pool, async_tree_memoization, pickle_list
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
