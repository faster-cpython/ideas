
# Results vs. 3.11.0

- fork: python
- ref: 3c67ec394faac79d2608
- machine: windows-amd64
- commit hash: 3c67ec3
- commit date: 2023-02-07
- overall geometric mean: 1.10x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 192 ms: 1.06x faster                                                       |
| chameleon      | 5.15 ms                                                                  | 4.41 ms: 1.17x faster                                                      |
| docutils       | 1.59 sec                                                                 | 1.50 sec: 1.06x faster                                                     |
| html5lib       | 38.5 ms                                                                  | 34.1 ms: 1.13x faster                                                      |
| tornado_http   | 91.8 ms                                                                  | 90.5 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 59.1 ms: 1.20x faster                                                      |
| float          | 53.3 ms                                                                  | 47.3 ms: 1.13x faster                                                      |
| pidigits       | 147 ms                                                                   | 146 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 78.8 ms: 1.14x faster                                                      |
| regex_v8       | 13.5 ms                                                                  | 13.7 ms: 1.01x slower                                                      |
| regex_effbot   | 1.63 ms                                                                  | 1.68 ms: 1.03x slower                                                      |
| regex_dna      | 115 ms                                                                   | 121 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.38 ms: 1.43x faster                                                      |
| unpickle_pure_python | 150 us                                                                   | 120 us: 1.25x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 166 us: 1.22x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 33.5 ms: 1.09x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.65 us: 1.06x faster                                                      |
| xml_etree_generate   | 52.3 ms                                                                  | 49.5 ms: 1.06x faster                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 88.5 ms: 1.04x faster                                                      |
| pickle_dict          | 18.6 us                                                                  | 18.5 us: 1.01x faster                                                      |
| pickle               | 6.47 us                                                                  | 6.77 us: 1.05x slower                                                      |
| json_loads           | 13.5 us                                                                  | 14.2 us: 1.05x slower                                                      |
| unpickle             | 8.01 us                                                                  | 9.39 us: 1.17x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                               |

Benchmark hidden because not significant (2): pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.2 ms: 1.21x faster                                                      |
| django_template | 23.9 ms                                                                  | 20.2 ms: 1.18x faster                                                      |
| mako            | 7.20 ms                                                                  | 6.15 ms: 1.17x faster                                                      |
| genshi_xml      | 38.0 ms                                                                  | 32.6 ms: 1.17x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.18x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 25.6 ns: 1.68x faster                                                      |
| asyncio_tcp             | 674 ms                                                                   | 466 ms: 1.44x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.38 ms: 1.43x faster                                                      |
| deltablue               | 2.68 ms                                                                  | 1.96 ms: 1.37x faster                                                      |
| richards                | 32.1 ms                                                                  | 23.9 ms: 1.34x faster                                                      |
| mypy2                   | 276 ms                                                                   | 208 ms: 1.33x faster                                                       |
| comprehensions          | 15.4 us                                                                  | 11.7 us: 1.32x faster                                                      |
| unpickle_pure_python    | 150 us                                                                   | 120 us: 1.25x faster                                                       |
| go                      | 97.5 ms                                                                  | 78.8 ms: 1.24x faster                                                      |
| pickle_pure_python      | 203 us                                                                   | 166 us: 1.22x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 58.1 ns: 1.22x faster                                                      |
| genshi_text             | 17.3 ms                                                                  | 14.2 ms: 1.21x faster                                                      |
| scimark_monte_carlo     | 45.8 ms                                                                  | 37.9 ms: 1.21x faster                                                      |
| raytrace                | 206 ms                                                                   | 170 ms: 1.21x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.18 ms: 1.21x faster                                                      |
| fannkuch                | 255 ms                                                                   | 213 ms: 1.20x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 21.1 us: 1.20x faster                                                      |
| nbody                   | 70.9 ms                                                                  | 59.1 ms: 1.20x faster                                                      |
| hexiom                  | 4.46 ms                                                                  | 3.73 ms: 1.20x faster                                                      |
| chaos                   | 47.3 ms                                                                  | 39.6 ms: 1.19x faster                                                      |
| nqueens                 | 65.1 ms                                                                  | 54.6 ms: 1.19x faster                                                      |
| django_template         | 23.9 ms                                                                  | 20.2 ms: 1.18x faster                                                      |
| mako                    | 7.20 ms                                                                  | 6.15 ms: 1.17x faster                                                      |
| chameleon               | 5.15 ms                                                                  | 4.41 ms: 1.17x faster                                                      |
| genshi_xml              | 38.0 ms                                                                  | 32.6 ms: 1.17x faster                                                      |
| spectral_norm           | 71.8 ms                                                                  | 61.5 ms: 1.17x faster                                                      |
| scimark_sor             | 77.7 ms                                                                  | 67.0 ms: 1.16x faster                                                      |
| pprint_pformat          | 1.05 sec                                                                 | 907 ms: 1.16x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 445 ms: 1.15x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 78.8 ms: 1.14x faster                                                      |
| json                    | 3.20 ms                                                                  | 2.81 ms: 1.14x faster                                                      |
| logging_format          | 7.13 us                                                                  | 6.28 us: 1.14x faster                                                      |
| deepcopy                | 240 us                                                                   | 211 us: 1.13x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.48 sec: 1.13x faster                                                     |
| pyflate                 | 302 ms                                                                   | 267 ms: 1.13x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 34.1 ms: 1.13x faster                                                      |
| float                   | 53.3 ms                                                                  | 47.3 ms: 1.13x faster                                                      |
| sympy_str               | 184 ms                                                                   | 164 ms: 1.13x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 269 ms: 1.11x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 171 ms: 1.11x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 89.5 ms: 1.11x faster                                                      |
| sympy_integrate         | 13.7 ms                                                                  | 12.4 ms: 1.10x faster                                                      |
| scimark_fft             | 183 ms                                                                   | 166 ms: 1.10x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.01 us: 1.10x faster                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 44.0 ms: 1.10x faster                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 1.88 us: 1.10x faster                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 33.5 ms: 1.09x faster                                                      |
| sqlglot_parse           | 929 us                                                                   | 851 us: 1.09x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.6 ms: 1.09x faster                                                      |
| pycparser               | 686 ms                                                                   | 633 ms: 1.08x faster                                                       |
| async_generators        | 180 ms                                                                   | 167 ms: 1.08x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.05 ms: 1.08x faster                                                      |
| meteor_contest          | 74.4 ms                                                                  | 69.1 ms: 1.08x faster                                                      |
| thrift                  | 487 us                                                                   | 452 us: 1.08x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 58.7 ms: 1.07x faster                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 480 ms: 1.07x faster                                                       |
| coverage                | 55.3 ms                                                                  | 51.8 ms: 1.07x faster                                                      |
| docutils                | 1.59 sec                                                                 | 1.50 sec: 1.06x faster                                                     |
| 2to3                    | 204 ms                                                                   | 192 ms: 1.06x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.65 us: 1.06x faster                                                      |
| xml_etree_generate      | 52.3 ms                                                                  | 49.5 ms: 1.06x faster                                                      |
| telco                   | 3.93 ms                                                                  | 3.72 ms: 1.05x faster                                                      |
| async_tree_memoization  | 374 ms                                                                   | 356 ms: 1.05x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 88.5 ms: 1.04x faster                                                      |
| bench_thread_pool       | 856 us                                                                   | 823 us: 1.04x faster                                                       |
| async_tree_none         | 313 ms                                                                   | 302 ms: 1.04x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.9 ms: 1.04x faster                                                      |
| generators              | 33.5 ms                                                                  | 33.0 ms: 1.02x faster                                                      |
| tornado_http            | 91.8 ms                                                                  | 90.5 ms: 1.02x faster                                                      |
| python_startup          | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 18.5 us: 1.01x faster                                                      |
| pidigits                | 147 ms                                                                   | 146 ms: 1.00x faster                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 61.7 ms: 1.01x slower                                                      |
| pathlib                 | 72.9 ms                                                                  | 73.7 ms: 1.01x slower                                                      |
| regex_v8                | 13.5 ms                                                                  | 13.7 ms: 1.01x slower                                                      |
| create_gc_cycles        | 666 us                                                                   | 676 us: 1.01x slower                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.68 ms: 1.03x slower                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.45 ms: 1.03x slower                                                      |
| pickle                  | 6.47 us                                                                  | 6.77 us: 1.05x slower                                                      |
| json_loads              | 13.5 us                                                                  | 14.2 us: 1.05x slower                                                      |
| regex_dna               | 115 ms                                                                   | 121 ms: 1.05x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.82 us: 1.09x slower                                                      |
| unpickle                | 8.01 us                                                                  | 9.39 us: 1.17x slower                                                      |
| dask                    | 267 ms                                                                   | 349 ms: 1.31x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.10x faster                                                               |

Benchmark hidden because not significant (5): pickle_list, coroutines, python_startup_no_site, async_tree_io, xml_etree_iterparse
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
