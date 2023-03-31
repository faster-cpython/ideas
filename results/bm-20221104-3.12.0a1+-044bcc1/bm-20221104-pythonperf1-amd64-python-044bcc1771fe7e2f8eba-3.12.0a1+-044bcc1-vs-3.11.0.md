
# Results vs. 3.11.0

- fork: python
- ref: 044bcc1771fe7e2f8eba
- machine: windows-amd64
- commit hash: 044bcc1
- commit date: 2022-11-04
- overall geometric mean: 1.00x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 207 ms: 1.02x slower                                                        |
| chameleon      | 5.15 ms                                                                  | 5.21 ms: 1.01x slower                                                       |
| docutils       | 1.59 sec                                                                 | 1.62 sec: 1.02x slower                                                      |
| html5lib       | 38.5 ms                                                                  | 36.7 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 65.2 ms: 1.09x faster                                                       |
| pidigits       | 147 ms                                                                   | 149 ms: 1.02x slower                                                        |
| float          | 53.3 ms                                                                  | 55.8 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 86.9 ms: 1.03x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.62 ms: 1.01x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.2 ms: 1.05x slower                                                       |
| regex_dna      | 115 ms                                                                   | 123 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.56 ms: 1.39x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.63 us: 1.06x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 143 us: 1.05x faster                                                        |
| xml_etree_parse      | 92.1 ms                                                                  | 89.9 ms: 1.02x faster                                                       |
| json_loads           | 13.5 us                                                                  | 13.3 us: 1.02x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 205 us: 1.01x slower                                                        |
| pickle_dict          | 18.6 us                                                                  | 18.9 us: 1.02x slower                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 37.4 ms: 1.02x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 66.0 ms: 1.07x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.89 us: 1.07x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.92 us: 1.07x slower                                                       |
| unpickle             | 8.01 us                                                                  | 9.31 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 23.9 ms                                                                  | 22.9 ms: 1.04x faster                                                       |
| mako            | 7.20 ms                                                                  | 7.05 ms: 1.02x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 37.7 ms: 1.01x faster                                                       |
| genshi_text     | 17.3 ms                                                                  | 17.5 ms: 1.01x slower                                                       |
| Geometric mean  | (ref)                                                                    | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1+-044bcc1 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 7.71 ms                                                                  | 5.56 ms: 1.39x faster                                                       |
| mypy2                   | 276 ms                                                                   | 225 ms: 1.23x faster                                                        |
| pylint                  | 319 ms                                                                   | 286 ms: 1.11x faster                                                        |
| unpack_sequence         | 43.1 ns                                                                  | 38.9 ns: 1.11x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.39 ms: 1.10x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.94 ms: 1.09x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 65.2 ms: 1.09x faster                                                       |
| richards                | 32.1 ms                                                                  | 29.8 ms: 1.08x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 43.0 ms: 1.06x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.63 us: 1.06x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.59 sec: 1.05x faster                                                      |
| html5lib                | 38.5 ms                                                                  | 36.7 ms: 1.05x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 143 us: 1.05x faster                                                        |
| django_template         | 23.9 ms                                                                  | 22.9 ms: 1.04x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.57 ms: 1.04x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 86.9 ms: 1.03x faster                                                       |
| fannkuch                | 255 ms                                                                   | 248 ms: 1.03x faster                                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 89.9 ms: 1.02x faster                                                       |
| mako                    | 7.20 ms                                                                  | 7.05 ms: 1.02x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.3 us: 1.02x faster                                                       |
| go                      | 97.5 ms                                                                  | 95.5 ms: 1.02x faster                                                       |
| sympy_str               | 184 ms                                                                   | 180 ms: 1.02x faster                                                        |
| pprint_pformat          | 1.05 sec                                                                 | 1.03 sec: 1.02x faster                                                      |
| scimark_sor             | 77.7 ms                                                                  | 76.2 ms: 1.02x faster                                                       |
| coverage                | 55.3 ms                                                                  | 54.4 ms: 1.02x faster                                                       |
| pyflate                 | 302 ms                                                                   | 298 ms: 1.02x faster                                                        |
| raytrace                | 206 ms                                                                   | 204 ms: 1.01x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 42.9 ms: 1.01x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 37.7 ms: 1.01x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 64.6 ms: 1.01x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.62 ms: 1.01x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.63 us: 1.00x slower                                                       |
| deepcopy                | 240 us                                                                   | 242 us: 1.01x slower                                                        |
| pickle_pure_python      | 203 us                                                                   | 205 us: 1.01x slower                                                        |
| chameleon               | 5.15 ms                                                                  | 5.21 ms: 1.01x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                       |
| logging_format          | 7.13 us                                                                  | 7.21 us: 1.01x slower                                                       |
| spectral_norm           | 71.8 ms                                                                  | 72.7 ms: 1.01x slower                                                       |
| sympy_sum               | 98.9 ms                                                                  | 100 ms: 1.01x slower                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 2.09 us: 1.01x slower                                                       |
| genshi_text             | 17.3 ms                                                                  | 17.5 ms: 1.01x slower                                                       |
| 2to3                    | 204 ms                                                                   | 207 ms: 1.02x slower                                                        |
| pickle_dict             | 18.6 us                                                                  | 18.9 us: 1.02x slower                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 35.0 ms: 1.02x slower                                                       |
| pidigits                | 147 ms                                                                   | 149 ms: 1.02x slower                                                        |
| docutils                | 1.59 sec                                                                 | 1.62 sec: 1.02x slower                                                      |
| async_generators        | 180 ms                                                                   | 183 ms: 1.02x slower                                                        |
| meteor_contest          | 74.4 ms                                                                  | 75.9 ms: 1.02x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 74.4 ms: 1.02x slower                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 37.4 ms: 1.02x slower                                                       |
| bench_thread_pool       | 856 us                                                                   | 875 us: 1.02x slower                                                        |
| create_gc_cycles        | 666 us                                                                   | 683 us: 1.03x slower                                                        |
| coroutines              | 14.8 ms                                                                  | 15.2 ms: 1.03x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 49.7 ms: 1.03x slower                                                       |
| scimark_fft             | 183 ms                                                                   | 188 ms: 1.03x slower                                                        |
| chaos                   | 47.3 ms                                                                  | 48.8 ms: 1.03x slower                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.17 ms: 1.03x slower                                                       |
| sqlglot_parse           | 929 us                                                                   | 961 us: 1.03x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 63.7 ms: 1.04x slower                                                       |
| float                   | 53.3 ms                                                                  | 55.8 ms: 1.05x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 14.2 ms: 1.05x slower                                                       |
| regex_dna               | 115 ms                                                                   | 123 ms: 1.07x slower                                                        |
| xml_etree_iterparse     | 61.8 ms                                                                  | 66.0 ms: 1.07x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.50 ms: 1.07x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.89 us: 1.07x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.92 us: 1.07x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.79 us: 1.07x slower                                                       |
| async_tree_none         | 313 ms                                                                   | 336 ms: 1.07x slower                                                        |
| generators              | 33.5 ms                                                                  | 36.1 ms: 1.08x slower                                                       |
| async_tree_memoization  | 374 ms                                                                   | 403 ms: 1.08x slower                                                        |
| async_tree_io           | 744 ms                                                                   | 803 ms: 1.08x slower                                                        |
| asyncio_tcp             | 674 ms                                                                   | 732 ms: 1.09x slower                                                        |
| comprehensions          | 15.4 us                                                                  | 17.2 us: 1.12x slower                                                       |
| unpickle                | 8.01 us                                                                  | 9.31 us: 1.16x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.00x slower                                                                |

Benchmark hidden because not significant (15): pprint_safe_repr, hexiom, thrift, scimark_lu, sympy_expand, xml_etree_generate, sympy_integrate, telco, deepcopy_memo, logging_silent, async_tree_cpu_io_mixed, sqlglot_normalize, tornado_http, dask, pycparser
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
