
# Results vs. 3.11.0

- fork: python
- ref: b6bd7ffcbc1ffaa68e34
- machine: windows-amd64
- commit hash: b6bd7ff
- commit date: 2022-12-06
- overall geometric mean: 1.12x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 186 ms: 1.10x faster                                                       |
| chameleon      | 5.15 ms                                                                  | 4.22 ms: 1.22x faster                                                      |
| docutils       | 1.59 sec                                                                 | 1.50 sec: 1.06x faster                                                     |
| html5lib       | 38.5 ms                                                                  | 34.8 ms: 1.11x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 57.5 ms: 1.23x faster                                                      |
| float          | 53.3 ms                                                                  | 47.7 ms: 1.12x faster                                                      |
| pidigits       | 147 ms                                                                   | 147 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 77.2 ms: 1.16x faster                                                      |
| regex_v8       | 13.5 ms                                                                  | 13.7 ms: 1.01x slower                                                      |
| regex_effbot   | 1.63 ms                                                                  | 1.69 ms: 1.04x slower                                                      |
| regex_dna      | 115 ms                                                                   | 119 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.31 ms: 1.45x faster                                                      |
| unpickle_pure_python | 150 us                                                                   | 116 us: 1.29x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 166 us: 1.23x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 32.7 ms: 1.12x faster                                                      |
| xml_etree_generate   | 52.3 ms                                                                  | 47.9 ms: 1.09x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.67 us: 1.05x faster                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 89.1 ms: 1.03x faster                                                      |
| json_loads           | 13.5 us                                                                  | 13.3 us: 1.01x faster                                                      |
| pickle_dict          | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                      |
| pickle               | 6.47 us                                                                  | 6.87 us: 1.06x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.09x faster                                                               |

Benchmark hidden because not significant (3): xml_etree_iterparse, unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup | 18.4 ms                                                                  | 18.1 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.7 ms: 1.26x faster                                                      |
| genshi_xml      | 38.0 ms                                                                  | 31.5 ms: 1.21x faster                                                      |
| mako            | 7.20 ms                                                                  | 6.00 ms: 1.20x faster                                                      |
| django_template | 23.9 ms                                                                  | 20.3 ms: 1.18x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.21x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 25.3 ns: 1.70x faster                                                      |
| json_dumps              | 7.71 ms                                                                  | 5.31 ms: 1.45x faster                                                      |
| richards                | 32.1 ms                                                                  | 23.4 ms: 1.37x faster                                                      |
| deltablue               | 2.68 ms                                                                  | 1.97 ms: 1.36x faster                                                      |
| mypy2                   | 276 ms                                                                   | 206 ms: 1.34x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 19.3 us: 1.31x faster                                                      |
| unpickle_pure_python    | 150 us                                                                   | 116 us: 1.29x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 55.4 ns: 1.28x faster                                                      |
| scimark_sor             | 77.7 ms                                                                  | 61.1 ms: 1.27x faster                                                      |
| genshi_text             | 17.3 ms                                                                  | 13.7 ms: 1.26x faster                                                      |
| scimark_monte_carlo     | 45.8 ms                                                                  | 36.3 ms: 1.26x faster                                                      |
| go                      | 97.5 ms                                                                  | 78.0 ms: 1.25x faster                                                      |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.11 ms: 1.25x faster                                                      |
| nbody                   | 70.9 ms                                                                  | 57.5 ms: 1.23x faster                                                      |
| pickle_pure_python      | 203 us                                                                   | 166 us: 1.23x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.22 ms: 1.22x faster                                                      |
| hexiom                  | 4.46 ms                                                                  | 3.65 ms: 1.22x faster                                                      |
| raytrace                | 206 ms                                                                   | 169 ms: 1.22x faster                                                       |
| deepcopy                | 240 us                                                                   | 197 us: 1.21x faster                                                       |
| fannkuch                | 255 ms                                                                   | 210 ms: 1.21x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 31.5 ms: 1.21x faster                                                      |
| mako                    | 7.20 ms                                                                  | 6.00 ms: 1.20x faster                                                      |
| json                    | 3.20 ms                                                                  | 2.67 ms: 1.20x faster                                                      |
| pprint_pformat          | 1.05 sec                                                                 | 888 ms: 1.18x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 53.2 ms: 1.18x faster                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 1.74 us: 1.18x faster                                                      |
| spectral_norm           | 71.8 ms                                                                  | 60.9 ms: 1.18x faster                                                      |
| nqueens                 | 65.1 ms                                                                  | 55.3 ms: 1.18x faster                                                      |
| django_template         | 23.9 ms                                                                  | 20.3 ms: 1.18x faster                                                      |
| pyflate                 | 302 ms                                                                   | 259 ms: 1.17x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 440 ms: 1.16x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 77.2 ms: 1.16x faster                                                      |
| sqlglot_parse           | 929 us                                                                   | 804 us: 1.16x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 164 ms: 1.15x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 41.3 ms: 1.15x faster                                                      |
| logging_format          | 7.13 us                                                                  | 6.24 us: 1.14x faster                                                      |
| sqlglot_transpile       | 1.13 ms                                                                  | 994 us: 1.14x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 30.4 ms: 1.13x faster                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 32.7 ms: 1.12x faster                                                      |
| logging_simple          | 6.60 us                                                                  | 5.91 us: 1.12x faster                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 43.2 ms: 1.12x faster                                                      |
| float                   | 53.3 ms                                                                  | 47.7 ms: 1.12x faster                                                      |
| scimark_fft             | 183 ms                                                                   | 164 ms: 1.11x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.51 sec: 1.11x faster                                                     |
| html5lib                | 38.5 ms                                                                  | 34.8 ms: 1.11x faster                                                      |
| async_generators        | 180 ms                                                                   | 163 ms: 1.10x faster                                                       |
| coverage                | 55.3 ms                                                                  | 50.1 ms: 1.10x faster                                                      |
| 2to3                    | 204 ms                                                                   | 186 ms: 1.10x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 67.8 ms: 1.10x faster                                                      |
| sympy_expand            | 298 ms                                                                   | 273 ms: 1.09x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 47.9 ms: 1.09x faster                                                      |
| thrift                  | 487 us                                                                   | 455 us: 1.07x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.8 ms: 1.06x faster                                                      |
| sympy_str               | 184 ms                                                                   | 173 ms: 1.06x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.50 sec: 1.06x faster                                                     |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 483 ms: 1.06x faster                                                       |
| dask                    | 267 ms                                                                   | 254 ms: 1.05x faster                                                       |
| bench_thread_pool       | 856 us                                                                   | 815 us: 1.05x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.67 us: 1.05x faster                                                      |
| comprehensions          | 15.4 us                                                                  | 14.7 us: 1.05x faster                                                      |
| async_tree_memoization  | 374 ms                                                                   | 362 ms: 1.03x faster                                                       |
| xml_etree_parse         | 92.1 ms                                                                  | 89.1 ms: 1.03x faster                                                      |
| sympy_sum               | 98.9 ms                                                                  | 95.7 ms: 1.03x faster                                                      |
| dulwich_log             | 43.4 ms                                                                  | 42.1 ms: 1.03x faster                                                      |
| coroutines              | 14.8 ms                                                                  | 14.4 ms: 1.03x faster                                                      |
| telco                   | 3.93 ms                                                                  | 3.86 ms: 1.02x faster                                                      |
| async_tree_none         | 313 ms                                                                   | 308 ms: 1.02x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.3 us: 1.01x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                      |
| python_startup          | 18.4 ms                                                                  | 18.1 ms: 1.01x faster                                                      |
| generators              | 33.5 ms                                                                  | 33.1 ms: 1.01x faster                                                      |
| create_gc_cycles        | 666 us                                                                   | 660 us: 1.01x faster                                                       |
| pidigits                | 147 ms                                                                   | 147 ms: 1.01x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.7 ms: 1.01x slower                                                      |
| async_tree_io           | 744 ms                                                                   | 753 ms: 1.01x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.72 us: 1.03x slower                                                      |
| regex_effbot            | 1.63 ms                                                                  | 1.69 ms: 1.04x slower                                                      |
| regex_dna               | 115 ms                                                                   | 119 ms: 1.04x slower                                                       |
| asyncio_tcp             | 674 ms                                                                   | 711 ms: 1.06x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.87 us: 1.06x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.12x faster                                                               |

Benchmark hidden because not significant (8): pycparser, xml_etree_iterparse, pathlib, gc_traversal, python_startup_no_site, bench_mp_pool, unpickle, pickle_list
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
