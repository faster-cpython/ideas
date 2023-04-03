
# Results vs. 3.11.0

- fork: python
- ref: 2e343fc465ed0206340c
- machine: windows-amd64
- commit hash: 2e343fc
- commit date: 2022-11-10
- overall geometric mean: 1.04x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 198 ms: 1.03x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.89 ms: 1.06x faster                                                       |
| html5lib       | 38.5 ms                                                                  | 35.7 ms: 1.08x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 93.4 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 63.1 ms: 1.12x faster                                                       |
| float          | 53.3 ms                                                                  | 54.1 ms: 1.02x slower                                                       |
| pidigits       | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 84.7 ms: 1.06x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.58 ms: 1.03x faster                                                       |
| regex_dna      | 115 ms                                                                   | 124 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.38 ms: 1.43x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.56 us: 1.10x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 190 us: 1.07x faster                                                        |
| unpickle_pure_python | 150 us                                                                   | 140 us: 1.07x faster                                                        |
| json_loads           | 13.5 us                                                                  | 13.1 us: 1.03x faster                                                       |
| unpickle             | 8.01 us                                                                  | 7.75 us: 1.03x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.6 ms: 1.01x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 36.3 ms: 1.01x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.3 us: 1.03x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.80 us: 1.04x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 64.5 ms: 1.04x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.96 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 16.1 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.20 ms                                                                  | 6.55 ms: 1.10x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.7 ms: 1.10x faster                                                       |
| genshi_text     | 17.3 ms                                                                  | 15.8 ms: 1.09x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 35.3 ms: 1.08x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.09x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1+-2e343fc |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 7.71 ms                                                                  | 5.38 ms: 1.43x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 32.2 ns: 1.34x faster                                                       |
| mypy2                   | 276 ms                                                                   | 225 ms: 1.23x faster                                                        |
| richards                | 32.1 ms                                                                  | 27.2 ms: 1.18x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.76 ms: 1.16x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.35 ms: 1.14x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.32 ms: 1.13x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 63.1 ms: 1.12x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.55 ms: 1.10x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 65.3 ms: 1.10x faster                                                       |
| django_template         | 23.9 ms                                                                  | 21.7 ms: 1.10x faster                                                       |
| unpickle_list           | 2.80 us                                                                  | 2.56 us: 1.10x faster                                                       |
| raytrace                | 206 ms                                                                   | 188 ms: 1.09x faster                                                        |
| genshi_text             | 17.3 ms                                                                  | 15.8 ms: 1.09x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 65.3 ns: 1.09x faster                                                       |
| fannkuch                | 255 ms                                                                   | 236 ms: 1.08x faster                                                        |
| scimark_monte_carlo     | 45.8 ms                                                                  | 42.3 ms: 1.08x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.55 sec: 1.08x faster                                                      |
| html5lib                | 38.5 ms                                                                  | 35.7 ms: 1.08x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.91 us: 1.08x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 35.3 ms: 1.08x faster                                                       |
| go                      | 97.5 ms                                                                  | 91.2 ms: 1.07x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 190 us: 1.07x faster                                                        |
| unpickle_pure_python    | 150 us                                                                   | 140 us: 1.07x faster                                                        |
| coroutines              | 14.8 ms                                                                  | 13.9 ms: 1.07x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 280 ms: 1.07x faster                                                        |
| pprint_safe_repr        | 512 ms                                                                   | 481 ms: 1.06x faster                                                        |
| deepcopy                | 240 us                                                                   | 226 us: 1.06x faster                                                        |
| regex_compile           | 89.7 ms                                                                  | 84.7 ms: 1.06x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.07 ms: 1.06x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 73.4 ms: 1.06x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 70.4 ms: 1.06x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.89 ms: 1.06x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 32.7 ms: 1.05x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 24.1 us: 1.05x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 885 us: 1.05x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 4.28 ms: 1.04x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 45.5 ms: 1.04x faster                                                       |
| sympy_str               | 184 ms                                                                   | 177 ms: 1.04x faster                                                        |
| pyflate                 | 302 ms                                                                   | 291 ms: 1.04x faster                                                        |
| sqlglot_normalize       | 189 ms                                                                   | 182 ms: 1.04x faster                                                        |
| nqueens                 | 65.1 ms                                                                  | 62.8 ms: 1.04x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 1.01 sec: 1.04x faster                                                      |
| coverage                | 55.3 ms                                                                  | 53.4 ms: 1.03x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.1 us: 1.03x faster                                                       |
| unpickle                | 8.01 us                                                                  | 7.75 us: 1.03x faster                                                       |
| 2to3                    | 204 ms                                                                   | 198 ms: 1.03x faster                                                        |
| regex_effbot            | 1.63 ms                                                                  | 1.58 ms: 1.03x faster                                                       |
| async_generators        | 180 ms                                                                   | 175 ms: 1.03x faster                                                        |
| pycparser               | 686 ms                                                                   | 669 ms: 1.03x faster                                                        |
| sympy_integrate         | 13.7 ms                                                                  | 13.3 ms: 1.02x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 179 ms: 1.02x faster                                                        |
| logging_format          | 7.13 us                                                                  | 6.99 us: 1.02x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 47.5 ms: 1.02x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 97.3 ms: 1.02x faster                                                       |
| dask                    | 267 ms                                                                   | 263 ms: 1.01x faster                                                        |
| xml_etree_generate      | 52.3 ms                                                                  | 51.6 ms: 1.01x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 36.3 ms: 1.01x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 62.4 ms: 1.01x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 43.9 ms: 1.01x slower                                                       |
| generators              | 33.5 ms                                                                  | 33.9 ms: 1.01x slower                                                       |
| comprehensions          | 15.4 us                                                                  | 15.6 us: 1.01x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 676 us: 1.01x slower                                                        |
| float                   | 53.3 ms                                                                  | 54.1 ms: 1.02x slower                                                       |
| tornado_http            | 91.8 ms                                                                  | 93.4 ms: 1.02x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 74.4 ms: 1.02x slower                                                       |
| pidigits                | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| python_startup          | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 63.2 ms: 1.03x slower                                                       |
| async_tree_memoization  | 374 ms                                                                   | 387 ms: 1.03x slower                                                        |
| gc_traversal            | 1.40 ms                                                                  | 1.45 ms: 1.03x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 19.3 us: 1.03x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.80 us: 1.04x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 64.5 ms: 1.04x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 16.1 ms: 1.05x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 784 ms: 1.05x slower                                                        |
| async_tree_none         | 313 ms                                                                   | 330 ms: 1.05x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.79 us: 1.07x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.96 us: 1.08x slower                                                       |
| regex_dna               | 115 ms                                                                   | 124 ms: 1.08x slower                                                        |
| asyncio_tcp             | 674 ms                                                                   | 746 ms: 1.11x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, docutils, bench_thread_pool, telco, logging_simple, xml_etree_parse, regex_v8, thrift
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
