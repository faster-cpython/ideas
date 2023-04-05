
# Results vs. 3.11.0

- fork: python
- ref: c4170c36b0b54c10456f
- machine: windows-amd64
- commit hash: c4170c3
- commit date: 2023-01-29
- overall geometric mean: 1.10x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 199 ms: 1.03x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.43 ms: 1.16x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.53 sec: 1.04x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 35.1 ms: 1.10x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 61.8 ms: 1.15x faster                                                       |
| float          | 53.3 ms                                                                  | 48.2 ms: 1.10x faster                                                       |
| pidigits       | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 79.7 ms: 1.13x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| regex_dna      | 115 ms                                                                   | 121 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.15 ms: 1.50x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 120 us: 1.24x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 176 us: 1.15x faster                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 34.3 ms: 1.07x faster                                                       |
| json_loads           | 13.5 us                                                                  | 12.8 us: 1.06x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 87.3 ms: 1.05x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 50.1 ms: 1.04x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.78 us: 1.01x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.5 us: 1.01x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.3 ms: 1.02x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.78 us: 1.03x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.73 us: 1.04x slower                                                       |
| unpickle             | 8.01 us                                                                  | 8.95 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 19.0 ms: 1.04x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 16.3 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 30.8 ms: 1.24x faster                                                       |
| genshi_text     | 17.3 ms                                                                  | 14.0 ms: 1.23x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.16 ms: 1.17x faster                                                       |
| django_template | 23.9 ms                                                                  | 20.9 ms: 1.14x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.19x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4+-c4170c3 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 26.2 ns: 1.64x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.15 ms: 1.50x faster                                                       |
| richards                | 32.1 ms                                                                  | 23.1 ms: 1.39x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 489 ms: 1.38x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 1.99 ms: 1.35x faster                                                       |
| comprehensions          | 15.4 us                                                                  | 12.0 us: 1.28x faster                                                       |
| mypy2                   | 276 ms                                                                   | 216 ms: 1.28x faster                                                        |
| logging_silent          | 71.0 ns                                                                  | 55.7 ns: 1.27x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 61.9 ms: 1.26x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 120 us: 1.24x faster                                                        |
| genshi_xml              | 38.0 ms                                                                  | 30.8 ms: 1.24x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 37.0 ms: 1.24x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 14.0 ms: 1.23x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 20.8 us: 1.22x faster                                                       |
| go                      | 97.5 ms                                                                  | 80.6 ms: 1.21x faster                                                       |
| raytrace                | 206 ms                                                                   | 171 ms: 1.21x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 3.76 ms: 1.19x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.70 ms: 1.19x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 60.8 ms: 1.18x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.16 ms: 1.17x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.43 ms: 1.16x faster                                                       |
| pyflate                 | 302 ms                                                                   | 260 ms: 1.16x faster                                                        |
| sympy_str               | 184 ms                                                                   | 159 ms: 1.16x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.27 ms: 1.16x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 176 us: 1.15x faster                                                        |
| nqueens                 | 65.1 ms                                                                  | 56.4 ms: 1.15x faster                                                       |
| deepcopy                | 240 us                                                                   | 208 us: 1.15x faster                                                        |
| nbody                   | 70.9 ms                                                                  | 61.8 ms: 1.15x faster                                                       |
| django_template         | 23.9 ms                                                                  | 20.9 ms: 1.14x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 41.6 ms: 1.14x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 79.7 ms: 1.13x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 935 ms: 1.12x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 170 ms: 1.11x faster                                                        |
| scimark_lu              | 62.8 ms                                                                  | 56.7 ms: 1.11x faster                                                       |
| float                   | 53.3 ms                                                                  | 48.2 ms: 1.10x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.52 sec: 1.10x faster                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 1.87 us: 1.10x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 271 ms: 1.10x faster                                                        |
| pprint_safe_repr        | 512 ms                                                                   | 465 ms: 1.10x faster                                                        |
| html5lib                | 38.5 ms                                                                  | 35.1 ms: 1.10x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 167 ms: 1.10x faster                                                        |
| logging_format          | 7.13 us                                                                  | 6.54 us: 1.09x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 90.8 ms: 1.09x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.62 ms: 1.09x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.6 ms: 1.08x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.0 ms: 1.08x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 40.3 ms: 1.08x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.05 ms: 1.08x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 45.0 ms: 1.07x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.16 us: 1.07x faster                                                       |
| pycparser               | 686 ms                                                                   | 641 ms: 1.07x faster                                                        |
| meteor_contest          | 74.4 ms                                                                  | 69.6 ms: 1.07x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 34.3 ms: 1.07x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 874 us: 1.06x faster                                                        |
| thrift                  | 487 us                                                                   | 460 us: 1.06x faster                                                        |
| json_loads              | 13.5 us                                                                  | 12.8 us: 1.06x faster                                                       |
| fannkuch                | 255 ms                                                                   | 242 ms: 1.06x faster                                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 87.3 ms: 1.05x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 50.1 ms: 1.04x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.53 sec: 1.04x faster                                                      |
| regex_effbot            | 1.63 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 498 ms: 1.03x faster                                                        |
| bench_thread_pool       | 856 us                                                                   | 833 us: 1.03x faster                                                        |
| 2to3                    | 204 ms                                                                   | 199 ms: 1.03x faster                                                        |
| async_generators        | 180 ms                                                                   | 176 ms: 1.02x faster                                                        |
| coverage                | 55.3 ms                                                                  | 54.1 ms: 1.02x faster                                                       |
| dask                    | 267 ms                                                                   | 263 ms: 1.02x faster                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.78 us: 1.01x faster                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.5 us: 1.01x faster                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.70 us: 1.02x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 74.2 ms: 1.02x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| generators              | 33.5 ms                                                                  | 34.4 ms: 1.02x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.3 ms: 1.02x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.78 us: 1.03x slower                                                       |
| pidigits                | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| async_tree_io           | 744 ms                                                                   | 768 ms: 1.03x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 63.3 ms: 1.03x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 19.0 ms: 1.04x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.73 us: 1.04x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 695 us: 1.04x slower                                                        |
| gc_traversal            | 1.40 ms                                                                  | 1.47 ms: 1.05x slower                                                       |
| regex_dna               | 115 ms                                                                   | 121 ms: 1.05x slower                                                        |
| python_startup_no_site  | 15.4 ms                                                                  | 16.3 ms: 1.06x slower                                                       |
| unpickle                | 8.01 us                                                                  | 8.95 us: 1.12x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.10x faster                                                                |

Benchmark hidden because not significant (4): tornado_http, coroutines, async_tree_none, async_tree_memoization
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
