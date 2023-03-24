
# Results vs. 3.11.0

- fork: python
- ref: 3b9d793efcfd2c00c14f
- machine: windows-amd64
- commit hash: 3b9d793
- commit date: 2022-11-14
- overall geometric mean: 1.07x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 193 ms: 1.06x faster                                                       |
| chameleon      | 5.15 ms                                                                  | 4.59 ms: 1.12x faster                                                      |
| docutils       | 1.59 sec                                                                 | 1.52 sec: 1.05x faster                                                     |
| html5lib       | 38.5 ms                                                                  | 36.4 ms: 1.06x faster                                                      |
| tornado_http   | 91.8 ms                                                                  | 89.5 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 62.3 ms: 1.14x faster                                                      |
| float          | 53.3 ms                                                                  | 48.7 ms: 1.10x faster                                                      |
| pidigits       | 147 ms                                                                   | 146 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 82.3 ms: 1.09x faster                                                      |
| regex_v8       | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                      |
| regex_dna      | 115 ms                                                                   | 120 ms: 1.04x slower                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.70 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.12 ms: 1.51x faster                                                      |
| unpickle_pure_python | 150 us                                                                   | 130 us: 1.15x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 180 us: 1.13x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 33.9 ms: 1.08x faster                                                      |
| xml_etree_generate   | 52.3 ms                                                                  | 49.0 ms: 1.07x faster                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 87.6 ms: 1.05x faster                                                      |
| pickle_list          | 2.70 us                                                                  | 2.62 us: 1.03x faster                                                      |
| json_loads           | 13.5 us                                                                  | 13.3 us: 1.02x faster                                                      |
| pickle_dict          | 18.6 us                                                                  | 18.3 us: 1.02x faster                                                      |
| pickle               | 6.47 us                                                                  | 6.57 us: 1.02x slower                                                      |
| unpickle             | 8.01 us                                                                  | 8.25 us: 1.03x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                               |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.4 ms: 1.20x faster                                                      |
| genshi_xml      | 38.0 ms                                                                  | 32.2 ms: 1.18x faster                                                      |
| mako            | 7.20 ms                                                                  | 6.25 ms: 1.15x faster                                                      |
| django_template | 23.9 ms                                                                  | 21.6 ms: 1.10x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.16x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps              | 7.71 ms                                                                  | 5.12 ms: 1.51x faster                                                      |
| unpack_sequence         | 43.1 ns                                                                  | 30.8 ns: 1.40x faster                                                      |
| mypy2                   | 276 ms                                                                   | 212 ms: 1.31x faster                                                       |
| richards                | 32.1 ms                                                                  | 26.7 ms: 1.20x faster                                                      |
| genshi_text             | 17.3 ms                                                                  | 14.4 ms: 1.20x faster                                                      |
| deltablue               | 2.68 ms                                                                  | 2.24 ms: 1.20x faster                                                      |
| logging_silent          | 71.0 ns                                                                  | 59.9 ns: 1.19x faster                                                      |
| genshi_xml              | 38.0 ms                                                                  | 32.2 ms: 1.18x faster                                                      |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.25 ms: 1.17x faster                                                      |
| json                    | 3.20 ms                                                                  | 2.75 ms: 1.16x faster                                                      |
| go                      | 97.5 ms                                                                  | 84.0 ms: 1.16x faster                                                      |
| mako                    | 7.20 ms                                                                  | 6.25 ms: 1.15x faster                                                      |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.8 ms: 1.15x faster                                                      |
| unpickle_pure_python    | 150 us                                                                   | 130 us: 1.15x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 22.2 us: 1.14x faster                                                      |
| nbody                   | 70.9 ms                                                                  | 62.3 ms: 1.14x faster                                                      |
| spectral_norm           | 71.8 ms                                                                  | 63.1 ms: 1.14x faster                                                      |
| nqueens                 | 65.1 ms                                                                  | 57.5 ms: 1.13x faster                                                      |
| pickle_pure_python      | 203 us                                                                   | 180 us: 1.13x faster                                                       |
| fannkuch                | 255 ms                                                                   | 227 ms: 1.12x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 934 ms: 1.12x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 69.2 ms: 1.12x faster                                                      |
| chameleon               | 5.15 ms                                                                  | 4.59 ms: 1.12x faster                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 458 ms: 1.12x faster                                                       |
| raytrace                | 206 ms                                                                   | 184 ms: 1.12x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 4.00 ms: 1.12x faster                                                      |
| pyflate                 | 302 ms                                                                   | 272 ms: 1.11x faster                                                       |
| deepcopy                | 240 us                                                                   | 217 us: 1.10x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 56.9 ms: 1.10x faster                                                      |
| django_template         | 23.9 ms                                                                  | 21.6 ms: 1.10x faster                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 1.87 us: 1.10x faster                                                      |
| chaos                   | 47.3 ms                                                                  | 43.1 ms: 1.10x faster                                                      |
| mdp                     | 1.67 sec                                                                 | 1.53 sec: 1.10x faster                                                     |
| float                   | 53.3 ms                                                                  | 48.7 ms: 1.10x faster                                                      |
| regex_compile           | 89.7 ms                                                                  | 82.3 ms: 1.09x faster                                                      |
| logging_format          | 7.13 us                                                                  | 6.56 us: 1.09x faster                                                      |
| sqlglot_normalize       | 189 ms                                                                   | 174 ms: 1.08x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 33.9 ms: 1.08x faster                                                      |
| scimark_fft             | 183 ms                                                                   | 170 ms: 1.08x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 865 us: 1.07x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 69.3 ms: 1.07x faster                                                      |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.1 ms: 1.07x faster                                                      |
| xml_etree_generate      | 52.3 ms                                                                  | 49.0 ms: 1.07x faster                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 45.4 ms: 1.06x faster                                                      |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.06 ms: 1.06x faster                                                      |
| coverage                | 55.3 ms                                                                  | 52.0 ms: 1.06x faster                                                      |
| sympy_integrate         | 13.7 ms                                                                  | 12.9 ms: 1.06x faster                                                      |
| sympy_expand            | 298 ms                                                                   | 282 ms: 1.06x faster                                                       |
| 2to3                    | 204 ms                                                                   | 193 ms: 1.06x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 36.4 ms: 1.06x faster                                                      |
| pycparser               | 686 ms                                                                   | 650 ms: 1.05x faster                                                       |
| sympy_str               | 184 ms                                                                   | 175 ms: 1.05x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 87.6 ms: 1.05x faster                                                      |
| docutils                | 1.59 sec                                                                 | 1.52 sec: 1.05x faster                                                     |
| logging_simple          | 6.60 us                                                                  | 6.31 us: 1.05x faster                                                      |
| async_generators        | 180 ms                                                                   | 173 ms: 1.04x faster                                                       |
| dask                    | 267 ms                                                                   | 258 ms: 1.04x faster                                                       |
| pickle_list             | 2.70 us                                                                  | 2.62 us: 1.03x faster                                                      |
| sympy_sum               | 98.9 ms                                                                  | 96.1 ms: 1.03x faster                                                      |
| tornado_http            | 91.8 ms                                                                  | 89.5 ms: 1.03x faster                                                      |
| bench_thread_pool       | 856 us                                                                   | 835 us: 1.03x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.3 us: 1.02x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 18.3 us: 1.02x faster                                                      |
| python_startup          | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| dulwich_log             | 43.4 ms                                                                  | 43.1 ms: 1.01x faster                                                      |
| pidigits                | 147 ms                                                                   | 146 ms: 1.00x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.95 ms: 1.01x slower                                                      |
| coroutines              | 14.8 ms                                                                  | 15.0 ms: 1.01x slower                                                      |
| pickle                  | 6.47 us                                                                  | 6.57 us: 1.02x slower                                                      |
| regex_v8                | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.44 ms: 1.02x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.71 us: 1.02x slower                                                      |
| unpickle                | 8.01 us                                                                  | 8.25 us: 1.03x slower                                                      |
| async_tree_memoization  | 374 ms                                                                   | 386 ms: 1.03x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 325 ms: 1.04x slower                                                       |
| regex_dna               | 115 ms                                                                   | 120 ms: 1.04x slower                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.70 ms: 1.04x slower                                                      |
| asyncio_tcp             | 674 ms                                                                   | 708 ms: 1.05x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 783 ms: 1.05x slower                                                       |
| generators              | 33.5 ms                                                                  | 35.7 ms: 1.06x slower                                                      |
| thrift                  | 487 us                                                                   | 558 us: 1.15x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.07x faster                                                               |

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, xml_etree_iterparse, pathlib, unpickle_list, create_gc_cycles, comprehensions, bench_mp_pool, python_startup_no_site
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
