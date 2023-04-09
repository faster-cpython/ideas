
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 3516704
- commit date: 2023-04-08
- overall geometric mean: 1.08x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 207 ms: 1.01x slower                                        |
| chameleon      | 5.15 ms                                                                  | 4.62 ms: 1.11x faster                                       |
| docutils       | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                      |
| html5lib       | 38.5 ms                                                                  | 36.7 ms: 1.05x faster                                       |
| tornado_http   | 91.8 ms                                                                  | 89.7 ms: 1.02x faster                                       |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 56.5 ms: 1.25x faster                                       |
| float          | 53.3 ms                                                                  | 48.1 ms: 1.11x faster                                       |
| pidigits       | 147 ms                                                                   | 148 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 83.5 ms: 1.07x faster                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.53 ms: 1.06x faster                                       |
| regex_v8       | 13.5 ms                                                                  | 13.2 ms: 1.02x faster                                       |
| regex_dna      | 115 ms                                                                   | 123 ms: 1.06x slower                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.39 ms: 1.43x faster                                       |
| unpickle_pure_python | 150 us                                                                   | 127 us: 1.17x faster                                        |
| pickle_pure_python   | 203 us                                                                   | 184 us: 1.10x faster                                        |
| json_loads           | 13.5 us                                                                  | 13.0 us: 1.04x faster                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.2 ms: 1.04x faster                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 89.9 ms: 1.02x faster                                       |
| unpickle_list        | 2.80 us                                                                  | 2.74 us: 1.02x faster                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.7 ms: 1.01x faster                                       |
| pickle_dict          | 18.6 us                                                                  | 19.1 us: 1.02x slower                                       |
| unpickle             | 8.01 us                                                                  | 8.29 us: 1.03x slower                                       |
| pickle_list          | 2.70 us                                                                  | 2.82 us: 1.04x slower                                       |
| pickle               | 6.47 us                                                                  | 6.93 us: 1.07x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                       |
| python_startup_no_site | 15.4 ms                                                                  | 16.1 ms: 1.05x slower                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.8 ms: 1.25x faster                                       |
| genshi_xml      | 38.0 ms                                                                  | 30.5 ms: 1.25x faster                                       |
| mako            | 7.20 ms                                                                  | 6.22 ms: 1.16x faster                                       |
| django_template | 23.9 ms                                                                  | 21.1 ms: 1.13x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.19x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230408-pythonperf1-amd64-python-main-3.12.0a7+-3516704 |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| generators              | 33.5 ms                                                                  | 20.7 ms: 1.62x faster                                       |
| unpack_sequence         | 43.1 ns                                                                  | 28.2 ns: 1.53x faster                                       |
| json_dumps              | 7.71 ms                                                                  | 5.39 ms: 1.43x faster                                       |
| asyncio_tcp             | 674 ms                                                                   | 487 ms: 1.38x faster                                        |
| deltablue               | 2.68 ms                                                                  | 1.94 ms: 1.38x faster                                       |
| logging_silent          | 71.0 ns                                                                  | 54.4 ns: 1.30x faster                                       |
| richards                | 32.1 ms                                                                  | 25.2 ms: 1.27x faster                                       |
| mypy2                   | 276 ms                                                                   | 219 ms: 1.26x faster                                        |
| nbody                   | 70.9 ms                                                                  | 56.5 ms: 1.25x faster                                       |
| genshi_text             | 17.3 ms                                                                  | 13.8 ms: 1.25x faster                                       |
| genshi_xml              | 38.0 ms                                                                  | 30.5 ms: 1.25x faster                                       |
| sqlglot_parse           | 929 us                                                                   | 747 us: 1.24x faster                                        |
| mdp                     | 1.67 sec                                                                 | 1.39 sec: 1.20x faster                                      |
| sqlglot_transpile       | 1.13 ms                                                                  | 947 us: 1.19x faster                                        |
| deepcopy_memo           | 25.3 us                                                                  | 21.3 us: 1.19x faster                                       |
| spectral_norm           | 71.8 ms                                                                  | 60.4 ms: 1.19x faster                                       |
| json                    | 3.20 ms                                                                  | 2.72 ms: 1.18x faster                                       |
| unpickle_pure_python    | 150 us                                                                   | 127 us: 1.17x faster                                        |
| raytrace                | 206 ms                                                                   | 176 ms: 1.17x faster                                        |
| scimark_lu              | 62.8 ms                                                                  | 53.8 ms: 1.17x faster                                       |
| go                      | 97.5 ms                                                                  | 83.8 ms: 1.16x faster                                       |
| mako                    | 7.20 ms                                                                  | 6.22 ms: 1.16x faster                                       |
| nqueens                 | 65.1 ms                                                                  | 56.4 ms: 1.15x faster                                       |
| hexiom                  | 4.46 ms                                                                  | 3.87 ms: 1.15x faster                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.29 ms: 1.15x faster                                       |
| django_template         | 23.9 ms                                                                  | 21.1 ms: 1.13x faster                                       |
| chameleon               | 5.15 ms                                                                  | 4.62 ms: 1.11x faster                                       |
| scimark_fft             | 183 ms                                                                   | 164 ms: 1.11x faster                                        |
| chaos                   | 47.3 ms                                                                  | 42.6 ms: 1.11x faster                                       |
| logging_simple          | 6.60 us                                                                  | 5.94 us: 1.11x faster                                       |
| float                   | 53.3 ms                                                                  | 48.1 ms: 1.11x faster                                       |
| pickle_pure_python      | 203 us                                                                   | 184 us: 1.10x faster                                        |
| deepcopy                | 240 us                                                                   | 218 us: 1.10x faster                                        |
| scimark_monte_carlo     | 45.8 ms                                                                  | 41.6 ms: 1.10x faster                                       |
| pprint_safe_repr        | 512 ms                                                                   | 467 ms: 1.10x faster                                        |
| coroutines              | 14.8 ms                                                                  | 13.6 ms: 1.09x faster                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 470 ms: 1.09x faster                                        |
| pprint_pformat          | 1.05 sec                                                                 | 963 ms: 1.09x faster                                        |
| logging_format          | 7.13 us                                                                  | 6.55 us: 1.09x faster                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.89 us: 1.09x faster                                       |
| coverage                | 55.3 ms                                                                  | 50.8 ms: 1.09x faster                                       |
| comprehensions          | 15.4 us                                                                  | 14.2 us: 1.09x faster                                       |
| sqlglot_normalize       | 189 ms                                                                   | 174 ms: 1.08x faster                                        |
| fannkuch                | 255 ms                                                                   | 236 ms: 1.08x faster                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.0 ms: 1.08x faster                                       |
| regex_compile           | 89.7 ms                                                                  | 83.5 ms: 1.07x faster                                       |
| sympy_expand            | 298 ms                                                                   | 279 ms: 1.07x faster                                        |
| sympy_integrate         | 13.7 ms                                                                  | 12.8 ms: 1.07x faster                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.53 ms: 1.06x faster                                       |
| sympy_str               | 184 ms                                                                   | 174 ms: 1.06x faster                                        |
| meteor_contest          | 74.4 ms                                                                  | 70.5 ms: 1.05x faster                                       |
| scimark_sor             | 77.7 ms                                                                  | 73.7 ms: 1.05x faster                                       |
| pyflate                 | 302 ms                                                                   | 287 ms: 1.05x faster                                        |
| crypto_pyaes            | 48.3 ms                                                                  | 46.0 ms: 1.05x faster                                       |
| html5lib                | 38.5 ms                                                                  | 36.7 ms: 1.05x faster                                       |
| pycparser               | 686 ms                                                                   | 655 ms: 1.05x faster                                        |
| json_loads              | 13.5 us                                                                  | 13.0 us: 1.04x faster                                       |
| xml_etree_process       | 36.6 ms                                                                  | 35.2 ms: 1.04x faster                                       |
| thrift                  | 487 us                                                                   | 473 us: 1.03x faster                                        |
| dulwich_log             | 43.4 ms                                                                  | 42.3 ms: 1.03x faster                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 89.9 ms: 1.02x faster                                       |
| tornado_http            | 91.8 ms                                                                  | 89.7 ms: 1.02x faster                                       |
| docutils                | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                      |
| unpickle_list           | 2.80 us                                                                  | 2.74 us: 1.02x faster                                       |
| regex_v8                | 13.5 ms                                                                  | 13.2 ms: 1.02x faster                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 51.7 ms: 1.01x faster                                       |
| telco                   | 3.93 ms                                                                  | 3.90 ms: 1.01x faster                                       |
| pidigits                | 147 ms                                                                   | 148 ms: 1.01x slower                                        |
| 2to3                    | 204 ms                                                                   | 207 ms: 1.01x slower                                        |
| python_startup          | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                       |
| async_tree_io           | 744 ms                                                                   | 760 ms: 1.02x slower                                        |
| pickle_dict             | 18.6 us                                                                  | 19.1 us: 1.02x slower                                       |
| create_gc_cycles        | 666 us                                                                   | 688 us: 1.03x slower                                        |
| unpickle                | 8.01 us                                                                  | 8.29 us: 1.03x slower                                       |
| pickle_list             | 2.70 us                                                                  | 2.82 us: 1.04x slower                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 16.1 ms: 1.05x slower                                       |
| regex_dna               | 115 ms                                                                   | 123 ms: 1.06x slower                                        |
| pickle                  | 6.47 us                                                                  | 6.93 us: 1.07x slower                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.51 ms: 1.08x slower                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 67.1 ms: 1.10x slower                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.87 us: 1.12x slower                                       |
| async_generators        | 180 ms                                                                   | 211 ms: 1.17x slower                                        |
| pathlib                 | 72.9 ms                                                                  | 85.9 ms: 1.18x slower                                       |
| dask                    | 267 ms                                                                   | 360 ms: 1.35x slower                                        |
| Geometric mean          | (ref)                                                                    | 1.08x faster                                                |

Benchmark hidden because not significant (5): async_tree_memoization, xml_etree_iterparse, sympy_sum, bench_thread_pool, async_tree_none
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
