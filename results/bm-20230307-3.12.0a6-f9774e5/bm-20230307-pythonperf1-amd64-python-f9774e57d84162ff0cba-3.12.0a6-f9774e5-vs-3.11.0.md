
# Results vs. 3.11.0

- fork: python
- ref: f9774e57d84162ff0cba
- machine: windows-amd64
- commit hash: f9774e5
- commit date: 2023-03-07
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 194 ms: 1.05x faster                                                       |
| chameleon      | 5.15 ms                                                                  | 4.76 ms: 1.08x faster                                                      |
| docutils       | 1.59 sec                                                                 | 1.51 sec: 1.06x faster                                                     |
| html5lib       | 38.5 ms                                                                  | 34.8 ms: 1.10x faster                                                      |
| tornado_http   | 91.8 ms                                                                  | 90.6 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 53.3 ms                                                                  | 47.4 ms: 1.13x faster                                                      |
| nbody          | 70.9 ms                                                                  | 63.3 ms: 1.12x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.50 ms: 1.09x faster                                                      |
| regex_compile  | 89.7 ms                                                                  | 83.5 ms: 1.08x faster                                                      |
| regex_v8       | 13.5 ms                                                                  | 13.4 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.51 ms: 1.40x faster                                                      |
| unpickle_pure_python | 150 us                                                                   | 124 us: 1.21x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 175 us: 1.16x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 88.4 ms: 1.04x faster                                                      |
| xml_etree_process    | 36.6 ms                                                                  | 35.6 ms: 1.03x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.74 us: 1.02x faster                                                      |
| json_loads           | 13.5 us                                                                  | 13.4 us: 1.01x faster                                                      |
| pickle_dict          | 18.6 us                                                                  | 18.7 us: 1.00x slower                                                      |
| pickle_list          | 2.70 us                                                                  | 2.80 us: 1.04x slower                                                      |
| pickle               | 6.47 us                                                                  | 6.96 us: 1.08x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                               |

Benchmark hidden because not significant (3): xml_etree_iterparse, unpickle, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| python_startup_no_site | 15.4 ms                                                                  | 15.5 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.9 ms: 1.24x faster                                                      |
| genshi_xml      | 38.0 ms                                                                  | 30.9 ms: 1.23x faster                                                      |
| mako            | 7.20 ms                                                                  | 6.20 ms: 1.16x faster                                                      |
| django_template | 23.9 ms                                                                  | 20.9 ms: 1.14x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.19x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230307-pythonperf1-amd64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 27.9 ns: 1.55x faster                                                      |
| generators              | 33.5 ms                                                                  | 21.9 ms: 1.53x faster                                                      |
| asyncio_tcp             | 674 ms                                                                   | 463 ms: 1.45x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.51 ms: 1.40x faster                                                      |
| deltablue               | 2.68 ms                                                                  | 1.92 ms: 1.39x faster                                                      |
| richards                | 32.1 ms                                                                  | 24.5 ms: 1.31x faster                                                      |
| mypy2                   | 276 ms                                                                   | 211 ms: 1.31x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 56.5 ns: 1.26x faster                                                      |
| genshi_text             | 17.3 ms                                                                  | 13.9 ms: 1.24x faster                                                      |
| genshi_xml              | 38.0 ms                                                                  | 30.9 ms: 1.23x faster                                                      |
| unpickle_pure_python    | 150 us                                                                   | 124 us: 1.21x faster                                                       |
| fannkuch                | 255 ms                                                                   | 216 ms: 1.18x faster                                                       |
| go                      | 97.5 ms                                                                  | 82.6 ms: 1.18x faster                                                      |
| mdp                     | 1.67 sec                                                                 | 1.43 sec: 1.17x faster                                                     |
| json                    | 3.20 ms                                                                  | 2.74 ms: 1.17x faster                                                      |
| hexiom                  | 4.46 ms                                                                  | 3.83 ms: 1.16x faster                                                      |
| pickle_pure_python      | 203 us                                                                   | 175 us: 1.16x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.20 ms: 1.16x faster                                                      |
| nqueens                 | 65.1 ms                                                                  | 56.9 ms: 1.14x faster                                                      |
| django_template         | 23.9 ms                                                                  | 20.9 ms: 1.14x faster                                                      |
| raytrace                | 206 ms                                                                   | 180 ms: 1.14x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 40.4 ms: 1.13x faster                                                      |
| chaos                   | 47.3 ms                                                                  | 42.0 ms: 1.13x faster                                                      |
| sqlglot_normalize       | 189 ms                                                                   | 168 ms: 1.13x faster                                                       |
| float                   | 53.3 ms                                                                  | 47.4 ms: 1.13x faster                                                      |
| deepcopy_memo           | 25.3 us                                                                  | 22.6 us: 1.12x faster                                                      |
| nbody                   | 70.9 ms                                                                  | 63.3 ms: 1.12x faster                                                      |
| pyflate                 | 302 ms                                                                   | 270 ms: 1.12x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 43.3 ms: 1.12x faster                                                      |
| coverage                | 55.3 ms                                                                  | 49.9 ms: 1.11x faster                                                      |
| html5lib                | 38.5 ms                                                                  | 34.8 ms: 1.10x faster                                                      |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.2 ms: 1.10x faster                                                      |
| deepcopy                | 240 us                                                                   | 219 us: 1.09x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 68.0 ms: 1.09x faster                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 1.88 us: 1.09x faster                                                      |
| regex_effbot            | 1.63 ms                                                                  | 1.50 ms: 1.09x faster                                                      |
| logging_format          | 7.13 us                                                                  | 6.55 us: 1.09x faster                                                      |
| scimark_sor             | 77.7 ms                                                                  | 71.6 ms: 1.09x faster                                                      |
| scimark_fft             | 183 ms                                                                   | 169 ms: 1.08x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.10 us: 1.08x faster                                                      |
| chameleon               | 5.15 ms                                                                  | 4.76 ms: 1.08x faster                                                      |
| sympy_expand            | 298 ms                                                                   | 277 ms: 1.08x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 83.5 ms: 1.08x faster                                                      |
| pprint_pformat          | 1.05 sec                                                                 | 977 ms: 1.07x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 478 ms: 1.07x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 58.7 ms: 1.07x faster                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 479 ms: 1.07x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 67.2 ms: 1.07x faster                                                      |
| sqlglot_parse           | 929 us                                                                   | 871 us: 1.07x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.06 ms: 1.07x faster                                                      |
| sympy_str               | 184 ms                                                                   | 173 ms: 1.07x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.0 ms: 1.06x faster                                                      |
| docutils                | 1.59 sec                                                                 | 1.51 sec: 1.06x faster                                                     |
| async_tree_memoization  | 374 ms                                                                   | 356 ms: 1.05x faster                                                       |
| 2to3                    | 204 ms                                                                   | 194 ms: 1.05x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.1 ms: 1.05x faster                                                      |
| xml_etree_parse         | 92.1 ms                                                                  | 88.4 ms: 1.04x faster                                                      |
| bench_thread_pool       | 856 us                                                                   | 827 us: 1.04x faster                                                       |
| pycparser               | 686 ms                                                                   | 663 ms: 1.03x faster                                                       |
| async_tree_none         | 313 ms                                                                   | 304 ms: 1.03x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 42.2 ms: 1.03x faster                                                      |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.56 ms: 1.03x faster                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 35.6 ms: 1.03x faster                                                      |
| sympy_sum               | 98.9 ms                                                                  | 96.6 ms: 1.02x faster                                                      |
| unpickle_list           | 2.80 us                                                                  | 2.74 us: 1.02x faster                                                      |
| thrift                  | 487 us                                                                   | 476 us: 1.02x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.86 ms: 1.02x faster                                                      |
| tornado_http            | 91.8 ms                                                                  | 90.6 ms: 1.01x faster                                                      |
| regex_v8                | 13.5 ms                                                                  | 13.4 ms: 1.01x faster                                                      |
| python_startup          | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| json_loads              | 13.5 us                                                                  | 13.4 us: 1.01x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 18.7 us: 1.00x slower                                                      |
| create_gc_cycles        | 666 us                                                                   | 671 us: 1.01x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.5 ms: 1.01x slower                                                      |
| pathlib                 | 72.9 ms                                                                  | 73.9 ms: 1.01x slower                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.44 ms: 1.03x slower                                                      |
| bench_mp_pool           | 61.2 ms                                                                  | 63.1 ms: 1.03x slower                                                      |
| comprehensions          | 15.4 us                                                                  | 15.9 us: 1.03x slower                                                      |
| pickle_list             | 2.70 us                                                                  | 2.80 us: 1.04x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.79 us: 1.07x slower                                                      |
| pickle                  | 6.47 us                                                                  | 6.96 us: 1.08x slower                                                      |
| async_generators        | 180 ms                                                                   | 223 ms: 1.24x slower                                                       |
| dask                    | 267 ms                                                                   | 352 ms: 1.32x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                               |

Benchmark hidden because not significant (6): xml_etree_iterparse, unpickle, xml_etree_generate, async_tree_io, regex_dna, pidigits
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
