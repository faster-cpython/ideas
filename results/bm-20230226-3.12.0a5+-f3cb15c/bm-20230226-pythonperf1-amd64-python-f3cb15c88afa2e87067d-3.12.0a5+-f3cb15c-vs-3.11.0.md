
# Results vs. 3.11.0

- fork: python
- ref: f3cb15c88afa2e87067d
- machine: windows-amd64
- commit hash: f3cb15c
- commit date: 2023-02-26
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 200 ms: 1.02x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.45 ms: 1.16x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 35.1 ms: 1.10x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 89.4 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 58.7 ms: 1.21x faster                                                       |
| float          | 53.3 ms                                                                  | 48.0 ms: 1.11x faster                                                       |
| pidigits       | 147 ms                                                                   | 149 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 81.3 ms: 1.10x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.52 ms: 1.07x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| regex_dna      | 115 ms                                                                   | 118 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.38 ms: 1.43x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 118 us: 1.27x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 167 us: 1.22x faster                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 34.6 ms: 1.06x faster                                                       |
| json_loads           | 13.5 us                                                                  | 12.8 us: 1.06x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.73 us: 1.03x faster                                                       |
| unpickle             | 8.01 us                                                                  | 7.86 us: 1.02x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 52.9 ms: 1.01x slower                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.9 us: 1.01x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.78 us: 1.03x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.9 ms: 1.03x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.89 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.9 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.7 ms: 1.26x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 30.8 ms: 1.23x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.22 ms: 1.16x faster                                                       |
| django_template | 23.9 ms                                                                  | 20.8 ms: 1.15x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.20x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230226-pythonperf1-amd64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 26.2 ns: 1.64x faster                                                       |
| generators              | 33.5 ms                                                                  | 21.5 ms: 1.56x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.38 ms: 1.43x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 486 ms: 1.39x faster                                                        |
| richards                | 32.1 ms                                                                  | 23.2 ms: 1.39x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 1.94 ms: 1.38x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 54.5 ns: 1.30x faster                                                       |
| mypy2                   | 276 ms                                                                   | 215 ms: 1.28x faster                                                        |
| unpickle_pure_python    | 150 us                                                                   | 118 us: 1.27x faster                                                        |
| deepcopy_memo           | 25.3 us                                                                  | 20.0 us: 1.27x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 13.7 ms: 1.26x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 61.6 ms: 1.26x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 30.8 ms: 1.23x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 58.4 ms: 1.23x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 167 us: 1.22x faster                                                        |
| nbody                   | 70.9 ms                                                                  | 58.7 ms: 1.21x faster                                                       |
| raytrace                | 206 ms                                                                   | 173 ms: 1.19x faster                                                        |
| fannkuch                | 255 ms                                                                   | 216 ms: 1.18x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 3.84 ms: 1.16x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.45 ms: 1.16x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.22 ms: 1.16x faster                                                       |
| deepcopy                | 240 us                                                                   | 208 us: 1.15x faster                                                        |
| django_template         | 23.9 ms                                                                  | 20.8 ms: 1.15x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.79 ms: 1.15x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 41.3 ms: 1.14x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.47 sec: 1.14x faster                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 1.81 us: 1.14x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 162 ms: 1.13x faster                                                        |
| pprint_pformat          | 1.05 sec                                                                 | 938 ms: 1.12x faster                                                        |
| logging_format          | 7.13 us                                                                  | 6.37 us: 1.12x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 831 us: 1.12x faster                                                        |
| pyflate                 | 302 ms                                                                   | 270 ms: 1.12x faster                                                        |
| scimark_monte_carlo     | 45.8 ms                                                                  | 41.0 ms: 1.12x faster                                                       |
| go                      | 97.5 ms                                                                  | 87.5 ms: 1.11x faster                                                       |
| float                   | 53.3 ms                                                                  | 48.0 ms: 1.11x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 58.6 ms: 1.11x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 269 ms: 1.11x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.38 ms: 1.11x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 81.3 ms: 1.10x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 464 ms: 1.10x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 171 ms: 1.10x faster                                                        |
| html5lib                | 38.5 ms                                                                  | 35.1 ms: 1.10x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.5 ms: 1.10x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 57.4 ms: 1.09x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 44.4 ms: 1.09x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.04 ms: 1.08x faster                                                       |
| coverage                | 55.3 ms                                                                  | 51.0 ms: 1.08x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.11 us: 1.08x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.52 ms: 1.07x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 12.8 ms: 1.07x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 13.9 ms: 1.06x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 484 ms: 1.06x faster                                                        |
| xml_etree_process       | 36.6 ms                                                                  | 34.6 ms: 1.06x faster                                                       |
| json_loads              | 13.5 us                                                                  | 12.8 us: 1.06x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 70.6 ms: 1.05x faster                                                       |
| async_tree_memoization  | 374 ms                                                                   | 356 ms: 1.05x faster                                                        |
| thrift                  | 487 us                                                                   | 464 us: 1.05x faster                                                        |
| sympy_str               | 184 ms                                                                   | 176 ms: 1.04x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 41.9 ms: 1.04x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| tornado_http            | 91.8 ms                                                                  | 89.4 ms: 1.03x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.73 us: 1.03x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 96.9 ms: 1.02x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.85 ms: 1.02x faster                                                       |
| unpickle                | 8.01 us                                                                  | 7.86 us: 1.02x faster                                                       |
| 2to3                    | 204 ms                                                                   | 200 ms: 1.02x faster                                                        |
| async_tree_none         | 313 ms                                                                   | 308 ms: 1.02x faster                                                        |
| comprehensions          | 15.4 us                                                                  | 15.2 us: 1.01x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 52.9 ms: 1.01x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.9 us: 1.01x slower                                                       |
| pidigits                | 147 ms                                                                   | 149 ms: 1.02x slower                                                        |
| regex_v8                | 13.5 ms                                                                  | 13.8 ms: 1.02x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                                       |
| regex_dna               | 115 ms                                                                   | 118 ms: 1.03x slower                                                        |
| async_tree_io           | 744 ms                                                                   | 764 ms: 1.03x slower                                                        |
| pickle_list             | 2.70 us                                                                  | 2.78 us: 1.03x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.9 ms: 1.03x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.9 ms: 1.03x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 696 us: 1.05x slower                                                        |
| pickle                  | 6.47 us                                                                  | 6.89 us: 1.07x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 65.8 ms: 1.08x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.53 ms: 1.09x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.86 us: 1.11x slower                                                       |
| async_generators        | 180 ms                                                                   | 220 ms: 1.22x slower                                                        |
| dask                    | 267 ms                                                                   | 353 ms: 1.32x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (4): pycparser, bench_thread_pool, xml_etree_parse, pathlib
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
