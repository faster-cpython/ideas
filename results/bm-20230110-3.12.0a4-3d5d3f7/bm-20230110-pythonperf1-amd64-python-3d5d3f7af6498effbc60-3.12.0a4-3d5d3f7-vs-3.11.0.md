
# Results vs. 3.11.0

- fork: python
- ref: 3d5d3f7af6498effbc60
- machine: windows-amd64
- commit hash: 3d5d3f7
- commit date: 2023-01-10
- overall geometric mean: 1.11x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 190 ms: 1.07x faster                                                       |
| chameleon      | 5.15 ms                                                                  | 4.34 ms: 1.19x faster                                                      |
| docutils       | 1.59 sec                                                                 | 1.50 sec: 1.07x faster                                                     |
| html5lib       | 38.5 ms                                                                  | 35.3 ms: 1.09x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 56.6 ms: 1.25x faster                                                      |
| float          | 53.3 ms                                                                  | 46.3 ms: 1.15x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.13x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 78.9 ms: 1.14x faster                                                      |
| regex_v8       | 13.5 ms                                                                  | 13.7 ms: 1.01x slower                                                      |
| regex_dna      | 115 ms                                                                   | 121 ms: 1.05x slower                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.73 ms: 1.06x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.36 ms: 1.44x faster                                                      |
| unpickle_pure_python | 150 us                                                                   | 118 us: 1.26x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 166 us: 1.23x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 33.0 ms: 1.11x faster                                                      |
| xml_etree_generate   | 52.3 ms                                                                  | 47.6 ms: 1.10x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.62 us: 1.07x faster                                                      |
| json_loads           | 13.5 us                                                                  | 12.7 us: 1.06x faster                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 87.1 ms: 1.06x faster                                                      |
| pickle_dict          | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                      |
| xml_etree_iterparse  | 61.8 ms                                                                  | 61.1 ms: 1.01x faster                                                      |
| pickle               | 6.47 us                                                                  | 6.79 us: 1.05x slower                                                      |
| unpickle             | 8.01 us                                                                  | 8.68 us: 1.08x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.09x faster                                                               |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.3 ms: 1.30x faster                                                      |
| mako            | 7.20 ms                                                                  | 5.94 ms: 1.21x faster                                                      |
| genshi_xml      | 38.0 ms                                                                  | 31.5 ms: 1.21x faster                                                      |
| django_template | 23.9 ms                                                                  | 20.9 ms: 1.14x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.21x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230110-pythonperf1-amd64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 25.8 ns: 1.67x faster                                                      |
| json_dumps              | 7.71 ms                                                                  | 5.36 ms: 1.44x faster                                                      |
| asyncio_tcp             | 674 ms                                                                   | 474 ms: 1.42x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 1.93 ms: 1.38x faster                                                      |
| richards                | 32.1 ms                                                                  | 23.5 ms: 1.36x faster                                                      |
| mypy2                   | 276 ms                                                                   | 208 ms: 1.33x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 13.3 ms: 1.30x faster                                                      |
| deepcopy_memo           | 25.3 us                                                                  | 19.9 us: 1.28x faster                                                      |
| logging_silent          | 71.0 ns                                                                  | 55.9 ns: 1.27x faster                                                      |
| unpickle_pure_python    | 150 us                                                                   | 118 us: 1.26x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 56.6 ms: 1.25x faster                                                      |
| scimark_sor             | 77.7 ms                                                                  | 62.4 ms: 1.24x faster                                                      |
| scimark_monte_carlo     | 45.8 ms                                                                  | 37.1 ms: 1.23x faster                                                      |
| pickle_pure_python      | 203 us                                                                   | 166 us: 1.23x faster                                                       |
| raytrace                | 206 ms                                                                   | 169 ms: 1.22x faster                                                       |
| mako                    | 7.20 ms                                                                  | 5.94 ms: 1.21x faster                                                      |
| deepcopy                | 240 us                                                                   | 198 us: 1.21x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.17 ms: 1.21x faster                                                      |
| genshi_xml              | 38.0 ms                                                                  | 31.5 ms: 1.21x faster                                                      |
| go                      | 97.5 ms                                                                  | 80.8 ms: 1.21x faster                                                      |
| spectral_norm           | 71.8 ms                                                                  | 59.6 ms: 1.20x faster                                                      |
| json                    | 3.20 ms                                                                  | 2.68 ms: 1.19x faster                                                      |
| chameleon               | 5.15 ms                                                                  | 4.34 ms: 1.19x faster                                                      |
| hexiom                  | 4.46 ms                                                                  | 3.75 ms: 1.19x faster                                                      |
| pprint_pformat          | 1.05 sec                                                                 | 894 ms: 1.17x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.77 us: 1.16x faster                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 441 ms: 1.16x faster                                                       |
| pyflate                 | 302 ms                                                                   | 262 ms: 1.15x faster                                                       |
| float                   | 53.3 ms                                                                  | 46.3 ms: 1.15x faster                                                      |
| scimark_lu              | 62.8 ms                                                                  | 54.8 ms: 1.15x faster                                                      |
| sqlglot_normalize       | 189 ms                                                                   | 165 ms: 1.14x faster                                                       |
| django_template         | 23.9 ms                                                                  | 20.9 ms: 1.14x faster                                                      |
| regex_compile           | 89.7 ms                                                                  | 78.9 ms: 1.14x faster                                                      |
| logging_format          | 7.13 us                                                                  | 6.29 us: 1.13x faster                                                      |
| sqlglot_optimize        | 34.5 ms                                                                  | 30.4 ms: 1.13x faster                                                      |
| sqlglot_parse           | 929 us                                                                   | 829 us: 1.12x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 267 ms: 1.12x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 5.91 us: 1.12x faster                                                      |
| nqueens                 | 65.1 ms                                                                  | 58.4 ms: 1.12x faster                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 33.0 ms: 1.11x faster                                                      |
| mdp                     | 1.67 sec                                                                 | 1.51 sec: 1.11x faster                                                     |
| chaos                   | 47.3 ms                                                                  | 42.7 ms: 1.11x faster                                                      |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.02 ms: 1.10x faster                                                      |
| meteor_contest          | 74.4 ms                                                                  | 67.6 ms: 1.10x faster                                                      |
| scimark_fft             | 183 ms                                                                   | 166 ms: 1.10x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 47.6 ms: 1.10x faster                                                      |
| sympy_str               | 184 ms                                                                   | 169 ms: 1.09x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 35.3 ms: 1.09x faster                                                      |
| async_generators        | 180 ms                                                                   | 166 ms: 1.08x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.6 ms: 1.08x faster                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 44.6 ms: 1.08x faster                                                      |
| pycparser               | 686 ms                                                                   | 634 ms: 1.08x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.63 ms: 1.08x faster                                                      |
| thrift                  | 487 us                                                                   | 450 us: 1.08x faster                                                       |
| fannkuch                | 255 ms                                                                   | 237 ms: 1.08x faster                                                       |
| 2to3                    | 204 ms                                                                   | 190 ms: 1.07x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.62 us: 1.07x faster                                                      |
| docutils                | 1.59 sec                                                                 | 1.50 sec: 1.07x faster                                                     |
| json_loads              | 13.5 us                                                                  | 12.7 us: 1.06x faster                                                      |
| comprehensions          | 15.4 us                                                                  | 14.5 us: 1.06x faster                                                      |
| xml_etree_parse         | 92.1 ms                                                                  | 87.1 ms: 1.06x faster                                                      |
| coverage                | 55.3 ms                                                                  | 52.4 ms: 1.06x faster                                                      |
| dask                    | 267 ms                                                                   | 254 ms: 1.05x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 94.2 ms: 1.05x faster                                                      |
| bench_thread_pool       | 856 us                                                                   | 817 us: 1.05x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 494 ms: 1.04x faster                                                       |
| generators              | 33.5 ms                                                                  | 32.6 ms: 1.03x faster                                                      |
| dulwich_log             | 43.4 ms                                                                  | 42.3 ms: 1.03x faster                                                      |
| python_startup          | 18.4 ms                                                                  | 18.2 ms: 1.01x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                      |
| xml_etree_iterparse     | 61.8 ms                                                                  | 61.1 ms: 1.01x faster                                                      |
| bench_mp_pool           | 61.2 ms                                                                  | 60.9 ms: 1.01x faster                                                      |
| coroutines              | 14.8 ms                                                                  | 14.7 ms: 1.00x faster                                                      |
| regex_v8                | 13.5 ms                                                                  | 13.7 ms: 1.01x slower                                                      |
| pathlib                 | 72.9 ms                                                                  | 74.0 ms: 1.02x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.70 us: 1.02x slower                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.43 ms: 1.02x slower                                                      |
| async_tree_none         | 313 ms                                                                   | 321 ms: 1.03x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 768 ms: 1.03x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.79 us: 1.05x slower                                                      |
| regex_dna               | 115 ms                                                                   | 121 ms: 1.05x slower                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.73 ms: 1.06x slower                                                      |
| unpickle                | 8.01 us                                                                  | 8.68 us: 1.08x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.11x faster                                                               |

Benchmark hidden because not significant (5): create_gc_cycles, pidigits, python_startup_no_site, async_tree_memoization, pickle_list
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
