
# Results vs. 3.11.0

- fork: python
- ref: 70be5e42f6e288de32e0
- machine: windows-amd64
- commit hash: 70be5e4
- commit date: 2022-12-11
- overall geometric mean: 1.06x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 201 ms: 1.01x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.68 ms: 1.10x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 36.2 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 62.7 ms: 1.13x faster                                                       |
| float          | 53.3 ms                                                                  | 49.7 ms: 1.07x faster                                                       |
| pidigits       | 147 ms                                                                   | 147 ms: 1.00x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.54 ms: 1.06x faster                                                       |
| regex_compile  | 89.7 ms                                                                  | 84.9 ms: 1.06x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.6 ms: 1.01x slower                                                       |
| regex_dna      | 115 ms                                                                   | 120 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.41 ms: 1.43x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 130 us: 1.15x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 184 us: 1.11x faster                                                        |
| unpickle_list        | 2.80 us                                                                  | 2.60 us: 1.08x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.3 ms: 1.04x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.2 ms: 1.02x faster                                                       |
| json_loads           | 13.5 us                                                                  | 13.3 us: 1.02x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.1 ms: 1.02x slower                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.2 us: 1.03x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.83 us: 1.05x slower                                                       |
| pickle               | 6.47 us                                                                  | 7.21 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| python_startup         | 18.4 ms                                                                  | 19.0 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.4 ms: 1.19x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 32.6 ms: 1.17x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.18 ms: 1.17x faster                                                       |
| django_template | 23.9 ms                                                                  | 22.2 ms: 1.07x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.15x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3+-70be5e4 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 29.1 ns: 1.48x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.41 ms: 1.43x faster                                                       |
| asyncio_tcp             | 674 ms                                                                   | 499 ms: 1.35x faster                                                        |
| mypy2                   | 276 ms                                                                   | 221 ms: 1.25x faster                                                        |
| deltablue               | 2.68 ms                                                                  | 2.17 ms: 1.23x faster                                                       |
| richards                | 32.1 ms                                                                  | 26.3 ms: 1.22x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 14.4 ms: 1.19x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 59.5 ns: 1.19x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 21.5 us: 1.18x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 32.6 ms: 1.17x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 61.6 ms: 1.17x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.18 ms: 1.17x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 66.7 ms: 1.17x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.78 ms: 1.15x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 130 us: 1.15x faster                                                        |
| nbody                   | 70.9 ms                                                                  | 62.7 ms: 1.13x faster                                                       |
| deepcopy                | 240 us                                                                   | 214 us: 1.12x faster                                                        |
| scimark_monte_carlo     | 45.8 ms                                                                  | 41.2 ms: 1.11x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 184 us: 1.11x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.38 ms: 1.11x faster                                                       |
| go                      | 97.5 ms                                                                  | 88.5 ms: 1.10x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.68 ms: 1.10x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.88 us: 1.10x faster                                                       |
| raytrace                | 206 ms                                                                   | 189 ms: 1.09x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 4.10 ms: 1.09x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.11 us: 1.08x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 972 ms: 1.08x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.55 sec: 1.08x faster                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 474 ms: 1.08x faster                                                        |
| nqueens                 | 65.1 ms                                                                  | 60.4 ms: 1.08x faster                                                       |
| fannkuch                | 255 ms                                                                   | 237 ms: 1.08x faster                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.60 us: 1.08x faster                                                       |
| django_template         | 23.9 ms                                                                  | 22.2 ms: 1.07x faster                                                       |
| float                   | 53.3 ms                                                                  | 49.7 ms: 1.07x faster                                                       |
| pyflate                 | 302 ms                                                                   | 282 ms: 1.07x faster                                                        |
| html5lib                | 38.5 ms                                                                  | 36.2 ms: 1.06x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.54 ms: 1.06x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.73 us: 1.06x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 282 ms: 1.06x faster                                                        |
| sqlglot_parse           | 929 us                                                                   | 878 us: 1.06x faster                                                        |
| thrift                  | 487 us                                                                   | 460 us: 1.06x faster                                                        |
| regex_compile           | 89.7 ms                                                                  | 84.9 ms: 1.06x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 59.8 ms: 1.05x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 180 ms: 1.05x faster                                                        |
| sympy_str               | 184 ms                                                                   | 176 ms: 1.04x faster                                                        |
| sympy_integrate         | 13.7 ms                                                                  | 13.1 ms: 1.04x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 33.1 ms: 1.04x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.09 ms: 1.04x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 494 ms: 1.04x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 45.6 ms: 1.04x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.9 ms: 1.04x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 35.3 ms: 1.04x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 47.0 ms: 1.03x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 178 ms: 1.03x faster                                                        |
| telco                   | 3.93 ms                                                                  | 3.84 ms: 1.02x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 72.8 ms: 1.02x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 51.2 ms: 1.02x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.3 us: 1.02x faster                                                       |
| coverage                | 55.3 ms                                                                  | 54.5 ms: 1.01x faster                                                       |
| 2to3                    | 204 ms                                                                   | 201 ms: 1.01x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                      |
| async_generators        | 180 ms                                                                   | 179 ms: 1.01x faster                                                        |
| coroutines              | 14.8 ms                                                                  | 14.7 ms: 1.00x faster                                                       |
| pidigits                | 147 ms                                                                   | 147 ms: 1.00x slower                                                        |
| regex_v8                | 13.5 ms                                                                  | 13.6 ms: 1.01x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.1 ms: 1.02x slower                                                       |
| comprehensions          | 15.4 us                                                                  | 15.7 us: 1.02x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 683 us: 1.03x slower                                                        |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 19.0 ms: 1.03x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 19.2 us: 1.03x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 75.4 ms: 1.03x slower                                                       |
| async_tree_memoization  | 374 ms                                                                   | 387 ms: 1.03x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 63.6 ms: 1.04x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.83 us: 1.05x slower                                                       |
| regex_dna               | 115 ms                                                                   | 120 ms: 1.05x slower                                                        |
| async_tree_none         | 313 ms                                                                   | 331 ms: 1.06x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.78 us: 1.06x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.51 ms: 1.08x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 803 ms: 1.08x slower                                                        |
| pickle                  | 6.47 us                                                                  | 7.21 us: 1.11x slower                                                       |
| generators              | 33.5 ms                                                                  | 38.0 ms: 1.13x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (6): bench_thread_pool, xml_etree_parse, dask, unpickle, pycparser, sympy_sum
Ignored benchmarks (6) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
